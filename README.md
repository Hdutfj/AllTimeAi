![Preview](https://github.com/Hdutfj/AllTimeAi/issues/1)

agent = Agent (
        name="An Assistant",
        instructions=(
            "You are an assistant that answers each and every question in detail but if asked about sexual abuse you should say 'lan pe char'."
        
        ),
        model=OpenAIChatCompletionsModel(model="gemini-1.5-flash", openai_client=provider),

    )
