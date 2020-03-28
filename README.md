# covid-19
This repository contains raw Covid-19 case data for some California counties, plus the Massachusetts data for counties and some cities, in .csv files.  Data was pulled from the [JHU project](https://github.com/CSSEGISandData/COVID-19), various state, county, and city public health and covid-19 websites and documents.  All data is taken either from the JHU project (prior to 2020-03-09 when they stopped collecting per-county data), or from official websites and documents on those websites, or from [WaybackMachine](https://web.archive.org/) archived snapshots of those websites (used to backfill data).  In some cases, back-filled data was entered by combing through past press releases announcing new cases.  Where press release information differs from JHU, press releases are used instead as JHU county numbers are not completely reliable.

Note that currently all data is entered by manual transcription rather than automatic scraping in part due to the lack of consistent data display.

Any empty cells represent dates for which data was not available, either because the website was not updated (for example, some sites only reported M/W/F) or because the WaybackMachine didn't contain a snapshot for the relevant dates.  When total case/death numbers don't change betwen one available time point and the next, values are automatically filled in between.

## Data sources:  

### California

#### Contra Costa County
https://www.coronavirus.cchealth.org/  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  

#### Los Angeles County  
http://publichealth.lacounty.gov/media/Coronavirus/  
Testing numbers: http://publichealth.lacounty.gov/acd/docs/COVID19SurveillanceDataLAC.pdf  
Live data entered as of 2020-03-15, backfilled using press releases and WaybackMachine archive snapshots.

#### Orange County  
https://www.ochealthinfo.com/phs/about/epidasmt/epi/dip/prevention/novel_coronavirus  
Live data entered as of 2020-03-15, backfilled using JHU to 2020-03-06 and WaybackMachine archive snapshots from 2020-03-06 to 2020-03-14.  Note that until 2020-03-15, values were only updatd Mon/Wed/Fri

#### Placer County  
https://www.placer.ca.gov/6448/Cases-in-Placer  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  Note that new data is only guaranteed to be released Mon/Wed/Fri.  

Website unavailable in MA from 2020-03-22 to 2020-03-23.  Number of cases on 2020-03-23 based on other data reporting websites, in theory pulling from the same source.

#### Solano County  
http://www.solanocounty.com/depts/ph/ncov.asp  
Live data entered as of 2020-03-19, backfilled using press releases and WaybackMachine archive snapshots.  (No JHU data available for this county.)

Data for 2020-03-26 not available, PDF with data corrupted.

### Massachusetts

#### State/county
https://www.mass.gov/info-details/covid-19-cases-quarantine-and-monitoring  
Website provides county breakdown for cases in a PDF available from this site.  Death attributions to county are based on press release when available.  

Live data entered as of 2020-03-15, backfilled using JHU data and WaybackMachine archive snapshots.

#### Arlington, MA  
https://www.arlingtonma.gov/departments/health-human-services/health-department/coronavirus-information  
Past updates: https://www.arlingtonma.gov/departments/health-human-services/health-department/past-coronavirus-updates  
Live data entered as of 2020-03-15, backfilled using past updates from website.  

No case numbers provided from 2020-03-21 through 2020-03-25.

#### Belmont, MA  
https://www.belmont-ma.gov/home/urgent-alerts/covid-19-information-for-the-town-of-belmont-find-all-updates-here  
Live data entered as of 2020-03-19, backfilled using prior notices and WaybackMachine archive snapshots.

#### Watertown, MA  
https://www.watertown-ma.gov/965/CORONAVIRUS  
Live data entered as of 2020-03-15, backfilled using past updates on page and WaybackMachine archive snapshots.  

Daily case number updates started on 2020-03-23.
