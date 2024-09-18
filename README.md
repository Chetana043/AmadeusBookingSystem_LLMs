# AmadeusBookingSystem_LLMs

This project presents an advanced travel search application that leverages natural language processing (NLP) and the Amadeus travel API. By enabling users to search for flights and hotels using conversational queries, the application simplifies travel planning, making it more intuitive and accessible. It bridges the gap between human language and complex travel data systems, providing a user-friendly interface for finding and booking travel arrangements.

## Overview

- **Streamlit**: Provides a responsive web-based user interface.
- **Langchain**: Powers natural language processing, enabling sophisticated understanding of user queries.
- **Amadeus API**: Retrieves comprehensive travel data, including flight offers and hotel availability.

The application processes user queries in natural language, extracting key details such as destinations, dates, and preferences. It then converts this information into structured parameters for API calls, fetches relevant data, and returns the results in a human-readable format.

## Objectives

The primary goals of this project are:

- To simplify the travel search process by allowing users to input queries in natural language, removing the need for complex form-filling or industry-specific jargon.
- To demonstrate the integration of advanced language models with traditional API-based services, showcasing how NLP can enhance user experiences in various industries.
- To improve the accuracy and relevance of search results by converting conversational language into precise API queries, enhancing the overall user experience in travel planning.

## Tech Stack

- **Streamlit**: For creating a dynamic, web-based UI.
- **Langchain**: For advanced natural language understanding and prompt structuring.
- **Amadeus API**: For accessing travel-related data.
- **Llama 3 Model (via Ollama)**: For interpreting and generating natural language queries.

## Implementation

### Language Model: Llama 3 via Ollama

This project utilizes the **Llama 3** large language model through **Ollama**, a lightweight container for running LLMs efficiently. Llama 3 excels at text generation, summarization, and question-answering, making it ideal for handling user queries and converting them into structured API requests.

```python
model = Ollama(model="llama3")
```

### Amadeus API Integration

Two primary Amadeus API endpoints are integrated:

1. **Flight Offers Search API**  
   - Allows users to search for flight offers based on origin, destination, dates, and number of passengers.
   - Returns detailed flight information such as pricing, airlines, and itineraries.

2. **Hotel Search API**  
   - Enables users to find hotels in a specific city, providing information about available accommodations.

Both APIs are authenticated using Amadeus credentials.

### ChatPromptTemplate for NLP

The project uses **ChatPromptTemplate** from Langchain to structure prompts for the language model. This template ensures that the model processes user queries systematically and accurately. Specific prompts are used to extract key information for query interpretation and result formatting.

### Usage
Once the app is running, you can input travel-related queries in natural language. For example:

"Find me flights from New York to London on November 10th."
"Show available hotels in Paris for two people from December 5th to December 10th."
The application will interpret your query, fetch the appropriate data from the Amadeus API, and display the results in a clear, user-friendly format.

