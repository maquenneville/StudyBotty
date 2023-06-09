# StudyBotty

StudyBotty is an AI-powered question-answering system that helps users find answers to their questions using a combination of pre-loaded documents, tables, and online resources.

# Features
- Ingests documents from various file formats (PDF, DOCX, CSV, XLSX, TXT, and various image formats).
- Processes and stores document embeddings for quick context retrieval.
- Determines the appropriate agent (DocAgent, TableAgent, MathAgent, LiteratureAgent, or ScienceAgent, more to come) to answer a given question.
- If an answer isn't found within the pre-loaded documents, StudyBotty searches Google for additional context.
- Utilizes OpenAI's ChatGPT for natural language understanding and generation.
- New enhanced accessibility for interacting using only voice commands, with AI-generated voice responses.

# Setup
- Clone the repository to your chosen directory
- Install the required Python packages:

  pip install -r requirements.txt
  
- Fill in the required fields in the config.ini file, including your Pinecone API key, Pinecone Environment, Pinecone Index name, OpenAI API key, Wolfram Alpha API key, Google Custom Search Engine API key, Google Custom Search Engine ID and ElevenLabs API key.

# Usage
- To start StudyBotty, run the main script:

python study_botty.py

- StudyBotty will ask if you'd like enhanced accessibility, you can either enter "yes" or simply press enter to begin the voice prompting.  Accessibility mode is still in it's early stages and does not yet support adding folders of docs.

- StudyBotty will prompt you to add a folder of documents. If you choose to add documents, enter the folder path when prompted. StudyBotty will ingest the documents, process them, and store their embeddings.

- StudyBotty will then ask if you'd like Google Assist for question-answering.  This will unlock the use of a google agent that will attempt to use google search to find an answer if one is not present in the docs.

Once the setup is complete, StudyBotty will be ready to answer your questions. Enter your question at the prompt, or enter a command (for switching between gpt-4/gpt-3.5-turbo, as well as an option for adding more docs mid QA session).  If it's a question, StudyBotty will use the appropriate agent to find the best answer. If an answer cannot be found within the pre-loaded documents, StudyBotty will search Google for additional context before attempting to answer your question again.

To exit StudyBotty, type "exit" at the question prompt.

# Notes

- This program, while stable, is still in alpha.  It's possible it will get lost at certain points, but for most docs it is a powerful QA bot.
