ASHRAE energy prediction III

Dataset Detail
train.csv
building_id - Foreign key for the building metadata.
meter - The meter id code. Read as {0: electricity, 1: chilledwater, 2: steam, 3: hotwater}. Not every building has all meter types.
timestamp - When the measurement was taken
meter_reading - The target variable. Energy consumption in kWh (or equivalent). Note that this is real data with measurement error, which we expect will impose a baseline level of modeling error. UPDATE: as discussed here, the site 0 electric meter readings are in kBTU.
building_meta.csv
site_id - Foreign key for the weather files.
building_id - Foreign key for training.csv
primary_use - Indicator of the primary category of activities for the building based on EnergyStar property type definitions
square_feet - Gross floor area of the building
year_built - Year building was opened
floor_count - Number of floors of the building
weather_[train/test].csv
Weather data from a meteorological station as close as possible to the site.

site_id
air_temperature - Degrees Celsius
cloud_coverage - Portion of the sky covered in clouds, in oktas
dew_temperature - Degrees Celsius
precip_depth_1_hr - Millimeters
sea_level_pressure - Millibar/hectopascals
wind_direction - Compass direction (0-360)
wind_speed - Meters per second
test.csv
The submission files use row numbers for ID codes in order to save space on the file uploads. test.csv has no feature data; it exists so you can get your predictions into the correct order.

row_id - Row id for your submission file
building_id - Building id code
meter - The meter id code
timestamp - Timestamps for the test data period
NOTE: dataset source : https://www.kaggle.com/c/ashrae-energy-prediction/data


Installation
- pip install lightgbm
- pip install tqdm

Execution
- Download dataset from above dataset source link and extract dataset to datasets/ashrae-energy-prediction/
- for eda analysis, open train_merge_eda file on jupyter notebook
- final model is implemented in kaggle notebook. so open kaggle and copy notebook final model implementation, add ASHRAE dataset on input by clicking add bottom found on the top. then execute for feature selection, training & predicting validation and test dataset

Subnission file
- You can find submission file at
--- light gbm - https://cutt.ly/HrcJMll
--- linear regression - https://cutt.ly/ArcJ9ZB


requirement min. 8GB RAM, best with gpu
