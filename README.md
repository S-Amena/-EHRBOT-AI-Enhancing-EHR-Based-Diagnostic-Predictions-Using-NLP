# 🤖🩺 AI Healthcare Chatbot

Get quick, AI-powered answers to your health-related questions anytime — whether it's symptoms, wellness tips, or basic medical guidance.Upload medical documents like prescriptions or lab reports, and the chatbot intelligently extracts and explains the key health insights.

![image alt](https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/7bb46327d8710b94f495624a2845cab9424b10f3/Login%20Page%20using%20Supabase%20Authentification.png)

Overview: AI Healthcare Chatbot
The AI Healthcare Chatbot is an intelligent medical assistant that provides personalized, real-time responses to health-related queries using Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG).
It enhances user experience by integrating semantic search on medical documents and interactive chat history, enabling smarter health conversations.

Built with:
Streamlit for frontend
Groq LLM (LLaMA 3.1 8B) for fast medical Q&A
MistralAI embeddings + Hugging Face for semantic search
Qdrant for vector storage
Supabase for authentication and message history
Tavily API for web-enhanced answers

✅ Key Features
🧠 LLM-Powered Medical Q&A
Provides accurate, context-aware health guidance using Groq's LLaMA 3.1 model.

📄 PDF Upload and Context Retrieval
Users can upload medical reports (PDF), which the chatbot understands and uses to give document-specific answers.

🗂️ RAG with Qdrant Vector Search
Smart retrieval of relevant text from documents or previous chats to ground responses.

👤 User Authentication via Supabase
Secure sign-up and login with email validation and password checks.

💬 Personal Chat History
Stores conversations by user and chat session, enabling users to revisit previous interactions.

🔍 Web-Augmented Responses (via Tavily)
The chatbot includes real-time web context when answering general or unclear medical queries.

⚙️ Scalable and Privacy-Focused
Clean separation of chat sessions per user, and secure handling of sensitive health data with authentication and context filtering.

