# 🧮 Text to Math Problem Solver and Data Search Assistant

This Streamlit application enables users to input natural language math problems and receive step-by-step solutions. It leverages LangChain's tools, including LLMMathChain and WikipediaAPIWrapper, powered by Groq's Gemma2-9b-It model, to provide detailed explanations and relevant information.

---

## 🚀 Features

- **Natural Language Math Problem Solving**: Input math problems in plain English and receive detailed, step-by-step solutions.
- **Wikipedia Integration**: Fetches relevant information from Wikipedia to provide context and explanations.
- **Reasoning Capabilities**: Handles logic-based and reasoning questions using a custom prompt template.
- **Interactive Chat Interface**: Maintains a chat history for seamless user interaction.

---

## 🛠️ Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/ssarthak0/Text-to-Math-Problem-Solver-and-Data-Search-Assistant
   cd ssarthak0/Text-to-Math-Problem-Solver-and-Data-Search-Assistant
   ```

2. **Create and Activate a Virtual Environment**

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set Environment Variables**

   Create a `.env` file in the root directory and add your Groq API key:

   ```env
   GROQ_API_KEY=your_groq_api_key
   ```

---

## 🧪 Usage

1. **Run the Application**

   ```bash
   streamlit run app.py
   ```

2. **Interact with the App**

   - Enter your **Groq API Key** in the sidebar.
   - Input your math problem or question in the provided text area.
   - Click on **"Find my answer"** to receive a detailed solution.

---

## 📄 Prompt Template

The application uses the following prompt to guide the reasoning tool:

```plaintext
You're an agent tasked with solving users' mathematical questions. Logically arrive at the solution and provide a detailed explanation, displaying it point-wise for the question below.
Question: {question}
Answer:
```

---

## 📚 Dependencies

langchain
python-dotenv
ipykernel
langchain-community
pypdf
pymupdf
wikipedia
langchain-text-splitters
langchain-openai
pandas
openai
langchain-groq
numexpr

Ensure all dependencies are installed as per the `requirements.txt` file.

---

## 📝 Notes

- The application initializes three tools:
  - **Wikipedia Tool**: Fetches information from Wikipedia.
  - **Calculator Tool**: Solves mathematical expressions.
  - **Reasoning Tool**: Handles logic-based questions using a custom prompt.
- These tools are combined into an agent using LangChain's `initialize_agent` function.
- The chat interface maintains a history of interactions for context.

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙏 Acknowledgements

- [LangChain](https://www.langchain.com/)
- [Streamlit](https://streamlit.io/)
- [Groq](https://www.groq.com/)
