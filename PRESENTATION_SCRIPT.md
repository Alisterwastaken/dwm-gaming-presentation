# 🎙️ Presentation Script: Mobile Gaming & In-App Purchase Behavior
**Course:** Data Warehousing & Mining (DWM) — ISE 1 Assignment 2  
**Speakers:** Alister Pereira & Nevan Nunes  
**Estimated Time:** 8–10 Minutes (approx. 1 min per slide)

---

## 📌 Speaker Division Overview
- **Alister:** Slide 1 (Intro & Problem Statement), Slide 3 (Business Questions), Slide 5 (Interactive Looker Studio Dashboard), Slide 7 (Business Recommendations)
- **Nevan:** Slide 2 (Dataset & Data Exploration), Slide 4 (Data Visualizations & Rationales), Slide 6 (Key Findings), Slide 8 (Conclusion & Wrap-up)

---

## Slide 01: Title & Problem Statement
*Displayed: Slide 01 / 08*  
**Speaker: Alister**

> **[Alister]:**  
> "Good morning, respected Professor and classmates. Today, Nevan and I are excited to present our DWM ISE project titled: **Mobile Gaming and In-App Purchase Behavior**.
>
> The Indian mobile gaming industry has seen explosive growth over recent years, with millions of young players clocking hours every single day. However, from a business perspective, game studios face a critical monetization paradox: free-to-play titles attract enormous user bases, but **only a tiny fraction ever convert to paying players**. Even worse, aggressive ad monetization often backfires, driving players to abandon the game entirely.
>
> In this study, we analyzed survey data collected from 77 young gamers across 21 distinct attributes to uncover the psychological triggers behind in-game spending, identify ad tolerance thresholds, and pinpoint the exact churn drivers that cause players to quit. Our goal is to translate raw player feedback into data-driven monetization and retention strategies.
>
> I’ll now hand over to Nevan to walk us through the dataset and initial data exploration."

---

## Slide 02: Dataset & Data Exploration
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 02 / 08*  
**Speaker: Nevan**

> **[Nevan]:**  
> "Thank you, Alister. 
>
> For our analysis, we gathered primary data through a targeted Google Form conducted between October 5th and 7th, 2026. We gathered **77 total responses** across **21 attributes**. 
>
> Looking at our top KPI cards: 74 of our respondents are active gamers, while 3 indicated they do not play mobile games.
>
> We categorized our 21 attributes into five key dimensions:
> 1. **Demographics:** Age group, year of study, gender (which skewed 89.6% male), and primary device.
> 2. **Gaming Habits:** Weekly hours, genre, preferred play time, and solo vs. squad play style.
> 3. **Monetization Metrics:** Spend rates, monthly budget tiers, purchase triggers, and payment methods.
> 4. **User Experience:** Ad sentiment, game satisfaction ratings, quit drivers, and subscription willingness.
> 5. **Metadata:** Unique timestamps and validation checks.
>
> During our Data Quality Assessment, we encountered a few practical data challenges:
> - The 3 non-gamers skipped survey sections via conditional branching.
> - 7 responses had partial entries for satisfaction and quit reasons.
> - Multi-select responses—like purchased item categories and quit reasons—were stored as comma-separated strings that required string tokenization and frequency encoding during data preparation.
>
> Having cleaned and structured the data, Alister will now walk through the business questions that guided our study."

---

## Slide 03: Business Questions
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 03 / 08*  
**Speaker: Alister**

> **[Alister]:**  
> "To give our data mining an objective direction, we formulated **five core business questions**:
>
> 1. **Question 1:** *What are the primary spending patterns and monthly spend distributions?* This helps us segment the player base into micro-spenders versus high-value 'whales'.
> 2. **Question 2:** *Which specific items and triggers convert free players into paying customers?* We wanted to see whether battle passes, cosmetics, or loot boxes offer the highest conversion ROI.
> 3. **Question 3:** *How do ad experiences affect player retention?* Specifically, at what frequency do ads trigger game abandonment?
> 4. **Question 4:** *Is a monthly subscription model viable for this demographic?* Can studios introduce an ad-free tier with perks to establish predictable recurring revenue?
> 5. **Question 5:** *What are the leading causes of churn?* By ranking churn drivers—whether it's ads, boredom, pay-to-win mechanics, or friends quitting—studios can prioritize retention engineering.
>
> Nevan will now demonstrate how we visualized the data to answer these questions."

---

## Slide 04: Data Visualization
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 04 / 08*  
**Speaker: Nevan**

> **[Nevan]:**  
> "On Slide 4, we’ve highlighted six core charts, each selected with a specific analytical rationale:
>
> - **Top-Left (Monthly Spend Distribution):** We used a horizontal bar chart to showcase spend tiers. You’ll immediately notice a bimodal 'barbell' pattern: 31% spend in the ₹1–100 micro-tier, while 34% spend upwards of ₹1,000 per month.
> - **Top-Right (Ad Sentiment Breakdown):** Using a doughnut chart, we see that only 12% of players don't mind ads. A startling 29% have quit a game due to ads, and 24% are willing to pay to remove them.
> - **Middle-Left (Top Items Purchased):** Skins and cosmetics dominate the bar chart with 57 mentions, followed by in-game currency and battle passes. Loot boxes and pay-to-win items rank much lower.
> - **Middle-Right (Quit Reasons Radar):** The radar chart illustrates multi-factorial churn. 'Too many ads' (38 mentions) and 'Boring/repetitive gameplay' (37 mentions) form the two dominant vertices.
> - **Bottom-Left (Satisfaction):** The polar area chart indicates that while average satisfaction is high at 4.15 out of 5, 18% of gamers rate their experience 3 or lower.
> - **Bottom-Right (Subscription Willingness):** The pie chart reveals our biggest surprise: although only 9% definitively say 'Yes', a massive **47% say 'Maybe'**, creating a large persuadable audience.
>
> Alister will now present our Interactive Looker Studio Dashboard."

---

## Slide 05: Interactive Dashboard
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 05 / 08*  
**Speaker: Alister**

> **[Alister]:**  
> "To enable business stakeholders to explore these relationships interactively, we built a BI dashboard using **Google Looker Studio**.
>
> *[Point to screen or click on the live dashboard]*  
> As you can see embedded right here in the slide, the dashboard features real-time interactive slicers for Gender, Age Group, Game Title, and Spend Tiers.
>
> Our top KPI scorecards instantly summarize the cohort: 77 total respondents, 4.15 average satisfaction, and a 60.8% spend conversion rate.
>
> Through cross-filtering, selecting a specific game—such as *Mobile Legends: Bang Bang* or *Valorant*—automatically cross-filters the device split and spend metrics for that cohort. We've also included an offline summary tab as a backup, and an external direct launch button for full-screen analysis.
>
> Now, let’s synthesize what the data actually tells us in our Key Findings."

---

## Slide 06: Key Findings
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 06 / 08*  
**Speaker: Nevan**

> **[Nevan]:**  
> "Synthesizing our exploratory and visual analysis, five decisive findings emerge:
>
> 1. **Cosmetics Rule Monetization:** 77% of paying gamers purchase skins, with 'Looks and Aesthetic Style' cited by 59% as their primary motivation. Pay-to-win items, by contrast, generate severe player backlash.
> 2. **Ads are the Primary Churn Driver:** Over 56% of surveyed gamers cited excessive ads as their primary reason for leaving a game.
> 3. **The Bimodal Spend Curve:** The player base splits into casual micro-spenders (₹1–100) and dedicated whales (₹1,000+). Mid-tier spending (₹100–300) is almost non-existent.
> 4. **The Untapped 'Maybe' Majority:** Nearly half (47%) of respondents are open to a monthly subscription pass if priced appropriately.
> 5. **Social Play as an Engagement Anchor:** 66% of respondents play in squads or hybrid modes. When friends quit, individual players churn soon after.
>
> Alister will now explain how we translate these findings into business recommendations."

---

## Slide 07: Business Value & Recommendations
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 07 / 08*  
**Speaker: Alister**

> **[Alister]:**  
> "Data insights are only as valuable as the decisions they drive. In our Business Value Matrix on Slide 7, we propose five direct interventions:
>
> 1. **Cosmetic-First Economy:** Shift completely away from pay-to-win mechanics toward seasonal cosmetic bundles and battle passes. This protects player goodwill while maximizing revenue from aesthetic buyers.
> 2. **Intelligent Ad Capping & Ad-Free Pass:** Cap interstitial ads to a maximum of 3 per session, rely predominantly on rewarded-video ads, and offer an entry-level ₹49/month ad-free subscription. This mitigates up to 40% of ad-driven churn.
> 3. **Tiered Subscription Model:** Target the 47% 'Maybe' cohort with three structured tiers—Basic (₹49), Premium (₹149), and Elite (₹299)—backed by a 7-day free trial.
> 4. **Social & Squad Retention Features:** Introduce squad milestones and 'invite a lapsed friend' mutual incentives to combat cascade squad churn.
> 5. **Frictionless UPI Integration:** Because UPI accounts for 74% of transactions, studios must integrate direct one-tap UPI SDKs and offer micro-transaction bundles from ₹10 to ₹50 to capture impulse spenders.
>
> Nevan will now conclude our presentation."

---

## Slide 08: Conclusion & Wrap-Up
*Action: [Next Slide / Right Arrow →]*  
*Displayed: Slide 08 / 08*  
**Speaker: Nevan**

> **[Nevan]:**  
> "To conclude, our study of 77 young Indian gamers proves that players **want** to engage and spend—provided the game respects their time and avoids intrusive ads or pay-to-win barriers.
>
> By executing the full data analytics lifecycle—from Google Forms data collection, to Python and Sheets preprocessing, to Chart.js exploratory analysis, and finally Looker Studio BI dashboarding—we demonstrated how data moves from **raw observations → clear insights → business decisions → tangible value**.
>
> We would like to thank our professor and peers for your time and attention. Alister and I are now open to any questions!"

---

## 💡 Quick Tips for Delivery:
- **Pacing:** Keep a natural conversational pace; aim for ~1 minute per slide.
- **Handoffs:** Use natural physical or verbal cues when handing off between Alister and Nevan.
- **On Slide 5 (Dashboard):** Click on the embedded Looker Studio report to demonstrate interactivity (e.g., clicking on a filter chip or bar chart).
- **Navigation:** Use the Left/Right arrow keys or the on-screen buttons to smoothly advance slides.
