Application Classes and Libraries for using the UNMETERED APIs for Partners

Please refer to http://api.hostbillapp.com/ for basic account, ordering and support functions.

UNMETERED.Report - A Tool to Check Address for Available Solutions
##
# Call : checkAddress - Check Address and/or Generate Report

   
   
   Endpoint URL : //ajax.unmetered.io/report/check
   
   Input Fields ( HTTP POST or GET )
   
     apartment (optional) - Apartment or Unit Number
     houseNumber - Building or House Number
     vector - Street Direction (N, S, E, W, etc)
     street - Street Name (without Direction except in Calgary, AB, Canada)
     city - City / Municipality / Town Name
     province (if applicable) - State or Province
     country (default: Canada) - Service Country (Bangladesh, Canada, England, France, India, USA, etc)
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
# Call : orderURL - Generate Pre-Filled Ordering URL
   
   Input Fields ( HTTP GET or POST )
   
     GET Endpoint URL - //ajax.unmetered.io/report/order/[report-number]
     
     POST Endpoint URL - //ajax.unmetered.io/report/order
      
         id : report number

   Response Fields
 
     if "status : fail"
     
       status : fail
       info (if available) : remarks regarding failure

     else
     
       status : success
       browser will automatically redirect to order page in management portal

 
##

   
