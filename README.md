# ai-social-media-agent
AI social media automation agent

## AI Social Media Agent (LangGraph + Gemini)

A free, local-first AI social media agent** that researches a topic, drafts a post, critiques it, and delivers a polished, ready-to-publish caption.

- Tech: Python, LangGraph, LangChain (Gemini), DuckDuckGo Search
- Use‑case: Quickly generate high‑quality social posts with an agentic workflow
- Cost: You only pay for your own Gemini API usage (no extra SaaS)

---

### Features

- **Agentic workflow** – `Search → Draft → Review → Finalize`
- **Web research** – pulls fresh context from DuckDuckGo
- **LLM-powered writin**

**g** – uses Gemini Flash via `langchain-google-genai`

- **Automatic critique + rewrite** – improves tone, clarity, engagement, and hashtags
- **Portfolio-friendly** – saves the final caption to `final_post.md` for easy sharing

---

### How it works

1. **Search**
    
    Uses `duckduckgo-search` to gather short snippets about your topic.
    
2. **Draft**
    
    Calls Gemini (via `ChatGoogleGenerativeAI`) to generate the first version of the post.
    
3. **Review**
    
    Asks Gemini to critique the draft for engagement, clarity, and hashtag usage.
    
4. **Finalize**
    
    Rewrites the post using the critique and writes the result to `final_post.md`.
    

You interact with it from the terminal by providing just **one input: the topic**.

---

### Getting started

### 1. Clone the repository

```bash
git clone https://github.com/Aaryankansari/ai-social-media-agent.git
cd ai-social-media-agent
```

### 2. Configure your environment

Create a `.env` file in the project root:

```bash
GOOGLE_API_KEY=your-google-api-key-here
```

Make sure this API key has access to the Gemini models.

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

### Running the agent

From the project root:

```bash
python main.py
```

You’ll be prompted for a topic, for example:

```
Enter a topic for the social media post: agentic AI for creators
```

The script will:

1. Research the topic
2. Write an initial draft
3. Critique and improve it
4. Print the result in the terminal and save it to `final_post.md`

`final_post.md` is ignored by git so generated content doesn’t clutter your commits.

---

### Tech stack

- `Python 3.10+`
- `langgraph`
- `langchain-google-genai`
- `duckduckgo-search`
- `python-dotenv`

---

### Ideas for extensions

- Add **platform-specific styles** (X, LinkedIn, Instagram, TikTok)
- Schedule posts or send them to a **social media API**
- Store past posts and topics in a **database** for reuse and analytics

Feel free to fork this, experiment with prompts, or open issues/PRs with suggestions.