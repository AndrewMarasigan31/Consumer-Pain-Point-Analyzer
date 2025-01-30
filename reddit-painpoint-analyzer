import praw
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk
import json
import re
from collections import Counter

# Initialize resources
nltk.download(['vader_lexicon', 'stopwords', 'wordnet', 'punkt'])

class RedditPainPointAnalyzer:
    def __init__(self, config_path='config/config.json'):
        with open(config_path) as f:
            config = json.load(f)
            
        self.reddit = praw.Reddit(
            client_id=config['client_id'],
            client_secret=config['client_secret'],
            user_agent=config['user_agent']
        )
        
        self.sia = SentimentIntensityAnalyzer()
    
    # Include all analysis methods from previous implementation
    # [Previous analysis code here...]

if __name__ == '__main__':
    analyzer = RedditPainPointAnalyzer()
    results = analyzer.analyze_multiple_sources()
    print(results)
