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

On 2020-06-30, an additional 3842 cases were received, so the past daily counts were updated to include these new cases.

#### Contra Costa County
https://www.coronavirus.cchealth.org/  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  

Case numbers corrected based on public health dashboard as of 2020-04-16, previously off by one day (daily numbers reported were actually from the previous day, mistakenly entered as being for the date reported).

As of 2020-09-08, case and test numbers now listed by collection date rather than date reported to the department.  Similarly, deaths now listed by date of death rather than date reported to the department.  All numbers for the last 7 days are considered incomplete, as they are still being reported.  
Updated past numbers to match newly available values, EXCEPT for total deaths.  Since only daily deaths are listed with past values, past total deaths aren't updated, and will continue to reflect total reported deaths moving forward.

Cumulative deaths not available for 2020-12-24, interpolated based on numbers for 2020-12-23 and 2020-12-25.

Date not available for 2021-03-12.  Total deaths for that date filled in by extrapolating.  All other numbers are reported with all history every day, so were filled in the following day.


#### Los Angeles County  
http://publichealth.lacounty.gov/media/Coronavirus/  
Testing numbers: http://publichealth.lacounty.gov/acd/docs/COVID19SurveillanceDataLAC.pdf  
Live data entered as of 2020-03-15, backfilled using press releases and WaybackMachine archive snapshots.

Because Los Angeles switched on 2020-04-24 from reporting numbers as of 12 PM that day to reporting numbers as of 8 PM the previous day, cases and deaths were adjusted accordingly.  Tracing back through archived snapshots, it appears that the switch happened on 2020-03-11, so cumulative numbers from that day have been removed (27 cases, 1 death) and all other numbers have been moved back 1 day.

Beginning 2020-04-28, Los Angeles County now provides a dashboard listing past numbers for cases and testing.  Note that unlike the case numbers currently recorded, these numbers do NOT include Long Beach and Pasadena, which have their own public health departments.  Past testing numbers updated to match values available from the dashboard, which include only electronically-reported testing.

Added hospitalization numbers using data provided on the LA County dashboard as of 2020-06-30, backfilling with those numbers.  Note that these numbers do NOT include Long Beach or Pasadena, which maintain separate reporting.  Long Beach hospitalization numbers added and backfilled as of 2020-06-30.  Pasadena does not (as of 2020-07-01) report hospitalization numbers.

Test number reporting changed as of 2020-07-01 - the LA Department of Public Health now reports persons tested separately from tests performed, since some people will be tested multiple times.  The numbers also changed significantly.

Data for LA County not reported from 2020-07-03 through 2020-07-06, as they took the system offline to improve the data processing systems.

Hospitalization data not updated on LA public health dashboard after 2020-07-23.  Hospitalization numbers taken from California public health dashboard, which includes per-county hospitalization counts.

Data for 2020-12-24 not provided due to Christmas holiday.  Cumulative case and death numbers interpolated from 12-23 and 12-25 data, daily case and death numbers then calculated based on cumulative.

Detailed daily cases and test data not available for 2021-02-17 - despite the dashboard stating the data is through 2021-02-17, it only included up to 2021-02-16.

Due to reporting issues, a backlog of ~900 previously unreported deaths was added to the total on 2021-02-23.  These deaths actually occurred in the previous months.

The data dashboard for 2021-03-05 didn't include updated numbers for persons tested or tests by date, values not added.

The data dashboard for 2021-03-06 numbers for persons tested is from 2021-03-05, not 2021-03-06.  Added numbers for previous day since they weren't available before, but persons tested remains 1 day behind.

The data dashboard appears to have technical issues starting 2021-03-31, couldn't connect to the server so couldn't retrieve data for test numbers beginning 2021-03-30.  Issue finally resolved by 2021-04-04, data available for 2021-04-03.

The Locations & Demographics page used as source for reported daily/total cases and deaths appears to have an issue on 2021-04-20 - although it claims that the data was updated, the numbers are all identical to the values from 2021-04-19.

##### Long Beach

Daily data collection for Long Beach paused after 2021-03-15 due to technical difficulties with the dashboard - updated daily values not available.


#### Orange County  
https://www.ochealthinfo.com/phs/about/epidasmt/epi/dip/prevention/novel_coronavirus  
Live data entered as of 2020-03-15, backfilled using JHU to 2020-03-06 and WaybackMachine archive snapshots from 2020-03-06 to 2020-03-14.  Note that until 2020-03-15, values were only updatd Mon/Wed/Fri.

Orange County public health began publishing a full timeseries graph of case numbers with updated values, as of 2020-03-27.  Case numbers are amended to match updated data as it changes.

Disclaimer on website: "Data posted each day are always preliminary and subject to change. More information may become available as individual case investigations are completed."

As of 2020-06-24, Orange County significantly changed its display and the counts of testing and cases, removing the previously-available tables.  Unfortunately, the display only includes numbers back to 2020-04-26.  Numbers have been back-updated to that point, but may be incorrect before that.
*  Removed the daily cases by date reported, replaced with daily cases by specimen collection date.  Daily cases by date reported will continue to be tracked based on the dashboard daily number, but will no longer be back-updated.
*  Number of cumulative cases significantly modified (down).
*  Cumulative test counts switched from date reported to specimen collection date, numbers significantly lower.

As of 2020-06-25, the old dashboard and figures are back...not sure what happened the previous day.

As of 2020-06-26, the *new* reporting system is back again, with lower case and testing numbers!  Not sure what's going on, there's no provided info or explanation for the changing reporting on the website.

With the new system, I will no longer be updating past numbers, to avoid further confusion, only adding the new daily and cumulative totals reported each day.  The exception is hospitalization - updated past numbers back to 2020-06-12, the earliest date displayed on the dashboard.

As of 2020-09-03, reported cumulative case numbers are separated into PCR only (reported to state) vs antigen positive.  Daily case numbers are now PCR only.  
The timeseries data will now include the sum of PCR + antigen positive cases, though neither this nor the PCR-only cumulative number matches the past cumulative counts, so the case numbers don't exactly match between 2020-09-02 and 2020-09-03.

On 2020-12-29, shifted OC testing numbers forward one day so that the date reflects the date reported, not the cumulative total as of date collected, since all the actual numbers are reported totals, not collection date totals - this way it also matches the date of reported cases and deaths.

Values for 2021-01-01 not provided due to the holiday, calculated by interpolating between 2020-12-31 and 2021-01-02.

Values for 2021-01-03 not provided due to server upgrades, calculated by interpolating between 2021-01-02 and 2021-01-04.

Values for 2021-01-18 not provided due to the holiday, calculated by interpolated between 2021-01-17 and 2021-01-19.

Values for 2021-02-12 not provided on the dashboard due to the holiday (?not sure why, President's Day is 02-15), though separate numbers for daily cases, deaths, and tests on 02-12 and 02-13 were both reported on the main web page 02-13.  Antigen cases not available, since that's only reported on the dashboard.

Similar to 2021-02-12, values for 2021-02-15 not provided on the dashboard due to President's Day, but daily case, death, and testing numbers provided later.

Death reporting lower than actual values starting on 2021-02-23 due to technical issues.  Noted as resolved on 2021-03-17.

Missed values for 2021-02-28, able to calculate previous numbers based on daily values for 2021-03-01, but couldn't calculate cumulative antigen cases as no daily number provided.  Calculated total antigen cases by interpolating between 2021-02-27 and 2021-03-01.

Values for 2021-04-04 not provided due to the holiday.

#### Placer County  
https://www.placer.ca.gov/6448/Cases-in-Placer  
Live data entered as of 2020-03-19, backfilled using JHU data, press releases, and WaybackMachine archive snapshots.  Note that new data is only guaranteed to be released Mon/Wed/Fri.  

Placer county case numbers backfilled on 2020-04-14 based on historical data now available from the Placer public health dashboard.

As of 2020-10-02, data will only be reported Mon-Fri, new numbers will no longer be available for Sat/Sun.

#### Solano County  
http://www.solanocounty.com/depts/ph/ncov.asp  
Live data entered as of 2020-03-19, backfilled using press releases and WaybackMachine archive snapshots.  (No JHU data available for this county.)

Data for 2020-03-26 not available, PDF with data corrupted.

Data only reported Mon-Fri, new numbers not available for Sat/Sun.

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

No data was provided for 2020-08-23, due to a server/system upgrade over the weekend.  Numbers are linearly interpolated based on values 2020-08-22 and 2020-08-24 and adjusted to match state total, since the reported daily numbers for 2020-08-24 simply reflect the difference between 2020-08-24 and 2020-08-22 rather than true daily values.

Due to a technical issue, 24800 lab results (positive and negative) were delayed and could not be included in the 2021-01-29 report, but are included in the 2021-01-30 report.  The numbers for 2021-01-29 are therefore artifically lower than reality, and the numbers for 2021-01-30 are artifically higher.

Due to a reporting issue, on 2021-03-02 863 cases previously counted positive have been corrected to be negative and removed from the total confirmed cases.


##### Quest Reporting Error
Due to a reporting error by Quest, a large backlog of test results were suddenly received around 2020-04-24.  Massachusettts backfilled daily state case and test numbers on 2020-04-24 with these previously missing reports based on when the results should have been reported, which affected case and test numbers dating back to 2020-04-13.  Note that the previously-entered cumulative case and testing numbers will now be incorrect.  Testing and state-wide case calculations should switch to use of the daily test numbers, which are updated with each published dashboard report.

Unfortunately, they did not similarly provide updates for county numbers, so all county case numbers from 2020-04-13 to 2020-04-23 are potentially lower than the actual numbers.


##### Probable Cases Added
On 2020-06-01, per CDC guidance, department of public health added probable cases and deaths to confirmed totals, following a retrospective review dating back to 2020-03-01.

From the public health website:
> Today, the Department of Public Health will begin reporting both confirmed and probable COVID-19 cases and deaths. This change is in accordance with guidance from the Centers for Disease Control to include “probable” COVID-19 cases and deaths in data collection and reporting efforts.

> This change will increase the number of cases and deaths reported in Massachusetts. Today’s newly reported totals are a result of a retrospective review of probable cases and deaths dating back to March 1, 2020.

Total number of confirmed and probable deaths decreased as of 2020-06-30 due to removal of duplicate reports.

##### Probable Cases and County Numbers Removed
As of 2020-08-12, Massachusetts no longer provides daily probable cases or per-county case or death numbers.  These numbers have been moved to the weekly report or simply removed altogether.  Interestingly, the total deaths in the daily dashboard **DOES** still include probable deaths.

Probable cases are now available only in the weekly report.

Similarly, cumulative confirmed cases per county are now available only in the weekly report.  However, these numbers don't match reported values before 2020-08-12 because they only include confirmed cases, not probable cases, and there's no back-reporting of per-county splits between probable and confirmed cases, so there's no way to reconcile the numbers.

Cumulative deaths per county are no longer available anywhere.  The weekly report only includes deaths per county for the last 2 weeks.

##### County Numbers Added
As of 2020-08-19, county cases and deaths have been added, both daily and cumulative counts.  However, the case numbers reflect only confirmed cases rather than including both probable and confirmed cases, so they're not comparable to the numbers from the last two months, and have not been added to the existing spreadsheet.  Deaths continue to include both probable and confirmed cases.

To avoid a gap and difficulty in calculating daily deaths, the per-county cumulative deaths have been calculated to interpolate along a straight line between 2020-08-11 (the last reported date) to 2020-08-19.

County deaths also interpolated for 2020-08-23, when the public health department provided no data due to a server/system upgrade.

##### Probable Case Definition Changed
As of 2020-09-02, the definition of "probable" cases has changed to match the definition released 2020-08-06 by the Council of State and Territorial Epidemiologists.  It now includes only individuals with one of the following:
*  Positive antigen test
*  Covid-19 listed as underlying or contributing cause of death
*  Appropriate symptoms and likely exposure

Past reporting of probable cases has been updated to match this new definition, and satte-wide probable cases have been added back to the daily dashboard.  Per-county probably cases still not available.

##### Dashboard Changes 2020-11-02
As for 2020-11-02, numbers available on the dashboard and in the accompanying source files have been modified.  

The number of total individuals tested is no longer reported on the dashboard, though it's still included in the Testing2.csv source file under "Molecular Total".

Antibody testing numbers are no longer reported, either in the dashboard or the source files.

##### Holiday Reporting
Due to the Thanksgiving holiday, no dashboard was published for 2020-11-26.  Instead, the report provided 2020-11-27 contained the aggregate across both days.  To prevent a gap in the state and county numbers for Thanksgiving, values have been filled in by interpolating between 11-25 and 11-27.

Due to the Christmas holiday, no dashboard was published for 2020-12-25.  Instead, the report provided 2020-12-26 contained the aggregate across both days.  Filled in values by interpolating between 12-24 and 12-26.

Similarly, due to the New Years holiday, no dashboard was published for 2021-01-01.  Instead, the report provided 2021-01-02 contained the aggregate across both days.  Filled in values by interpolating between 2020-12-31 and 2021-01-02.

Due to the Easter holiday, no dashboard data was available for 2021-04-04.

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

## Vaccination

### CDC
https://covid.cdc.gov/covid-data-tracker/#vaccinations

As of 2021-02-22, the CDC stopped reporting distributed doses.  They instead started reporting "delivered" doses, but no longer provided this information per jurisidiction, only for the entire country.

As of 2021-02-26, the CDC began reporting distributed doses per state again.

### California
https://covid19.ca.gov/vaccines/

From the CA website:  
Once a week, the federal government announces anticipated allocation figures for each state. The number of allocated doses provided by the federal government is a projection and subject to change. Local providers are required to place their orders which are reviewed by the state and submitted to the federal government. The federal government then authorizes the order and submits the request to the manufacturer. The manufacturer or central distributor ships the vaccine directly to local providers. It can take a week or longer for allocation by the federal government to arrive at public health offices or providers for administration.

*  Doses ordered = doses requested by the state, in an order submitted to the federal Warp Speed vaccine management program  
*  Doses shipped = doses marked by the federal program as having been ordered from the manufacturers, to be shipped directly to the states  
*  Doses delivered = doses received by the state facilities

Prior to 2021-02-01, doses ordered and shipped did NOT include doses distributed as part of the CDC Long Term Care (LTC) program.  However, starting 2021-02-01, doses shipped and delivered DO include doses from the LTC program.  Also, starting 2021-02-01, doses ordered was no longer reported, replaced with doses delivered.