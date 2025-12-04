**About Me - CS 516 Information Retrieval System**

**Student Information**
Name: Arshiya Khan
Student ID: Mscs24009
University: Information Technology University (ITU)
Program:  MS Computer Science
Course: CS 516 - Information Retrieval and Text Mining
Semester: Fall 2025
Instructor: Dr. Ahmad Mustafa

**Project Overview**
This repository contains the implementation of a complete Information Retrieval System as part of CS 516 Homework Assignment 3. The system implements both BM25 and TF-IDF retrieval algorithms and operates entirely on local hardware without cloud dependencies.

Key Features:
- Dual Algorithm Implementation: BM25 (probabilistic) and TF-IDF (vector space)
- Local Execution: No external APIs or cloud databases required
- Automatic Encoding Detection: Handles various file encodings
- Persistent Indexing: Save and load indexes for efficient reuse
- Comprehensive Evaluation: Precision, Recall, MAP metrics
- Modular Architecture: Clean separation of components

**Technical Stack**
Core Technologies:
- Programming Language: Python 3.8+
- Libraries: scikit-learn, rank-bm25, NLTK, pandas, joblib

Development Environment:
- Platform: Google Colab / Local machine
- Version Control: Git & GitHub
- Documentation: LaTeX for report, Markdown for documentation

**System Architecture**
Input Layer → Preprocessing → Indexing → Storage → Retrieval → Output
CSV File   Text Cleaning   BM25/TF-IDF Local File Query Proc Ranked Results
Encoding    Tokenization    Indexing    Storage  Relevance   Evaluation
Detection  Stopword Removal                        Scoring     Metrics

**Quick Setup Instructions**

**1. Open Google Colab**
Go to https://colab.research.google.com
Click "New Notebook"

**2. Install Packages**
```python
!pip install scikit-learn rank-bm25 nltk pandas joblib tqdm chardet
```

**3. Upload File**
```python
from google.colab import files
files.upload()
```
Select your Articles.csv file

**4. Run Complete Code**
Copy the IR system code into one cell and run it

**5. Use System**
Type commands in interactive mode:
- `/q your query` - Search
- `/a bm25` or `/a tfidf` - Choose algorithm
- `/t 10` - Set number of results
- `/stats` - Show statistics
- `/exit` - Quit

**Sample Queries to Test:**
- `technology`
- `business`
- `education`
- `health`
- `sports`

**Expected Results:**
- Index builds in 2-5 seconds
- Queries return in under 10ms
- Shows document ID, score, and preview

**Quick Commands:**
```python
# BM25 search
results = ir_system.search_bm25("query", 5)

# TF-IDF search
results = ir_system.search_tfidf("query", 5)

# Save index
ir_system.save_index("index.pkl")

# Load index
ir_system.load_index("index.pkl")
```

**Troubleshooting:**
- Missing packages? Re-run install command
- File errors? Ensure Articles.csv is uploaded
- NLTK errors? Code auto-downloads required data
- Memory issues? Use smaller dataset

**Done!** System ready for searching.
**Research Integration:**
Applied theoretical concepts from:
- Robertson & Zaragoza (BM25 framework)
- Salton & McGill (Vector Space Model)
- Manning et al. (Modern Information Retrieval)

**Key Challenges & Solutions**
Challenge 1: Encoding Issues
Problem: CSV file had Windows-1252 encoding causing Unicode errors
Solution: Implemented automatic encoding detection using chardet library

Challenge 2: NLTK Resource Management
Problem: Missing punkt_tab tokenizer resources
Solution: Added automatic download with fallback mechanisms

Challenge 3: Memory Efficiency
Problem: Large document collection memory usage
Solution: Implemented sparse matrix representation and efficient data structures

Challenge 4: Algorithm Comparison
Problem: Different scoring ranges between BM25 and TF-IDF
Solution: Implemented score normalization for fair comparison

**Ethical Considerations**
Academic Integrity:
- All code implemented independently with minimal AI assistance
- AI tools used only for error debugging and LaTeX template generation
- Complete disclosure of AI usage provided in technical report
- Proper citations for all referenced materials

Data Privacy:
- System operates entirely locally with no data transmission
- No external APIs or cloud services used
- Complete control over data processing and storage

**Future Enhancements**
Planned Improvements:
1. Query Expansion: Implement pseudo-relevance feedback
2. Semantic Search: Integrate word embeddings for better understanding
3. Distributed Indexing: Scale to larger document collections
4. Web Interface: Create user-friendly search interface
5. Multi-language Support: Extend to multiple languages

Research Extensions:
1. Learning to Rank: Implement machine learning for ranking
2. Neural IR Models: Explore transformer-based retrieval
3. Cross-lingual IR: Enable search across different languages
4. Real-time Indexing: Support for streaming document updates

**Assignment Requirements Met**
Local Execution: Completed - Google Colab/Local Python
TF-IDF Algorithm: Completed - scikit-learn implementation
BM25 Algorithm: Completed - rank-bm25 library
Reproducibility: Completed - Complete documentation
No Cloud DBs: Completed - Local file storage
Evaluation: Completed - Precision/Recall/MAP
Well-structured Code: Completed - Modular OOP design
Technical Report: Completed - LaTeX documentation

**Acknowledgments**
Academic Support:
- Dr. Ahmad Mustafa: Course instructor for guidance and feedback
- ITU Faculty: For providing excellent learning resources
- Classmates: For productive discussions and peer learning

Technical Resources:
- Scikit-learn Documentation: For TF-IDF implementation guidance
- NLTK Community: For natural language processing tools
- Open Source Community: For valuable libraries and tools

References:
1. Robertson, S., & Zaragoza, H. (2009). The Probabilistic Relevance Framework
2. Salton, G., & McGill, M. J. (1986). Introduction to Modern Information Retrieval
3. Manning, C. D., Raghavan, P., & Schütze, H. (2008). Introduction to Information Retrieval

**Contact Information**
Email:mscs24009@itu.edu.pk

University: Information Technology University, Lahore

**License**
This project is for academic purposes as part of CS 516 coursework at Information Technology University. All rights reserved by the author.

Course: CS 516 - Information Retrieval and Text Mining
Instructor: Dr. Ahmad Mustafa
Semester: Fall 2025
