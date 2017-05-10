# Working with big data

This tutorial takes you through the process of working with a big data set (over 10 million rows) using the following tools:

* Command line (Terminal on a Mac/Linux or PowerShell on PC)
* Google Cloud Storage
* Google BigQuery
* SQL

## Part 1: Creating and understanding a big dataset using command line

Although many 'big data' scenarios don't involve you actually creating the dataset yourself, in this tutorial we are going to compile a very large dataset ourselves, using command line, just because we can.

You can find out more about command line in [my GitHub repo on that topic](https://github.com/paulbradshaw/commandline), but here are the key points as far as big data is concerned:

* Command line allows you to work with files on your computer without having to open software packages like Excel or Word
* One thing we can do with command line, for example, is combine hundreds of spreadsheet files into a very large dataset
* We can also use command line to find out the first line in a large dataset, or to count how many rows it has - which we couldn't do in Excel

In this part you'll learn how.

### Getting the data - in pieces

We'll be working with police crime data. You can [download historical crime data from the data.police.uk archives page](https://data.police.uk/data/archive/) - note that these are very large files indeed, and that you only need to download one of these. It's always important to read the explanations on pages like these - on this page the important paragraph is this:

> "With the exception of the latest month’s archive, the data on this page is out of date and should not be used. These snapshots are provided for archival purposes, and we recommend you use data from the custom download page for most purposes."

Although the data files are labeled 'January 2017', 'February 2017' and so on, they actually contain not just that month's crime data but *all crimes from 2010 up to that point*. As a result, each file is larger than the one before it, and the most recent ones supersede the earlier ones (because the data is more up to date).

If you were writing a story about this data you should use the data at [data.police.uk/data/archive/latest.zip](https://data.police.uk/data/archive/latest.zip), which always contains the latest set.

Each of the links points to a zip file. In some cases this may be too large for your computer. So, for the purposes of this exercise you may find it better to download the earliest zip files from May 2013 (686.5 MB) and use those. (An alternative would be to download the file to some server space that you are 'renting', but I'm not going to cover that here.)

### Combining data using `cat` or `type`

Once you have downloaded and unzipped the file, you should have a folder with hundreds of CSV files from different forces, different months and years, and different types of data (one for crimes, one for outcomes, and a third for stop and search).

You will need to combine all of the files belonging to one particular category - let's say crimes - into a single file.

To combine multiple CSV files you can use the `cat` command (Mac/Linux) or `type` (Windows). You'll [find instructions here](https://github.com/paulbradshaw/commandline/blob/master/joining.md)

### Understanding the large file you've just created

This new file will be too big to open in Excel or Google Sheets, but you can find out a little bit about it by using other aspects of command line.

For example, you will need to know what the column headings are in your new file. To do this you can use the `head` command (or in Windows PowerShell, `Get-Content`). You'll [find instructions on how to use `head` for this purpose here](https://github.com/paulbradshaw/commandline/blob/master/head.md); [similar instructions for PowerShell are here](https://technet.microsoft.com/en-us/library/ee176843.aspx).

If you want to check how many lines of data are in the file, you can [use `wc` in Terminal](http://www.tecmint.com/wc-command-examples/) (in PowerShell, use `| Measure-Object` after your `Get-Content` command, as [explained here](https://technet.microsoft.com/en-us/library/ee176843.aspx)).

*Before* you do this, note that it will take a long time for the process to complete. When I did this on a file with 37 million lines (January 2017), it took around an hour to find out. But that's useful to know because when you see how quickly Google BigQuery conducts the same query, it's quite amazing.

## Part 2: Uploading the data to Google Cloud

There are various ways to work with data in Google Cloud Platform (GCP). These include:

* Google Cloud Datastore
* Google Cloud SQL
* Google Cloud Bigtable
* Google BigQuery
* Google Cloud Storage

An [overview of the tools](https://cloud.google.com/datastore/docs/concepts/overview?hl=en_US) says:

> "If you need a relational database with full SQL support for an online transaction processing (OLTP) system, consider Google Cloud SQL. If you don’t require support for ACID transactions or if your data is not highly structured, consider Google Cloud Bigtable.
If you need interactive querying in an online analytical processing (OLAP) system, consider Google BigQuery. If you need to store large immutable blobs, such as large images or movies, consider Google Cloud Storage."

We just need to store a lot of data, so we're using **Google Cloud Storage**

You can access Google Cloud Storage at [https://console.cloud.google.com/storage](https://console.cloud.google.com/storage)

Create a new project by clicking '**Create bucket**' and choose the type of 'storage class' that most fits your use case, and the region closest to where you'll be accessing the data.

Now upload data to your bucket. Click '**Upload files**' and find the file that you want to upload.

If you know how to use command line you can also launch Cloud Shell by clicking the 'shell prompt' button to the right of the search box at the top of the page. [Guidance on using Google Cloud Shell is available here](https://cloud.google.com/shell/docs/quickstart)

## Part 3: Adding the data to a project in Google BigQuery

Now that you have the data in Google Cloud Storage, you can query it in [Google BigQuery](https://bigquery.cloud.google.com/welcome). 

You can upload data directly (as [detailed here](https://cloud.google.com/bigquery/quickstart-web-ui#load_data_into_a_table) but there's a 10MB limit on using the BigQuery UI. This is why we began in Cloud Storage and uploaded there first - but for smaller jobs you can avoid that.

Your project from Google Cloud Storage should be visible in the left hand column, or you can create a new project within that column. 

Once created, hover over the project name and click the 'plus' icon to add data to that project. The main window will now display settings for you to do this. In *Location* choose *Google Cloud Storage* and then click *view files* to select the file you uploaded previously.

In the *schema* area it's better to add them manually rather than use 'Automatically detect'. This also allows you to rename fields to be lower case and without spaces etc.

When you've finished with the settings click **Create Table** and 


## Part 4: Querying the data using SQL

### Export the results as a CSV
