# A1 - Data Curation

The goal of this project is to analyze Wikipedia traffic using data from the two Wikipedia REST API endpoints. The analyzed data goes from January 2008 through August 2020.

### Data Sources

Two data sources are used in this project.

* **Legacy Pagecounts API:** This API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides the monthly page views from Juanuary 2008 through July 2016, for desktop and mobile traffic.

* **Pageviews API:** This API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides the monthly views from July 2015 through August 2020, broken down into desktop, mobile app and mobile web. Unlike the legacy API, this source gives the user the opportunity to filter out crawlers data.


Text is available under the [Creative Commons Attribution-ShareAlike License](https://creativecommons.org/licenses/by-sa/3.0/); additional terms may apply. See [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en) for details on Wikimedia Foundation, as well as the [Terms and Conditions](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions) of the Wikimedia Foundation REST API.

### Output Data

The csv file generated after combining both data sources has the following columns:

| Column                  | Description                                                                     |
|-------------------------|---------------------------------------------------------------------------------|
| year                    | YYYY                                                                            |
| month                   | MM                                                                              |
| pagecount_all_views     | Sum of all views from Pagecounts API (legacy) for a specific month.             |
| pagecount_desktop_views | Total desktop views from Pagecounts API (legacy) for a specific month.          |
| pagecount_mobile_views  | Total mobile views from Pagecounts API (legacy) for a specific month.           |
| pageview_all_views      | Sum of all views from Pageviews API for a specific month.                       |
| pageview_desktop_views  | Total desktop views from Pageviews API for a specific month.                    |
| pageview_mobile_views   | Sum of mobile app and mobile web views from Pageviews API for a specific month. |


### Packages Requirements

The Jupyter Notebook uses the following packages:  

* json
* requests
* pandas: A version >= 1.0.3 is needed for use of json_normalize function
* numpy
* matplotlib


### Project License

Plese refer to the project [MIT license](LICENSE) for more details.


