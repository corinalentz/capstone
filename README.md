# Capstone: Recommending Art
By: Corina Lentz

## Problem Statement

The goal of this project is to build a recommender engine that can take in an artist’s name and recommend similar artists based on the art tags the artists share.

I'm confident that this recommender would be valuable for museums to drive engagement on their social media and websites, which could then be used to increase museum memberships, special exhibit ticket sales, and online sales for related merchandise.

## The Data

The dataset I am using for this project is the Metropolitan Museum of Art Open Access Initiative dataset. It is maintained and updated by the Metropolitan Museum of Art. The dataset currently contains 475,897 rows and 54 columns. Each row is one piece of art. The columns provide information about the artwork such as country it was created in, materials used, name of the item that the artwork is, classification of the artwork, department where the artwork is housed, and so on. The columns also have information about the artist such as name, date of birth/death, nationality, role in the project, and so on. Due to size restrictions, the dataset (and saved dataframes) will not be uploaded to this repo but it can be found on GitHub [here [1]](https://github.com/metmuseum/openaccess). 

## Background

The Metropolitan Museum of Art was established in 1870 in New York City, NY. Today the museum spans two sites in New York City: The Met Fifth Avenue and The Met Cloisters [[2]](https://www.metmuseum.org/about-the-met). In addition to housing a large collection of artwork, the Metropolitan Museum also has robust conservation and scientific research departments dedicated to developing new techniques in conservation and art analytics [[3]](https://www.metmuseum.org/about-the-met/conservation-and-scientific-research/projects).

## Data Cleaning & Pre-Processing

During data cleaning and pre-processing I dropped all rows that contained null values in the **Tags** and **Artist Display Name** columns, filtered out rows that contained 10 of the 18 departments in the **Department** column, merged together rows that had the same **Artist Display Name** values, and created dummy columns based on the unique **Tag** column values. This left me with a dataframe containing 4,774 unique artists/artist group rows and 878 unique tag columns.

## EDA

In my exploration of the cleaned and processed data I found that the most common tags were Men and Women respectively. Some other common tags included Portraits, Landscapes, Trees, and Human Figures. The least common tags were only seen on a single artwork and included things such as Pigeons, Plows, and Clothing.

## Conclusions & Next Steps

I am happy to say that I did successfully build a recommender engine that can take in an artist's name and recommend similar artists based on art tags that the artists share.

For next steps I would recommend adding art movements to the tags and include additional artworks from some of the departments that were filtered out during our initial cleaning and pre-processing. Lastly, I would like to see this recommender hosted on a website so that others can use it.