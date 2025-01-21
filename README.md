# README

This repository contains three Jupyter notebooks designed for parsing and analyzing repositories and code snippets in Python, Java, and C using embedding techniques and similarity analysis. These notebooks are ideally run on **Google Colab** to leverage its computational resources.

---

## 1. **PythonSim.ipynb**
### Description
This notebook focuses on Python repositories and code snippet analysis. It employs [**inspect4py**](https://github.com/SemanticRepoHub/inspect4py) repository parsing library, and  **RepoSim4Py** model (pipeline)[1](https://github.com/SemanticRepoHub/RepoSim4py); and [2](https://huggingface.co/Henry65/RepoSim4Py) to:

- Genate Python code snippets embeddings and compute their similarity. 
- Parse and extract repository metadata.
- Generate multi-level embeddings (code, documentation, README, and requirements).
- Compute semantic similarity between repositories at different levels.

### Key Features
- Code Snippet similarity
- Extract all the information: functions, imports, classes, methods, code, etc ... from a Python repository
- Uses embeddings to represent repositories at various granularities.
- Computes cosine similarity scores for code, documentation, README, and overall repository content.
- Outputs similarity results in a clear tabular format.

### Ideal Use Case

- Understanding how to generate embeddings from code snippets, and compute their similarity (cosine similarity)
- Understanding how to use inspect4py and extract information
- Analyzing Python repository structures and relationships.
- Performing semantic comparisons of Python codebases.

---

## 2. **JavaSim.ipynb**
### Description
This notebook extends the analysis framework to Java repositories using a similar embedding approach. It covers:
- Genate Java code snippets embeddings and compute their similarity. Here we are using [Unixcoder DL model](https://huggingface.co/Lazyhope/unixcoder-nine-advtest) (more research is needed).  
- Parsing Java repositories for code and documentation.

### Key Features
- Uses a custom embedding model for Java - more exploration will be needed.
- Understand how to extract code and documentation from Java files

### Ideal Use Case
- Basic semantic analysis of Java snippets. More research is needed to understand what is best model to use - we used Unixcoder just as an example. 
- Identifying relationships between Java projects based on embeddings.

---

## 3. **parsing_java_c_test.ipynb**
### Description
This notebook demonstrates repository parsing techniques for Java and C projects. It:
- Extracts metadata, dependencies, and code structure.
- Provides basic analysis for repositories written in Java and C.

### Key Features
- Focuses on metadata extraction and structure visualization.
- Demonstrates parsing without in-depth embedding generation.

### Ideal Use Case
- Preprocessing and metadata extraction for Java and C projects.
- Repository structure analysis before applying advanced embedding techniques.

---

## How to Use
1. Open any of the notebooks in **Google Colab** accessing to these links:.

   * [PythonSim.ipynb](https://colab.research.google.com/drive/1BWSxM95NPGrmkpXH_2iGiKSpDUhpt_WE?usp=sharing)
   * [JavaSim.ipynb](https://colab.research.google.com/drive/1ZhsSyosX1p4Xy0-88YM1n62JENqydi7S?usp=sharing)
   * [parsing_java_c_test.ipynb](https://colab.research.google.com/§drive/1yy6x7BjHz_vlMfov2KODghR4tjOCi6gq?usp=sharing)

---

## Requirements
- **Google Colab** environment - with a google account will be enough to run those. 
- If running the notebooks locally, Python packages such as `transformers`, `torch`, and other dependencies (automatically installed in each notebook).
- Note that inspect4py needs a **Python 3.10** condaenviroment (see bellow code) - this is necessary **only** do when running the notebooks locally. In google colab not need to create a conda enviroment, they work directly with the provided code.

```
--note conda must be installed beforehand, go to https://conda.io/projects/conda/en/stable/user-guide/install/linux.html
conda create --name py10 python=3.10
conda activate py10
```
---

## Note
These notebooks are designed for demonstration purposes and provide insights into code and repository parsing (using ASTs) analysis (using embeddings). 
