# hello-world-Ai-api
# https://docs.google.com/document/d/1q1eVkB-Pz-8zsCecvHGAKsjetWG4hGph-3r2XHbb_xc/edit?usp=sharing
#code 1
pip install -Uq langchain langchain-google-genai

from langchain_google_genai import ChatGoogleGenerativeAI
from google.colab import userdata

# Retrieving API Key securely
GOOGLE_API_KEY = userdata.get('GOOGLE_API_KEY')

# Initializing the Gemini 2.0 model
llm: ChatGoogleGenerativeAI = ChatGoogleGenerativeAI(
    model="gemini-2.0-flash-exp",
    api_key=GOOGLE_API_KEY,
)

# Simple Hello World Prompt
response = llm.invoke("Hello, world!")
print(response)
#code 2
llm : ChatGoogleGenerativeAI = ChatGoogleGenerativeAI(
    model= "gemini-2.0-flash-exp",
    api_key= GOOGLE_API_KEY,
)

response = llm.invoke("Who is the founder of Pakistan")
print(response)
