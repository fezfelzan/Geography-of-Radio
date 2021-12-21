# Geography-of-Radio
================================================================================
        
        THE GEOGRAPHY OF RADIO:
       
       Real-time Radio Station Audio 
      Sampling, Processing, and Logging 
             as a Proxy for
      Spatiotemporal Popular Music Trends
================================================================================

21-12-21   Michael Felzan, GIS 8990, Fall 2021


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

   In the "Code" repo :    
        - 'fezCC.js' -- copy of the javascript file lifted from the FCC 'FM and TV 
           Propagation Curve Calculator' website. It is used for calculating the
           distance you'd have to be from a radio tower (given a tower's ERP and
           HAAT) to receive a field strength of 60dBu (local coverage)
        - 'Final Geog of Radio Notebook (8990).ipynb' -- Jupyter Notebook which
           holds all of the code operations associated with this study
        - [rest of the files] : files needed to initiate ACRCloud API setup

================================================================================

(End)                  M.J. Felzan [8990]                            21-12-2021
