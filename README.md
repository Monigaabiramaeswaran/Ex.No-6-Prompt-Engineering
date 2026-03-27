Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Aim: 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

# Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

# Program:
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated text
generated_text = input()

print("Generated Review:\n")
print(generated_text)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

# Insight generation
compound = sentiment['compound']

if compound >= 0.05:
    print("\nInsight: The review is positive and highly suitable for marketing promotion.")
elif compound <= -0.05:
    print("\nInsight: The review is negative and may highlight product issues that need attention.")
else:
    print("\nInsight: The review tone is neutral and could be improved with more specific pros or cons.")

# Positive condition (compound ≥ 0.05)

# Input review:
text
This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.
Possible sentiment + insight:

text
Sentiment Analysis:
{'neg': 0.0, 'neu': 0.45, 'pos': 0.55, 'compound': 0.91}

Insight: The review is positive and highly suitable for marketing promotion.

# Negative condition (compound ≤ -0.05)

# Input review:

text
This smartphone is terrible, the battery dies quickly and the camera quality is awful.
Possible sentiment + insight:

text
Sentiment Analysis:
{'neg': 0.63, 'neu': 0.37, 'pos': 0.0, 'compound': -0.75}

Insight: The review is negative and may highlight product issues that need attention

# Neutral condition (-0.05 < compound < 0.05)

# Input review:

text
This smartphone is okay, it works as expected but nothing really stands out.
Possible sentiment + insight:

text
Sentiment Analysis:
{'neg': 0.05, 'neu': 0.86, 'pos': 0.09, 'compound': 0.02}

Insight: The review tone is neutral and could be improved with more specific pros or cons.

# Result: 

This experiment shows that Python can integrate an AI sentiment tool (VADER in NLTK) to automatically analyze text and classify it as positive, negative, or neutral based on the compound score.overall, the code proves that combining AI APIs with Python logic enables automated, actionable feedback for real-world reviews like smartphone user comments.
