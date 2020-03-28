# COVID19.Api
A public API for getting latest informations and statistics of the Coronavirus spreading and global activity.

### How it works
Currently it just directly grabs and downloads the sources from GitHub and parses them through the API wrapper, generating a decent JSON object. I am using ticks for the time formatting, to avoid confusion for reversed european/american days/months.
Very soon after commiting this read-me, I'll implement caching so the requests will be practically instantaneous.

# Endpoints
|  Request  | Output  |
| ------------ | ------------ |
| https://167.86.121.152:15022/api/v1/covid19/today | Get unfiltered data of today. Use `&country` to filter countries/regions, and/or use `&province` to filter the province/state. |
| https://167.86.121.152:15022/api/v1/covid19/yesterday | Get unfiltered data of yesterday. Use `&country` to filter countries/regions, and/or use `&province` to filter the province/state. |
| https://167.86.121.152:15022/api/v1/covid19/range | Get unfiltered data within a range. Use `&start` for start date and `&end` for end date using the example format: `03 28 2020`. Use `&country` to filter countries/regions, and/or use `&province` to filter the province/state. |

### Examples
- [Austria Info](https://167.86.121.152:15022/api/v1/covid19/data?country=austria)
- [US, Massachusetts](https://167.86.121.152:15022/api/v1/covid19/data?country=us&province=massachusetts)
- [Romania (20th March to today)](https://167.86.121.152:15022/api/v1/covid19/range?start=03%2025%202020&country=romania)

# Sources: 
> [CSSEGISandData/**COVID-19**](https://github.com/CSSEGISandData/COVID-19)
