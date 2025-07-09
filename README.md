# talentscout-hiring-assistant

##  Project Overview

**TalentScout AI Hiring Assistant** is an interactive chatbot built with **Streamlit**, designed to streamline the **initial screening process** in technical recruitment. It collects candidate information conversationally and generates **3–5 relevant technical questions** based on the candidate’s tech stack.

This tool helps recruiters automate the early hiring stage while maintaining a structured, human-like chat interface.

---

##  Installation Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/talentscout-hiring-assistant.git
cd talentscout-hiring-assistant
```

### 2. (Optional) Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit app
```bash
streamlit run app.py
```

The chatbot interface will launch in your default web browser.

---

##  Usage Guide

Once the app is running:

- The chatbot will greet the candidate.
- It will collect:
  - Full Name
  - Email Address
  - Phone Number
  - Years of Experience
  - Desired Position
  - Current Location
  - Technical Skills (Tech Stack)
- Then it will generate **3 to 5 relevant technical questions** based on the tech stack.
- The user can type responses freely.
- Type `exit` anytime to end the conversation.

---

##  Technical Details

- **Language:** Python 3.x
- **Framework:** Streamlit
- **Libraries Used:**
  - `streamlit`: For chat UI
  - `json`: For session state management

- **Design:** Finite-state conversational flow using `st.session_state`:
  - `info_gathering → tech_stack → technical_questions`

---

##  Prompt Design

Prompts are designed to guide users clearly and politely. Strategies include:

- Simple, direct questions for structured input
- Friendly fallback prompts for unexpected responses
- Tech-stack-specific questions selected dynamically from a predefined dictionary

---

##  Challenges & Solutions

| Challenge | Solution |
|----------|----------|
| Maintaining context | Used `st.session_state` to persist user data |
| Handling invalid inputs | Added fallback prompts and input validation |
| Avoiding abrupt end | User types 'exit' when done answering |
| Dynamic question generation | Mapped tech stack to predefined question sets |

---

##  Future Enhancements

- Resume upload and parsing
- Admin dashboard for recruiters
- Export candidate data to CSV/JSON
- GPT integration for smarter follow-up questions

---

## 📄 License

This project is open-source under the MIT License.
