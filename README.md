 >>uv init .  ## project setup
 >>uv add fastapi inngest llama-index-core llama-index-readers-file python-dotenv qdrant-client uvicorn streamlit openai  ## techstack setup
 
 create Open ai api key
 Add api key to .env file
 
 terminal 1: uv run uvicorn main:app
 terminal 2: npx inngest-cli@latest dev -u http://127.0.0.1:8000/api/inngest --no-discovery  #innjest dev server opens on localhost::8288
 
 terminal 3: docker run -d --name qdrantRagDb -p 6333:6333 -v "$(pwd)/qdrant_storage:/qdrant/storage" qdrant/qdrant
 
 *******Build loader and streamlit pages*******
 terminal 4: uv run streamlit run .\streamlit_app.py
