##HTTP Response Scavenger Hunt

####Assignment

For this Lab you will be making HTTP requests in your terminal using **curl** and scavenging for data in the response you get back. **curl** is short for "Client for URL's" and is a tool that allows us to make HTTP requests in our terminal.  

___________________________________________

**Phase 1: Make a GET request to google**

In terminal:

`curl -v https://www.google.com`

Find your response header

  **1.** What status did you get back?  
    200 OK
  **2.** What content-type did you get back?  
    text/html; charset=ISO-8859-1
  **3.** What came after the key "Set-Cookie"?  
      NID=67=AwKD2LfZtSPZW7IPU4sFotOUj7qzKmcrzMZ2r-SALqqgUs3Ub91-xkbsjVuPQ8xW8kafijf3YPuQiSoqd4vZIozOmMsHzakCift4s32UJN2FBQk-rP-NWxXoWGTUiGE0; expires=Wed,
  **4.** What date did this request come back on?  
    15-Oct-2014 21:48:00
  **5.** What came after the key "Transfer-Encoding?"  
    chunked

Find your response body

  **1.** What was the first line in your response body?  
  17259,4000116,4003510,4007661,4007830,4008067,4008133,4008142,4009016,4009033,400
_______________________________________________

**Phase 2: Make a GET request to the OMDBAPI**

In terminal:

`curl -v http://www.omdbapi.com`  

Find your response header

  **1.** What status did you get back?  
      200 OK
  **2.** What content-type did you get back?  
     text/html; charset=utf-8
  **3.** What was your content length?  
     11859
  **4.** What date did this request come back on?  
    Tue, 15 Apr 2014 21:52:24 GMT
Find your response body

  **1.** What was the first line in your response body?  
  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
___________________________________________________

**Phase 3: Make a GET request to the OMDBAPI with parameters**

In terminal:  

`curl -v http://www.omdbapi.com/?s=Titanic`

Find your response header

  **1.** What status did you get back? 
    200 OK 
  **2.** What content-type did you get back?
    text/html; charset=utf-8
  **3.** What was your content length?  
    792
Find your response body

  **1.** Look at the data that came back. What data structures do these look like?  strings
  **2.** What year did Titanic II come out?  
    2010

_______________________________________________________________________

**Phase 4: Make a GET request to the OMDBAPI with different parameters**

Now search for one of your favorite movies.

`%20*`

*If the title of your favorite movie has spaces, replace these with %20*  
i.e. `curl -v http://www.omdbapi.com/?t=the%20matrix` 

Find the response header  

  **1.** What was the Cache-Control?  
    no-cache
  **2.** What value is after the key Expires?  
  -1

Find the response body

  **1.** What year was your favorite movie released?  
      1990
  **2.** What was your favorite movie rated?  
  "PG-13"
