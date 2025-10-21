# [Mood Flow Analytics](https://s.craft.me/eOwTsRACWYvvke)

## Python analysis pipeline

<details>
  <summary>Phase 1: Setup & Exploration</summary>

  - Load data
  - Inspect structure
  - Understand distributions

</details>

<details>
  <summary>Phase 2: Data Cleaning</summary>

  - Handle missing values
  - Validate ranges
  - Remove duplicates

</details>

<details>
  <summary>Phase 3: Feature Engineering</summary>

  - Create derived features
  - Encode categorical variables
  - Calculate lag features

</details>

<details>
  <summary>Phase 4: Exploratory Data Analysis</summary>

  - Visualize distributions
  - Create correlation heatmap
  - Identify patterns

</details>

<details>
  <summary>Phase 5: Correlation Analysis</summary>

  - Calculate correlations
  - Rank feature importance
  - Generate insights

</details>

<details>
  <summary>Phase 6: Predictive Modeling</summary>

  - Build ML model
  - Train and evaluate
  - Make predictions

</details>

#### Phase 1-3 (LOAD & INSPECT DATA, DATA CLEANING & VALIDATION, FEATURE ENGINEERING
  - **Clean data** - No missing values means less preprocessing work
  - ✅ **Good data quality** - All ranges make sense
  - ✅ **Solid dataset** - 300 entries across 50 users is great for analysis
  - ✅ Understood the user distribution (50 users, 2-11 days each)
  - ✅ **Complete feature engineering** - Created ALL the features (Sleep_Deficit, Day_of_Week, Is_Weekend, Is_Active, High_Screen_Time, Sleep_Quality_Score, High_Mood, High_Productivity, Previous_Day_Mood,Previous_Day_Productivity)
  - **Interesting observation:** Screen_Time goes up to 11 hours (someone's having a binge day! 😅)
  - **Good distribution:** Most people have "Good" sleep quality (120/300 entries)
  - **50 lag values missing** - Expected and correct (first day per user)

#### Phase 4 (Exploratory Data Analysis)

**Histograms** - "What's the shape of my data?"

Purpose: Understand the DISTRIBUTION - how spread out or concentrated the data is

![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/83D9B154-0992-4713-BE24-5198F5A0AF3D_2/3JfyfgDPNy9SS2PC3OTf9CJvl7hU6TFHdysVllpJeAAz/Image.png)



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/C56E0631-F5D7-45BD-AB70-FDF661AEE1E1_2/1tccuG1eevQVECsyocfBD4MMHmiptD5OeJGoX2I6uLkz/Image.png)

**Scatter Plots** - "Is there a relationship between two things?"

Purpose: Visualize if/how one variable correlates with another



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/3FEBEECA-F9B3-44FE-B4FB-9B3872593EAA_2/4otdadfp4zHVQh4EvjGzyYxoINj0xmYOvNITBN0JMEQz/Image.png)

**Box Plots** - "How does a categorical factor affect my outcome?"

Purpose: Compare how different GROUPS behave (Poor vs Good sleep, Sunny vs Rainy weather, etc.)

![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/56B3D484-21B3-4E29-B581-C01D0DEE08E7_2/C1InaYiyuvTNNh5Uir5OmYsxL9y7L1NiUj4E51yCgGcz/Image.png)

**Line Graphs** (Time Series) - "How do patterns change over time?"

Purpose: See TRENDS and PATTERNS within an individual's data

![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/1BB8395F-B20B-4BEA-8E97-E2A1649F0D5B_2/Whx9PulBJJReWMn0CQndi8b6tP0GRkgyNhPQmp1Xpfoz/Image.png)



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/4BF55D23-557F-4339-B3B0-DD1F7D1C7E50_2/kNZE9ytfTb2B3xExs6BHuNSpMVZVbMUBkuzR5BpKIHwz/Image.png)



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/2FEA7C13-428F-4BB7-AD00-1991032F1077_2/PIlkhA2GNudWoFb0XasLXyn73wHF59RQVYI4V9W8Ytwz/Image.png)



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/303BE126-64C1-423C-9F44-753C04631CF5_2/WTRdyY8H3iJxjEinFKoURHWvxZdhR7Dl0ttkAp2G6akz/Image.png)



![Image.png](https://resv2.craft.do/user/full/34de0a68-4b4d-ecb0-6c1b-0c3cfda2286e/doc/0469BF34-0BF8-4904-BBEA-2BC67DCEA968/BA3A2DC5-4A79-4308-9D57-81F07B5DD90E_2/TMoUZbeD75BelyTRkk4jNsxIwFYOrrQ0IqcmrYIyG8Yz/Image.png)
