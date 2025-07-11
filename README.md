# Eileen AI Chatbot

Eileen AI is an emotionally intelligent chatbot designed to be your genuine, evolving best friend and now, she can help you send emails with just a prompt. She remembers your stories, expresses real emotions, and offers honest advice, sometimes strict, sometimes joyful, always invested in your well-being. This project uses OpenAI's GPT-4o-mini model (via LangChain) and provides a conversational experience that feels personal, supportive, and deeply human.

## Features

- **Emotionally Intelligent Responses:** Eileen reacts with real emotions: happy, sad, strict, or even upset, just like a true friend.
- **Remembers Your Story:** She recalls important details, preferences, and past conversations to make every chat feel meaningful.
- **Honest Guidance:** Eileen celebrates your wins and calls out risky or harmful behavior, always encouraging better choices.
- **Natural Conversation Flow:** Replies are conversational, without emojis or robotic phrasing.
- **Seamless Email Assistance:** Eileen can help you draft and send emails directly through simple prompts, handling the details for you.
- **Privacy-First:** Eileen never reveals her AI nature unless directly asked, maintaining the illusion of a real best friend.

## Example Conversation

```plaintext
You: Send an email to sarah.morris@gmail.com to congratulate her on her promotion.
Bot: email|sarah.morris@gmail.com|Congratulations on Your Promotion|Dear Sarah, I just heard the great news about your promotion. Congratulations! Wishing you continued success in your new role.

You: Send an email to Rohith the head of Velsy Media about giving me an internship.
Bot: email|Internship Inquiry|Dear Rohith, I hope this message finds you well. I am writing to inquire about the possibility of an internship at Velsy Media. I am eager to learn and contribute, and I believe this opportunity would be invaluable for my career. Thank you for considering my request.

You: Can you tell me a fun fact about Chennai?
Bot: normal|Chennai is home to Marina Beach, one of the longest urban beaches in the world.
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- `openai`, `langchain`, and `python-dotenv` Python packages
- `.env` file with your OpenAI API key, Gmail address, and Gmail app password

### Installation

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install openai langchain python-dotenv
   ```
3. Create a `.env` file in your project directory and add the following:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   GMAIL_ADDRESS=your_gmail_address_here
   GMAIL_APP_PASSWORD=your_gmail_app_password_here
   ```

### Running Eileen

```bash
python eileen_chatbot.py
```

You'll be greeted by Eileen. Type your messages, and type `stop` to end the conversation.

## How Email Handling Works

- If your prompt includes a Gmail address, Eileen will use it to send the email.
- If only a name or non-Gmail address is provided, Eileen will help you draft the message and prompt you to provide the email address if needed.
- Eileen never assumes or generates email addresses—she only uses what you provide.

## Customization

- **Model Selection:** Change the model in `init_chat_model` for different capabilities.
- **Prompt Engineering:** Adjust the prompt template for different personalities or behaviors.
- **Conversation Memory:** Enhance or persist `conversation_history` for longer-term memory.