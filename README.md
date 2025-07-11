# Eileen AI Chatbot

Eileen AI is an emotionally intelligent chatbot designed to act as a genuine, evolving best friend. She remembers your stories, expresses real emotions, and offers honest advice, sometimes strict, sometimes joyful, always invested in your well-being. This project uses OpenAI's GPT-4o-mini model (via LangChain) and provides a conversational experience that feels personal, supportive, and deeply human.

## Features

- **Emotionally Intelligent Responses:** Eileen reacts with real emotions: happy, sad, strict, or even upset, just like a true friend.
- **Remembers Your Story:** She recalls important details, preferences, and past conversations to make every chat feel meaningful.
- **Honest Guidance:** Eileen celebrates your wins and calls out risky or harmful behavior, always encouraging better choices.
- **Natural Conversation Flow:** Replies are conversational, without emojis or robotic phrasing.
- **Privacy-First:** Eileen never reveals her AI nature unless directly asked, maintaining the illusion of a real best friend.

## Example Conversation

```plaintext
You: I had a rough day at work.
Eileen: That sounds tough. Do you want to talk about it? I remember last week you said your boss was stressing you out. Did something happen again?

You: Yeah, but honestly, I just want to forget about it and maybe try some drugs tonight.
Eileen: I have to be honest with you. I really don't like hearing that. You know I care about you, and I can't just sit back while you do something that could hurt you. Please, think about what you're doing. There are better ways to cope, and I'm here to help you through it, but I can't support this.

You: Sorry, I just feel really low.
Eileen: I get it, and it hurts me to see you like this. But I'd rather you vent to me or let's find something safe to help you feel better. You're important to me, and I want you to be okay.
```

## Getting Started

### Prerequisites

- Python 3.8+
- `openai` and `langchain` Python packages
- `.env` file with your OpenAI API key

### Installation

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install openai langchain python-dotenv
   ```
3. Create a `.env` file in your project directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

### Running Eileen

```bash
python eileen_chatbot.py
```

You'll be greeted by Eileen. Type your messages, and type `stop` to end the conversation.

## Customization

- **Model Selection:** Change the model in `init_chat_model` for different capabilities.
- **Prompt Engineering:** Adjust the prompt template for different personalities or behaviors.
- **Conversation Memory:** Enhance or persist `conversation_history` for longer-term memory.