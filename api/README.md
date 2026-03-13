# FastAPI Azure Integration
```python
from fastapi import FastAPI
from openai import AzureOpenAI

app = FastAPI()
client = AzureOpenAI(api_key="...", azure_endpoint="...", api_version="2024-02-15-preview")

@app.post("/chat")
async def chat(prompt: str):
    response = client.chat.completions.create(model="gpt-4", messages=[{"role": "user", "content": prompt}])
    return {"response": response.choices[0].message.content}
```