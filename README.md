# mlops-zoomcamp projects EDA

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://mlops-zoomcamp-projects.streamlit.app/)


This project analyzes the title of projects from the [mlops-zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp) course from a CSV file, processes it, and visualizes the results using various techniques. 

In order to create the CSV file with the projects, I used the [Peer review assignments - MLOps Zoomcamp 2022](https://docs.google.com/spreadsheets/d/e/2PACX-1vQYTps829bmaN-aaJPiBUc3UwtN3e_llI44DKv-rQDsmVRMS1No7XWQqOyNI4ZbFbIvN351Q-G6edCP/pubhtml#). There could be mistakes, since they don't explicitly provide the title. Upcoming iterations of the course should provide the title of the projects, so that the procedure is easier and error-prone.

## Dependencies
The project depends on the following Python packages:
- pandas
- string
- matplotlib
- nltk
- wordcloud
- gensim

If you do not have these packages installed, you can install them using pip:
```bash
pip install pandas matplotlib nltk wordcloud gensim
```

## Description of Functions
The script contains the following functions:

- `read_data(filename)`: Reads a CSV file using pandas.
- `preprocess_text(text)`: Preprocesses the text by lowercasing, removing punctuation, tokenizing, removing stop words, and lemmatizing.
- `calculate_word_frequency(processed_titles)`: Calculates the frequency of each word in the processed titles.
- `plot_top_titles(data)`: Plots the top 10 most frequent project titles.
- `plot_word_frequency(word_freq)`: Plots the top 20 most frequent words in the project titles.
- `generate_wordcloud(processed_titles)`: Generates a word cloud from the processed titles.
- `perform_topic_modeling(processed_titles)`: Performs LDA topic modeling on the processed titles.
- `perform_analysis(filename)`: Orchestrates all of the above functions to perform the analysis on the given filename.

## Usage
To use this script, you need to have a CSV file with a column called `project_title`. 

```python
data_path = './Data/mlops_2022.csv'
perform_analysis(data_path)
```

This line sets the path to the data file and calls the `perform_analysis` function with it. Replace `./Data/mlops_2022.csv` with the path to your data file. The `perform_analysis` function will read the data, preprocess the project titles, calculate and plot word frequencies, generate a word cloud, and perform topic modeling.

## Output
This script produces several plots:
- A bar plot of the top 10 most frequent project titles.
- A bar plot of the top 20 most frequent words in the project titles

## Possible Extensions


- **Automation**: Include more automation features to streamline the process of analyzing new data files.

- **Testing**: Implement a comprehensive suite of tests. This could include unit tests, integration tests.

- **Additional Analysis Techniques**: Exploring new ways to analyze and visualize text data.



## Contributing

We welcome contributions to this project! Here's how you can help:

1. **Fork the Repository**: Click the 'Fork' button at the top right of this page and clone your forked repository to your local machine.

2. **Create a New Branch**: From your local repository, create a new branch for your feature or bugfix.

3. **Make Your Changes**: Make your changes to the new branch. Be sure to test your changes!

4. **Commit and Push Your Changes**: Once you're happy with your changes, commit them with a meaningful commit message and push the branch to your forked repository on GitHub.

5. **Create a Pull Request**: From your forked repository on GitHub, click the 'New pull request' button located at the top of your repo. Ensure it is asking to pull from your branch to the main branch of this repository.

We will review your changes and, if they are accepted, they will be included in the project.

If you have any questions about contributing, please feel free to contact us. Thank you for your interest in improving our project!
