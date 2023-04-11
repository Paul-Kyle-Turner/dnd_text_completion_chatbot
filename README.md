# TTRPG Rules Lawyer
This is a quick project to create a dnd chat bot for rules using pinecone and openai.

# Setup
1) (Optional) Create a virtual environment and enter it using your virtual engine of choice.

2) Create a .env file with the following :
   * OPENAI_API_KEY=openai_api_key
   * PINECONE_API_KEY=pinecone_api_key
    
3) Install dependencies : 
```
pip install openai pinecone-client python-dotenv chromadb
```

4) Create a logs directory at the root of the chatbot.

5) Add additional informtion for the chatbot to the ./pdfs/Rules folder.  Note that no pdfs of TTRPGs have been added to the github, Wizards of the Coast and Piazo probably wouldn't like that.  You can purchase the PDFs from Wizards or Piazo to increase the amount of context delivered to the LLM.

6) Run pineconce_chatbot.ipynb notebook cells.  Note that if you do not run the chroma cells the chatbot will still function just without any additional context information from the books.

# Prompt change
Note that changing the prompt will change the expected behavior of the llm.  The prompt is currently looking for TTRPG rules and information about TTRPGs.  

Changing the prompt one should write as if they are the chat bot writing a first message to the user.

You can also add in different pdf files to change the context that is delivered to the LLM.
