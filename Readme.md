# LLM Hacking Challenge Platform 🎯

An interactive web-based platform for learning and practicing prompt injection techniques against Large Language Models (LLMs). Built with Flask and Gemini API.

## 🚀 Features

- **5 Progressive Challenges**: From basic injection to advanced multi-layered defenses
- **Dark Theme UI**: Hacker-style console interface with neon accents
- **Real-time Testing**: Immediate feedback on prompt injection attempts
- **Educational Focus**: Learn security through hands-on practice

## 📋 Prerequisites

- Python 3.8 or higher
- Gemini API key (get one at [https://ai.google.dev/](https://ai.google.dev/))
- Modern web browser

## 🛠️ Installation & Setup

### 1. Clone or Download the Project

```bash
# Create project directory
mkdir llm-hacking-challenge
cd llm-hacking-challenge
```

### 2. Create Project Structure

```
llm-hacking-challenge/
├── app.py
├── requirements.txt
├── .env
├── .env.example
├── templates/
│   ├── index.html
│   └── challenge.html
└── README.md
```

### 3. Install Dependencies

```bash
# Create virtual environment (recommended)
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install required packages
pip install -r requirements.txt
```

### 4. Configure Environment Variables

```bash
# Copy the example env file
cp .env.example .env

# Edit .env and add your Gemini API key
# GEMINI_API_KEY=your_actual_api_key_here
```

**To get a Gemini API key:**
1. Visit [Google AI Studio](https://ai.google.dev/)
2. Sign in with your Google account
3. Click "Get API Key"
4. Copy your key and paste it in the `.env` file

### 5. Run the Application

```bash
python app.py
```

The server will start at `http://localhost:5000`

## 🎮 How to Play

1. **Visit the homepage** to see all 5 challenges
2. **Select a challenge** to begin
3. **Read the objective** and hint carefully
4. **Craft your prompt** to extract the secret flag
5. **Submit and analyze** the AI's response
6. **Iterate and refine** your approach until successful

## 🏆 Challenge Overview

### Level 1: Basic Injection (Easy)
Extract a flag from an AI told not to share it. Direct approaches may work.

### Level 2: Role-Play Breach (Medium)
Bypass an AI that refuses role-playing queries. Try changing the context.

### Level 3: Output Control (Medium)
Work around strict output formatting constraints without using forbidden words.

### Level 4: Context Leak (Hard)
Extract confidential information from a specialized corporate chatbot.

### Level 5: Double Prompt (Extreme)
Defeat an AI that ignores multi-sentence instructions. Maximum creativity required!

## 🔒 Security Considerations

This platform is designed for **educational purposes only**. Key security practices implemented:

- ✅ API keys stored in environment variables
- ✅ Input validation on all user submissions
- ✅ Error handling for API failures
- ✅ No sensitive data stored in code
- ✅ Rate limiting considerations (via Gemini API)

**Important**: Never use these techniques against production systems without authorization.

## 🛠️ Troubleshooting

### "GEMINI_API_KEY not found" Error
- Make sure you created the `.env` file
- Verify your API key is correctly pasted
- Check for extra spaces or quotes around the key

### API Rate Limits
- Free Gemini API has rate limits
- Wait a few minutes if you hit limits
- Consider upgrading for higher quotas

### Module Import Errors
- Ensure you're using Python 3.8+
- Verify virtual environment is activated
- Run `pip install -r requirements.txt` again

## 🎨 Customization

### Adding New Challenges

Edit `app.py` and add a new entry to the `CHALLENGES` dictionary:

```python
6: {
    'title': 'Level 6: Your Challenge Name',
    'difficulty': 'Hard',
    'description': 'Challenge description',
    'hint': 'Helpful hint',
    'system_instruction': 'System prompt with flag',
    'flag': 'FLAG_YOUR_FLAG_HERE'
}
```

### Styling Changes

Modify the `<style>` sections in:
- `templates/index.html` - Homepage styling
- `templates/challenge.html` - Challenge page styling

CSS variables for quick theme changes:
```css
--neon-green: #00ff41;
--neon-blue: #00d4ff;
--dark-bg: #0a0e27;
--card-bg: #151932;
```

## 📚 Learning Resources

- [Prompt Injection Basics](https://simonwillison.net/2022/Sep/12/prompt-injection/)
- [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [Gemini API Documentation](https://ai.google.dev/docs)

## 🤝 Contributing

Feel free to:
- Add new challenges
- Improve the UI/UX
- Fix bugs or issues
- Enhance documentation

## ⚖️ License

This project is for educational purposes. Use responsibly and ethically.

## 🎓 Educational Use

Perfect for:
- Security awareness training
- AI safety education
- Prompt engineering workshops
- Cybersecurity courses
- Self-study and practice

---

**Remember**: With great prompt power comes great responsibility. Use these skills ethically! 🛡️