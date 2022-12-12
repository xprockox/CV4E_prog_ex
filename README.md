# Michael Procko
### CV4Ecology Programming Example

This repo serves as a programming example for the Summer Workshop on Computer Vision Methods for Ecology 2023

Within this repo, you will find:
- Procko_M_prog_ex.ipynb: a code which...
    + imports raw camera trap detection data and concatenates into one dataframe
    + filters camera trap detection data into independent detections using a 30-minute threshold for wildlife detections and 1-minute threshold of human-related detections
    + formats camera trap detection data into station * week detection data, with the days each camera was active per week being calculated to allow for sampling effort calculations later
    + calculates weekly detections and detection rates (using the sampling effort of each camera) for elk, deer, black bears, cougars, coyotes, bobcats, hikers, mountain bikers, horseback riders, motorized vehicles, and domestic dogs 
    + constructs a random forest model, currently set up to classify stations-weeks where elk were detected as a binary response variable. Elk detection/non-detection was predicted as a function of all human-related detection rates
    + extracts variable importance information from the random forest algorithm to identify the strongest predictors of elk detection/non-detection
    + plots variable importance
    + assesses random forest model accuracy with confusion matrix and calculation of precision/recall/F1 scores
    + plot the relationship between hiker detection rate and elk detection probability using a GAM spline
- raw_data.zip
    + .zip containing all raw detection data
- MASTER_DEPLOYMENTS_2022-10-11.csv
    + .csv containing data on camera deployments (camera start date, end date, etc.)

Note that the following four-letter appreviations are used for all wildlife species, each corresponding to the first two letter of their genus & species: {'ceca' : elk, 'odhe' : black-tailed deer, 'uram' : blackbear, 'puco' : cougar, 'cala' : coyote, 'lyru' : bobcat}
