# Feature-Selection-using-Metaheuristic-Approaches-for-Intrusion-Detection-System

There are two folders in the repository:
1. MH_Algorithms
2. datasets

There is one python notebook in the repository:
Feature_Selection_Notebook.ipynb , this is the main file which performs data processing, feature selection and classification for this study.

# MH_Algorithms
In this folder, there are five python (.py) files.
1. de.py [contains the implementation of the differential evolution]
2. fpa.py [contains the implementation of the flower pollination algorithm]
3. pso.py [contains the implementation of the particle swarm optimization]
4. sca.py [contains the implementation of the sine cosine algorithm]
5. functionHO.py  [contains the implementation of fitness function for this study]

Each algorithm is implementation based on the algorithm provided in the original research paper.
Each of the four algorithms has four functions in their implementation:
/init_position() -> generates initial population with floating point values for the problem
/binary_conversion() -> converts the initial population vector into a binary (0/1) vector
/jfs() -> contains the main algorithm implementation
/boundary() -> helps in normalization

*functionHo.py has two functions:
/fun() -> calculates the fitness score
/error_rate  -> contains the machine learning model for fitness evaluation

# datasets
In this folder, there are two .csv files.
1. UNSW-NB15_training-set.csv  [contains 175341 records]
2. UNSW-NB15_testing-set.csv   [contains 82332 records]
The UNSW-NB15 dataset (Moustafa and Slay, 2016) was generated using an IXIA PerfectStorm program. The
tcpdump program was used to record 100 GB of raw network data (pcap files). Each pcap file is 1000 MB in size to
facilitate packet analysis. To create 49 features with the class label, Argus and Bro-IDS approaches were utilized, and
12 processes were carried out. This dataset is separated into two parts: training and testing. 
The training set has 175,341 records, whereas the testing set contains 82,332 records that can be attack or normalnon-attack. Analysis, backdoor,
DoS, Exploits, Fuzzers, Generic, Reconnaissance, Shellcode, and Worms are the nine types of attacks undertaken
against the UNSW-NB15 dataset. The dataset has "label" values of 0 and 1, with 0 representing no
attack and 1 representing an attack. So, using the information at our disposal, this study attempts to predict whether a
particular datapoint belongs to the attack or non-attack group.


#How to reproduce the results
1. Copy all the folders and files in google drive
2. Open Feature_Selection_Notebook.ipynb with google collaboratory
3. Run the cells one by one
4. During run you need to - 
    A. Hybridization:
        a. Select first model
		b. Update parameter values
		c. select second model
		d. Update parameter values
	B. Single Run:
	    a. Select first model
		b. Update parameter values
		c. No need to run second model and its subsequent cells
	C. Fitness evaluation model:
	    a. Select KNN / GaussianNB in functionHo.py (by default KNN)
		
