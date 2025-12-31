# Competitive Analysis Tool

> **AI-Powered Market Intelligence CLI Tool**

A powerful command-line competitive analysis tool built with **NeuroLink**, designed to help merchants make data-driven pricing decisions through automated market research and intelligent recommendations.

---

## 📋 Executive Summary

This project provides an intelligent CLI tool that empowers merchants to understand their competitive positioning in real-time. By accepting product images, names, or specifications as input, the system analyzes the market landscape and delivers actionable insights including competitor pricing, market trends, and strategic recommendations to increase order volume and revenue.

### Problem Statement

- **Manual price research** is time-consuming and inefficient
- **Lack of real-time market intelligence** leads to missed opportunities
- **Difficulty identifying optimal pricing strategies** results in lost sales
- **No unified view** of competitor landscape across multiple platforms

### Solution

An AI-powered competitive analysis tool that:
- ✅ Accepts multiple input formats (images, product names, specifications)
- ✅ Performs intelligent product identification using AI vision models
- ✅ Gathers real-time pricing data from multiple e-commerce platforms
- ✅ Analyzes market positioning with lowest, average, and highest price metrics
- ✅ Identifies refurbished products separately for accurate comparison
- ✅ Generates actionable business recommendations

---

## 🎯 Key Features

### Multi-Modal Input Processing
- **Product Image**: AI-powered image analysis to identify products from Image
- **Product Name**: Direct text-based product search
- **Product Specification**: Detailed spec-based matching for accurate results

### Intelligent Market Analysis
- **Real-time Price Discovery**: Fetch current prices from multiple online marketplaces
- **Market Metrics**: Automatic calculation of min, max, and average prices
- **Refurbished Product Detection**: Separate tracking of new vs. refurbished offerings
- **Competitor Intelligence**: Identify which platforms sell the product and at what price

### AI-Driven Recommendations
- **Strategic Pricing Suggestions**: AI-generated recommendations based on market data
- **Action Items**: Specific steps merchants can take to increase competitiveness
- **Revenue Optimization**: Insights to maximize order volume and profitability

---

## 🏗️ Technical Architecture

### Technology Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **AI Framework** | [NeuroLink](https://github.com/juspay/neurolink) | Universal AI platform with MCP server integration |
| **LLM Provider** | Google Gemini / OpenAI / Anthropic | Language model for reasoning and recommendations |
| **Vision AI** | Multi-modal LLM (Gemini Vision) | Image analysis and product identification |
| **Web Search** | MCP (Model Context Protocol) / Web Search API | Real-time web search capabilities |
| **Runtime** | Node.js with TypeScript | Type-safe development environment |
| **Interface** | CLI (Command Line Interface) | Efficient Interaction |


---

## 🔄 High-Level Workflow

```mermaid
graph TD
    A[User Input:<br/>Image/Name/Spec] --> B{Image<br/>Provided?}
    
    B -->|Yes| C[AI Vision Model<br/>Extract Product Details]
    B -->|No| D[Search Query Formation]
    C --> D
    
    D --> E[Web Search via MCP<br/>Multiple E-commerce Sites]
    
    E --> F[Product Matching & Filtering<br/>Separate New vs Refurbished]
    
    F --> G[Market Analysis<br/>Calculate Min/Avg/Max Prices]
    
    G --> H[LLM Analysis<br/>Generate Insights]
    
    H --> I[CLI Output:<br/>Prices, Metrics, Recommendations]
    

```

---

## 📊 Detailed Workflow Stages

### Stage 1: Input Processing
**Input Options:**
- Product image (JPG, PNG)
- Product name (Text)
- Product specifications (Text)

**Process:**
1. If image provided → Send to AI vision model(Gemini-2.5-flash) via NeuroLink
2. Extract product name, brand, model, key features
3. Combine with user-provided text inputs
4. Form a web search query

### Stage 2: Web Search & Data Collection

1. Execute web search using MCP integration in NeuroLink
2. Collect data from multiple e-commerce platforms:
3. Collect and listings products with:
   - Website name
   - Product price
   - Product description
   - Product condition (new/refurbished)

### Stage 3: Product Matching & Filtering
1. Apply filtering to match exact products
2. Eliminate irrelevant or mismatched results
3. Categorize products:
   - **New products** (primary category)
   - **Refurbished products** (separate tracking)

### Stage 4: Market Analysis
**Metrics Calculated:**
- **Lowest Price**: Minimum price found across all platforms
- **Average Price**: Mean price across all listings
- **Highest Price**: Maximum price found
- **Price Distribution**: By platform and product condition

### Stage 5: AI-Powered Recommendations
**Input to LLM:**
- Collected market data
- Merchant's product price
- Merchant's website name


**AI Analysis:**
- Compare merchant pricing vs. market
- Identify competitive advantages/disadvantages
- Generate specific actionable recommendations:
  - Pricing adjustments
  - Marketing strategies
  - Competitive positioning

### Stage 6: CLI Output
**Formatted Output Includes:**
```
=== Competitive Analysis Report ===

Product: [Identified Product Name]
Your Price: ₹X,XXX on [Your Website]

╔═══════════════════════════════════════════════════╗
║              MARKET PRICE ANALYSIS                ║
╚═══════════════════════════════════════════════════╝

Lowest Price:  ₹X,XXX  (Platform Name)
Average Price: ₹X,XXX
Highest Price: ₹X,XXX  (Platform Name)

╔═══════════════════════════════════════════════════╗
║           COMPETITOR PRICING BREAKDOWN            ║
╚═══════════════════════════════════════════════════╝

1. Amazon      - ₹X,XXX (New)
2. Flipkart    - ₹X,XXX (New)
3. eBay        - ₹X,XXX (Refurbished) *


╔═══════════════════════════════════════════════════╗
║         ACTIONABLE RECOMMENDATIONS                ║
╚═══════════════════════════════════════════════════╝

📊 Strategic Insights:
- [AI-generated market positioning analysis]

💡 Recommended Actions:
1. [Specific pricing recommendation]
2. [Marketing strategy suggestion]
3. [Competitive advantage to leverage]

🎯 Expected Impact:
- Increase order volume by X%
- Improve competitive positioning
- [Additional benefits]
```

---

## � Business Value

### For Merchants
- ⏱️ **Save Time**: Automate hours of manual market research
- 💰 **Increase Revenue**: Data-driven pricing optimization
- 📈 **Boost Competitiveness**: Real-time market intelligence
- 🎯 **Make Better Decisions**: AI-powered strategic recommendations

### ROI Metrics
- **Time Savings**: 90% reduction in manual research time
- **Pricing Accuracy**: Real-time data vs. outdated manual checks
- **Decision Speed**: Instant insights vs. hours/days of analysis
- **Scalability**: Analyze unlimited products without additional effort

---