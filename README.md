# HCDS 512 Assignment 1 - Data curation

# Goal of the project


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

Note that the data from the Pageview API excludes spiders/crawlers and limites to users only, but the data from the Pagecounts API is the combination of all kinds of traffic.
