Application Classes and Libraries for using the UNMETERED APIs for Partners

Please refer to http://api.hostbillapp.com/ for basic account, ordering and support functions.

UNMETERED.Report - A Tool to Check Address for Available Solutions
##
# Check Address and/or Generate Report

   Call Name : checkAddress
   
   Endpoint URL : //ajax.unmetered.io/report/check
   
   Input Fields ( HTTP POST or GET )
   
     apartment (optional) - Apartment or Unit Number
     houseNumber - Building or House Number
     vector - Street Direction (N, S, E, W, etc)
     street - Street Name (without Direction except in Calgary, AB)
     city - City / Municipality / Town Name
     province (if applicable) - State or Province (if Service Address Country has States)
     country (default: Canada) - Service Country (Bangladesh, Canada, India, France, USA, etc)
     partner - Affiliate / Coupon / Partner Code to Pre-Fill into Transaction
     
   Response Fields - There are 3 possible results to a "Check Address" query : fail, similar, exact
   
     if "status : fail"
   
       status : fail
       result : error message passed from lookup partner(s)
     
     if "status : similar"
     
       status : similar
       result : array of similar valid service address(es)
       
     if "status : exact"
     
       status : exact
       result : id number of report for requested service address
       
##
# Generate Pre-Filled Ordering URL

   Call Name : orderURL
   
   Input Fields ( HTTP GET or POST )
   
     GET
       
       Endpoint URL - //ajax.unmetered.io/report/order/[report-number]
     
     ##
     
     POST
       
       Endpoint URL - //ajax.unmetered.io/report/order
       
         id : report number value
 
##

   
