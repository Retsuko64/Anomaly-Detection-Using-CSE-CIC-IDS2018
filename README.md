# Anomaly-Detection-Using-CSE-CIC-2018

- ### Group Number: 23

- ### Link to the sample data: https://drive.google.com/file/d/1EMe83pWkccHg3mD5LLuCaHURjYjx7fjo/view?usp=sharing (It's a compressed (.rar) file so you have to decompress it)
When attempting to run the dataset using pandas read_csv() function, the function looks for the dataset inside a folder named 'archive' (Ex: pd.read_csv('./archive/03-02-2018.csv') ). So either be sure the dataset is inside such folder, or feel free to change it in any way as long as it points to the dataset (.csv) file.

- ### Started By:
  - [Khaled El Arabi El Azzouzi](https://github.com/Khaledazzouzii)
  - [Obadah Nidal Ghizawi](https://github.com/Whiffed2022)
  - [Hassan Fakih Osman](https://github.com/Retsuko64)

- ### Professor:
  - [Umut Mennan Güder](https://github.com/umutguder)

- ## Intro:
In this project, we build an anomaly-based intrusion detection system (IDS) using Machine Learning algorithms. To do that we used the CSE-CIC-IDS2018 dataset from the University of New Brunswick, which is a collaborative project between the Communications Security Establishment (CSE) and the Canadian Institute for Cybersecurity (CIC).<br>The dataset is of size (aprox.) 450 GB from the original source (https://www.unb.ca/cic/datasets/ids-2018.html). So instead we rely on the dataset found on Kaggle in the link: https://www.kaggle.com/datasets/solarmainframe/ids-intrusion-csv

- ## About the dataset:
The CSE-CIC-IDS2018 dataset from Kaggle contains 10 files each captured in a specific day with different types of attacks:
  - 03-02-2018:                   ['Benign', 'Bot']
  - 02-28-2018 - 03-01-2018:      ['Benign', 'Label', 'Infilteration']
  - 02-22-2018 - 02-23-2018:      ['Benign', 'Brute Force -Web', 'Brute Force -XSS', 'SQL Injection']
  - 02-21-2018 :                  ['Benign', 'DDOS attack-LOIC-UDP', 'DDOS attack-HOIC']
  - 02-20-2018:                   ['Benign', 'DDoS attacks-LOIC-HTTP']
  - 02-16-2018:                   ['Benign', 'DoS attacks-SlowHTTPTest', 'DoS attacks-Hulk', 'Label']
  - 02-15-2018:                   ['Benign', 'DoS attacks-GoldenEye', 'DoS attacks-Slowloris']
  - 02-14-2018:                   ['Benign', 'FTP-BruteForce', 'SSH-Bruteforce']

In our study, we relied on data from dates: 03-02-2018 - 03-01-2018 - 02-23-2018 - 02-14-2018. Which covers the following attacks: Infilteration, Brute Force -XSS, Brute Force -Web, SQL Injection, Bot, FTP-BruteForce, and SSH-Bruteforce. These datasets were merged, preprocessed, and applied to different models. Note: If you will manually download the datasets from kaggle, there might be some issues with files 02-28-2018 - 03-01-2018 - 02-16-2018 because the column row (first row) is repeated multiple times, making pandas assign dtype 'object' to all the columns. So if thats the case, you can change them to dtype 'float' (There is a sample code included in our notebook), however, there is no such issue with our sample data.

- ## Machine Learning Algorithms Used:
    - Decision Trees
    - Voting Classifier (Made up of Decision Trees, Random Forest, and AdaBoost)
    - Isolation Forest

The code also includes K-NN and Random Forest. But in our report we covered only whats on the list.

- ## Libraries Used:
  - Numpy
  - Scikit-Learn
  - Matplotlib (For data visualization)
  - Seaborn (For data visualization)
  - Pandas

However, bear in mind that these libraries are already installed in Colab, but if you will run this locally then you have to install these packages manually by opening CMD (Terminal) and type:
> pip install -r requirements.txt

Which would install all the packages for you, or you can install them manually one by one:
> pip install numpy

And so on..

## For more details on how we preprocessed the dataset, and how we created different models along with their results, plus our Exploratory Data Analysis. Read our report! 
