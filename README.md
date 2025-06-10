# Microbit Soil Data Analysis

This repository will:
1. Help you **get started** with beginner electronics, microcontroller programming, data collection, and machine learning.
2. Provide an example of how to collect **soil moisture data** with a micro:bit and process it for Data Analysis and Machine Learning.
3. Demonstrate how to visualize sensor data and apply a simple AI forecasting model (XGBoost) using Google Colab.

# What do you need for this project?

* 1x micro:bit
* 1x micro:bit Sensor Shield V2
* 1x Soil Humidity Sensor
* 1x Battery
* 1x USB to USB-C Cable

We used components from Keyestudio's "37 in 1 Starter Kit for BBC micro:bit". Check your kit and collect the required parts.

<img src="https://github.com/user-attachments/assets/48e07f26-d444-4d3e-a994-d0298162884e" alt="List" width="500" height="500">

# Step 1: Software Setup

Follow the steps in the [`Software_Setup`](./Software_Setup/) folder:

1. Download the [`microbit-data-log.hex`](./Software_Setup/microbit-data-log.hex) file.
2. Open https://makecode.microbit.org and import the `.hex` file to review the program.
3. Change the **date** and **log frequency** to your desired setting.
4. Download the modified program and flash it to your micro:bit using the USB cable.

# Step 2: Data Logging and Export

1. Place the soil sensor into the soil and power your micro:bit.
2. Start your micro:bit and let it log data (soil moisture, light, sound, temperature) for the desired time period.
3. After logging, connect your micro:bit to your computer via USB.
4. A `MICROBIT` drive will appear.
5. Inside the drive, open the `.HTML` file — this will allow you to download your logged data as a `.csv` file to your computer.

# Step 3: Data Analysis and Machine Learning

Now it's time to analyze the data you just collected!

1. Download the [`Soil_Moisture_ML_Microbit.ipynb`](./Software_Setup/Soil_Moisture_ML_Microbit.ipynb) notebook from the `Software_Setup` folder.
2. Open **Google Colab**: https://colab.research.google.com
3. In Google Colab:
    - Click **File → Upload Notebook** and upload the `Soil_Moisture_ML_Microbit.ipynb` file.
    - Then click **Files → Upload Files** (left sidebar) and upload your `.csv` data file.
    - Update the filename in the notebook's `pd.read_csv()` line if needed.
4. Run all the cells in the notebook: **Runtime → Run All**.
5. You will explore:
    - Exploratory Data Analysis (EDA) with pairplots, heatmaps, boxplots
    - Time series visualization of Soil Moisture
    - Forecasting Soil Moisture using an **XGBoost model** trained on lag features
    - Evaluation of the model (Test RMSE)

<img src="https://github.com/user-attachments/assets/8350e635-72a6-4634-af07-5711f67c6f54" alt="ML" width="700" height="500">

# Example of a Completed Setup

<img src="https://github.com/user-attachments/assets/9cbe39e9-1c9e-44bc-bc7e-fa912aaed3cb" alt="Setup" width="500" height="500">

# Summary

Once you follow the Software Setup and Data Analysis steps, you will have a complete workflow:
- Collect **real-world soil moisture data** with your micro:bit
- Process and analyze the data using Python and Google Colab
- Apply a simple **AI forecasting model (XGBoost)** to predict future soil moisture trends
- Visualize and interpret your results!

---

Happy experimenting!



