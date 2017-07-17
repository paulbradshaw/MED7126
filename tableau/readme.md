# How to: create a treemap in Tableau Public

Treemaps are a great alternative to pie charts when you want to tell a story about the composition of something: whereas pie charts can be limiting, treemaps allow users to drill down into 'parts of parts', and group elements within particular categories.

In this post I'm going to show you how to create a treemap in the free visualisation software Tableau Public to show how the majority of BuzzFeed's content views in 2015 took place away from its website. 

This data suits a treemap particularly well: although the traffic is broadly split between 'website', 'Facebook', 'Snapchat', 'YouTube' and 'other', there are also subdivisions within some of those platforms - for example, Facebook traffic is split between video and images, and website traffic is split between direct visits, those via Google, and those via Facebook. A treemap allows users to explore those subtleties in a way that pie charts do not.

## Step 1: Get the data in the right format

To create a treemap it is vital that you get the data in the correct format to begin with. In particular, you will need to make sure that as well as a primary 'category' column, you also have a second 'sub category' column. They don't have to have these names, but that general concept is important. A third column should contain the values to be visualised.

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/tableau/treemapdataformat.png)

The key feature to look for in this data structure is that you should expect to see categories in your main 'category' column appear more than once. In our BuzzFeed data, for example, the platform category 'website' appears 3 times - once for each sub category of 'Direct traffic', 'Traffic from Google' and 'Traffic from Facebook'.

Also, make sure that your values only use numbers - don't add percentage symbols, commas or other characters that might lead to it being interpreted as text and mean you have to reclassify the data later.

## Begin creating your chart

In Tableau Public, connect to the data you've just created, and go to your empty worksheet. On the left you should see your category (in this case, 'Platform') and sub category (in this case 'Category') columns in the *Dimensions* area; and underneath that in the *Measures* area, your values (in this case, 'Traffic %').

Click and drag your main category dimension ('Platform') into the *Rows* area at the top. Then do the same with your measure ('Traffic %') so that it looks like this:

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/tableau/treemaprows.png)

Tableau will automatically draw a chart for you - but ignore that. Instead, look to the right hand side where the 'Show me' menu should now be showing which chart types you can use with this combination of data. If it doesn't show, click 'Show me' in the upper right corner.

One of the options available should be the treemap - it's normally the first option four rows down. Click on this to change the chart to a treemap.

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/tableau/treemapshowme.png)

## Customising the colours
