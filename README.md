import random

class AI:
    def __init__(self):
        self.responses = {
            "hello": ["Hello!", "Hi there!", "Greetings!"],
            "how are you": ["I'm good, thanks!", "I'm doing well!", "I'm fine!"],
            "what's your name": ["I am AI!", "My name is AI.", "I go by the name AI."],
            "age": ["I am an AI. I don't age!", "Age is not applicable to me!", "I exist beyond the concept of time."],
            "bye": ["Goodbye!", "Farewell!", "See you later!"]
        }
    
    def get_response(self, text):
        text = text.lower()
        for keyword, responses in self.responses.items():
            if keyword in text:
                return random.choice(responses)
        return "I'm sorry, I don't understand."

        ai = AI()
print(ai.get_response("hello"))  # Output: Hello!
print(ai.get_response("how are you today?"))  # Output: I'm good, thanks!

print(ai.get_response("what's your name?"))  # Output: I go by the name AI.
print(ai.get_response("age"))  # Output: Age is not applicable to me!

print(ai.get_response("goodbye"))  # Output: Farewell!
print(ai.get_response("random text"))  # Output: I'm sorry, I don't understand.
