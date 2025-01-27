# Convert any Corpus of Text into a *Graph of Knowledge*

![Knowledge Graph Banner](./assets/KG_banner.png)
*A knowledge graph generated using this code* 


## What is a knowledge graph?
A knowledge graph, or semantic network, visualizes a network of real-world entities—such as objects, events, situations, or concepts—and their interconnections. Typically stored in a graph database, knowledge graphs are displayed as interconnected nodes and edges, reflecting the relationships between entities.

Source: https://www.ibm.com/topics/knowledge-graph

## How to create a simple knowledge graph from a body of work?
1. Clean the Text Corpus: Prepare the body of work by removing unnecessary elements.
2. Extract Concepts and Entities: Identify and extract key concepts and entities from the text.
3. Determine Relationships: Identify relationships between these entities.
4. Define the Graph Schema: Create a schema for the graph structure.
5. Populate the Graph: Add nodes (concepts) and edges (relationships) based on the extracted data.
6. Visualize and Query: Optionally, visualize the graph and perform queries. Graphs are visually appealing and can be analyzed to gain insights into the text.

## Why Graph?
Knowledge graphs are valuable for various purposes:
1. Graph Algorithms: Calculate node centralities to determine the importance of concepts.
2. Community Detection: Identify clusters of related concepts.
3. Connectedness Analysis: Explore connections between seemingly unrelated concepts.
4. Graph Retrieval Augmented Generation (GRAG): Enhance interaction with the text using graphs for more profound queries compared to traditional Retrieval Augmented Generation (RAG).

## This project
This project demonstrates how to generate a knowledge graph from a PDF document. The approach involves:

1. Splitting Text: Dividing the text into chunks.
2. Concept Extraction: Using a language model to identify concepts and their relationships within each chunk.
3. Contextual Relationships: Establishing relationships between concepts mentioned in the same text chunk.
4. Graph Construction: Creating nodes and edges based on extracted concepts and relationships.
5. The process is simplified and run locally using the Mistral 7B model, which is cost-effective and efficient. 

The detailed steps are documented in the **[extract_graph.ipynb](https://github.com/rahulnyk/knowledge_graph/blob/main/extract_graph.ipynb)**

The notebook implements the method outlined in the following flowchart. 

<img src="./assets/Method.png"/>

**[Here is a Medium article explaining the method in detail ](https://medium.com/towards-data-science/how-to-convert-any-text-into-a-graph-of-concepts-110844f22a1a)**



---
## Tech Stack

### Mistral 7B
<a href="https://mistral.ai/news/announcing-mistral-7b/"><img src="https://mistral.ai/images/logo_hubc88c4ece131b91c7cb753f40e9e1cc5_2589_256x0_resize_q97_h2_lanczos_3.webp" height=50 /></a>

The [Mistral 7B Openorca](https://huggingface.co/Open-Orca/Mistral-7B-OpenOrca). model is used to extract concepts from text chunks effectively.

### Ollama
<a href="https://ollama.ai"><img src='https://github.com/jmorganca/ollama/assets/3325447/0d0b44e2-8f4a-4e99-9b52-a5c1c741c8f7 ' height='50'/></a>

Ollama facilitates the local hosting of models like Mistral 7B. Install Ollama and run ollama run zephyr to use the model locally.

### Pandas 
Utilized for managing dataframes and graph schema.

### NetworkX 
<a href="https://networkx.org"><img src="https://networkx.org/_static/networkx_logo.svg" height=50 /><a/>

A Python library for handling and analyzing graphs efficiently.

### Pyvis
[Pyvis python library](https://github.com/WestHealth/pyvis/tree/master) enables JavaScript-based graph visualizations using Python, allowing you to host interactive graphs online.
