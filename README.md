Online Semi-Supervised Boostig (OSSB) in data stream mining


📁 Project Description
Implementation of OSSB (Online Semi-Supervised Boosting) algorithm for streaming data with concept drift handling and partial labeling support.


1- Install Dependencies

bash
pip install river pandas numpy matplotlib scikit-learn


2- Prepare Your Dataset

    -Convert your dataset to CSV format

    -Ensure the last column contains target labels

    -Update the data path in the code:
  data_path = "path/to/your/dataset.csv"  # SET THIS PARAMETER

3- Configure Parameters (commented in code)


# SET THESE PARAMETERS:
W_size = 200                  # Window size
M = 10                        # Number of base models
p_value_threshold = 0.9       # Confidence threshold for pseudo-labeling
gamma = 0.5                   # RBF similarity parameter
k_neighbors = 10              # Neighbors for consensus
initial_batch_size = 100      # Initial labeled data size
label_percentage = 0.05       # Percentage of available labels
drift_delta = 0.001           # Drift detection sensitivity


4- Run the Code

bash
python OSSB.py


⚙️ Key Features

* Online Learning: Processes data streams incrementally

* Semi-Supervised: Handles partially labeled data (5% labels by default)

* Concept Drift Detection: Uses ADWIN for automatic drift detection

* Ensemble Management: Dynamically adds/removes models based on performance

* Pseudo-Labeling: Conservative labeling using conformal prediction

* Adaptive Boosting: AdaBoost-style weight updates


📊 Output
* Real-time accuracy tracking

* Drift point detection and visualization

* Ensemble performance monitoring

* Interactive accuracy plot with drift points marked
  

🎯 Parameter Configuration Guide
Parameter	Description	Recommended Value
W_size:‌  	Sliding window size	100-300
M:      	Number of base models	5-15
p_value_threshold:	Pseudo-label confidence	0.8-0.95
label_percentage:	Available labels	0.05 (5%)-- 0.15 (15%)
drift_delta:    	Drift sensitivity	0.001-0.01



 📞 Contact
If you have any questions, please feel free to contact me:
Email: sh.khezri@pnu.ac.ir, shirin.khezri@gmail.com

