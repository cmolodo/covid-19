# covid-19
This repository contains raw Covid-19 case data for some California counties, plus the Massachusetts data for counties and some cities, in .csv files.  Data was pulled from the [JHU project](https://github.com/CSSEGISandData/COVID-19), various state, county, and city public health and covid-19 websites and documents.  All data is taken either from the JHU project (prior to 2020-03-09 when they stopped collecting per-county data), or from official websites and documents on those websites, or from [WaybackMachine](https://web.archive.org/) archived snapshots of those websites (used to backfill data).  In some cases, back-filled data was entered by combing through past press releases announcing new cases.  Where press release information differs from JHU, press releases are used instead as JHU county numbers are not completely reliable.

Note that currently all data is entered by manual transcription rather than automatic scraping in part due to the lack of consistent data display.

Any empty cells represent dates for which data was not available, either because the website was not updated (for example, some sites only reported M/W/F) or because the WaybackMachine didn't contain a snapshot for the relevant dates.  When total case/death numbers don't change betwen one available time point and the next, values are automatically filled in between.

## Data sources:  

### California
#### State numbers
https://www.cdph.ca.gov/Programs/CID/DCDC/Pages/Immunization/nCoV2019.aspx  
https://www.cdph.ca.gov/Programs/OPA/Pages/New-Release-2020.aspx  
Live data entered as of 2020-04-01, backfilled using press releases.

#### Contra Costa County
https://www.coronavirus.cchealth.org/  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  

Case numbers corrected based on public health dashboard as of 2020-04-16, previously off by one day (daily numbers reported were actually from the previous day, mistakenly entered as being for the date reported).

#### Los Angeles County  
http://publichealth.lacounty.gov/media/Coronavirus/  
Testing numbers: http://publichealth.lacounty.gov/acd/docs/COVID19SurveillanceDataLAC.pdf  
Live data entered as of 2020-03-15, backfilled using press releases and WaybackMachine archive snapshots.

Because Los Angeles switched on 2020-04-24 from reporting numbers as of 12 PM that day to reporting numbers as of 8 PM the previous day, cases and deaths were adjusted accordingly.  Tracing back through archived snapshots, it appears that the switch happened on 2020-03-11, so cumulative numbers from that day have been removed (27 cases, 1 death) and all other numbers have been moved back 1 day.

Beginning 2020-04-28, Los Angeles County now provides a dashboard listing past numbers for cases and testing.  Note that unlike the case numbers currently recorded, these numbers do NOT include Long Beach and Pasadena, which have their own public health departments.  Past testing numbers updated to match values available from the dashboard, which include only electronically-reported testing.

#### Orange County  
https://www.ochealthinfo.com/phs/about/epidasmt/epi/dip/prevention/novel_coronavirus  
Live data entered as of 2020-03-15, backfilled using JHU to 2020-03-06 and WaybackMachine archive snapshots from 2020-03-06 to 2020-03-14.  Note that until 2020-03-15, values were only updatd Mon/Wed/Fri.

Orange County public health began publishing a full timeseries graph of case numbers with updated values, as of 2020-03-27.  Case numbers are amended to match updated data as it changes.

Disclaimer on website: "Data posted each day are always preliminary and subject to change. More information may become available as individual case investigations are completed."

#### Placer County  
https://www.placer.ca.gov/6448/Cases-in-Placer  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  Note that new data is only guaranteed to be released Mon/Wed/Fri.  

Placer county case numbers backfilled on 2020-04-14 based on historical data now available from the Placer public health dashboard.

#### Solano County  
http://www.solanocounty.com/depts/ph/ncov.asp  
Live data entered as of 2020-03-19, backfilled using press releases and WaybackMachine archive snapshots.  (No JHU data available for this county.)

Data for 2020-03-26 not available, PDF with data corrupted.

### Massachusetts

#### State/county
https://www.mass.gov/info-details/covid-19-cases-quarantine-and-monitoring  
Website provides county breakdown for cases in a PDF available from this site.  Death attributions to county are based on press release when available.  

Live data entered as of 2020-03-15, backfilled using JHU data and WaybackMachine archive snapshots.

Massachusetts reported no hospitalization numbers on 2020-04-14, switched to per hospital census in a separate report on 2020-04-15.

Massachusetts started providing weekly per-city cases on 2020-04-15, with previous day's numbers.

Until 2020-04-02, Dukes and Nantucket county cases were combined into a single figure.  As of 2020-04-02, they were split.  Separate numbers for each county were backfilled based on information from Martha's Vineyard and Nantucket hospital patient reports.  However, it appears that the state figures lag behind the local figures, as the combined reported cases are higher than the totals reported by the state.  Per-county numbers have been trimmed to match the state totals.

Unfortunately, deaths for Dukes and Nantucket are still reported combined.  Deaths are attributed based on couty websites, but may change as later data is collected, however.  
Martha's Vineyard (Dukes county): https://marthas-vineyard.com/coronavirus  
Martha's Vineyard hospital: https://www.mvhospital.com/health-resources/resources-and-information-on-coronavirus-covid-19  
Nantucket county: https://www.nantucket-ma.gov/1711/Covid-19-Day-to-Day-Timeline  
Nantucket hospital: http://nantuckethospital.org/home/coronavirus-news-and-information/nantucket-coronavirus-testing-updates/

Deaths affected:
* 2020-04-06 (attributed to Dukes)

##### Massachusetts Dashboard
Massachusetts started providing a "dashboard" on 2020-04-20, which changed the way much of the data was reported.

One new feature is reporting of state-wide daily cases, deaths, and testing numbers that are corrected moving forward as additional data comes in.  This is captured in the MA_state_daily.csv file.  Unfortunately, cases only go back to 2020-03-07, and testing only goes back to 2020-03-16.  However, since there were fewer than 10 cumulative cases on 2020-03-06 and fewer than 1000 cumulative tests on 2020-03-15, it's probably not a serious issue.  

One additional note on state-wide daily death numbers is that they differ significantly from the daily numbers calculated based on cumulative totals reported for each day.  This is because the daily deaths reflect the actual date of death rather than when the death was reported - there is a several day lag in reporting.

The dashboard also switched from reporting per-county daily deaths to per-county cumulative deaths.  As a result, some calculated cumulative numbers fluctutated as past deaths were reassigned to the correct counties.  (For example, Berkshire county apparently "lost" one death on 2020-04-20.)

On 2020-05-18, daily case and test numbers were changed from date reported to date tested, to more accurately reflect the number of people tested and the percent positive for each day.  

From the public health website:  
> Today, the Department will start releasing daily data charts that will sort the number of new COVID-19 cases and the number of new COVID-19 tests by the date of test, instead of by the date these metrics were reported to the Department.  DPH believes it is more precise and useful to present this data by how many people are getting tested each day and of those, how many tests are positive (making the person a case of COVID-19).

##### Quest Reporting Error
Due to a reporting error by Quest, a large backlog of test results were suddenly received around 2020-04-24.  Massachusettts backfilled daily state case and test numbers on 2020-04-24 with these previously missing reports based on when the results should have been reported, which affected case and test numbers dating back to 2020-04-13.  Note that the previously-entered cumulative case and testing numbers will now be incorrect.  Testing and state-wide case calculations should switch to use of the daily test numbers, which are updated with each published dashboard report.

Unfortunately, they did not similarly provide updates for county numbers, so all county case numbers from 2020-04-13 to 2020-04-23 are potentially lower than the actual numbers.


#### Arlington, MA  
https://www.arlingtonma.gov/departments/health-human-services/health-department/coronavirus-information  
Past updates: https://www.arlingtonma.gov/departments/health-human-services/health-department/past-coronavirus-updates  
Live data entered as of 2020-03-15, backfilled using past updates from website.  

No case numbers provided from 2020-03-21 through 2020-03-25.

Arlington started making past case numbers available on town health website as of 2020-04-16, updated data to match provided numbers.

#### Belmont, MA  
https://www.belmont-ma.gov/home/urgent-alerts/covid-19-information-for-the-town-of-belmont-find-all-updates-here  
Live data entered as of 2020-03-19, backfilled using prior notices and WaybackMachine archive snapshots.

#### Watertown, MA  
https://www.watertown-ma.gov/965/CORONAVIRUS  
Live data entered as of 2020-03-15, backfilled using past updates on page and WaybackMachine archive snapshots.  

Daily case number updates started sporadically on 2020-03-23.
