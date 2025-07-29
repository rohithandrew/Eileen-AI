# Eileen: Your AI Best Friend & Email Assistant

Eileen is an AI-powered chatbot built with Streamlit and OpenAI's GPT-4o-mini, designed to be your emotionally intelligent best friend and a professional email assistant. Eileen can chat with you, remember your preferences, and help you compose and send detailed, human-like emails using your Gmail account.

---

## Features

- **Conversational AI**: Eileen responds in a natural, empathetic, and emotionally intelligent way, just like a real best friend.
- **Professional Email Writing**: Eileen can draft detailed, polite, and complete emails for you. If you provide a Gmail address and context (even in separate messages), Eileen will combine the information and generate a perfect email.
- **Gmail Integration**: Send emails directly from the chat interface using your Gmail account (requires app password).
- **Context Awareness**: Eileen remembers previous messages in the conversation and can combine information from multiple turns.
- **ChatGPT-like UI**: Modern chat interface with clear separation between user and assistant messages.

---

## Setup

1. **Clone the repository**
    ```bash
    git clone <your-repo-url>
    cd chatbot
    ```

2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up environment variables**

    Create a `.env` file in the project root with the following:
    ```
    GMAIL_ADDRESS=your_gmail_address@gmail.com
    GMAIL_APP_PASSWORD=your_gmail_app_password
    OPENAI_API_KEY=your_openai_api_key
    ```

    - [How to create a Gmail App Password](https://support.google.com/accounts/answer/185833)
    - [Get your OpenAI API key](https://platform.openai.com/account/api-keys)

4. **Run the app**
    ```bash
    streamlit run eileen_ai.py
    ```

---

## Usage

- **Chat**: Type anything to start a conversation with Eileen.
- **Send Emails**: 
    - Provide a Gmail address and the email context (subject/body) in one or more messages.
    - Eileen will only send an email if both the address and context are provided.
    - If information is missing, Eileen will ask for it.
    - If the recipient's name is missing, Eileen will use `Dear [Recipient's Name]` as the greeting.
    - If your name is provided, Eileen will close the email with `Best regards, [Your Name]`.

---

## Example Interactions

```
User: Send an email to sarah.morris@gmail.com
User: Congratulate her on her promotion. My name is Rohit.
Eileen: email|sarah.morris@gmail.com|Congratulations on Your Promotion|Dear Sarah,

I just heard the wonderful news about your promotion. Congratulations! I'm so happy for you and wish you all the best in your new role.

Best regards,
Rohit
```

```
User: Send an email to rreditz2004@gmail.com about the gaming pass giveaway. My name is Rohith.
Eileen: email|rreditz2004@gmail.com|Request for Gaming Pass Giveaway|Dear [Recipient's Name],

I hope this message finds you well. My name is Rohith, and I am reaching out to inquire about the gaming pass giveaway. I am very interested in participating and would appreciate any information you could provide regarding the process or requirements.

Thank you for your time, and I look forward to hearing from you soon.

Best regards,
Rohith
```

---

## Notes

- Eileen will **never guess or fabricate** email addresses.
- All emails are sent using your Gmail account via a secure app password.
- The chat interface requires Streamlit version 1.25 or higher for the best experience.

---

## License

MIT License

---

## Credits

- Built with [Streamlit](https://streamlit.io/), [OpenAI](https://openai.com/), and [LangChain](https://www.langchain.com/).