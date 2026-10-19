# Google Play Store App Insights — Looker Studio

This project answers the questions in the supplied App Insights case study using the Looker Studio dashboard.

## Project overview

The Looker dashboard reports **9,638 apps**, **75.2 billion installs**, **2.1 billion reviews**, and an **average rating of 4.17**. It displays **33 categories**, app-size bins, a free/paid split, content-rating counts and averages, and details for highly reviewed apps.

<img width="1440" height="1078" alt="Screenshot 2026-10-03 164202" src="https://github.com/user-attachments/assets/b492cadc-a2c2-4822-8bf4-2df5ed392209" />
<img width="1441" height="1078" alt="Screenshot 2026-10-11 185046" src="https://github.com/user-attachments/assets/48567b0f-114d-4dd4-9878-96c37c862902" />
<img width="1437" height="1078" alt="Screenshot 2026-10-11 185108" src="https://github.com/user-attachments/assets/f2d5259c-db8c-4182-ab30-a340ce032b93" />
<img width="1447" height="1078" alt="image" src="https://github.com/user-attachments/assets/37470232-7f60-425c-9f92-7f96dee72b95" />


The second Looker page includes genre counts above one million installs, app size versus installs, top-reviewed apps, and record counts by app type.

## Basic-level questions

### 1. What is the average rating of apps in the dataset?

**Answer:** The Looker dashboard reports an average rating of **4.17 out of 5**. This is the overall app-rating average; it does not imply all apps have ratings near 4.17.

### 2. How many unique categories of apps are there?

**Answer:** **33 categories**

### 3. What is the distribution of app sizes?

**Answer:** The Power BI reference dashboard shows **3,779 apps in the 0–10 MB bin**, 1,546 in 10–20 MB, 1,104 in 20–30 MB, 620 in 30–40 MB, 451 in 40–50 MB, 281 in 50–60 MB, 207 in 60–70 MB, 140 in 70–80 MB, 114 in 80–90 MB, and 170 in 90–100 MB. The 0–10 MB range is the largest visible bin.

### 4. How many free vs. paid apps are there?

**Answer:** The Looker donut chart shows **92.2% free** and **7.8% paid**. Its record-count table lists **8,886 free** apps and **751 paid** apps, plus one record with no displayed type. The shares and counts are rounded/displayed values from the report.

### 5. What is the most common content rating for apps?

**Answer:** **Everyone** is the most common content rating, with **7,883 apps**. The other displayed counts are Teen (**1,035**), Mature 17+ (**393**), Everyone 10+ (**322**), Adults only 18+ (**3**), and Unrated (**2**).

### 6. What are the top 5 most installed apps?

**Answer:** The table lists **Facebook**, **WhatsApp Messenger**, **Instagram**, **Messenger – Text and Video Chat for Free**, and **Subway Surfers**. Each is displayed as having **1B installs**.

### 7. How many apps have a rating of 4.0 and above?

**Answer:** **6,282 apps**. 

### 8. What is the average number of reviews for free vs. paid apps?

**Answer:** The Looker table reports **2.1 billion total reviews for free apps** and **6.6 million total reviews for paid apps**. These are totals, not average reviews per app.

### 9. What is the average app size for each category?

**Answer:** The Looker chart shows the ten categories with the largest displayed average app sizes: **Game (41.68 MB)**, **Family (27.36 MB)**, **Travel & Local (24.20 MB)**, **Sports (24.06 MB)**, **Entertainment (23.71 MB)**, **Parenting (22.51 MB)**, **Health & Fitness (20.75 MB)**, **Food & Drink (20.69 MB)**, **Auto & Vehicles (20.04 MB)**, and **Medical (19.23 MB)**. The chart shows only these ten categories, not every category in the dataset.

### 10. How many apps were last updated in 2018?

**Answer:** The Looker KPI reports **6,272 apps updated in 2018**. This is a count of app records with a 2018 last-updated date, not the number of update events during the year.

## Medium-level questions

### 1. What is the correlation between the number of installs and the app rating?

**Answer:** The scatter plot shows ratings across several install levels, with points spanning a broad rating range. The visual alone does not establish that installs cause higher ratings.

### 2. Which app categories have the highest average rating?

**Answer:** **Events (4.44)** highest, followed by **Art & Design (4.36)**, **Education (4.35)**, **Books & Reference (4.34)**, and **Personalization (4.33)**.

### 3. How does the price of an app affect its average rating?

**Answer:** Ratings in the Looker price plot are mostly between about **4.0 and 4.4** across the displayed price range, with a few higher or lower points. The plot does not show an obvious monotonic pattern or quantify a relationship.

### 4. What is the distribution of app ratings across different content ratings?

**Answer:** The Looker table reports **Adults only 18+ (4.30; 3 apps)**, **Everyone 10+ (4.23; 322)**, **Teen (4.23; 1,035)**, **Everyone (4.17; 7,883)**, **Mature 17+ (4.12; 393)**, and **Unrated (4.10; 2)**. It presents average ratings and group counts rather than the full distribution of individual rating values. The Adults-only and Unrated averages are based on very small groups.

### 5. Which genres have the most apps with over 1 million installs?

**Answer:** The top displayed genres are **Tools (273 apps)**, **Action (180)**, **Photography (173)**, **Entertainment (154)**, **Productivity (147)**, **Communication (140)**, **Sports (124)**, **Health & Fitness (112)**, **Personalization (110)**, and **Arcade (109)**. 

### 6. How frequently do apps get updated? What is the average time between updates?

**Answer:** The annual trend rises from **1 app in 2010** to about **6.3K in 2018**, with a steep increase in the final years shown.  Neither report gives the average time between updates: each app has a single `Last Updated` date in the case-study data, so consecutive update intervals cannot be derived from these screenshots.

### 7. What is the impact of app size on the number of installs?

**Answer:** **App size has little direct impact on installs.** Apps of the same size (e.g. exactly 100 MB) range from 500 installs to 100M. Both heavy and light categories reach the top: Game apps average 41.7 MB and lead with 13.5 B installs, while light categories like Communication (11 B) and Tools (8 B) follow close behind. Most apps are small (63% under 20 MB) and large apps are rare, but installs do not consistently rise or fall with size.

### 8. Which apps have the highest number of reviews, and what are their ratings?

**Answer:** The displayed top-reviewed apps are:

| App | Reviews | Rating | Installs |
| --- | ---: | ---: | ---: |
| Facebook | 78.2M | 4.1 | 1B |
| WhatsApp Messenger | 69.1M | 4.4 | 1B |
| Instagram | 66.6M | 4.5 | 1B |
| Messenger – Text and Video Chat | 56.6M | 4.0 | 1B |
| Clash of Clans | 44.9M | 4.6 | 100M |
| Clean Master – Space Cleaner | 42.9M | 4.7 | 500M |
| Subway Surfers | 27.7M | 4.5 | 1B |
| YouTube | 25.7M | 4.3 | 1B |
| Security Master – Antivirus | 24.9M | 4.7 | 500M |
| Clash Royale | 23.1M | 4.6 | 100M |

### 9. How does the content-rating distribution differ between free and paid apps?

**Answer:** 

| Content rating | Free | Paid |
| --- | ---: | ---: |
| Everyone | 6,101 | 511 |
| Teen | 867 | 45 |
| Mature 17+ | 342 | 15 |
| Everyone 10+ | 274 | 31 |
| Adults only 18+ | 3 | 0 |
| Unrated | 1 | 0 |


### 10. What are the top 5 categories with the most installs?

**Answer:** **Game (13.5B)**, **Communication (11B)**, **Tools (8B)**, **Family (6.2B)**, and **Productivity (5.8B)**. 

## Advanced-level questions

### 1. What are the top 10 apps with the highest ratings, and how do their reviews and installs compare?

**Answer:** After filtering for apps with more than 100K reviews, the top 10 all rate between 4.8 and 4.9. Four apps reach 4.9: Learn Japanese, JW Library, Six Pack in 30 Days and Tickets + PDA 2018. JW Library stands out with about 922.8K reviews at 4.9, so its rating is backed by a large user base.

### 2. What update patterns or seasonal trends appear over time?

**Answer:** The annual counts rise sharply, from **1 in 2010** to approximately **6.3K in 2018**; the most pronounced increases occur in 2017 and 2018. 

### 3. How does the average rating change with installs? (Binned analysis)

**Answer:** **4.03** for the 1K–10K tier, **4.10** for 10K–100K, **4.20** for 1K or less, **4.20** for 100K–1M, **4.27** for 1M–10M, **4.36** for 10M–100M, **4.37** for 100M–500M, and **4.22** for 500M+. The displayed pattern rises through the 100M–500M tier, then declines in the 500M+ tier. 

### 4. What themes do high- and low-rated app reviews contain?

**Answer:** This cannot be answered from the supplied reports. They show review counts and app ratings, but not the text of user reviews. Sentiment analysis requires review text; a review total alone does not reveal positive or negative themes.

### 5. What is the relationship between app genre and user ratings?

**Answer:** **Casual;Brain Games (mean 4.48, median 4.5)**, **Events (4.44, 4.5)**, **Art & Design;Creativity (4.35, 4.5)**, **Parenting (4.34, 4.5)**, **Arcade;Action & Adventure (4.34, 4.5)**, and **Health & Fitness (4.25, 4.5)**.

