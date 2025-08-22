# LLM Semantic Book Recommender

A production-ready semantic book recommendation system powered by Large Language Models (LLMs) and vector similarity search. This application provides intelligent book recommendations based on semantic content matching and emotional tone analysis.

![Book Recommender](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/UI-Streamlit-red)
![OpenAI](https://img.shields.io/badge/LLM-OpenAI-purple)

## 🚀 Features

- **Semantic Search**: Find books based on descriptive queries rather than just keywords
- **Emotional Tone Filtering**: Filter recommendations by emotional tones (Happy, Sad, Angry, Surprising, Suspenseful)
- **Category Filtering**: Browse books by genre/category
- **Vector Similarity**: Powered by ChromaDB and OpenAI embeddings for high-quality recommendations
- **API Key Management**: Secure OpenAI API key input with validation

## 📁 Repository Structure

```
llm-semantic-book-recommender/
├── data/
│ └── books_with_emotions.csv # Main dataset with book metadata and emotion scores
├── chroma_books_db/ # Chroma vector database directory
├── 01_data_exploration_and_preprocessing.ipynb # Notebook for data exploration and preprocessing
├── 02_embedding_generation.ipynb # Notebook for generating embeddings
├── 03_chromadb_setup.ipynb # Notebook for setting up ChromaDB
├── 04_recommendation_algorithm_development.ipynb # Notebook for developing recommendation algorithm
├── app.py # Main Streamlit application
├── requirements.txt # Python dependencies
└── README.md
```
    


## 📊 Notebooks Explained

### 1. `01_data_exploration_and_preprocessing.ipynb`
**Purpose**: Initial data analysis and preparation of the book dataset.

**Key Contents:**
- Dataset loading and basic statistics
- Missing value analysis and handling
- Data cleaning and normalization
- Emotion score distribution analysis
- Category exploration and simplification
- Thumbnail URL processing and validation
- Data quality checks and validation

**Output**: Cleaned and preprocessed dataset ready for embedding generation.

### 2. `02_embedding_generation.ipynb`
**Purpose**: Generate semantic embeddings for book descriptions using OpenAI.

**Key Contents:**
- OpenAI API integration setup
- Batch processing for embedding generation
- Embedding quality validation
- Storage optimization strategies
- Error handling and retry mechanisms

**Output**: Vector embeddings for all book descriptions stored in ChromaDB.

### 3. `03_chromadb_setup.ipynb`
**Purpose**: Set up and configure the Chroma vector database.

**Key Contents:**
- ChromaDB initialization and configuration
- Vector collection creation
- Metadata schema design
- Index optimization
- Persistence configuration
- Query performance testing

**Output**: Fully configured and populated Chroma vector database.

### 4. `04_recommendation_algorithm_development.ipynb`
**Purpose**: Develop and test the semantic recommendation algorithm.

**Key Contents:**
- Similarity search implementation
- Emotion-based ranking algorithms
- Category filtering logic
- Performance benchmarking
- Recall and precision testing
- Algorithm optimization

**Output**: Production-ready recommendation engine logic.


## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- OpenAI API key
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/JayRathod341997/llm-semantic-book-recommender.git
   cd llm-semantic-book-recommender
   
2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Set up OpenAI API key**
   - Obtain your API key from [OpenAI](https://platform.openai.com/account/api-keys).

5. **Run the application**
   ```bash
   streamlit run app.py
   ```
   
6. **Access the app**
   - Open your browser and navigate to `http://localhost:8501`.
   - Enter your OpenAI API key to start using the book recommender.
   - Explore book recommendations by entering descriptive queries and selecting emotional tones or categories.
   - Enjoy discovering new books tailored to your preferences!
     
