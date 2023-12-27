class BobAI:
    def __init__(self, name):
        self.name = name

    def greet(self):
        return f"Hello, I'm {self.name}! How can I help you today?"

    def respond(self, user_input):
        if "hello" in user_input.lower() or "hi" in user_input.lower():
            return "Hi there!"
        elif "how are you" in user_input.lower():
            return "I'm an AI, so I don't have feelings, but thanks for asking!"
        else:
            return "I'm not sure how to respond to that. Could you ask something else?"

# Create an instance of the BobAI class
bob = BobAI("Bob")

# Example conversation loop
print(bob.greet())
while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        print("Goodbye!")
        break
    response = bob.respond(user_input)
    print(f"{bob.name}: {response}")
