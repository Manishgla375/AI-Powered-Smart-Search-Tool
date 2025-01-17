##A Smart Search Tool for Analytics Vidhya’s free courses
#1. Introduction
I built a Smart Search Tool for Analytics Vidhya’s free courses. The goal was to help users easily find relevant courses using natural language queries. This tool saves time and improves the user experience by providing quick and accurate results.
#2. Data Collection & Preparation
I collected data from Analytics Vidhya’s Free Courses platform, including course titles, descriptions, ratings, and levels. The data was cleaned, duplicates were removed, and a single field (Course_Text) was created by combining titles and
descriptions for better search accuracy. 
#3. Embedding and Vector Database
I used the all-MiniLM-L6-v2 model to convert course text into numerical embeddings. These embeddings were stored in a
FAISS (Facebook AI Similarity Search) database, which allows fast and efficient retrieval of relevant course information. 
#4. Retrieval-Augmented Generation (RAG) System MY system combines information retrieval (FAISS) with text generation (GPT-4). When users enter a query, FAISS retrieves
the best results, and GPT-4 generates a user-friendly response summarizing the course recommendations. 
#5. Deployment
I deployed the tool on Hugging Face Spaces using Gradio for the user interface. Users can access my tool through a public URL, ask questions, and get course recommendations instantly. 
#6. Challenges and Solutions One challenge was deploying the FAISS index on Hugging Face Spaces. We solved this by compressing the FAISS index into
a zip file and adding code in app.py to unzip and load it during deployment. 
#7. Conclusion MY project successfully built a Smart Search tool for free Analytics Vidhya courses. Users can now easily search and find
relevant courses using simple natural language queries, saving time and enhancing their learning experience.
