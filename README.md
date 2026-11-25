📚 What if you could chat with your own documents? I built a RAG chatbot that does exactly that!

Generic AI doesn’t know what’s inside your files. So I built a Retrieval-Augmented Generation (RAG) system in n8n that answers questions using my own documents.

It has two parts:

1️⃣ Ingestion pipeline (runs automatically)
📂 Drop a new file into Google Drive and the workflow starts.
✂️ The text is split into smaller chunks with a Recursive Character Text Splitter.
🔢 OpenAI embeddings turn each chunk into a vector.
🗄️ The vectors are stored in a Supabase vector database.

2️⃣ Chat agent
💬 I ask a question in the chat.
🧠 The AI Agent (Google Gemini) searches the vector store for the most relevant chunks.
✅ It answers using those chunks, so the response is grounded in my files instead of guesses.

What I learned:

- Why chunking matters for retrieval quality
- How embeddings and vector search find meaning, not just keywords
- Giving an agent a vector store as a tool
- Keeping the knowledge base up to date automatically

Upload a document, and it’s searchable in seconds. 🚀