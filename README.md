# Google Play Store App Insights — Looker Studio

This project is a data storytelling and dashboarding case study focused on the Google Play Store dataset. The goal was to analyze app performance and answer a structured set of business questions using a Looker Studio dashboard, while also documenting the key findings, challenges, and recommendations for future improvement.

Live dashboard:
https://datastudio.google.com/s/nFzav0hpAdk

## Project overview

The repository contains a dashboard and supporting analysis built around the Google Play Store App Insights case study. The work focuses on understanding how apps perform across categories, price points, content ratings, install ranges, app sizes, and update patterns.

The dashboard summarizes the app dataset with business-ready metrics such as:

- Total apps analyzed
- Total installs
- Total reviews
- Average app rating
- Distribution of free vs. paid apps
- App size and content rating breakdowns
- Category and genre performance
- Update trends over time

The overall story presented by the dashboard is that the Google Play ecosystem is dominated by free apps, with a large majority of users installing communication, productivity, entertainment, and gaming apps. At the same time, app quality is not determined solely by price or size; higher-rated apps can appear across a wide range of install volumes and categories.

## Why this project matters

This project is useful because it blends business analysis with data visualization. Instead of only reporting raw numbers, it turns a large app dataset into actionable insights that help answer questions like:

- Which app categories attract the most users?
- How does app size influence installs or ratings?
- Are free apps much more common than paid apps?
- Which content ratings are dominant in the ecosystem?
- What patterns exist in app updates and historical growth?

This type of dashboard is valuable for product teams, app analysts, and digital strategy stakeholders who want to understand what is working in the app marketplace.

## Project requirements

The project was designed around a clear set of analytical requirements:

1. Analyze the available Google Play app dataset without losing the original business context.
2. Build a dashboard that can answer both basic and advanced questions from the case study.
3. Represent the data in a clear, visual, and intuitive way for non-technical stakeholders.
4. Validate core metrics such as average rating, install totals, free-vs-paid split, and category distribution.
5. Document not only the final findings but also the reasoning and limitations of the analysis.
6. Present the insights in a format that is easy to review and share.

These requirements guided both the dashboard design and the written analysis in the supporting documentation.

## Repository structure

The repository is intentionally lightweight and contains the main analysis materials:

- `README.md` — project summary and documentation
- `Solutions.md` — business questions and answers for the case study
- `docs/` — supporting documentation and reference files
- `screenshots/` — dashboard screenshots showing key visuals and layouts

## Tools and technologies

This project relies mainly on business intelligence and reporting tools rather than a traditional software stack.

### Primary tools

- Google Looker Studio
  - Used to build the dashboard
  - Ideal for interactive reporting, KPI cards, charts, tables, and filters
- Google Play Store dataset / app metrics source
  - Main input for the case study analysis
- Power BI reference material
  - Used as a benchmark and comparison point for validation of findings

### Workflow used

- Review the app dataset and case-study business questions
- Identify the important dimensions and KPIs
- Build dashboard visuals for summary and deeper analysis
- Cross-check metric calculations and interpretation
- Document answers, insights, and recommendations

## Methodology

The analysis followed a practical business intelligence workflow:

1. Understand the problem context
   - The project starts with a case study and a clear set of exploration questions.

2. Define the key metrics
   - Average rating
   - Total installs
   - Number of apps by category
   - App size distribution
   - Free vs paid share
   - Review counts
   - Update trends

3. Design meaningful visuals
   - KPI cards for quick summary
   - Donut charts for free vs paid
   - Bar charts for category performance
   - Scatter plots for installs vs ratings
   - Tables for top apps and category comparisons

4. Interpret with caution
   - Some patterns are descriptive, not causal
   - Visual trends need business context before being treated as direct recommendations

## Challenges faced

Several challenges were encountered while building and interpreting the dashboard.

### 1. Large and multi-dimensional dataset
The Google Play dataset contains many app attributes, including category, content rating, price, size, installs, rating, and review metrics. Combining these dimensions in a clear dashboard required careful filtering and chart selection.

### 2. Understanding metric interpretation
Some metrics are intuitive but can be misleading without context. For example, a high average rating does not necessarily mean that most apps are rated highly, and install counts can vary massively across categories and app types.

### 3. Need for meaningful business questions
A dashboard is much more useful when tied to decision-driven questions. The project had to balance technical completeness with practical business interpretation.

### 4. Data quality and ambiguous categories
Some rows or classifications may be incomplete or inconsistent, especially when comparing free vs paid apps, content ratings, or category-level distributions. The analysis needed to keep interpretation honest and not overstate certainty.

### 5. Turning analysis into insight
The hardest part was not generating charts but translating them into clear business insights that a stakeholder could act on without a technical background.

## Key insights from the analysis

The analysis produced several important findings:

- Average rating is around 4.17 out of 5, indicating generally positive sentiment.
- Free apps dominate the store, with around 92.2% of the surveyed apps being free.
- The most common content rating is "Everyone".
- Game, Communication, Tools, Family, and Productivity categories lead in total installs.
- App size does not have a direct and obvious relationship with install success.
- High-quality apps can appear in many categories, not only in premium or paid segments.
- Apps with large review volumes often also have very high install numbers, suggesting a strong connection between user engagement and visibility.

The visualizations also show that category and content strategy matter as much as raw product quality. For example, a category like Games may dominate installs because of user behavior and retention, but that does not mean all app types should be treated the same way.

## Dashboard highlights

The project includes visual summaries such as:

- KPI cards for dataset overview
- App category and genre rankings
- Install distribution by app type and content rating
- Rating trends and pricing comparisons
- Top reviewed and highly installed apps
- Update frequency and historical app growth

Screenshots of the dashboard are included in the repository to provide a visual record of the reporting experience.

<img width="1440" height="1078" alt="Looker dashboard overview" src="https://github.com/user-attachments/assets/b492cadc-a2c2-4822-8bf4-2df5ed392209" />
<img width="1441" height="1078" alt="Looker dashboard second view" src="https://github.com/user-attachments/assets/48567b0f-114d-4dd4-9878-96c37c862902" />
<img width="1437" height="1078" alt="Dashboard detail view" src="https://github.com/user-attachments/assets/f2d5259c-db8c-4182-8bf4-2df5ed392209" />
<img width="1447" height="1078" alt="Dashboard chart comparison" src="https://github.com/user-attachments/assets/37470232-7f60-425c-9f92-7f96dee72b95" />

## Recommendations for improvement

To take the project further, the following improvements would make the analysis more actionable:

### 1. Add deeper segmentation
Break the data down by geography, app category, and user acquisition channel to understand where performance differences are driven by audience behavior.

### 2. Include a review text sentiment layer
The current dashboard focuses on rating and counts. Adding text-based sentiment analysis would reveal what users actually like or dislike about apps.

### 3. Introduce trend-based forecasting
Append time-series analysis to forecast install and rating evolution, especially during app update cycles and seasonal changes.

### 4. Add conversion metrics
A stronger product view would combine installs with retention, review frequency, and update behavior to show whether high installs translate into long-term engagement.

### 5. Improve business storytelling
Set up narrative sections or executive summary pages to explain the story behind the numbers, not just the numbers themselves.

### 6. Expand the data model
If the dataset is updated, add more dimensions such as app age, developer performance, and monetization strategy to support richer strategic analysis.

## Conclusion

This project demonstrates how a moderately complex dataset can be transformed into a compelling business dashboard with clear, actionable insights. The work is not only about generating charts; it is about turning raw app metadata into strategic understanding.

The strongest value of the project lies in its combination of:

- structured business questions
- dashboard-driven storytelling
- clear KPI visualization
- practical insight generation
- honest interpretation of trends and limitations

This makes the repository a strong example of a case-study-driven analytics project that bridges raw data and decision-making.

## Related files

- `Solutions.md` contains the complete question-answer breakdown for the case study.
- `docs/App Insights (PowerBI).pdf` serves as a reference for comparison and validation.
- `screenshots/` contains the dashboard snapshots used to support the narrative.
