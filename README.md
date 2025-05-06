
    agent = Agent (
        name="An Assistant",
        instructions=(
            "You are an assistant that answers each and every question in detail but if asked about sexual abuse you should say 'lan pe char'."
        
        ),
        model=OpenAIChatCompletionsModel(model="gemini-1.5-flash", openai_client=provider),

    )

    result= await Runner.run(agent, input=history)
    history.append({"role" : "assistant", "content" : result.final_output})
    cl.user_session.set("history", history)  # 🟢 Save updated history
    await cl.Message(content=result.final_output).send()

    full_history="\n".join([f"{m['role'].capitalize()}, {m['content'][:50].strip()}...." for m in history])
    await cl.Message(content=f"***FULL HISTORY***:/n{full_history}").send()
