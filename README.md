# Cle-Elum-Ridge
README - metadata, 24 July 2023 (Data processed by John Cramblitt, jcramb@uw.edu)

Eastern Cascades Forest-Snow Observations 2022-2023

&nbsp;
&nbsp;

**Processed Camera Data** - Daily snow depth measured using 5cm increments on 3 poles at each of 12 sites, fractional forest snow cover area, and canopy 
                        snow presence all extracted from daily time-lapse images.  
                        
**Snow Disappearance Date and Gap Fraction** - Snow Disappearance Date calculated using camera data or ground temperature sensors and canopy gap fraction 
                        calculated as a percentage of total pixels in a hemispherical image which are sky. 
                        
**Cleaned Temprature Data** -  Time series of temprature data recorded by 10 HOBO sensors at each site (9 placed ground level and one in a tree measuring 
                        air temperature).

**Software Used** - ImageJ with the Hemispherical 2.0 Plugin to threshold hemispherical images, and Gap Light Analyzer 2.0 to calculate site openness.


&nbsp;
&nbsp;

## **List of abbreviations/headers**

**CN:**		Cle Elum North

**CS:**		Cle Elum South 

**Site:**		Refers to the ridge aspect (North or South)

**Plot:**		Refers to the individual 10m x 10m grids, which are labeled by basal area factor

**Position:**	Refers to the location within a plot. A numerical value refers to the position of a temprature sensor, pole values such as "pole1" refers to 
          the position of a pole
          
**LocationID:**	Identifier including site, plot, and position. For instance, CN-20-1 refers to stake 1 at the Cle Elum North ridge site with a basal area factor 
            of 20 and CN-20-pole1 refers to pole 1 at this same site. 
            
**LocID:**		Identifier including site, plot, and CamID used in timelapse camera processing.

**BAF:**		Basal area factor

**CamID:**		Camera ID: unique to each camera (typically camera model and a number)

**Zopudate:**	Date recorded by ZOPU camera 

**Zoputime:**	Time recorded by ZOPU camera

**Garddate:**	Date recorded by GARD camera

**Gardtime:**	Time recorded by GARD camera

**Pole1obs:**	Snow depth measured relative to half-meter marks 

**Pole1:**		Snow depth adjusted for how much of the pole is underground 

**FSCA:**		Fractional snow cover area: refers to the area of the 10x10 plot that is covered with snow (measured with visual best esimate)

**Canopy_snow:**	Recorded as a y/n value for presence of snow in the canopy (measured with visual best esimate)

**median_gapf:**	The median gap fraction value taken from all the gap fractions calculated for each individual LocationID   

**min_gapf:**	The minimum gap fraction value taken from all the gap fractions calculated for each individual LocationID  

**max_gapf:**	The maximum gap fraction value taken from all the gap fractions calculated for each individual LocationID  

**SiteOpenness:** Output from Gap Light Analyzer 2.0, giving the percent of a site that is canopy 

**SiteOpennessAdjusted:** A value calculated by subracting the site openness from 100, to obtain the percent of a site that is open sky

**SDD:**		Snow disapearance date

**SDD1:**		First snow disappearance date (SDD2 is second, SDD3 is third, etc.)

**CN201_temp:**	This example would describe time series temperature data recorded by sensor at site CN, Plot 20, Position 1

**CN20A_temp:**	This example would describe time series air temperature data recorded by sensor at site CN, Plot 20

&nbsp;
&nbsp;

## **Methods**

**Snow Depth:** Measured to the nearest 5cm tape mark, rounding up if exaclty between tape marks.

**FSCA:** Estimated based on snow cover percentage of 10x10 plot, to the nearest 10%

**Imagetime:** In general, the image closes to noon for each day was chosen. If this image could not be used, the next consecutive image was chosen. 

**Gap Fraction:** Typically, five images of different exposure were taken at each LocationID. One image was chosen for each LocationID based on best exposure. Each best image was converted into a black/white bitmap file using ImageJ with the Hemispherical 2.0 plugin. Then, site openness was calculated using Gap Light Analyzer 2.0. Alternatively, ImageJ with the Hemispherical 2.0 plugin was used to calculate gap fraction for every exposure, and summary statistics (median, min, and max gap fraction)were then generated for each LocationID. 

**SDD:** For pole positions (LocationIDs ending in pole), snow presence is determined by a nonzero snow depth value for a given pole, and snow disappearance dates are days where snow is not present, but was the previous day. For stake positions (LocationIDs ending in a number), snow presence is determined based on temperature thresholds. For snow to be present, the maximum daily temperature the daily temperature range must be below 1.5 °C for 48 consecutive hours. Snow disappearance dates are taken as days where snow is not present, but was the previous day.   



