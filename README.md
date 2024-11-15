# Local PDF Chat Application with Llama3 LLM, Langchain, Ollama, and Streamlit

A PDF chatbot is a chatbot that can answer questions about a PDF file. It can do this by using a large language model (LLM) to understand the user's query and then searching the PDF file for the relevant information. The application uses the concept of Retrieval-Augmented Generation (RAG) to generate responses in the context of a particular document. RAG applications augment their generation capabilities by retrieving relevant information from an external knowledge base. This allows RAG applications to produce more informative and comprehensive responses to a wider range of prompts and questions.
### For detailed explaination of how this works follow my [Medium Artcle](https://medium.com/@harjot802/building-a-local-pdf-chat-application-with-mistral-7b-llm-langchain-ollama-and-streamlit-67b314fbab57)
## Running Llama3 Locally using Ollama 🦙

Ollama allows you to run open-source large language models, such as Llama 3, locally. It bundles model weights, configuration, and data into a single package, defined by a Modelfile, optimizing setup and configuration details, including GPU usage.

**For Mac and Linux Users:**
Ollama effortlessly integrates with Mac and Linux systems, offering a user-friendly installation process. Mac and Linux users can swiftly set up Ollama to access its rich features for local language model usage. Detailed instructions can be found here: [Ollama GitHub Repository for Mac and Linux](https://github.com/ollama/ollama).

**For Windows Users:**
For Windows users, the process involves a few additional steps, ensuring a smooth Ollama experience:

1. **Install WSL 2:** To enable WSL 2, kindly refer to the official Microsoft documentation for comprehensive installation instructions: [Install WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install).

2. **Install Docker:** Docker for Windows is a crucial component. Installation guidance is provided in the official Docker documentation: [Install Docker for Windows](https://docs.docker.com/desktop/install/windows-install).

3. **Utilize Docker Image:** Windows users can access Ollama by using the Docker image provided here: [Ollama Docker Image](https://hub.docker.com/r/ollama/ollama).

Run Docker-Container:

```
docker run -d -v ollama:/root/.ollama -p 11435:11434 -p 8501:8501 --name llama3 ollama/ollama
```

Now you can easily use Llama3 in the command line (CMD) using the following command:

```
docker exec -it llama3 ollama run llama3
```
## Usage
#### NOTE: First install Ollama in docker and run Llama3 as stated above

-1. Get in the shell

 ```
 docker exec -it llama3 sh
 ```

0. Prepare the system:
   
 ```
 apt update
 apt install git pip -y
 ```

1. Clone this repository:
   
 ```
 cd
 git clone https://github.com/stefanmaeder/pdfchat-Llama3.git
 ```
2. Install all the depenedencies :
   
```
cd pdfchat-Llama3
pip install -r requirements.txt
```
3. Open terminal and run the following command:
```
streamlit run app.py &
```
## Application Preview :
![image](https://github.com/SonicWarrior1/pdfchat/assets/73881129/32f9685b-f70e-48da-8e6f-9fdce1fdd0cc)
