# Project Goal

To be the ultimate machine whisperers. Save our company millions (or perhaps billions) of dollars by being able to forcast and predict failures before they actually happen.

# Datasets
- NASA Turbofan Engine Fault Dataset: https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan
  - Unit Number
  - Time in Cycles
  - Operational Settings
  - Sensor Measurements
  
# Strategy
- Using the provided dataset, we can solve the problem by getting the following:
  - How many more cycles a turbofan has until failure
  - Will this turbofan fail within X cycles?
  - Will this fan fail within a certain timeframe?
 
 # ETL
 Three types of documents are provided: Traning, Testing, Ground truth 
   - Training data: It is the aircraft engine run-to-failure data.
   - Testing data: It is the aircraft engine operating data without failure events recorded.
   - Ground truth data: It contains the information of true remaining cycles for each engine in the testing data.
   
   The goal with these files is to pre-process them and see if we can predict when the engine will fail with the given aircraft engine operation and failure events history.

# End Goal



Thoughts from Emily
- Great start!
- If you're using a forecasting approach, consider using RMSE as the way to evaluate your model.
- Your dataset is actually quite noisy, you'll probably want to normalize some of those columns. Try to loop through the headers and apply a function to normalize them.
- You should have quite a few engines; are you going to build a separate model for each one? Or are you going to build one global model on all of the data?
