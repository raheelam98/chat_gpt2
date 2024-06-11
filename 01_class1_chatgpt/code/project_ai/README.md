# Open Ai

```python
from openai import OpenAI
from dotenv import load_dotenv, find_dotenv
import os

_ : bool = load_dotenv(find_dotenv()) # read local .env file

client : OpenAI = OpenAI()   
```

*** Note ***

_ “under score” before variable (python ) :- use variable only one-time 

find_dotenv() :-  (find the path of .env) python-dotenv library that searches for a .env file in the current working directory or its parents.

load_dotenv() :- loads environment variables from a .env file

pwd : tell the path of current 

```python
def chat_completion(prompt: str) -> str:

    response: ChatCompletion = client.chat.completions.create(
        messages=[
            {
                "role": "user",
                "content": prompt,
            }
        ],
        model="gpt-3.5-turbo-1106",
    )
    return response.choices[0].message.content

chat_completion("what is 1+1?")  
```

*** Explination ***

def chat_completion(prompt : str )-> str:
Input :- str (promp) , response :- str  {-> str:}

response: ChatCompletion = client.chat.completions.create()
client :- local-machine / docker-container etc {send request to generative-ai-server }

messages :- first parameter of function (here message is list)

model="ai_modle",

return response.choices[0].message.content
return dictionary.first-index.key(message).content
dictionary has choices, first index of choice.

*** Prompt Engineering ****
1) Role 2) Task 3) Context 4) Response
Role: Define the user's goal or objective.
Task: Specify the action or task the user wants to accomplish.
Context: Provide the relevant background information or situation.
Response: The desired output or answer from the AI model.

*** Gherkin: behavior-driven development (BDD), {keywords :: "Given", "When", "Then"}  ****
Gherkin :- human-readable language used for writing test cases and scenarios in behavior-driven development (BDD).
uses a syntax similar to natural language, with keywords like "Given", "When", and "Then" to describe expected behavior.