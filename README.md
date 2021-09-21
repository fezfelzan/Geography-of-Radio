# Geography-of-Radio
================================================================================
         THE GEOGRAPHY OF RADIO:
       
       Real-time Radio Station Audio 
      Sampling, Processing, and Logging 
             as a Proxy for
      Spatiotemporal Popular Music Trends
================================================================================
20-09-21   Michael Felzan, GIS 8990, Fall 2021


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

!!!!!NOTE !!! !  !: The RadioTestRun 'working directory' folder talked about in 
     this README file was too large to include in this GitHub repo -- I have 
     posted this folder on my personal Dropbox. Link:


       https://www.dropbox.com/sh/4t690q7cio1thqo/AAD8htMXRI72Jl9kETuV27lKa?dl=0




GitHub Repo File Descriptions:

   - 'Felzan_Final_Report_5572.docx' -- Final Report document
   - 'Felzan_RadioGarden_Final.ipynb' -- copy of the final Jupyter Notebook 
      containing all of this project's code (there is also a copy in the Dropbox
      'RadioTestRun' repo)
   - 'Radio Garden ETL Flow Map.png' -- main ETL flow map image used in 5572 final 
      report
   - 'fezCC.js' -- copy of the javascript file lifted from the FCC 'FM and TV 
      Propagation Curve Calculator' website. (This file also exists in the
      'RadioTestRun' working directory on the Dropbox link)



Message about 'RadioTestRun' Working Directory included on Dropbox link:
  As of now, the project working directory titled 'RadioTestRun' included thru the 
  Dropbox link is not 'blank' -- it contains a combination of the 'startup files' 
  and the files created via running the project code contained in the Jupyter 
  Notebook. The  Jupyter Notebook is organized in a way so that, if the user is 
  running the Notebook at the base of the project working directory, and the 
  working directory has all of the necessary startup files, the user may just 
  input their own directory path and API keys at the top of the Notebook, and the 
  rest of the Notebook should run properly. However, because I'm not yet confident 
  this script would fully run properly on another computer, I want to provide a 
  repository/ Notebook that includes proof of the data I've compiled with the script. 
  This working directory repo is therefore more of a display, of the files necessary 
  to run this project's ETL, and the kinds of files that are produced using it.


'RadioTestRun' Working Directory File Descriptions:
   - ['acrcloud'] -- this folder is the result of running the setup.py, and contains
   the ACRCloud modules (recognizer.py) needed to identify track names via audio 
   clips using the ACRCloud API.
   - ['build'] -- this folder is additionally related/ necessary to the above 
   'acrcloud' functionality.
   - ['dist'] -- this folder is additionally created from running the ACRCloud
   'setup.py' 
   - 'Felzan_RadioGarden_Final.ipynb' -- this is ~the~ project Jupyter Notebook.
   - 'fezCC.js' -- the javascript file that was lifted/reworked from the FCC
   'FM and TV Propagation Curve Calculator' website. This file is used/opened/
    parameterized within the Jupyter Notebook to calculate distance from a 
    radio tower to receive a field strength of 60 dBu, given specific HAAT
    and ERP values.
   -['pyacrcloud.egg-info'] -- if I remember correctly, this file is ALSO created
   after running the ACRCloud 'setup.py'
   -'setup.py' -- this Python file is run at the command line to properly install
    the ACRCloud packages, so that 'recognizer.py' may be imported.
   -['StationInfoTables'] -- this folder is created by the Jupyter Notebook. It
    houses .CSV files for every station which contain the station tower's technical 
    details (lat/long; ERP; HAAT; Dist @ 60dBu)
   -['STATIONS'] -- this folder contains folders for every radio station. Every 
    radio station must have a folder and a .txt file set up (containing the stream
    URL on the .txt file's second line) in order for the Jupyter Notebook to run
    properly. The .txt file also serves as the track play log for each station.
   -'test.py' --  pretty sure this file is not necessary (came along with the 
    ACRCloud installation files), but I included it for good measure
   


================================================================================
(End)                  M.J. Felzan [8990]                            20-09-2021
