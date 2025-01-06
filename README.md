### Deezer Network Genre Analysis

Analyzing Community Structures and Genre Preferences in Deezer User Networks
This repository contains the code, data, and resources for a network science project focused on analyzing user communities and genre preferences in Deezer networks. The project explores community detection, centrality measures, and the role of influential users in genre dissemination across three regions: Romania, Croatia, and Hungary.

#### Project Overview

The project applies network science methodologies to answer the following key questions:

- What are the most central genres within user communities?

- Which genres act as bridges between communities?

- How do user communities and their genres differ across Romania, Croatia, and Hungary?

- What roles do high-degree and diverse-taste users play in community connectivity?


#### Features

Data preprocessing and graph construction using Deezer datasets.
Community detection using Louvain and Girvan-Newman algorithms.
Centrality analysis to identify influential genres and users.
Regional comparison of community structures and genre preferences.
Visualization of network structures and genre dynamics.


### Technologies Used
Python 3.x

### Libraries:
networkx - Graph processing
pandas - Data manipulation
matplotlib & seaborn - Visualization
numpy - Numerical operations

### File Structure

```
deezer-network-genre-analysis/
│
├── data/                     # Raw and processed Deezer datasets         
│
├── src/                      # Source code for the project
│   ├── main.ipynb            # Data loading and preprocessing
│
├── output/                  # Output visualizations and findings
│   ├── main_executed.ipynb/
│   └── genre_centrality_plots/
│
├── README.md                 # Project documentation (this file)
├── requirements.txt          # Required Python libraries
└── report.pdf                # Final project report
```

#### Setup Instructions

Clone the Repository
```
git clone https://github.com/azizbekasadov/deezer-network-genre-analysis.git

cd deezer-network-genre-analysis
```

Install Dependencies
Ensure Python is installed, then run:
```
pip install -r requirements.txt
```
OR
```
make run 
```
Make sure you have installed WSL and run make commands on dos2unix on Windows, or simply use the command as it is on Unix-based OS.

Run the Code
Preprocess the data:
python src/data_preprocessing.py
Build the graph and detect communities:
python src/community_detection.py
Analyze genre centrality and influence:
python src/genre_analysis.py
View Results
Outputs will be stored in the results/ directory.

**Key Results**

* Community Structures: Visualizations of user communities for each country.
* Genre Influence: Central and bridging genres identified using degree and betweenness centrality.
* Regional Insights: Comparative analysis across Romania, Croatia, and Hungary.

**Contributions**

**Author	Contribution**
All authors conceived and designed the idea of the project, drafted the proposal and presentation.


Elena Baranauskaite	- 24-718-165 found the dataset, proposed project idea, authored the main data [preprocessing script](https://github.com/azizbekasadov/deezer-network-genre-analysis/blob/main/src/graph_data_precomputation_all_countries.ipynb) and prepared [ready-to-consume files](https://github.com/azizbekasadov/deezer-network-genre-analysis/tree/main/data) with communities, centralities and genres for easier analysis. Conduced analysis for research questions on **"What are the most central musical genres within user communities, indicating strong intra-community connections?"** and **"Which genres act as bridges between communities or isolate
users in Romania?"** and prepared the report sections with visualizations on them. Authored the [code](https://github.com/azizbekasadov/deezer-network-genre-analysis/blob/main/src/analysis_for_questions_1_2_RO_.ipynb) that facilitates this analysis with visualizations.


Azizbek Asadov - 23-747-041 did datasets preprocessing (main.ipynb), cleaning and separation due to the region, set up github repo and environment to work on the project, contributed to the research question, "How do users with diverse musical tastes influence network dynamics and cross-community connections?," by formulating the research objective, conducting data analysis, and interpreting the findings, did the analysis of the findings corresponding to the datasets per each selected region (Romania, Hungary, Croatia) and observed centrality effects (betweenness and closeness) and derived implications for each region.\\



Teodora Nae -	22-748-107 contributed to the analysis of network dynamics and genre diversity across Romania, Hungary and Croatia, especially for research questions 4 and 5. Also, authored the code that facilitates the visualization of correlations between genre diversity and centrality metrics, offering a clearer understanding of the roles played by diverse-taste users and high-degree nodes in bridging and isolating communities. As well as, contributing to the report and presentation. 


Baran Özgür Taş - 24-744-336 Conducted analysis for research question 3 and prepared the report section with visualizations. Also authored the conclusion.\\
All Authors discussed and reached the conclusions. All Authors revised and accepted the final version of this document as well as prepared the presentation.


**License**

This project is licensed under the MIT License.

**Contact**

For questions, contributions, or collaborations, please contact:
Azizbek Asadov – azizbek.asadov@uzh.ch

**DEPRECATED**
We no longer support Docker for project assembly.

### DOCKER DEPLOYMENT INSTRUCTIONS

**Prerequisites**

**Install Docker Desktop:** Download Docker Desktop for Mac and install it.
**Clone Your GitHub Repository:** Clone your repository locally or ensure the Dockerfile is accessible.

**Project Structure**
```
project/
│
├── Dockerfile
├── requirements.txt (optional, for Python dependencies)
├── Makefile
├── src/
│   ├── main.ipynb
├── latex/
|   ├── presentation/
|   |   ├── main.tex
|   |   ├── references.bib
|   ├── report/
|   |   ├── main.tex
|   |   ├── references.bib
│
└── resources/
```

### Build and Run the Docker Container

**Step 1: Build the Docker Image**
Navigate to your project directory in the terminal and run:
```
docker build -t deezer .
```
**Step 2: Run the Docker Container**
Run the container and map the ports:
```
docker run -p 8888:8888 deezer
```
**Step 3: Access the Jupyter Notebook**
Once the container is running, look for a URL in the terminal output, such as:
```
http://127.0.0.1:8888/?token={your_token_here}
```
Then, open this URL in your web browser to access the Jupyter Notebook interface.

**Stopping the Docker Container**

Press Ctrl+C in the terminal to stop the container.
Alternatively, stop it via the Docker Desktop interface.
Troubleshooting

**Dependencies not found:**
Ensure all dependencies are listed in requirements.txt.
Notebook not accessible:
Confirm Docker Desktop is running.
Check the port mapping (-p 8888:8888) and browser URL.
