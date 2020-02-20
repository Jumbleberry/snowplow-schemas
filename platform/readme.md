# Jumbleberry-Platform Tracking Events

## Events

| Event Name | Event Description | Parameters | 
| --- | --- | --- |
| `home_export` | When a user clicks Export button from dashboard view | `campaign_name`,<br/> `campaign_id`,<br/> `date_range`|
| `campaign_export` | When a user clicks Export button from campaign-performance view | `campaign_name`,<br/> `campaign_id`,<br/> `date_range`|
| `campaign_click` | When a campaign is viewed from search bar or Discover view | `campaign_name`,<br/> `campaign_id`,<br/> `featured_campaign`,<br/> `recommended_campaign`,<br/> `new_campaign`,<br/> `verticals`,<br/> `countries`,<br/> `features`|
`search` | When users click on filter button from Discover view  | `verticals`,<br/> `countries`,<br/> `features`, <br/>  `refine`|
`apply` | When users click on apply-to-run button from campaign view | `campaign_name`,<br/> `campaign_id`,<br/> `verticals`,<br/> `countries`,<br/> `features`|
`report_campaign` | when a user clicks on filter-report button from campaign report | `date_range`,<br/> `campaigns` |
`report_sub` | when a user clicks on filter-report button from sub id report | `date_range`, <br/> `campaigns`, <br/>  `groups`|
`submit` | when a user submits application to run a campaign | `campaign_name`,<br/> `campaign_id`,<br/> `verticals`,<br/> `countries`,<br/> `features`, <br/> `expected_epc`|



## Parameters

| Parameter Name | Parameter Description | 
| --- | --- |
|`campaign_name` | name of the campaign from hitpath |
|`campaign_id` | campaign_id from hitpath |
|`featured_campaign` | when a user clicked on a campaign under featured campaigns (boolean type) |
|`recommended_campaign` | when a user clicked on a campaign under recommended campaigns (boolean type) |
|`new_campaign` | when a user clicked on a campaign under new campaigns (boolean type) |
`verticals` | a list of objects that contains vertical name(s) associated with the events (`campaign_click`, `filter_campaign`, `apply`, `submit`) |
|`countries` | a list of objects that contains country code(s) associated with the events (`campaign_click`, `filter_campaign`, `apply`, `submit`) |
|`expected_epc` | a list of objects that contains epc values associated with `submit` event  |
|`features` | a list of objects that contains feature name(s) associated with the event (`search`) |
|`refine` | associated with the event (`search`) and contains `refine_type`, `min` and `max` |
|`date_range` | associated with `report_sub` or `report_campaign` event, to show the date range which includes `range_type` that contains list of objects and `start_date` and `end_date` |
|`campaign_filter` | a string of campaign id(s) separated by comma, associated with `report_sub` or `report_campaign` event |
|`groups` | associated with `report_sub` event, to show if a user aggregates the data by `campaign`, `funnel`, `c1`, `c2`, and/or `c3` |
