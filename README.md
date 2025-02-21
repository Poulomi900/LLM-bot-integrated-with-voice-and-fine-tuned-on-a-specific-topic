

# Product Management Interview Bot

An interactive command-line bot designed to simulate a product management interview. This tool leverages GPT-4 for generating interview questions, evaluating user responses based on a detailed rubric, and providing guidance on how to answer questions effectively. The bot integrates speech recognition and text-to-speech functionalities to offer a hands-free, conversational experience.

## Features

- **Interview Question Generation:**  
  Uses a ChromaDB collection combined with GPT-4 to generate product management interview questions based on real content.

- **Voice Interaction:**  
  Integrates speech recognition (via `speech_recognition`) and text-to-speech (via `pyttsx3`) to allow users to interact with the bot verbally.

- **Answer Evaluation:**  
  Evaluates candidate responses using a detailed rubric that scores problem breakdown, creative thinking, and technical insight.

- **Interactive Follow-up:**  
  Supports commands such as rephrasing, elaboration, and follow-up questions to refine and expand interview questions and answers.

## Prerequisites

- **Python:** Version 3.7 or later  
- **API Access:** An OpenAI API key with access to GPT-4  
- **Hardware:**  
  - Microphone (for speech input)  
  - Speakers (for audio output)

## Dependencies

Install the required Python libraries with:

```bash
pip install chromadb openai SpeechRecognition pyttsx3

## Setup

Clone the Repository:
-bash
-Copy
-git clone https://github.com/your-username/product-management-interview-bot.git
-cd product-management-interview-bot

Configure API Keys:

-Open the Python script(s) and replace the placeholder API keys ('your-openai-api-key' or 'use-your-openai-api') with your actual OpenAI API key.

ChromaDB Collection:
-Ensure that you have an existing ChromaDB collection named "product_management_questions" with relevant documents. Adjust the collection name or document handling as needed.




## Usage

Run the bot by executing the main script:

-bash
-Copy
-python your_script_name.py

Upon running the script, you will be presented with two options:

## Let the Bot Ask an Interview Question:

- The bot retrieves random documents from the ChromaDB collection.
- It generates a product management interview question using GPT-4.
- You can respond using your voice, ask for rephrasing, request elaboration, or pose follow-up questions.
- Once your answer is complete, the bot evaluates your response based on a predefined rubric.

## Provide Your Own Interview Question:

- You can supply your own product management interview question.
- The bot will then generate detailed guidelines on how to approach and answer the question with Good, Better, and Best strategies.


## Code Structure

1) Speech Functions:
- speak_text(text): Converts text to speech using pyttsx3.
- listen_to_user(): Captures and transcribes user speech via speech_recognition.

2) Document Handling:
- get_random_documents(collection, num_documents): Retrieves a random set of documents from the ChromaDB collection.

3) Question Generation & Manipulation:
- generate_product_management_question(documents): Uses GPT-4 to generate an interview question based on provided documents.
- elaborate_or_rephrase_question(question, action): Requests GPT-4 to either rephrase or elaborate on an interview question based on a given command.

4)Answer Evaluation:
-evaluate_answer_with_gpt4(question, user_answer): Uses GPT-4 to evaluate the candidate’s response against a detailed rubric.
-generate_guidelines_with_gpt4(user_question): Provides guidelines for answering a given interview question using a tiered approach.

5)Command Detection:
- detect_command(user_input): Detects keywords (e.g., "rephrase", "elaborate") from the user's voice input to determine the intended action.

6)Main Function:
-main(): Combines all functions to provide an interactive interview simulation.

7)Future Enhancements
-Improved Error Handling:
Enhance the robustness of voice input/output and API error management.

8)Extended Interaction:
-Incorporate more advanced multi-turn dialogue capabilities for a richer interview simulation.

9)User Interface:
Develop a graphical user interface (GUI) to complement the command-line version.


## License
This project is licensed under the MIT License.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request or open an issue for suggestions.

## Contact
For any questions or support, please contact your-email@example.com.


