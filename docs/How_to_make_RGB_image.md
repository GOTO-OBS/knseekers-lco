# How to make a three colour RGB image using SAOImageDS9

To make three colour RGB images, many professional astronomers use the application SAOImageDS9 (hereafter referred to as DS9). DS9 is an astronomical imaging and data visualisation application that supports FITS images, commonly used as the data format for astronomical imaging. It is fully funded by the Chandra X-ray Science Center (CXC) and is licensed in part under the GNU General Public License, version 3.

  

To learn more about DS9, please visit the about page [here](https://sites.google.com/cfa.harvard.edu/saoimageds9/about).

  

You can find detailed documentation including the reference and user manuals, along with FAQs and tutorials [here.](https://sites.google.com/cfa.harvard.edu/saoimageds9/documentation)

  

----------

# Downloading and Installing DS9

DS9 is released once per year with beta versions available to download between major releases. For this project, we recommend downloading Release Version 8.5 to avoid any potential issues with a beta version.

  

Navigate to the download page [here](https://sites.google.com/cfa.harvard.edu/saoimageds9/download). Please note that Chrome users may have issues downloading from this page - if so, please follow the instructions at the top of the page for Chrome download. If you have any issues, please ask for help on the Kilonova Seekers - LCO: STAR slack pages.

  

You will first need to identify what operating system your computer is, as the installation is a little different for each. This will either be Linux, MacOS, or Windows.

## Windows Installation

1.  If you are using a Windows computer, please click on the drop-down menu next to the Windows icon.
    
2.  You should see the single option for “Windows 64 bit”. Double click this to download the .exe file.
    
3.  Once this file is downloaded, navigate to your downloads folder on your computer, and double click on the file to begin installation.
    

## MacOS Installation

If you are using a Mac, we recommend downloading the Aqua application version which avoids downloading any additional dependencies.

  

1.  Please click on the drop-down menu next to the MacOS icon, and navigate down to the list of AQUA versions.
    
2.  Identify your OS version and chip - if you don’t know this, you can find out by clicking on the Apple icon in the top left of your screen and selecting “About this Mac”. For example, it may say macOS Big Sur, Chip Apple M1.
    
3.  Find your OS version and chip from the list of AQUA options. For the example given in step 2, you would select Big Sur 11 Apple Silicon. Double click this to begin installation.
    
4.  Once this file is downloaded, navigate to your downloads folder and double click on the file to begin installation. You may need to click and drag the application into the /Applications directory if prompted.
    

  

Please note, if the installation shows warnings after installation run the following command at the prompt in a Terminal window:

% xattr -c /Applications/SAOImageDS9.app

If you have any issues, please ask for help in the slack.

## Linux Installation

1.  If you are using a Linux computer, please click on the drop-down menu next to the Linux icon.
    
2.  You will see a list of options for different Linux distributions. Please identify which distribution you are using, and which chip your computer has (this will either be Intel or ARM64). Double click on your version to begin installation.
    
3.  Once this file is downloaded, navigate to your downloads folder and double click on the file to begin installation.
    

  

Now that you have downloaded and installed DS9, you are ready to open the application and begin making some images!

----------

# Making a three-colour image

To start making an image, open up the DS9 program. You will be presented with a window that looks like the following image:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf5F0UT0qutQ0G4kA3jabiot-MTFe9bsR8y3-Ricgr9M3YRdbYjw_uNVYNyMzQTxN_tf3NfIDVNOycN4h4XKNh58t4G532XBqIfE-JDJz351dqFvDyAyh2DX2nLZ4saDcRyI8aON0dlJjglbjiENlnMBVdM-FSB9l6iqtOo?key=MnPqDCPDD18USPYIaw_BIQ)

Please note that my computer is in dark mode, so some of the colours may be inverted compared to your display. If DS9 is not working after your installation, please contact one of the members of the team on Slack.

  

On the DS9 user manual and on other online resources, there are plenty of tutorials to make a three-colour image, or if you want to play around with more complicated options, so if you are interested, please do look beyond the resources we have here. To get started however, please follow these instructions to make a simple three colour image.

  

## Step 1 - Downloading Data

To use DS9, you will need to download the image data onto your computer.

  

To begin, please click the link to learn [how to download data from the LCO archive](https://github.com/GOTO-OBS/knseekers-lco/blob/main/docs/How_to_download_data_from_LCO.md). If you have already downloaded data to use for the other tutorials to make a light-curve, please note the following in italics:

  

*To avoid losing track of where data is, I recommend creating a directory to store the data on your computer for each object, and move the data here from your downloads folder. For this tutorial, I am creating an image for GOTO24gap, so I will create a directory with this name in my documents. I will then move the downloaded data here and unzip it.*

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdsZv0NGbQqFdBWUY27Hhg5_v8xW2pMCxqwLnhX7IrSIl-LJ_hfojlwG92v-sNizJL-yAqgDCNYCYiXbUdIxTz2fGdtQw_i2jW0ZAdZCWonHNFcYwTvcJf_uymuAMiXuv4nBz_gB_VQhHXlU3Uy3VA7Fnr_3BLQRG2hQj-V7g?key=MnPqDCPDD18USPYIaw_BIQ)
*You can see here that I have an unzipped file, with the name structure as follows:*
-   *lco_data - indicates the data source.*
    
-   *20240924 - the data was downloaded onto my computer on the 24th September 2024.*
    
  
*Inside this directory, there are a number of files with the extension .fits.fz. These are the individual image files.*

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe1rnpGryzRSdVqXkJ2Et6PrBN5jqxBC0aY5HxNAOGfsGDfizDAF9SaR_h--X4xp1JUiMkx3k2f5DS_bibQMhhTKOW49Sdkgw3cEOQy_y3oQdTlrRIshhPMl9bwFuMDilSlYullcwRCthtirFVS88eGq62Ltgnf_-f7ABTe?key=MnPqDCPDD18USPYIaw_BIQ)

*Each of these filenames will match the image names on the LCO archive, so you can match the data there. You will notice that the timestamp in the file name may not match the time column from the science archive, this is because the time used in the file name is the “Date at start of local observing night”. Please just keep an eye out and make sure you label your data in a way that makes sense to you.*

  

**You may find it easier to download just the data you need for an individual epoch (“time of observation”) at a time.**

  

In this case, I just want to make an image with the data from the first observation, taken at about 5:00 on the 21st September 2024. I can download just that data from the archive by simply checking the correct boxes for this time range as follows.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe313kKzIkp1r4GTup12d-6MQvDAiQvhADcaDYoyqXqmWUJ1w4CVzMiC8lW-CxzKhpPAiD6IQwP_W9lJc0XDChUAQVgmdADwGbC5Ztd32h56P3Bydrm7l8zYdVwAWhfmHE9pIM5Cp7fSUYoqBxh9Dy-pBNXuFo1naYyNyQS4g?key=MnPqDCPDD18USPYIaw_BIQ)

As you can see, this will only download three files, instead of all the data for this object. Please move this data from your downloads file to somewhere in your documents folder, with an appropriate directory name so you don’t get confused between epochs. I typically label things with the object name, followed by the date of the observation, and a shortened version of the time stamp to differentiate between multiple epochs on a given date. For this example, I might call my directory something like “GOTO24gap-20240921-5”.

  

At this stage, please either note down which file name corresponds to each filter from the archive, or rename your files to account for this (but please maintain the .fits.fz extension at the end of each file - DS9 won’t work without this). For example, the file with the code -0086- corresponds to the “gp” filter, in other words “g-band”.

  

## Step 2 - Creating an RGB Frame on DS9

  

Now that you have downloaded the data, you can get started on actually using DS9.

  

1.  In the DS9 window, go to the top of the page and click the “Frame” menu. There will be the option “New Frame RGB”. Please click this.
    

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe19d2E7FufTwq_f-LTp2uP_VRsd8scgBKZmnpSCsI_ZatU2gqcZ7wEQ2IeDohWbH2e-fkxBk4Wvs29HjN2dTVszHZzA9Of8b_DVWvau0HxhJFaBQt6ath9jHmwxAL_b8nDUprD8mFljVud-WAqCXKOSPL6Cj46ybAb1jRE?key=MnPqDCPDD18USPYIaw_BIQ)

Once you have clicked this, the RGB window will open.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdA7GCTyPtD4taSL4IGtBC-XSBV_8W_ELiZnwgR5QV1eOSKdg547x-9UTmGMHRvYuJsTSxyzeflb63mWsu0Y3X2Uar-8jQqCzrsGw5QskptcuWUNQT67y9asgWcdNg8K8oNb0vydaZjVA8tdMVPjH67NLcaobcUiRADGxicEw?key=MnPqDCPDD18USPYIaw_BIQ)

 2. This is where you will specify which file should be read in for each colour. To start with, please ensure the “Red” band is selected in the “Current” column of the RGB window. You will now need to click “File -> Open…” in the main DS9 window and select the red file.
    

 This is where things may get a little confusing. Our observations are taken in the g, r and i filters, from the SDSS survey. This means that:
    

 - “Red” = i

 -  “Green” = r
   
 -   “Blue” = g

    

3.  So in this case, you will need to select the file corresponding to the observation in the i-band. This is the file with the extension -0088- in our current example.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfx7qj3CTQ7PxzE1k6gqm_9UJoPQbgCb5-iCwSENgH4vnjUbsCVffD-9gp-64G8i97kz2nVgYvvvFlH_4OmDvIhzvM5rUkBFW8ZF-JVBALg1f1BHKLlPbJWsOLqLaRO2UEcpxhS4cQCI-cJbA0tP2kIHL6vrzrl916Q4r0Z?key=MnPqDCPDD18USPYIaw_BIQ)
    

4.  In the RGB window, change the current band to “Green” and open the green (r-band) file.
    
5.  In the RGB window, change the current band to “Blue” and open the blue (g-band file).
    
6.  You have now loaded the three individual filters into the program. The next step is to scale the data to make a false-colour image.
    

  

## Step 3 - Scale the Frames

The next step is to scale the frames to create the false-colour image. I expect at this stage that the image will be mostly a black background, with perhaps a few point-like features. With the RGB window open, if you select different check-boxes in the “view” column, you may notice that different features in the image appear in different colours. Different observations in different filters have been taken with different exposure times, and are of varying quality, so the individual frames need to be scaled separately to make the false-colour image.

  

First, let’s look at the red (i-band) filter image.

  

1.  From the RGB window, select the current image to be red, and view only red, like so:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc4n5iwDQH4u6SbjTND8tgzpnKd0_nIUIk-bAKePV1FNk3WKmViHcOuQlHuaedxjEqRXjkEkBUXcCoSMAAXod0eA6-qKDusTswUsSsJXMqKq5GdNpC_QU6EmhtDT_z2f7bdk68d0VCNYGgOdP_OK61cUbTCHF2cPdiDdBta?key=MnPqDCPDD18USPYIaw_BIQ)
    

You will notice that any features on the black background will now show up as just red sources.

2.  We can now use various scaling options to highlight the sources. I like to start with “zscale”. Please select this by clicking “Scale” -> “zscale”.
    

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFe5WIwv8AwWl42gyfGiRsdvs2CDNIeRIt9uSMhoVmNaMUDieVQDhuxQQ6yLBlHVrAhJ7-7JleWgJcZJ21PYwiI8CUsoko4Zv8_M31M7JUA8JWhIDHirVlL0aF2i12hX3t2nXXlSTTL4YX7dvqLc9GT8Kqr1zo3wwqU4FA?key=MnPqDCPDD18USPYIaw_BIQ)

If you hover your cursor over the image and move it around, you should notice that the “r”, “g” and “b” values change. We can use these values to make the image look better.

3.  Click on “Scale” -> “Scale Parameters”. A window will open, with a histogram that represents the value counts of the brightness of each pixel in this image.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdMX6TUy1wKTyZ4xVi5SKlAyoMLd_uEyy9MsxfY3_gDz1efsYrmPnE9nOso--spHGX0T8OPX0OZaEfdeX6_MxY8Bmib3VkBLqA2UTLnxrA0UZmi5Z5sIk0kia9duu0f01eUuSH9mtXSgZQsITRfQ0VeabGoG3Cwqc4soD2JkQ?key=MnPqDCPDD18USPYIaw_BIQ)![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdln5uMduE7WeJxXPpWzHpcj8gNqNGkkqMptYTZ3F2WDMpM1CTgGN93au1Ut_rW_L1JzOUq8p2UP_9-zeUKHMgXuvgOwGIcBD1h0jEobAR2WGZKicbZ9Yjh2NvkNsC-HXRCqwFDsdHlFKHsGAT37F_oXODHMjTZJ9YwPkrWvA?key=MnPqDCPDD18USPYIaw_BIQ)
    

By hovering over the image, enter the lowest number you see for the “r” value into the “Low” limit of the Scale Parameters window, and the highest number into the “High” limit. Click “Apply”. You will now see that the image is mostly just a black background again with very few red features. We may have gone too high with our “High” limit - in other words, we are scaling too much to the brightest objects in the image. Play around with these numbers until you have a single-colour image you are happy with. You should be able to see stars and galaxies clearly, but the background should be mostly black with very few underlying features. This might take a lot of trial and error!

*As a hint, it is helpful that in our image we know the feature we are most interested in is at the very middle of the picture. Make sure you scale so that we can see the galaxy and the transient it contains!*
    

4.  Change to another of the RGB filters by modifying the RGB window, and repeat the scaling using that filter.
    
5.  Repeat for the final filter.
    
6.  You may need to go back and modify previous filters so that you can see the image clearly, and it is not dominated by any one filter colour. After a while, you will have something that looks like the night sky!
    

As an example, this is what I came up with after a few minutes of fine-tuning:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeHSWvrTF92Ac-3qlGR05UdXVIHIOGcZbEqR3ZnlgM-j1nyMsmVMjbZBSnqZ6z2L074bQSLEJ0qkHinCPvjNuR8cJZdEED0ullBKvEQ4oiJhfFLkHcbodCFW4nJ2MqaFmGTYrpP8cuBL3uJSdHpObNaJX5iL7fz7npZuj_ovA?key=MnPqDCPDD18USPYIaw_BIQ)

You can see the host galaxy of the transient in the very middle of this image, with the Type Ia supernova SN2024vrj (otherwise known as GOTO24gap) just towards the lower half of the galaxy.

  

## Step 4 - Saving the RGB Image

You can export the RGB image you have created as a PNG or JPEG file. To do this, go to File -> Export and select the option you require.

  

## Additional Extras

The image you have created is quite large, so play around with the options to see if you can crop it down to just focus on the region of the sky you are most interested in. Make sure the cropping is applied to each frame!

  

Now that you have created an image for one epoch, try repeating this for many different epochs. If you maintain the same scaling for each of the RGB filters for each epoch, and apply the same cropping, you can create a GIF to show the evolution of the transient over time!


