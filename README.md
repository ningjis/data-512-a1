# HCDS 512 Assignment 1 - Data curation

# Goal of the project
The goal of this projrct is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2021. In this project, data about Wikipedia page traffic from two different Wikimedia REST API endpoints are combined into a single dataset.Some simple data processing steps are performed on the data, and the analysis is done based on tbe processsed data. All steps are performed in a single Jupyter notebook, `hcds-a1-data-curation.ipynb`. The five JSON-formatted source data file is available, with the naming convention for the source data files being `apiname_accesstype_firstmonth-lastmonth.json`, and the analysis is done based on `en-wikipedia_traffic_200712-202108.csv`, with the final result shown in `result.png`.

# License of Source Data


# APIs
* Wikimedia Legacy Pagecounts API : https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
* Wikimedia Pageviews API : https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

# Curated Data

The processed data are stored into a single CSV file with the following headers:

| Column | Value | 
| ------ | ------ |
| year | YYYY | 
| month | MM | 
|pagecount_all_views| Number of views for all clients reported by the (Legacy) Pagecounts API |
|pagecount_desktop_views | Number of views for desktop clients reported by the (Legacy) Pagecounts API |
|pagecount_mobile_views	| Number of views for mobile clients reported by the (Legacy) Pagecounts API |
|pageview_all_views| Number of views for all clients reported by the Pageviews API |
|pageview_desktop_views| Number of views for desktop clients reported by the Pageviews API |
|pageview_mobile_views| Number of views for mobile-app and mobile-web clients reported by the Pageviews API |

# Known Issues & Special Considerations

1. Note that the data from the Pageview API excludes spiders/crawlers and limites to users only, but the data from the Pagecounts API is the combination of all kinds of traffic.

2. Note that there was about 1 year of overlapping (from July 2015 to July 2016) traffic data between the two APIs, resulted in a spike in the figure during the analysis step.
