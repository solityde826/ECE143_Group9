<!------------------------------------------ TITLE BLOCK --------------------------------------------------------------->
<h1 align="center"> Group 9: Analysis and Prediction of Graduate School Admissions </h1>

<p align="center">
    Course Project for UCSD ECE 143: Programming for Data Analytics
    <br /> <br />
    <a href="https://github.com/solityde826"> Chengzhan Gao </a>
    ·
    <a href="how016@ucsd.edu"> Houtianfu Wang </a>
    ·
    <a href="ken010@ucsd.edu"> Kendrick Nguyen </a>
    ·
    <a href="w8dong@ucsd.edu"> Weirong Dong </a>
    ·
    <a href="vpawar@ucsd.edu"> Varun Pawar </a>
</p>


<!------------------------------------------ TABLE OF CONTENTS ---------------------------------------------------------->
<details open="open">
  <summary><h2 style="display: inline-block"> Table of Contents </h2></summary>
  <ol>
    <li>
      <a href="#about-the-project"> About The Project </a>
      <ul>
        <li><a href="#datasets"> Datasets </a></li>
        <li><a href="#job-to-be-done"> Job To Be Done </a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started"> Getting Started </a>
      <ul>
        <li><a href="#prerequisites"> Prerequisites </a></li>
        <li><a href="#how-to-run"> How to Run </a></li>
      </ul>
    </li>
    <li><a href="#file-architecture"> File Architecture </a></li>
  </ol>
</details>


<!------------------------------------------ About The Project ---------------------------------------------------------->
## About The Project

Every student applying for a college education surely wants to know what are the chances of getting into their dream school. 
Our project is designed to visualize and predict the probability of admission of certain students and the universities to 
which they apply, which is beneficial for the students in need.

The results of this project are expected to help worldwide students who are applying for master’s programs. With our prediction 
as guidelines, they could apply a better application strategy if they already know for which kind of universities they are more 
attractive, so that they have a much bigger chance of admission.

### Datasets

The selected datasts includes parameters of interest, such as GRE Scores and Undergraduate GPAs, that are considered significant 
during graduate application processes.

* Graduate Admission Results via [GradCafe Statistics (scraped)](https://github.com/AlpAribal/gradcafestats/blob/master/data/submissions.csv)
* Graduate Admission Results via [Kaggle](https://www.kaggle.com/datasets/mohansacharya/graduate-admissions?resource=download)

### Job To Be Done
1. Firstly, a data analysis will be carried out to explore the basic statistics and properties of the dataset, and build up the 
relationship among different parameters. 
2. Then based on the data analysis results, several prediction models (like logistic regression, naive bayes, support vector machine, 
nearest neighbor classifier, etc.) will be trained. 
3. A UI will be implemented that would allow users to input parameters (GRE scores, TOEFL scores etc.) to predict probability of 
admission using our trained models. 


<!------------------------------------------ Getting Started ---------------------------------------------------------->
## Getting Started
Unfortunately, the Graduate Admission Results via [GradCafe Statistics (scraped)](https://github.com/AlpAribal/gradcafestats/blob/master/data/submissions.csv)
dataset was too large to push to the repository. Download the dataset and place it inside the `data/raw_data` folder.

Now to get a local copy up and running follow these steps.

### Prerequisites
Clone the repository:
```
git clone https://github.com/solityde826/ECE143_Group9
```

Install the following dependencies:
* implicit
* Jupyter
* Matplotlib
* numpy
* openpyxl
* pandas
* PyTorch
* scikit-learn
* seaborn
* xgboost 

or alternatively run,
```
pip install -r requirements.txt
```

### How to Run
1. Run the `doc/presentation_visualizations.ipynb` notebook to obtain visuals from the presentation
2. Run the `src/RecommenderSys.py` script to predict your admission chances

<!------------------------------------------ File Architecture  ---------------------------------------------------------->
## File Architecture
```
[ECE143_Group9]
├─ 📁data
    ├─ 📁cleaned_data
        ├─ 📁dataGroupByUniversity
            ├─ 📄Brown University.csv
            ├─ 📄UCLA.csv
            ├─ 📄University Of Pennsylvania.csv
        ├─ 📄cleaned_grad_cafe_admissions.csv
        ├─ 📄cleaned_kaggle_grad_admissions.csv
        ├─ 📄grad_cafe_admissions_updated.csv
        ├─ 📄unlabled_grad_cafe_admissions.csv
    ├─ 📁raw_data
        ├─ 📄kaggle_grad_admissions.csv
        ├─ 📄submissions.csv
    ├─ 📁university_rank
        ├─ 📄rank_processed.xlsx
        ├─ 📄university_rank.csv
├─ 📁doc
    ├─ 📁analysis_plots
      ├─ 📄...
    ├─ 📄presentation slides.pdf
    ├─ 📄presentation_visualizations.ipynb
├─ 📁model
    ├─ 📄best_model.model
    ├─ 📄best_model.sav
    ├─ 📄LinearReg.pkl
    ├─ 📄saved_model.pt
    ├─ 📄XGBRegressorodel.pkl
├─ 📁src
    ├─ 📄ANN_class.py
    ├─ 📄ANN_Kaggle_Prediction_Pytorch.py
    ├─ 📄backup_code.py
    ├─ 📄data_cleaning_wrangling.py
    ├─ 📄Different_Regressors_on_Kaggle_data.py
    ├─ 📄grad_cafe_analysis_visualization.py
    ├─ 📄helper.py
    ├─ 📄kaggle_analysis_visualization.py
    ├─ 📄MapUni2Rank.py
    ├─ 📄naive_Bayes.py
    ├─ 📄prediction.py
    ├─ 📄RecommenderSys.py
├─ 📁testing
    ├─ 📄...
├─ 📄.gitignore
├─ 📄README.md
```
