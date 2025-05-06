import chainlit as cl
import os
from agents import Agent, AsyncOpenAI, Runner, OpenAIChatCompletionsModel, set_tracing_disabled
from dotenv import load_dotenv

load_dotenv()
GEMINI_API_KEY=os.getenv("GEMINI_API_KEY")
set_tracing_disabled(True)

provider= AsyncOpenAI(
    api_key=GEMINI_API_KEY,
    base_url="https://generativelanguage.googleapis.com/v1beta/",  # ⚠️ Verify this URL
)

@cl.on_chat_start
async def on_chat_start():
    cl.user_session.set("history", [])
    await cl.Message(content="YOUR ASSISTANT BOT, How can i help you?").send()

@cl.on_message
async def handle_message(message: cl.Message):
    history = cl.user_session.get("history")
    history.append({"role" : "user", "content" : message.content})
