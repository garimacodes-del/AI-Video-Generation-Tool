# AI-Video-Generation-Tool
An AI-based automation tool that creates short from videos trending news articles using NLP and generative AI.

# AI Video Generation Tool

An AI-powered application that automates the creation of short videos from trending news articles using NLP and generative video tools like Lumen5 or InVideo.

---

#Features

- Fetches trending news using NewsAPI
- Auto-generates a short news script using NLP
- Creates 30–60 second videos using generative video APIs
- Designed for social media sharing, news platforms, and content creators

---

##  Workflow / Pipeline

1. **Trending News Fetching**
   - Source: [NewsAPI.org](https://newsapi.org)
   - Filters news by region (e.g., US)

2. **Script Generation**
   - Uses a template-based approach or NLP summarization techniques

3. **Video Generation**
   - Tools: Lumen5 / InVideo API (or alternative)
   - Includes overlays, text, and background visuals

---

## Example Code

```python
import requests

# Step 1: Fetch News
url = "https://newsapi.org/v2/top-headlines"
params = {"country": "us", "apiKey": "YOUR_API_KEY"}
response = requests.get(url, params=params)
articles = response.json()["articles"]

# Step 2: Generate Script
template = "Title: {title}\n\n{content}"
script = template.format(title=articles[0]["title"], content=articles[0]["description"])

# Step 3: Generate Video (Pseudo)
video_payload = {"text": script, "duration": 60, "style": "news"}
# response = requests.post(video_api, json=video_payload, headers={"Authorization": "Bearer API_KEY"})

