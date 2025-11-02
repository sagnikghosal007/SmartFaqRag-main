# SmartFaqRag 🚀

A simple and powerful **RAG (Retrieval-Augmented Generation)** pipeline built with **Spring AI** and **Spring Boot** for intelligent FAQ management and question answering.

---

## 🎯 What is this?

**SmartFaqRag** helps you build an intelligent FAQ system that can:

- 🧠 Store and search through your documents  
- 💬 Answer questions based on your content  
- ⚙️ Use any AI model you want (local or paid)

---

## ✨ Features

- 🔍 **Smart Document Search** — Find relevant information quickly  
- 🤖 **Flexible Model Support** — Use any local or paid AI model  
- 🌐 **OpenRouter Integration** — Seamless access to 100+ models through one API  
- 📚 **Easy Document Management** — Simple APIs to add and query documents  
- 🚀 **Spring Boot** — Fast, reliable, and easy to deploy  

---

## 🛠️ Quick Start

### Prerequisites

- **Java 17+**
- **Maven** or **Gradle**

---

### ⚙️ Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/sagnikghosal007/SmartFaqRag.git
   cd SmartFaqRag
2. **Configure Your Model**

Choose **one** of the following configuration options and update your `application.properties` file accordingly.

---

### 🅰️ Option 1: Using OpenRouter (Recommended)

```properties
# application.properties
spring.ai.openai.base-url=https://openrouter.ai/api/v1
spring.ai.openai.api-key=${OPENROUTER_API_KEY}
spring.ai.openai.chat.options.model=meta-llama/llama-3.1-8b-instruct:free
```


### 🅱️ Option 2: Using Local Models (LM Studio)

```properties
# application.properties
spring.ai.openai.base-url=http://localhost:1234/v1
spring.ai.openai.api-key=lm-studio
```
### 🆎 Option 3: Using Other Paid APIs

```properties
# OpenAI
spring.ai.openai.api-key=${OPENAI_API_KEY}

# OR Anthropic
spring.ai.anthropic.api-key=${ANTHROPIC_API_KEY}
```
## ▶️ Run the Application

```bash
./mvnw spring-boot:run
```

## 🤖 Model Options

### 🪄 Option 1: OpenRouter (Easiest Way)

Use [**OpenRouter**](https://openrouter.ai/) to access multiple AI models through a single API key.

✅ **Free models:** Llama, Mistral, etc.  
💎 **Paid models:** GPT-4, Claude, Gemini, and 100+ others  
🔑 **Single API key** for everything  
💰 **Pay-as-you-go** pricing  

Get your API key here: [https://openrouter.ai/](https://openrouter.ai/)

---

### 🖥️ Option 2: Local Models (via LM Studio)

Run models locally on your own machine.

1. Download [**LM Studio**](https://lmstudio.ai/)  
2. Load any compatible model (Llama, Mistral, etc.)  
3. Start the local inference server  
4. Update your app configuration: spring.ai.openai.base-url=http://localhost:1234/v1


---

### 🔗 Option 3: Direct API Access

Use APIs directly from major AI providers:

- **OpenAI:** GPT-3.5, GPT-4  
- **Anthropic:** Claude models  
- **Others:** Any OpenAI-compatible API  

---

## 🔮 Coming Soon

- 📁 **Document Upload API** — Add your own documents dynamically  
- 🧮 **PostgreSQL + pgvector** — Production-grade vector storage for scalability  
- 💬 **Conversation History**  
- 🧾 **Multiple Document Formats**  
- ⚡ **Batch Processing**  

---

## 🧠 Architecture Overview

flowchart TD
    A[🧑 User Query (API)] --> B[🔍 Retriever Layer<br/>(Embeddings + Vector Search)]
    B --> C[🧠 LLM Reasoning Layer<br/>(Spring AI + Chosen Model)]
    C --> D[💬 Final Answer Output]



---

## 🤝 Contributing

Pull requests are welcome! Feel free to:

- 🐞 Report bugs  
- 💡 Suggest features  
- 🧰 Improve documentation  

---

## 🧑‍💻 Author

**Sagnik Ghosal**






