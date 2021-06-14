# RNN_Intrusion-Detection_Keras
This project aims primarly to reproduce the results made by RC Staudemeyer in his article "Applying machine learning principles to the information security field through intelligent intrusion detection systems.".  
Then it proposes to compare the performance of several Recurrent Neural Networks and Classifiers on the KDD CUP'99, NSL KDD and UNSW NB-15 datasets.

## Usage
1. **Download the code:** 
    ```
    git clone https://github.com/sylvainlapeyrade/RNN_Intrusion-Detection_Keras.git
    ```
2. **Make sure the dependencies are met:** 
    ```
    pip install -r requirements.txt
    ```
3. **Download the datasets needed:**  
See [Data](#Data) and [Directory structure](#Directory-structure) for more information and links.
*The names of the datasets must be the same as in the processing files.*  

4. **Set the parameters for the training or let them by default.**

5. **Move the RNN_Intrusion-Detection_Keras folder:** 
    
    To train with Recurrent Neural Networks, run:
    ```
    python3 ./src/training_rnn.py 
    ```
    To train with Classifiers, run:
    ```
    python3 ./src/training_classifier.py
    ```
    To view the results, run:
    ```
    python3 ./src/results_visualisation.py
    ```
    *On linux use: `python3 path_to_file` and on windows use: `python3 path_to_file`*  

## Project structure
### Required packages:
Packages with the version used (tensorflow-gpu is only mandatory for gpu training):
* `scikit-learn==0.21.2` 
* `numpy==1.16.4`
* `pandas==0.25.0`
* `Keras==2.2.4`
* `tensorflow==1.14.0`
* `tensorboard==1.14.0`
* `tensorflow-gpu==1.14.0`

### Directory structure:
* RNN_Intrusion-Detection_Keras
    * data
        * [kddcup_traindata_10_percent.csv](http://kdd.ics.uci.edu/databases/kddcup99/) - 46 145 Ko
        * [kddcup_traindata.csv](http://kdd.ics.uci.edu/databases/kddcup99/) - 725 176 Ko
        * [kddcup_testdata_corrected.csv](http://kdd.ics.uci.edu/databases/kddcup99/) - 73 135 Ko
        * [KDDTest+.csv](https://www.unb.ca/cic/datasets/nsl.html) - 3 361 Ko
        * [KDDTest-21.csv](https://www.unb.ca/cic/datasets/nsl.html) - 1 772 Ko
        * [KDDTrain+.csv](https://www.unb.ca/cic/datasets/nsl.html) - 18 662 Ko
        * [KDDTrain+_20Percent.csv](https://www.unb.ca/cic/datasets/nsl.html) - 3 733 Ko
        * [UNSW_NB15_testing-set.csv](https://research.unsw.edu.au/projects/unsw-nb15-dataset) - 15 021 Ko
        * [UNSW_NB15_training-set.csv](https://research.unsw.edu.au/projects/unsw-nb15-dataset) - 31 537 Ko
    * logs
    * models
    * results
    * src
        * [kdd_processing.py](src/kdd_processing.py)
        * [results_visualisation.py](src/results_visualisation.py)
        * [training_classifier.py](src/training_classifier.py)
        * [training_rnn.py](src/training_rnn.py)
        * [unsw_processing.py](src/unsw_processing.py)

## Data
The project works with 3 differents datasets (although more could be tested) :
* [KDD Cup'99](https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) (1999).
* [NSL-KDD](https://www.unb.ca/cic/datasets/nsl.html) (2009).
* [UBSW-NB15](https://www.unsw.adfa.edu.au/unsw-canberra-cyber/cybersecurity/ADFA-NB15-Datasets/) (2015).

## References
This projet has been inspired by the the following article : "Applying long short-term memory recurrent neural networks to intrusion detection" by RC Staudemeyer - ‎2015.

## License
[MIT](LICENSE) © [Sylvain Lapeyrade](https://github.com/sylvainlapeyrade) - Project part of my internship at IRIT.
