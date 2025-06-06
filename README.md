# 570_redditscraper
### Reddit Review Analyzer for Restaurant Insights
#### Overview
Reddit Review Analyzer is an AI-powered dashboard that helps restaurant owners and marketers extract actionable insights from Reddit discussions. Built using Streamlit, Amazon Bedrock, and NLP tools, the dashboard scrapes relevant Reddit posts about a restaurant, analyzes sentiment, summarizes feedback, and answers custom user questions — all in real time.

#### Problem Statement
Reddit hosts thousands of honest restaurant reviews, but owners rarely have time to sift through them. Unlike Yelp or Google, Reddit reviews often capture nuanced feedback from real users.
#### Our goal was to create a tool that:

Surfaces the most relevant Reddit posts about a restaurant

Analyzes dish-specific and service-related feedback

Generates AI summaries and answers custom questions

#### Tech Stack
Frontend: Streamlit

NLP & Summarization: Amazon Bedrock Claude 3 (via LangChain)

Sentiment Analysis: VADER

Data Source: Reddit (via LangChain's Reddit wrapper)

Backend Logic: Python

#### Features
Restaurant Search: Input a restaurant name (and optionally a location)

Reddit Scraping: Pulls top Reddit posts about the restaurant using Reddit API

Sentiment Analysis: Calculates average VADER sentiment score for the posts

Summarization: Claude 3 Sonnet summarizes feedback into key bullet points

Custom Q&A: Users can ask any question (e.g., “What are the top dishes?”)

Post Transparency: All Reddit posts used are viewable directly in the app

External Link: Google search link for the restaurant’s official website

#### How It Works
Search: User inputs a restaurant name (optionally filters by city, timeframe, or chain).

Reddit Query: LangChain interfaces with Reddit API to fetch recent relevant posts.

Sentiment Score: Each post is scored using VADER; average sentiment is displayed.

Claude Summary: Top posts are passed to Claude with a structured prompt to extract insights.

User Q&A: User questions are routed to Claude for focused answers based only on retrieved content.

#### Design Decisions
Chose Claude over OpenAI for more structured summarization

Streamlit enabled fast prototyping and simple deployment

Token constraints were managed by limiting inputs to the top 10 Reddit posts

#### Future Enhancements
Weekly auto-refresh of summaries

Integrate Yelp or Google reviews for comparison

Train a custom NER model for dish extraction

Use BERTopic or clustering to group trends over time

Conduct usability testing with restaurant owners

#### Example Output
"Customers love the spicy chicken sandwich, but many complain about long weekend wait times."

Sentiment Score: 0.24 – Generally Positive
Sample Question: “What are the most popular dishes?”
Answer: “Spicy Chicken Sandwich, Paneer Tikka, and the House Chai were mentioned frequently in a positive light.”

#### Team
Chloe Feehan and Sujanya Srinath

#### Project Files
dashboard.py – Main Streamlit app

reddit_sentiment.py – Reddit scraping and sentiment processing logic

