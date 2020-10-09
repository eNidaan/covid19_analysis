# Data Description

## Nexoid COVID-19 Survival Calculator Vulnerability Data

[Nexoid](https://www.covid19survivalcalculator.com/) is a software company based in London. It has a data research team that uses collected user data to calculate the risk index of COVID-19 to people with different vulnerabilities.

Data is gathered from the [survival calculator](https://www.covid19survivalcalculator.com/en/calculator), which is a survey that asks questions on biometrics, behaviors, living environments, medical records, etc. Nexoid then analyzes it and calculates the infection rate and mortality rate per different factors, based on over 820,000 entries of submitted data. Read the [methodology](https://www.covid19survivalcalculator.com/en/research).

## Dataset

The survival calculator provides a complete dataset of all responses submitted. It contains information such as the respondents'

- geographical information
- behavior
- segmentation
- health conditions
- medications
- risk values

For complete details of all questions asked, visit the [COVID-19 Survival Calculator](https://www.covid19survivalcalculator.com/en/calculator).

Data is updated periodically, and is available back till _March 24th, 2020_.

## Accessing Data 

You can download all responses at the survival calculator's [website](https://www.covid19survivalcalculator.com/en/download). (~180 MB total)

Metadata describing the response analysis are [available](https://www.covid19survivalcalculator.com/en/download) as separate files, listed together with the master dataset.

Last updated _September 25th, 2020_.

## Structure

All survey responses are recorded in `master_dataset.csv`.

### Field Description

**Note**: Description is not yet complete, awaiting contribution.

| Field | Description | Type | Example |
|-|-|-|-|
| `survey_date` | Date on which the data was collected, in the format `M/D/YYYY` | string | 3/24/2020 |
| `region` | [2-letter continent code](https://datahub.io/JohnSnowLabs/country-and-continent-codes-list) in which the data was collected (based on IP address). Possible values are: <ul><li>`AF` for Africa</li><li>`AN` for Antarctica</li><li>`AS` for Asia</li><li>`EU` for Europe</li><li>`NA` for North America</li><li>`OC` for Oceania</li><li>`SA` for South and Central America</li></ul> | string | NA |
| `country` | [2-letter country code](https://www.iban.com/country-codes) representing the country in which the data was collected (based on IP address) | string | US |
| `ip_latitude` | Latitude associated with the IP address of submission | string | 38.5415 |
| `ip_longitude` | Longitude associated with the IP address of submission | string | -121.4968 |
| `ip_accuracy` | Accuracy of the geolocation associated with the IP address of submission, in terms of the maximum distance (in km) of error  | integer | 5 |
| `sex` | Sex of the respondent. Possible values are: `male` and `female` | string | female |
| `age` | Age range of the respondent, in intervals of 10 years | string | 40_50 |
| `height` | Height of the respondent, in cm | integer | 170 |
| `weight` | Weight of the respondent, in kg | integer | 102 |
| `bmi` | [Body mass index](https://en.wikipedia.org/wiki/Body_mass_index) of the respondent | float | 35.2 |
| `blood_type` | Blood type of the respondent. Possible values are: <ul><li>`ap` for A+</li><li>`an` for A-</li><li>`bp` for B+</li><li>`bn` for B-</li><li>`abp` for AB+</li><li>`abn` for AB-</li><li>`op` for O+</li><li>`on` for O-</li><li>`unknown`</li></ul> | string | bp |
| `insurance` | Does the respondent have private health insurance? Possible values are: `yes` and `no` | string | yes |
| `income` | Income level of the respondent. Possible values are: <ul><li>`high`</li><li>`med`</li><li>`low`</li><li>`blank` for respondent on social welfare/government support</li></ul> | string | high |
| `race` | Race of the respondent. Possible values are: <ul><li>`white`</li><li>`mixed`</li><li>`asian`</li><li>`black`</li><li>`hispanic`</li><li>`other`</li></ul> | string | white |
| `immigrant` | Is the respondent a native or an immigrant to the country he/she is in? Possible values are `native` and `immigrant`. | string | native |
| `smoking` | Does the respondent smoke or vape? Possible values are: <ul><li>`never` for never smoked or vaped</li><li>`vape` for vaping or using e-cigarettes</li><li>`yeslight` for light smoking (1-5 per day)</li><li>`yesmedium` for medium smoking (6-20 per day)</li><li>`yesheavy` for heavy smoking (>20 per day)</li><li>`quit0` for recently quit</li><li>`quit5` for quit >5 years ago</li><li>`quit10` for quit >10 years ago</li></ul> | string | quit10 |
| `alcohol` | Number of the days the respondent has consumed **alcohol** over the past 14 days. Values range from `0` to `14`.<br><br>`-1` is reserved for respondents who has never drunk alcohol. | integer | 4 |
| `cannabis` | Number of the days the respondent has consumed **cannabis (marijuana)** over the past 28 days. Values range from `0` to `28`.<br><br>`-1` is reserved for respondents who has never consumed cannabis. | integer | 6 |
| `amphetamines` | Number of the days the respondent has consumed **amphetamines (ice, speed)** over the past 28 days. Values range from `0` to `28`.<br><br>`-1` is reserved for respondents who has never consumed amphetamines. | integer | -1 |
| `cocaine` | Number of the days the respondent has consumed **cocaine** over the past 28 days. Values range from `0` to `28`.<br><br>`-1` is reserved for respondents who has never consumed cocaine. | integer | -1 |
| `lsd` | Number of the days the respondent has consumed **LSD (acid)** over the past 28 days. Values range from `0` to `28`.<br><br>`-1` is reserved for respondents who has never consumed LSD. | integer | -1 |
| `mdma` | Number of the days the respondent has consumed **MDMA (ecstacy)** over the past 28 days. Values range from `0` to `28`.<br><br>`-1` is reserved for respondents who has never consumed MDMA. | integer | -1 |
| `contacts_count` | Number of people the respondent was in close contact with over the past week. Values range from `0` to `20`.<br><br>`21` is reserved for >20 contacts. | integer | 21 |
| `house_count` |  |  |  |
| `public_transport_count` |  |  |  |
| `working` |  |  |  |
| `worried` |  |  |  |
| `rate_reducing_risk_single` |  |  |  |
| `rate_reducing_risk_single_social_distancing` |  |  |  |
| `rate_reducing_risk_single_washing_hands` |  |  |  |
| `rate_reducing_risk_house` |  |  |  |
| `rate_reducing_risk_house_social_distancing` |  |  |  |
| `rate_reducing_risk_house_washing_hands` |  |  |  |
| `rate_reducing_risk_house_sanitizer` |  |  |  |
| `rate_reducing_mask` |  |  |  |
| `rate_reducing_mask_type` |  |  |  |
| `rate_reducing_government_action` |  |  |  |
| `rate_reducing_government_control` |  |  |  |
| `rate_reducing_government_spend` |  |  |  |
| `covid19_positive` |  |  |  |
| `covid19_symptoms` |  |  |  |
| `covid19_contact` |  |  |  |
| `asthma` |  |  |  |
| `kidney_disease` |  |  |  |
| `liver_disease` |  |  |  |
| `compromised_immune` |  |  |  |
| `heart_disease` |  |  |  |
| `lung_disease` |  |  |  |
| `diabetes` |  |  |  |
| `hiv_positive` |  |  |  |
| `hypertension` |  |  |  |
| `other_chronic` |  |  |  |
| `nursing_home` |  |  |  |
| `health_worker` |  |  |  |
| `prescription_medication` |  |  |  |
| `opinion_infection` |  |  |  |
| `opinion_mortality` |  |  |  |
| `risk_infection` |  |  |  |
| `risk_mortality` |  |  |  |

**Note**: Fields may be empty.

## Attribution

This dataset is under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. You are free to use it for personal, educational, research, and commercial use provided you attribute the dataset to **Nexoid**.
