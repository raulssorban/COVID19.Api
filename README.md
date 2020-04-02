# COVID19.Api
A public API for getting latest informations and statistics of the Coronavirus spreading and global activity.

### How it works
Currently it just directly grabs and downloads the sources from GitHub and parses them through the API wrapper, generating a decent JSON object. I am using ticks for the time formatting, to avoid confusion for reversed european/american days/months.
Very soon after commiting this read-me, I'll implement caching so the requests will be practically instantaneous.

Use `&country` to filter countries/regions, `&province` to filter the province/state and/or `&city` to filder the city. These are all optional parameters, if none set, it'll return for ALL stats for countries, states and cities.

# Endpoints
|  Request  | Output  | Parameters |
| ------------ | ------------ | ------------ |
| https://167.86.121.152:15022/api/v1/covid19/yesterday | Get data of yesterday. | None and/or optional. |
| https://167.86.121.152:15022/api/v1/covid19/yesterdaytotal | Get total data of yesterday. | `&start` for start date and `&end` for end date using the example format: `28 03 2020` and/or optional. |
| https://167.86.121.152:15022/api/v1/covid19/daterange | Get data within a range. | None and/or optional. |
| https://167.86.121.152:15022/api/v1/covid19/datetotal | Get total data within a range. | `&start` for start date and `&end` for end date using the example format: `28 03 2020` and/or optional. |

### Examples
- [Austria Info (Yesterday)](https://167.86.121.152:15022/api/v1/covid19/yesterday?country=austria)
- [US, Massachusetts (Yesterday)](https://167.86.121.152:15022/api/v1/covid19/yesterday?country=us&province=massachusetts)
- [Romania (20th March to today)](https://167.86.121.152:15022/api/v1/covid19/datetotal?start=25%2003%202020&country=romania)

# Sources: 
> [CSSEGISandData/**COVID-19**](https://github.com/CSSEGISandData/COVID-19)
