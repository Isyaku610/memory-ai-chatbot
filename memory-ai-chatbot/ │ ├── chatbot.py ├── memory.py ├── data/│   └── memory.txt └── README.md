from memory import save_memory, get_memory

print("🤖 Memory AI Chatbot Activated!")

name = get_memory("username")

if name:
    print(f"Welcome back, {name}!")
else:
    name = input("What is your name? ")
    save_memory("username", name)
    print(f"Nice to meet you, {name}!")

while True:
    user = input(f"{name}: ").lower()

    if user == "exit":
        print("Bot: Goodbye! 👋")
        break

    elif "hello" in user or "hi" in user:
        print("Bot: Hello!")

    elif "python" in user:
        print("Bot: Python is powerful for AI and automation.")

    else:
        print("Bot: I am still learning.")
