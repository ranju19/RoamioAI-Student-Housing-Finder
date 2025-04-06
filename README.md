# RoamioAI-Student-Housing-Finder
Smart rental assistant that recommends student housing based on city and budget.
# 🏠 Roamio – AI Agent for International Student Housing

**Roamio** is a lightweight AI-powered chatbot that helps international students find rental housing based on their preferences, budget, and location. The assistant combines web search, semantic understanding, and localized student-specific insights to provide real-time listings, safety guidance, leasing tips, and budgeting advice — all through a conversational interface.

---

## 💡 What Is Roamio?

Roamio is designed as a helpful companion for students navigating housing in unfamiliar countries or cities. Given a natural-language query (e.g., “Find apartments in Miami under $800”), it searches the web, extracts meaningful listings, filters by budget, and supplements the results with local insights — making the housing process faster and more student-friendly.

---

## 🎯 Key Features

- 🔍 **Live Housing Search**  
  Uses a web search API to fetch real-time rental listings from websites like Rent.com.

- 💬 **Conversational Chatbot UI**  
  Built with Gradio, allowing users to type or click example queries in a simple chat window.

- 💰 **Budget-Based Filtering**  
  Extracts price ranges from natural language and filters listings accordingly.

- 🏙️ **City-Specific Guides**  
  Provides tailored advice for student housing in cities like Miami and Hartford, including:
  - Common leasing rules
  - Neighborhood tips
  - Transport options
  - Budget strategies

- 🌍 **Global Adaptability**  
  While city data is currently limited, Roamio offers fallback general advice for any unknown location.

---

## 🛠️ How It Works

1. **User Query**: A user types a housing query with natural language (e.g., “affordable housing in Hartford for students”).
2. **NLP Parsing**:
   - Extracts city and price range using regular expressions.
   - Creates a search query from the user input.
3. **Web Search**:
   - Sends the query to Serper.dev’s Google Search API.
   - Pulls back housing results with titles, links, and snippets.
4. **Price Filtering**:
   - Filters listings that match budget constraints.
   - Flags listings with terms like "cheap" or "affordable."
5. **City Guide Generation**:
   - If a city is recognized, adds detailed student-relevant insights like transportation and leasing rules.
6. **Response Composition**:
   - Combines listings + guide and returns a formatted, chat-style reply.

---

## 🧪 **Example Queries**

- Find apartments in Miami under $800
- Show houses in Hartford below $700
- Student housing near University of Miami
- Affordable rentals in Boston for international students

---

## **Tech Stack**

- Python
- Gradio – UI for chatbot interface
- Serper.dev API – Google search wrapper for web scraping
- Regex + NLP – Price and city extraction
- SentenceTransformers + ChromaDB (planned/extendable) – Optional semantic embedding or memory
- Custom JSON City Guides – Domain-specific knowledge base

  ---
  
## **City Guide Support**

- Built-in student-specific advice is available for:
- Miami, FL
- Hartford, CT

- Each guide includes:
- Neighborhood tips
- Public transport details
- Budget suggestions for prices under $700–$800
- Leasing rules specific to students

- Fallback guidance is provided for other cities with general housing tips.

---

## **Future Improvements**

- Expand city guides with global cities (e.g., London, Toronto, Sydney)
- Add memory + conversation history
- Integrate map or pricing heatmaps
- Include university dorm and roommate platforms
- Use semantic search via ChromaDB and vector embeddings

---
