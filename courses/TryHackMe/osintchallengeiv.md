# Digital Footprint — TryHackMe CTF  
I just completed the [Digital Footprint](https://tryhackme.com/room/osintchallengeiv?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=copy&sharerId=687937a5488df707cc460ae1) room on TryHackMe!  
This is a beginner-friendly OSINT Challenge.

## 1. Leaked Photo  
Download the image, extract metadata with ExifTool, find the coordinates (26°12'14.8"N 28°02'50.3"E), and paste them into Google Maps.  
The photo was taken in Johannesburg.  
Flag → THM{Johannesburg}

## 2. Archived Company Website  
Search online for: `warc-acme.com/jef/`, then open archive.org and check the **scandate** field → first archived date.  
Flag → THM{20160210224602}

## 3. Mysterious Landmark  
Open the image, it shows “The Spire of Dublin”. Search it on Google Maps and explore the surroundings until you find the building with the text “ARD OIFIG AN PHOIST”.  
Translate it: General Post Office  
Flag → THM{General Post Office}

## 4. Internal Documents  
Download the file and use ExifTool. In the metadata, there is a custom field: **markwilliams7243**.  
Search the username on Google → a YouTube channel appears. In the *About* section of the channel, the final flag is displayed.

Flag → THM{Y0u_f0und_7h3_fin4l_fl4g!}
