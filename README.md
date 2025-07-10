<header>
  <h1>🤖🩺 AI Healthcare Chatbot</h1>
  <p>Smart assistant for real-time health insights, document-based medical help, and secure AI interaction.</p>
</header>
<section>
  <h2>📌 Overview</h2>
  <p>
    The AI Healthcare Chatbot is a smart medical assistant designed to support users with real-time health advice,
    symptom guidance, and contextual medical report analysis. Powered by cutting-edge LLM technology, document
    understanding, and live web search, it serves as a personal health companion for users seeking trusted support.
  </p>
</section>

<section>
  <h2>✨ Key Features</h2>
  <ul>
    <li>🤖 <strong>AI-Powered Medical Q&A</strong> – Accurate, context-aware answers via Groq LLaMA 3.1 (8B)</li>
    <li>📄 <strong>Document Processing</strong> – Upload medical reports (PDF) for informed responses</li>
    <li>🔍 <strong>Web Search Integration</strong> – Real-time health info using Tavily API</li>
    <li>💬 <strong>Chat History Memory</strong> – Retains conversations using Qdrant semantic search</li>
    <li>🔐 <strong>Secure Authentication</strong> – Login system using Supabase</li>
  </ul>
</section>

<section>
  <h2>🖼️ Screenshots</h2>
  <div class="screenshot">
    <img src="https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/7bb46327d8710b94f495624a2845cab9424b10f3/Login%20Page%20using%20Supabase%20Authentification.png?raw=true" alt="Login Screen" />
    <p>Login Screen - Secure authentication interface</p>
  </div>
  <div class="screenshot">
    <img src="https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/2bc6e541bfd50dc00563991d630c01e890d7be0c/After%20sign%20this%20is%20UI%20Interface%20using%20Streamlit.png?raw=true" alt="Streamlit Interface" />
    <p>Home Interface after login using Streamlit</p>
  </div>
  <div class="screenshot">
    <img src="https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/69b3ec202f7ea47c54ef6e9fd69240ab7b94d2e9/Interaction%20to%20Chatbot%20for%20text%20Based%20response%20using%20LLm.png?raw=true" alt="Chat Interaction" />
    <p>Text-based chat with AI chatbot</p>
  </div>
  <div class="screenshot">
    <img src="https://github.com/S-Amena/Enhancing-EHR-Based-Diagnostic-Predictions-Using-NLP/blob/e8d72c1b97a633ac8f800fd083ef86f2fd6242a6/Response%20by%20the%20given%20Query.png?raw=true" alt="Response Output" />
    <p>Response generated for a medical query</p>
  </div>
</section>

<section>
  <h2>🛠️ Technologies Used</h2>
  <ul>
    <li><strong>Frontend:</strong> Streamlit</li>
    <li><strong>LLM:</strong> Groq (Llama 3.1 8B)</li>
    <li><strong>Embeddings:</strong> Hugging Face (E5-large-v2)</li>
    <li><strong>Vector DB:</strong> Qdrant</li>
    <li><strong>Auth & Storage:</strong> Supabase</li>
    <li><strong>Web Search:</strong> Tavily API</li>
  </ul>
</section>

<section>
  <h2>🚀 Getting Started</h2>
  <p><strong>Prerequisites:</strong></p>
  <ul>
    <li>Python 3.8+</li>
    <li>Streamlit</li>
    <li>API Keys for: Groq, Tavily, Qdrant, Supabase, Hugging Face</li>
  </ul>

  <p><strong>Installation:</strong></p>
  <pre><code>git clone https://github.com/username/ai-healthcare-chatbot.git
cd ai-healthcare-chatbot
pip install -r requirements.txt</code></pre>

  <p><strong>Create a <code>.env</code> file:</strong></p>
  <pre><code>
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
QDRANT_URL=your_qdrant_url
QDRANT_API_KEY=your_qdrant_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
HF_TOKEN=your_huggingface_token
  </code></pre>

  <p><strong>Run the app:</strong></p>
  <pre><code>streamlit run app.py</code></pre>
</section>

<section>
  <h2>💡 Usage</h2>
  <ul>
    <li><strong>Login:</strong> Secure email/password sign in</li>
    <li><strong>Chat:</strong> Ask health questions, upload documents, get responses</li>
    <li><strong>Document Processing:</strong> Upload prescriptions/lab reports for context-aware answers</li>
  </ul>
</section>

<section>
  <h2>🔧 Core Functionality</h2>
  <ul>
    <li><strong>RAG:</strong> Combines web search, uploaded documents, and previous chats</li>
    <li><strong>Authentication:</strong> Validated credentials using Supabase</li>
    <li><strong>Vector Search:</strong> Semantic search on conversations & documents via Qdrant</li>
  </ul>
</section>

<section>
  <h2>📊 Architecture</h2>
  <pre>
┌─────────────────┐     ┌───────────────┐     ┌─────────────────┐
│  User Interface │     │ Authentication │     │  File Upload    │
│    (Streamlit)  │────▶│   (Supabase)   │     │     Handler     │
└─────────────────┘     └───────────────┘     └────────┬────────┘
         │                                             │
         │                                             ▼
         │                                    ┌─────────────────┐
         │                                    │  PDF Processing │
         │                                    │  & Embedding    │
         │                                    └────────┬────────┘
         ▼                                             │
┌─────────────────┐                                    │
│  User Query     │                                    │
│   Processing    │                                    │
└────────┬────────┘                                    │
         │                                             │
         ▼                                             ▼
┌─────────────────┐     ┌───────────────┐     ┌─────────────────┐
│  Web Search     │     │ Vector Search │     │  Document Store  │
│    (Tavily)     │────▶│   (Qdrant)    │◀────│     (Qdrant)     │
└────────┬────────┘     └───────┬───────┘     └─────────────────┘
         │                      │
         ▼                      ▼
┌─────────────────────────────────────────────┐
│           LLM Response Generation           │
│              (Groq/Llama 3.1)               │
└────────────────────┬────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────┐
│              Response Storage               │
│        (Supabase + Qdrant Embedding)        │
└─────────────────────────────────────────────┘
  </pre>
</section>

<section>
  <h2>🔒 Privacy and Security</h2>
  <ul>
    <li>All API keys are stored securely using environment variables.</li>
    <li>User passwords are hashed and stored via Supabase Auth.</li>
    <li>Each chat session is tied to a unique user ID.</li>
  </ul>
</section>

<footer>
  <p>© 2025 AI Healthcare Chatbot | Developed by Syeda Amena</p>
</footer>

</body>







