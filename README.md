# The 'Mapping Warbler Song' Project
In this project, we'll build on the work of a previous project: 'Mapping Birdsong' (https://github.com/mikeallen-eco/mapping_birdsong). In that project, students picked a species, measured aspects of its song, and mapped them to reveal vocal dialects. It produced some interesting results, but our sample sizes were low. So, in this project, we'll double down on this approach and band together to increase our sample size. As a class, we'll measure sonogram properties to map the vocal dialects of a single species, the Prairie Warbler, across the eastern US. To do this, we'll use the > 500 high-quality songs for the species available via the Cornell Laboratory of Ornithology Macaulay Library's extensive collections. Most of those recorded songs were recorded by citizen scientists as part of their eBird checklists. We'll use low-tech tools (rulers! our eyes!) to collect 3 different measurements and then map them to see what the data tell us. While this analysis won't reveal WHY these patterns occur (e.g., learned dialects, local evolution), it may reveal some new questions that are worth exploring!

## Overview
Each group will be assigned 50 song recordings from the Prairie Warbler song database downloaded from the Macaulay Library. As a group, you will view the sonogram for each song and make 3 measurements, and record your data. Then we'll combine all the class data into one database and map the results.

## Phase 1: get and format your data files
0. If you don't have (or want) RStudio on your computer log into the virtual computer lab (https://it.rutgers.edu/virtual-computer-labs/). In the virtual lab, RStudio is located in the "Programs" folder in the "Class Software" subfolder.
1. Open a web browser and go to: https://github.com/mikeallen-eco/mapping_birdsong.
Download the code repository by clicking the green "Code" button. Unzip the folder it somewhere you can find it. (Don't change any folder or file names or locations yet.)
2. Now, look up Prairie Warbler in your field guide (or online) and take a look at the species' range map and the comments about their vocalizations.
3. Back in the web browser, go to https://www.macaulaylibrary.org/ and enter Prairie Warbler in the search box to start viewing sonograms for the species. View several examples of the species' sonograms. Look for variation among individuals. Is there an interesting property of the song that you think would be interesting to measure, either visually (e.g., syllable counts, max frequency) or with a ruler (e.g., syllables per second, total trill duration, duration of some other part of the song, etc.)? 
4. Use the 'filters' in the Macaulay website to limit your selection to 1) audio by clicking the speaker button in the header, and play around with other options by clicking "More filters" and checking boxes. Download a spreadsheet (csv file) for the resulting data by clicking "export". (Note: we won't actually use this data as we already have a downloaded version for the class in the "prawar_data" folder.)
5. Close the file you exported and open the csv file in the "prawar_data" folder. How many rows does it have?
6. Now it's time to process the song data file to make a data sheet for your group. Open the R project by double clicking the "mapping_warblers.Rproj" file. This will only work if you 1) are in a virtual lab workstation with RStudio installed, or 2) you have it installed on your own computer. (They are free programs.)
7. Within RStudio, open the file called "mapping_prawar.Rmd". This file contains code to process your raw Prairie Warbler data file (which should be the only file in your "prawar_data" folder) along with directions on how to run it. Follow the directions in that file. If you do it correctly, it should result in the creation of a new csv files that contains your group name and your assigned song numbers: e.g., "group_name_1_50_data_file.csv". The new file will be in the "my_output" folder. The file contains a subset of songs that your group will perform measurements on. We filtered the data to only include songs from the main part of the range, that were recorded in June or July, and with a "quality" rating of 3 or higher.
8. Move your newly-created data file from "my_output" to the newly-created folder "my_data".

Once you are done running the code for Steps 7 and 8 in RStudio, come back here to this Readme file on the web to finish the project...

## Phase 2: make your measurements
9. On your computer (outside of RStudio) navigate to the "my_data" folder and open it. 
10. Time to start making measurements on your assigned sonograms. The data file you created in Step 7-8 should be in the "my_data" folder. Open it using your favorite spreadsheet software. Make the columns wider if needed. Paste the first URL in the "link" column into a web browser. It will look something like this: https://macaulaylibrary.org/asset/110249
11. Now use a ruler to make your first measurement on the first clear song in the sonogram associated with that link. See the image in the "prawar_data" folder for an illustration of what the measurements mean. Briefly, they are:
num_sylables = the number of syllables ('notes') in the song.
freq_range_mm = the range of frequencies in mm (measured with ruler)
duration_mm = the length of the song in mm (measured with ruler)
two_khz_mm = the length of 2 kHz on the scale bar in mm (measured with ruler)
two_sec_mm = the length of 2 seconds on the scale bar in mm (with ruler)
Hint: measure the height of 1 kHz or 1 second to help you take accurate measurements. If the sonogram is not clear, there is no song, or if it seems to be the wrong species (Field Sparrows are occasionally mislabeled as Prairie Warblers), then enter NA in the measurement fields and enter a note into the "skip_notes" field.
12. Repeat this process for each link in the data file. Be sure to save your data file. You can stop partway and finish later. If you are on a virtual lab machine, be sure to email yourself the data or otherwise save it safely. You can also take the whole code repository with you by "zipping" the whole "mapping_warblers" folder you are working in and emailing it to yourself.
13. Once you are done collecting all your measurements, send the completed data file to michael ( d o. t ) allen (at) rutgers ( dot ) edu.

## Phase 3: make maps and plots summarizing our collective results
14. Download the compiled course data csv file and add it to your "my_data" folder.
15. Open the RStudio project again. Next, open the "mapping_prawar2.Rmd" file and follow the instructions to create maps and graphs summarizing the class measurements. Plots will be saved to your "my_output" folder.
16. Write a mini scientific paper with the following sections (~1 paragraph each, can be short paragraphs!): introduction, methods, results, discussion, literature cited (at least 2 primary references). Include the three maps we created as figures 1-3 with proper captions. Split up the writing among group members. Note: these "papers" can be relatively rough as we are writing them primarily in class. Turn it in via email with all group member names on it.