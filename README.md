# Telangana Weather Analysis — Power BI Dashboard

Hi, I'm Viswanath. This is a Power BI project where I analyzed weather data
for Telangana, India, covering the years 2021 to 2024.

The dataset had over 720,000 daily records — rainfall, temperature, humidity,
and wind readings from every district. I cleaned all of it, modelled it, and
built a 7-page interactive dashboard to make sense of it.

---

## Project Files

Everything is in this Google Drive folder — the Power BI file, the dataset,
and my full video walkthrough:

**[Open the project on Google Drive](https://drive.google.com/file/d/1oEQYHVhWuKxpbZrxJWCaZ0jO10bl8AnF/view?usp=sharing)**

Dashboard screenshots are in the `/screenshots` folder of this repository.

---

## How I Built It

### Getting the data in
This part was harder than I expected. The data came as 38 separate files
spread across folders. A few things went wrong while importing:

- Power BI couldn't read the RAR file, so I had to extract it first.
- One Excel file was corrupted and wouldn't open — I recovered it with another tool.
- The files were a mix of CSV and Excel, and Power BI quietly skipped the Excel one.
- One whole month of data went missing because of a deleted file.

I only caught these problems by checking the row count every time. The total
should have been 720,527 rows, and I kept fixing things until I hit that exact number.

### Cleaning the data
I used Power Query to fix the data types and check that every column was valid.
Some wind speed values were missing for early 2021 — that data was just never
recorded — so I left those blank instead of making up numbers.

### Modelling
I created a separate Calendar table and added a Season column to group the
months into Summer, Monsoon, Post-Monsoon, and Winter. Then I wrote 14 DAX
measures for the calculations.

### The dashboard
Seven pages: an Overview, a Geographic Map, and then a page each for Rainfall,
Temperature, Humidity, Wind Speed, and a final Comprehensive page that ties
everything together.

---

## What the Data Showed

A few things stood out:

- The monsoon does almost all the work — over 80% of the year's rain falls in
  just four months (June to September).
- Rainfall is very uneven. Nizamabad gets a lot; Hanumakkonda gets very little.
- Summer is the hottest season, and the highest reading was 46.8°C.
- Humidity is basically the opposite of heat — high after the monsoon, low in summer.
- Winter is the windiest season.

---

## Tools I Used

Power BI Desktop, Power Query, DAX, data modelling, and data visualization.

---

## A Note on the Data

The 2024 data only goes up to April, so I never compared it against the full
years. And as mentioned, some early-2021 wind data is missing in the source.
I kept it honest rather than filling gaps with fake values.

---

*Thanks for checking out my project. I'm looking for opportunities in data
analytics and business intelligence — feel free to reach out.*
