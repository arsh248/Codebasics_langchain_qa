# Codebasics Q&A 📝

<img width="1512" alt="Screenshot 2024-06-24 at 10 57 33 PM" src="https://github.com/arsh248/Codebasics_langchain_qa/assets/62460837/6df07755-3595-4e30-a173-23dfce714ce6">


This is a Streamlit application that provides a Q&A interface for the Codebasics FAQ dataset using a language model from Langchain. The application loads a pre-trained FAISS vector store and uses it to retrieve relevant answers based on user questions.

## Project Structure


- `main.py`: The main script to run the Streamlit application.
- `langchain_helper.py`: Contains helper functions to create and query the vector store.
- `codebasics_faqs.csv`: A CSV file containing FAQ questions and answers.
- `.env`: A file containing environment variables, specifically the Google API key.
- `README.md`: This file.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/arsh248/Codebasics_langchain_qa
    cd codebasics-qa
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up environment variables**:
    Create a `.env` file in the project root directory and add your Google API key:
    ```plaintext
    GOOGLE_API_KEY=your_google_api_key_here
    ```

4. **Prepare the vector database**:
    Ensure that the `codebasics_faqs.csv` file is in the project root directory. Run the following command to create the vector database:
    ```bash
    python langchain_helper.py
    ```

## Usage

1. **Run the Streamlit application**:
    ```bash
    streamlit run main.py
    ```

2. **Interact with the application**:
    Open your browser and go to `http://localhost:8501`. You can enter your questions in the input field, and the application will return answers based on the FAQs.

## Langchain Framework

[Langchain](https://github.com/hwchase17/langchain) is a framework for developing applications powered by language models. It provides a suite of tools for working with large language models, including utilities for prompt engineering, chaining together models, and more.

## Google Palm Model

The application uses the Google Palm model, a language model from Google that excels in natural language understanding and generation. It's accessed via the Langchain framework with an API key provided by Google. You can find more details about Google Palm [here](https://ai.googleblog.com/2023/04/announcing-palm-2-next-generation-large.html).

## FAISS Databases

[FAISS](https://github.com/facebookresearch/faiss) (Facebook AI Similarity Search) is a library for efficient similarity search and clustering of dense vectors. It is used in this project to create a vector database from the FAQ data, which allows for efficient retrieval of relevant documents based on user queries.

## Contributing

Contributions are welcome! If you have suggestions or find issues, please open an issue or submit a pull request.

