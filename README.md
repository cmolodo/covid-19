# covid-19
This repository contains raw Covid-19 case data for some California counties, plus the Massachusetts data for counties and some cities, in .csv files.  Data was pulled from the [JHU project](https://github.com/CSSEGISandData/COVID-19), various state, county, and city public health and covid-19 websites and documents.  All data is taken either from the JHU project (prior to 3/9 when they stopped collecting per-county data), or from official websites and documents on those websites, or from [WaybackMachine](https://web.archive.org/) archived snapshots of those websites (used to backfill data).  In some cases, back-filled data was entered by combing through past press releases announcing new cases.

Note that currently all data is entered by manual transcription rather than automatic scraping in part due to the lack of consistent data display.

Any empty cells represent dates for which data was not available, either because the website was not updated (for example, some sites only reported M/W/F) or because the WaybackMachine didn't contain a snapshot for the relevant dates.

## Data sources:  
### California
Contra Costa County  
https://www.coronavirus.cchealth.org/  
Live data entered as of 3/19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.

Los Angeles County  
http://publichealth.lacounty.gov/media/Coronavirus/  
Testing numbers: http://publichealth.lacounty.gov/acd/docs/COVID19SurveillanceDataLAC.pdf  
Live data entered as of 3/15, backfilled using press releases and WaybackMachine archive snapshots.

Orange County  
https://www.ochealthinfo.com/phs/about/epidasmt/epi/dip/prevention/novel_coronavirus  
Live data entered as of 3/15, backfilled using JHU to 3/6 and WaybackMachine archive snapshots from 3/6-3/14.  Note that until 3/15, values were only updatd Mon/Wed/Fri

Placer County  
https://www.placer.ca.gov/6448/Cases-in-Placer  
Live data entered as of 3/19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  Note that new data is only guaranteed to be released Mon/Wed/Fri.

Solano County  
http://www.solanocounty.com/depts/ph/ncov.asp  
Live data entered as of 3/19, backfilled using press releases and WaybackMachine archive snapshots.  (No JHU data available for this county.)

### Massachusetts
State/county (includes per-county breakdown usually reported in a PDF available from this site)  
https://www.mass.gov/info-details/covid-19-cases-quarantine-and-monitoring  
Live data entered as of 3/15, backfilled using JHU data and WaybackMachine archive snapshots.

Arlington, MA  
https://www.arlingtonma.gov/departments/health-human-services/health-department/coronavirus-information  
Past updates: https://www.arlingtonma.gov/departments/health-human-services/health-department/past-coronavirus-updates  
Live data entered as of 3/15, backfilled using past updates from website.

Belmont, MA
https://www.belmont-ma.gov/home/urgent-alerts/covid-19-information-for-the-town-of-belmont-find-all-updates-here  
Live data entered as of 3/19, backfilled using prior notices and WaybackMachine archive snapshots.

Watertown, MA  
https://www.watertown-ma.gov/965/CORONAVIRUS  
Live data entered as of 3/15, backfilled using past updates on page and WaybackMachine archive snapshots.
