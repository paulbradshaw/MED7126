# How to: create a treemap in Tableau Public

Treemaps are a great alternative to pie charts when you want to tell a story about the composition of something: whereas pie charts can be limiting, treemaps allow users to drill down into 'parts of parts', and group elements within particular categories.

In this post I'm going to show you how to create a treemap in the free visualisation software Tableau Public to show how the majority of BuzzFeed's content views in 2015 took place away from its website. 

This data suits a treemap particularly well: although the traffic is broadly split between 'website', 'Facebook', 'Snapchat', 'YouTube' and 'other', there are also subdivisions within some of those platforms - for example, Facebook traffic is split between video and images, and website traffic is split between direct visits, those via Google, and those via Facebook. A treemap allows users to explore those subtleties in a way that pie charts do not.

## Step 1: Get the data in the right format

To create a treemap it is vital that you get the data in the correct format to begin with. In particular, you will need to make sure that as well as a primary 'category' column, you also have a second 'sub category' column. They don't have to have these names, but that general concept is important. A third column should contain the values to be visualised.

![]()

The key feature to look for in this data structure is that you should expect to see categories in your main 'category' column appear more than once. In our BuzzFeed data, for example, the platform category 'website' appears 3 times - once for each sub category of 'Direct traffic', 'Traffic from Google' and 'Traffic from Facebook'.

## Bring the data into Tableau
