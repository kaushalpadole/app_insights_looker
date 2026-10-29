# App Insights — Google Play Store Analytics

## Project Overview

App Insights is a data analytics project built using **Google Looker Studio** to analyze application performance on the Google Play Store.

The project explores application ratings, installs, reviews, categories, genres, pricing, app sizes, content ratings, and update history to identify patterns in user satisfaction and app popularity.

The interactive dashboard transforms raw application data into visual insights that can help developers and product teams make informed decisions about product development, user engagement, and monetization.

**Live Dashboard:** [View App Insights](https://datastudio.google.com/s/nFzav0hpAdk)

## Business Problem

The Google Play Store contains applications with different ratings, download volumes, prices, sizes, and target audiences. Understanding these differences can help developers identify opportunities to improve application performance and user satisfaction.

This project investigates the following business questions:

* Which application categories generate the highest install volumes?
* How do ratings vary across categories and genres?
* How do free and paid applications differ?
* Is app size associated with the number of installs?
* Which applications receive the most reviews?
* How do ratings vary across different install tiers?
* What patterns appear in the recorded last-updated dates?

The objective is to identify meaningful patterns and translate them into actionable recommendations.

## Project Requirements

* Analyze the Google Play Store application dataset.
* Clean and prepare numeric and categorical fields for analysis.
* Handle missing values, duplicates, and inconsistent data formats.
* Create interactive visualizations using Google Looker Studio.
* Compare application performance across relevant categories.
* Identify trends and patterns in ratings, installs, reviews, and app sizes.
* Present key findings through an organized dashboard.
* Provide recommendations supported by the available data.

## Tools and Technologies

| Tool / Technology                | Purpose                                                    |
| -------------------------------- | ---------------------------------------------------------- |
| Google Looker Studio             | Interactive dashboards, KPI scorecards, tables, and charts |
| Google Play Store dataset        | Source data for application analysis                       |
| Data cleaning and transformation | Prepare data for accurate aggregation and visualization    |
| GitHub                           | Project documentation, screenshots, and analysis solutions |

## Dataset Description

The dataset contains information about Google Play Store applications.

| Column         | Description                      |
| -------------- | -------------------------------- |
| App            | Application name                 |
| Category       | Application category             |
| Rating         | Average user rating              |
| Reviews        | Number of user reviews           |
| Size           | Application size                 |
| Installs       | Application install-count band   |
| Type           | Free or paid classification      |
| Price          | Application price                |
| Content Rating | Intended audience classification |
| Genres         | Application genre                |
| Last Updated   | Recorded last-update date        |
| Current Ver    | Current application version      |
| Android Ver    | Minimum required Android version |

These fields help evaluate application popularity, user satisfaction, pricing, size, and update-date patterns.

## Dashboard Features

The Looker Studio dashboard includes:

* KPI scorecards for key application metrics.
* Category-wise application and install comparisons.
* Free versus paid application analysis.
* Application ratings and review comparisons.
* App-size distribution and category-level size comparisons.
* Content-rating distribution.
* Top-installed and highly reviewed applications.
* Average ratings by category, genre, and install tier.
* Scatter plots comparing installs with ratings, app size, and price.
* Application update-date trends.
* Tables highlighting highly rated and highly reviewed applications.

These visualizations make it easier to compare applications and identify patterns in the dataset.

## Data Cleaning and Preparation

Data preparation was necessary to make the source data suitable for analysis.

The main tasks included:

* Removing duplicate records.
* Removing a malformed source row where fields were incorrectly aligned.
* Converting install counts and review counts into numeric fields.
* Converting application prices into numeric values.
* Converting application sizes into MB where available.
* Handling missing ratings and sizes appropriately.
* Parsing last-updated dates.
* Creating year and month fields for update-date analysis.
* Creating install tiers for comparing average ratings.
* Creating a flag to identify applications rated 4.0 and above.

Missing ratings and sizes should not be treated as genuine zero values because doing so can distort averages and comparisons.

## Challenges Faced

### 1. Inconsistent Data Formats

Install counts, prices, and app sizes appeared in different formats. These values needed to be normalized before they could be analyzed numerically.

### 2. Missing Values

Some applications lacked ratings or usable size information. Appropriate handling was necessary to avoid misleading averages and visualizations.

### 3. Highly Skewed Install Counts

Install counts ranged from small values to billions. This made some visualizations difficult to interpret because smaller values became compressed alongside very large values.

Logarithmic scaling was used for scatter plots where appropriate to improve readability.

### 4. Choosing Appropriate Aggregations

Different business questions required different calculations. For example, total installs by category required summing install values, while average rating by category required calculating average ratings.

### 5. Date-Related Limitations

The dataset contains one recorded last-updated date per application rather than a complete history of releases. Therefore, the exact average time between consecutive updates cannot be calculated.

### 6. Unavailable Review Text

The dataset contains review counts but not the text of individual reviews. Consequently, identifying recurring complaints or conducting sentiment analysis was not possible using the available data alone.

## Key Insights

The following insights are based on the dashboard and its documented analysis.

### 1. Overall Application Ratings

The dashboard reports an average rating of approximately **4.17 out of 5**.

This provides an overall view of user ratings for the records included in the calculation.

### 2. Application Categories

The dataset contains **33 unique application categories**, demonstrating the variety of applications represented in the marketplace.

### 3. Free Versus Paid Applications

Free applications dominate the dataset.

The documented report lists 8,886 free apps and 751 paid apps, along with one record without a displayed type.

This indicates that free applications are more common in the analyzed data, although it does not establish which monetization strategy is more profitable.

### 4. Content Ratings

The Everyone content-rating group is the largest, containing **7,883 applications** in the documented analysis.

This suggests that applications intended for a broad audience form a substantial portion of the dataset.

### 5. Categories With High Install Volumes

The documented category analysis identifies the following leaders:

* Game: approximately 13.5 billion installs.
* Communication: approximately 11 billion installs.
* Tools: approximately 8 billion installs.
* Family: approximately 6.2 billion installs.
* Productivity: approximately 5.8 billion installs.

These figures indicate substantial install volume across gaming, communication, utility, and productivity applications.

### 6. Ratings Do Not Guarantee Popularity

Some highly rated applications have comparatively fewer reviews and installs than widely used applications.

Therefore, a high rating alone does not indicate that an application has a large audience.

Developers should evaluate ratings alongside installs, reviews, and other business metrics.

### 7. Application Size and Installs

The scatter-plot analysis does not reveal a simple, consistent relationship between app size and install volume.

Both relatively small and large applications can achieve substantial install counts.

Application size should therefore be considered alongside functionality, performance, user experience, and market demand.

### 8. Recorded Update-Date Trends

The documented update-date chart shows a substantial increase in the number of apps with recorded last-updated dates in later years, reaching approximately 6,300 applications in 2018.

This represents the distribution of recorded dates in the dataset, not the total number of updates released during each year.

### 9. Ratings Across Install Tiers

The documented analysis shows an average rating of approximately 4.37 for the 100M–500M install tier, compared with 4.22 for the 500M+ tier.

This indicates that average ratings do not necessarily increase continuously with install volume. The pattern is descriptive and does not establish causation.

### 10. Highly Reviewed Applications

Applications such as Facebook, WhatsApp Messenger, Instagram, and Messenger appear among the highly reviewed apps.

These applications combine substantial user engagement with large install counts, although their ratings differ.

Review volume and ratings should be evaluated together to understand application performance more effectively.

## Recommendations for Improving App Performance

### 1. Improve User Experience and Reliability

Developers should prioritize application stability, loading speed, navigation, and usability.

Regularly monitoring crashes, performance issues, and user feedback can help identify problems that negatively affect ratings and continued usage.

### 2. Optimize Application Size

Developers should evaluate opportunities to reduce unnecessary downloads and resource consumption without compromising important features.

Smaller downloads may benefit users with limited device storage or slower internet connections. The impact should be tested using installation completion rates, performance metrics, and user retention.

### 3. Use Category-Specific Benchmarks

Developers should compare their applications with others in the same category.

Relevant benchmarks include average ratings, install volumes, review counts, and application sizes.

These comparisons can help identify performance gaps and prioritize improvements based on the competitive environment.

### 4. Develop an Evidence-Based Monetization Strategy

Since free applications are much more common in the dataset, developers should carefully evaluate their pricing strategies.

Possible approaches include freemium functionality, optional premium features, subscriptions, or in-app purchases.

The most suitable strategy should depend on the target audience, user needs, conversion rates, and revenue performance rather than app counts alone.

### 5. Establish a Continuous Feedback Process

Developers should monitor ratings and review volumes regularly and investigate recurring user complaints.

Issues affecting usability, reliability, and essential functionality should be prioritized.

A consistent feedback process can help teams identify problems early and evaluate whether subsequent releases improve user satisfaction.

### 6. Plan and Evaluate Application Updates

Developers should maintain a structured release schedule and measure the effects of changes on ratings, engagement, retention, and stability.

A more complete release-history dataset would help evaluate update frequency and the relationship between releases and application performance.

### 7. Conduct Review Sentiment Analysis

Future analysis should incorporate the text of individual user reviews.

Sentiment analysis and topic classification could help identify recurring complaints, feature requests, and positive user experiences.

These findings could then guide product development priorities.

### 8. Measure More Than Installs and Ratings

Install counts and ratings alone do not provide a complete picture of application success.

Developers should also monitor active users, retention, conversion rates, revenue, crash rates, and customer lifetime value where applicable.

Combining these metrics would provide a more complete understanding of product performance.

## Project Limitations

* Install values are represented by approximate thresholds in the source dataset. Converting these values into numbers does not make them exact download counts.
* Comparisons and correlations do not establish cause and effect.
* Missing values and chart filters can affect the records included in calculations.
* A single recorded last-updated date per app is insufficient to calculate the average time between consecutive updates.
* Review text is not available, preventing sentiment and topic analysis.
* Results for content-rating groups with very few applications should be interpreted cautiously.
* The dataset does not contain all the business metrics needed to evaluate revenue, retention, or customer lifetime value.

## Repository Structure

* `README.md` — project overview, requirements, tools, challenges, insights, and recommendations.
* `Solutions.md` — answers to the project case-study questions.
* `docs/` — project reference PDF.
* `screenshots/` — dashboard screenshots.

## How to Explore the Project

1. Open the [live Looker Studio dashboard](https://datastudio.google.com/s/nFzav0hpAdk).
2. Explore the dashboard pages and available charts.
3. Review `Solutions.md` for the answers to the project questions.
4. Refer to the `screenshots/` folder for static dashboard views.

## Data Source

[Google Play Store Apps Dataset — Kaggle](https://www.kaggle.com/datasets/lava18/google-play-store-apps)

---

**Project Objective:** To use data analysis and visualization to understand Google Play Store application performance, identify actionable insights, and recommend improvements that app developers can evaluate against real-world product metrics.
