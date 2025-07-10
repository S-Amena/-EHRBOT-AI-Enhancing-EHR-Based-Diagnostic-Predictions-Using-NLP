# 🤖🩺 AI Healthcare Chatbot

Get quick, AI-powered answers to your health-related questions anytime — whether it's symptoms, wellness tips, or basic medical guidance.Upload medical documents like prescriptions or lab reports, and the chatbot intelligently extracts and explains the key health insights.

![image alt](https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/7bb46327d8710b94f495624a2845cab9424b10f3/Login%20Page%20using%20Supabase%20Authentification.png)

📌 Overview
The AI Healthcare Chatbot is a smart medical assistant designed to support users with real-time health advice, symptom guidance, and contextual medical report analysis. Powered by cutting-edge LLM technology, document understanding, and live web search, it serves as a personal health companion for users seeking trusted support.

✨ Key Features
🤖 AI-Powered Medical Q&A
Provides accurate, context-aware answers using Groq's LLaMA 3.1 (8B) model.

📄 Document Processing
Users can upload medical reports (PDF), which the chatbot understands and uses to provide informed, document-specific answers.

🔍 Web Search Integration
Pulls up-to-date health content using the Tavily API to support and enrich chatbot answers.

💬 Chat History Memory
Stores and retrieves conversations using Qdrant’s semantic search for contextual continuity.

🔐 Secure Authentication
Uses Supabase for email/password login and user session management.

🖼️ Screenshots


🛠️ Technologies Used
Layer	Technology
Frontend	Streamlit
LLM	Groq (LLaMA 3.1 8B)
Embeddings	Hugging Face (E5-large-v2)
Vector DB	Qdrant
Authentication & Storage	Supabase
Web Search	Tavily API

🔐 Environment Setup
Create a .env file in the root directory:

GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
QDRANT_URL=your_qdrant_url
QDRANT_API_KEY=your_qdrant_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
HF_TOKEN=your_huggingface_token

▶️ Run the App
streamlit run app.py

💡 Usage
👤 User Login – Sign up or log in securely.
💬 Chat – Ask health-related questions or upload reports.
📄 Document Upload – Get personalized answers using your uploaded PDFs.
🔄 Multi-Chat History – Navigate through multiple chat sessions and retrieve past interactions.

🔧 Core Functionality
🔍 Retrieval-Augmented Generation (RAG)
The chatbot uses:
Context from uploaded documents
Web search results
Chat memory (from Qdrant)
… to generate high-quality, relevant responses.

🛡️ Authentication
Password policy enforcement
Session state managed securely with Supabase

📚 Vector Search
Embeddings stored in Qdrant
Semantic search for contextual accuracy

📊 Architecture

![image](https://github.com/user-attachments/assets/7935c363-2883-48b5-8d38-3954b7d65af1)
┘

🔒 Privacy & Security
API keys managed via .env (never exposed to frontend)
Supabase ensures secure, hashed password storage
User chat history is isolated per account



