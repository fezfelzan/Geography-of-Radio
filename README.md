# Geography-of-Radio
================================================================================
        
        THE GEOGRAPHY OF RADIO:
       
       Real-time Radio Station Audio 
      Sampling, Processing, and Logging 
             as a Proxy for
      Spatiotemporal Popular Music Trends
================================================================================

30-09-21   Michael Felzan, GIS 8990, Fall 2021


Project Description:
  This project develops an ETL process for iteratively sampling radio station 
  streams to generate a database describing spatiotemporal trends of music 
  trends throughout the US. In particular, this ETL presents a process for 
  programmatically sampling mp3 audio clips of radio station stream URLs,
  identifying the songs playing in those sampled audio clips using a music
  recognition API, retrieving highly specific style/genre tags of each identified
  song from a music database API, determining the technical details about each
  radio tower (ERP, HAAT, distance given a specific dBu, geographic coordinates),
  and prepping all of this data to be interoperable in a GIS software like ArcGIS
  Pro. The website “radio.garden” is used as the main source of radio audio, while
  ACRCloud is used for the song recognition API, Discogs used for song 
  genre/style tag identification, and radio-locator.com for radio tower technical
  details.





GitHub Repo File Descriptions:


   - 'fezCC.js' -- copy of the javascript file lifted from the FCC 'FM and TV 
      Propagation Curve Calculator' website. (This file also exists in the
      'RadioTestRun' working directory on the Dropbox link)

================================================================================

(End)                  M.J. Felzan [8990]                            30-09-2021
