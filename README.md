# Reproducible code test - Ana Macanovic

Version 0.1.0

### Project for the Workshop "Best Practices for Writing Reproducible Code"



<p style="text-align: justify;"> The purpose of this code is to showcase some 
elements of my PhD project analysis and edit them in the Workshop 
"Best Practices for Writing Reproducible Code". The analyses match those
done in my project; but on a different dataset. Thus, some elements of my
code cannot be run on this dataset fully, but are included to test the
reproducibility.</p>

<p style="text-align: justify;"> This code performs an analysis of 
feminist texts from the first and second wave feminist organizations in the US.
The analysis includes cleaning the data and obtaining some basic
descriptive statistics on the
distribution of texts across the years and organizations. Further, it outputs
statistics on the word and character counts for each text, along with 
the statistics of the most frequent words in the whole corpus of texts. Finally,
the code explores how the texts from the first and the second wave differ in 
their word usage and tests whether unsupervised machine learning methods can 
identify these two waves without any input from the researcher. </p>

The two tested machine learning models models are:

1. Word2vec word vectorisation with k-means clustering (not run in the code, 
since the data is not suitable)

2. LDA topic modelling 


<p style="text-align: justify;">The data being analysed is a collection of texts
produced by several feministor ganizations from the US. The data includes texts
from the First and Second wave feminist organizations. The actual texts are not 
readable; the data is shuffled so all the words contained in the texts appear in
alphabetical order, because of copyright concerns.</p>
The data is pulled from:
```
Nelson, Laura K. "Computational grounded theory: A methodological framework." 
Sociological Methods & Research 49.1 (2020): 3-42.
```

The code consists of three analysis files - notebooks - R markdown files
(all located in the "notebooks" folder), loading and processing a single
.csv data source.


The structure is as follows:

1. File 1 loads and cleans up the data

2. File 2 loads the cleaned up data and performs basic descriptive statistics
on it, producing several graphs and tables.

3. File 3 loads the cleaned up data and tests whether automatic text analysis 
clustering methods can identify which texts come from the first or the second
wave based on their content and wrod usage. Finally, the accuracy of this
prediction is given.


### How to run this code?
To run the full analysis, you need to run the notebooks in the specified
oder.

1. Run the file "1_Data_loading_cleanup.Rmd"

2. Run the file "2_Descriptive_stats.Rmd"

3. Run the file "3_Topic_model.Rmd"

The essential steps and explanations are provided in the notebook files 
themselves. 

The output is written to the "results" folder, where one can see the 
graphs and tables resulting from the analysis. 

Please compare whether your output matches the results you can find on this
github page. 


### Requirements

This code requires a few libraries to be run. These are:

- readr
- quanteda
- tm
- dplyr
- magrittr
- stringi
- textcat
- h2o (this part can be skipped, since requires )
- psych
- ggplot2

You can use the following code to install all the needed packages:
```
install.packages(c("readr", "quanteda", "tm", "dplyr", "magrittr",
"stringi", "testcat", "psych", "ggplot2"))
```

Optionally, also install - <b> this is a java wrapper for R, so might not
be that easy to set up; you can skip this part and skip the part of the code
utilizing this package </b>

```
install.packages("h2o")
```


## Project organization

```
.
├── .gitignore
├── CITATION.md
├── LICENSE.md
├── README.md
├── requirements.txt
├── bin                <- Compiled and external code, ignored by git (PG)
│   └── external       <- Any external source code, ignored by git (RO)
├── config             <- Configuration files (HW)
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)

```

## License

This project is licensed under the terms of the [MIT License](/LICENSE.md)

## Citation

Please [cite this project as described here](/CITATION.md).
