# 🛍️ ShopSmart — AI-Powered E-Commerce Chatbot

A beautiful, fully-functional single-file e-commerce website featuring an AI-powered shopping assistant built with React.js, Tailwind CSS, and the Groq AI API.

---

## ✅ Completed Features

### 🏪 E-Commerce Landing Page
- **Sticky Navigation** — Logo, nav links, search, wishlist, cart, sign-in button, mobile hamburger menu
- **Hero Section** — Gradient background, tagline, CTA buttons, decorative blobs
- **Stats Bar** — 50K+ customers, 10K+ products, 99% satisfaction, 24/7 AI support
- **Featured Products Grid** — 6 products with emoji visuals, tag badges, price, star rating, and "Add to Cart" button
- **Promo Banner** — Discount offer section with gradient background
- **Testimonials** — 3 customer reviews with star ratings
- **Footer** — Company links, social icons, legal links, payment icons

### 🤖 AI Chatbot Widget
- **Floating Chat Button** — Fixed at bottom-right with animated pulse ring, shopping cart emoji, unread badge
- **Smooth Open/Close** — Slide-up animation when chat window opens
- **Chat Header** — Bot name, green online status dot, clear chat button, close button
- **Message Bubbles** — User messages (blue gradient, right), AI messages (white, left) with avatar icons
- **Typing Indicator** — Three animated bouncing dots while AI generates response
- **Timestamps** — Formatted time (e.g., 2:35 PM) shown under each message
- **Auto-scroll** — Chat automatically scrolls to the latest message
- **Quick Suggestions** — Chip buttons (Best Laptops, Today's Deals, Track Order, Return Policy)
- **Product Cards** — Compact product cards shown inline in chat when users ask about laptops, phones, audio
- **Welcome Message** — Friendly greeting when chat first opens
- **Clear Chat** — Button to reset conversation history
- **Keyboard Support** — Press Enter to send, Shift+Enter for newline

### 🔗 Groq AI Integration
- API endpoint: `https://api.groq.com/openai/v1/chat/completions`
- Model: `llama3-8b-8192`
- System prompt configured for e-commerce shopping assistant
- Full conversation history maintained across messages
- Graceful error handling for missing key, invalid key, rate limits

---

## 🚀 How to Get Started

### Step 1 — Get a Free Groq API Key
1. Go to [https://console.groq.com](https://console.groq.com)
2. Sign up for a free account
3. Navigate to **API Keys** → **Create API Key**
4. Copy your key

### Step 2 — Add Your Key
Open `index.html` in a text editor and find this line near the top of the `<script>` tag:

```js
const GROQ_API_KEY = "PASTE_YOUR_GROQ_API_KEY_HERE";
```

Replace it with your actual key:

```js
const GROQ_API_KEY = "gsk_xxxxxxxxxxxxxxxxxxxxxxxx";
```

### Step 3 — Open in Browser
Simply open `index.html` in any modern browser. No build step, no server required!

---

## 📁 Project Structure

```
index.html        ← Complete single-file application
README.md         ← This file
```

---

## 🔧 Tech Stack

| Technology      | Version | Purpose                        |
|----------------|---------|--------------------------------|
| React.js        | 18      | UI components (via CDN)        |
| Tailwind CSS    | 3.x     | Styling (via CDN)              |
| Babel Standalone| Latest  | JSX transpilation in browser   |
| Groq API        | —       | AI chat completions            |
| Font Awesome    | 6.4.0   | Icons                          |
| Google Fonts    | —       | Inter font family              |

---

## 💬 AI Configuration

```js
const GROQ_API_KEY = "PASTE_YOUR_GROQ_API_KEY_HERE";
const GROQ_ENDPOINT = "https://api.groq.com/openai/v1/chat/completions";
const GROQ_MODEL    = "llama3-8b-8192";
```

**System Prompt:**
> "You are an AI shopping assistant for ShopSmart, a premium e-commerce store. Help users find products, answer questions about price, delivery, return policy, and recommend products politely. Keep responses concise (2–4 sentences max) and friendly."

---

## 🛒 Mock Product Catalog

| Product                 | Price  | Category | Rating |
|------------------------|--------|----------|--------|
| MacBook Air M3          | $1,099 | Laptop   | 4.9    |
| Dell XPS 15             | $1,299 | Laptop   | 4.7    |
| ASUS ROG Zephyrus G14   | $999   | Laptop   | 4.6    |
| iPhone 15 Pro           | $999   | Phone    | 4.8    |
| Samsung Galaxy S24      | $799   | Phone    | 4.7    |
| Google Pixel 8 Pro      | $699   | Phone    | 4.6    |
| Sony WH-1000XM5         | $349   | Audio    | 4.9    |
| AirPods Pro 2nd Gen     | $249   | Audio    | 4.8    |
| iPad Pro 12.9"          | $1,099 | Tablet   | 4.8    |

---

## 🎯 Quick Suggestion Triggers

| Button Label       | Message Sent                            | Shows Products  |
|-------------------|-----------------------------------------|-----------------|
| 🔥 Best Laptops   | "What are the best laptops available?"  | Laptop cards    |
| 💰 Today's Deals  | "Show me today's best deals"            | Top 3 products  |
| 📦 Track Order    | "How can I track my order?"             | None            |
| ↩️ Return Policy  | "What is your return policy?"           | None            |

---

## ⚠️ Error Handling

| Scenario              | Message Shown                                      |
|-----------------------|----------------------------------------------------|
| No API key set        | Instructions to add the API key                    |
| Invalid API key (401) | "Invalid API key" message                         |
| Rate limited (429)    | "Too many requests, wait and retry" message        |
| Generic error         | "Something went wrong, try again" message          |

---

## 🔮 Features Not Yet Implemented

- [ ] Real product search with filters and sorting
- [ ] User authentication and saved wishlists
- [ ] Shopping cart persistence with localStorage
- [ ] Checkout flow and payment integration
- [ ] Order tracking system
- [ ] Product detail pages
- [ ] Search bar functionality
- [ ] Category browsing pages

---

## 📈 Recommended Next Steps

1. **Connect a real product API** (e.g., Fake Store API, or your own backend)
2. **Add localStorage** for cart persistence across sessions
3. **Implement user accounts** with wishlist sync
4. **Add product search** powered by vector embeddings
5. **Deploy to production** via the Publish tab
6. **Add analytics** to track chatbot conversation metrics
7. **Swap model** to `llama3-70b-8192` for higher quality responses

---

## 🌐 Deployment

To make this website live, go to the **Publish tab** and click Publish. No server configuration needed — it's a pure static site!
