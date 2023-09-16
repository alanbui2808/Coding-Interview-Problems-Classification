<h2 align='center'> Project Description </h2>

Grinding Leetcode - solving coding problems is no longer an unfamiliar thing to CS students who want to break into the industry and work for big tech companies. When solving coding problems, we often focus on the questions’ pattern, therefore correctly categorize them could help us efficiently allocate the time to approach the optimal solution. Despite the fact that most problems have labels given by the respective platforms, they are mostly categorized based on the rubrics of the platforms instead of candidates' experience. This includes a combination of time and space complexity contraints, implementability of the solution etc. However, I and including many more often agree that time complexity is the most important constaint during interviews. Thus, additional to the problem description there is time complexity required. An important note that coding problems can be telling stories, thus I will only choose problems that are directly correlated to Computer Science field. A pre-trained BERT is chosen to be fine-tuned to for this classification task. The metrics used is accuracy.

### Table of Contents

1. [Dataset Information](#dataset_info)
2. [Dependencies](#depend)
3. [Files](#files)
4. [How to Run](#run)

### Dataset Information<a name="dataset_info"></a>
120 problems taken from different platforms such as Leetcode, Hacker, Codeforces etc. An important note that coding problems can be telling stories, thus I will only choose problems that are directly correlated to Computer Science field. Each entry in the dataset contains the description of the problem and a time complexity in terms of big-O notation concatenated at the end. The dataset is annoted by various annotators with the following guideline: 1 (Easy) - if you think the solution for the given problem can be come up within 5 minutes that meet the time complexity required and 0 (Difficult) - if otherwise. The final label is aggregated by the following the min value among labels.

In other words, if either one annotator finds a problem difficult (label 0) then we should assign label 0 to that corresponding problem. If an annotator A comes up with solution withint 5 minutes and annotator B comes up with solution more than 5 minutes then it is also possible for annotator A to come up with solution more than 5 minutes. It means that if a problem is difficult for 1 annotator, then it can be difficult for both annotator but not the other way around.

### Dependencies<a name="depend"></a>  
1. Numpy: Perform several mathematical evaluations in the preprocessing of the datasets
   
    `pip install numpy  `

2. Pandas: Loading/Processing/Storing of the different datasets

    `pip install pandas `
  
3. Pytorch: Please follow this <a href="https://pytorch.org/get-started/locally/"> Link </a> for a suitable installments 

4. Transformers: BERT
   
    `pip install transformers`

### Files<a name="files"></a>
* `Annotation Guideline`: Guideline designed for annotators to follow to label the dataset.
* `final_dataset`: Aggregated dataset from annotators.
* `helpers`: Define helper functions for tokenization.

### How to Run<a name="run"></a>
* The notebook is pretty straightforward, you are recommended to run on Google Colab. However uploading the dataset can be a hassle :)
