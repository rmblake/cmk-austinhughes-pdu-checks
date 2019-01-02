# Check_MK Checks for Austin Hughes PDU Bars


Update 2019-01-02 - Due to no longer working in a check_mk/austin-hughes environment I'm not best placed to maintain this - as of this update this script still works AFAIK (Although at the role I was in production AH PDU bars never made it onto a management network due to OOB networking being bikeshedded out of the agenda), but I won't be able to accept any commits/updates or provide support going forward unless I land myself back in a similar environment!

## Introduction

These scripts are for monitoring Austin Hughes InfraPower PDU bars connected by an IP Dongle (The IPD-02-S). Tested with version Q216V3 (Released June 2016), and a V28C13/6C19-32A-WSi PDU bar. 

There are four checks: One for PDU state (As you can chain up to 16), One for circuit state (As 32A/3 Phase PDUs present multiple circuits), and one for each of 
standard/C19 socket states. Sockets that are turned off are considered critical. Performance data is kept (Power/Voltage/Current) where it is available, and WARN 
alarms are sent if a socket goes into an alarm state.

## How to use
Copy scripts into your /omd/sites/<instance>/local/share/check_mk/checks directory, add or re-inventorise your IP dongle in check_mk, and checks should appear. 

