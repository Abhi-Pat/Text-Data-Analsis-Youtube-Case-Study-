### Repository Extended Description
# Text-Data-Analsis-Youtube-Case-Study-
This repository follows a systematic approach to analyzing YouTube comments and related data through various data processing and visualization techniques.

**Steps Performed:**

1. **Data Preparation:**
   - Imported all necessary packages: `pandas`, `numpy`, `seaborn`, `matplotlib.pyplot`, `TextBlob`, `WordCloud`, `STOPWORDS`, `emoji`, `plotly.graph_objs`, `iplot`, `os`, `filterwarnings`, and `plotly.express`.
   - Loaded the CSV data and checked for missing values. Any missing values were identified and dropped, as the number of missing entries was minimal. The DataFrame was updated accordingly.

2. **Sentiment Analysis:**
   - Performed sentiment analysis on the comments to evaluate user sentiments.
   - Polarity values were inserted into the comments DataFrame, with the feature name defined as "polarity".

3. **WordCloud Analysis:**
   - Conducted exploratory data analysis (EDA) on the most positive and negative sentences.
   - The `comment_text` feature was transformed into a string format for word cloud generation.
   - **Conclusion:** Positive users tend to emphasize words like "best," "awesome," "perfect," "amazing," "look," and "happy." On the other hand, negative users focus on terms like "terrible," "worst," "horrible," "boring," and "disgusting."

4. **Emoji Analysis:**
   - Extracted emojis from the `comment_text` field and computed the frequency of each emoji in the `all_emojis_list`.
   - Visualized the data as a bar chart using `plotly.graph_objs` and `iplot`.
   - **Conclusion:** The majority of customers seem to be happy, as the most frequent emojis include "funny," "love," "heart," and "outstanding."

5. **Data Collection and Analysis:**
   - Collected data from YouTube by extracting CSV files from the additional data folder.
   - Exported and stored the data in CSV, JSON, and database formats.
   - Conducted graphical analysis on the extracted JSON files:
     - **Category Analysis:** Connected the category ID with the `item` column and mapped the category name to the category ID.
       - **Graph 1:** Relationship between category name and likes (`x='category_name'`, `y='likes'`).
       - **Graph 2:** Relationship between category name and like rate (`x='category_name'`, `y='like_rate'`).
     - **Scatter Charts:**
       - `x='views'`, `y='likes'`
       - `x='views'`, `y='like_rate'`
     - **Heatmap:** Correlation analysis between views, likes, and dislikes (`full_df[['views', 'likes', 'dislikes']].corr()`, annot=True).
     - **Bar Chart:** Visualized the total number of videos per channel (`x='channel_title'`, `y='total_videos'`).
     - **Punctuation Analysis:** Analyzed the relationship between punctuation in titles and tags with views, likes, and dislikes.
       - `x='count_punc'`, `y='likes'`
       - `x='count_punc'`, `y='views'`

This repository provides a comprehensive approach to analyzing YouTube data through sentiment analysis, emoji usage, word cloud generation, and detailed graphical analysis.
