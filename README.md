# 🚀 Semi-Supervised Machine Learning Approach for DDoS Detection


## 📌 Project Overview
This project implements a **Semi-Supervised Machine Learning** approach to detect **Distributed Denial-of-Service (DDoS) attacks** efficiently. By leveraging both labeled and unlabeled data, the model improves its accuracy while reducing dependency on fully labeled datasets.

## 🔥 Core Features
✅ **Semi-Supervised ML Approach**
   - **Hybrid Model**: Combines unsupervised co-clustering (for anomaly detection) with supervised Extra-Trees ensemble classifiers (for precise DDoS classification).
   - **Noise Reduction**: Filters irrelevant/normal traffic using entropy estimation and information gain ratio.  

✅ **NLP-Driven Traffic Analysis** 
   - **Text Semantics**: Treats HTTP flows as "text documents" for NLP-based feature extraction.
   - **N-gram & Chi-Square**: Uses N-gram sequences for pattern analysis and chi-square tests for automated feature selection.  

✅ **Real-Time Detection Architecture** 
   - **Sliding Window**: Monitors network traffic entropy over time windows to detect abrupt changes (DDoS indicators).
   - **Dynamic Clustering**: Splits traffic into 3 clusters (normal, attack, mixed) using co-clustering.  

✅ **Multi-Network Compatibility** 
   - Works across enterprise networks, home networks, and 3G/4G mobile networks.  

🚨 **Detection Performance**
- **Accuracy**: Achieves **99.15% malware detectio**n rate (as per the conclusion).
- **Low False Positives**: Only **0.45% false alarm rate**.
- **Novelty**: Detects malware missed by traditional antivirus scanners.

## 🚀 Getting Started
### 📜 Programming Languages:
- Python (backend and frontend)
- HTML, CSS, JavaScript (frontend design)

### 🤖 Machine Learning Frameworks/Techniques:
- **Algorithms**: Co-clustering, Extra-Trees (ensemble classifiers), SVM (mentioned in the conclusion).
- **Feature Selection**: Chi-square test, N-gram sequence analysis.
- **NLP Methods**: Text semantics analysis of HTTP flows treated as documents.

### 📂 Datasets:
- NSL-KDD
- UNBISCXIDS2012
- UNSW-NB15

### ⚙️ Technologies/Tools:
- **Web Framework**: Django
- **Database**: MySQL
- **Visualization Tools**: Column graphs, bar graphs, spline charts (for graphical analysis).
- **System Architecture**: Integration of NLP and semi-supervised ML for DDoS detection.

### 🌟 Additional Notes:
- The implementation uses Django for web interface development and MySQL for data storage.
- The project emphasizes combining unsupervised (co-clustering, entropy estimation) and supervised (Extra-Trees) methods for semi-supervised learning.

## 📦 Installation & Setup
1. **Clone the repository**:
   ```bash
   git clone https://github.com/darshbs/SemiSupervised-DDOS-Detection  
   cd DDOS_ATTACK  
   ```
2. **Set Up Virtual Environment** (Python)
    ```bash
    python -m venv venv  
    source venv/bin/activate  # Linux/Mac  
    venv\Scripts\activate     # Windows  
   ```

3. **Install dependencies**:
Run:
   ```bash
   pip install -r requirements.txt
   ```
4. **Configure MySQL Database**
    1. Create a MySQL database:
    ```bash
    CREATE DATABASE ddos_attack;  
    ```
    2. Update `settings.py`
    ```bash
    DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'ddos_attack',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
         }
      }
      ```
5. **Run Migrations**
   ```bash
   python manage.py makemigrations  
   python manage.py migrate  
   ```
6. **Download Datasets**
   Place the datasets (`NSL-KDD`, `UNSW-NB15`, `UNBISCXIDS2012`) in a folder like data/ (update paths in code if needed).
7. **Start the Django Server**
   ```bash
   python manage.py runserver  
   ```
   Visit `http://localhost:8000` to view the project.

🚨 **Troubleshooting**
- **MySQL Issues**: Ensure `mysqlclient` is installed and credentials match `settings.py`.
- **Missing Dependencies**: Add ML/NLP libraries (e.g., `nltk`, `scikit-learn`) to `requirements.txt`.

## 📊 **Dataset**
The project leverages the following **publicly available network intrusion datasets** for training and evaluation:

**Benchmark Datasets**
- **NSL-KDD**: A refined version of KDDCup99, used for benchmarking anomaly detection algorithms.
- **UNBISCXIDS2012**: Contains realistic traffic traces for evaluating DDoS attack patterns.
- **UNSW-NB15**: Modern dataset with hybrid traffic (normal + attack) for testing against evolving threats.

**Preprocessing & Feature Engineering**
- **Feature Extraction**:
   - N-gram sequences from HTTP flow headers (treated as text documents).
   - Chi-square test for automated feature selection.
- **Normalization**: Min-Max scaling applied to train/test subsets.
- **Data Splitting**: 60% training, 40% testing for model validation.
- **Noise Reduction**: Filtering irrelevant traffic via entropy-based clustering.

**Dataset Availability**
- All datasets are open-source and widely used in intrusion detection research.
- Download links:
   - NSL-KDD
   - UNSW-NB15
   - UNBISCXIDS2012



## 🚀 Future Enhancements
🔹 **Real-Time Processing**
   - Optimize entropy-based sliding window for low-latency detection in high-traffic networks.  
🔹 **Deep Learning Integration**
   - Experiment with LSTM/Transformer models for sequential traffic pattern analysis.  
🔹 **IoT Network Support**
   - Extend detection to IoT devices (e.g., smart home/industrial sensors).  
🔹 **Threat Intelligence Feeds**
   - Integrate live threat data (e.g., VirusTotal API) for dynamic attack signature updates.  

## 👨‍💻 Contributors / Team
✧ **M. Sai Darshan Balaji** - Team Lead, ML/NLP Engineer 
   - Co-clustering, Extra-Trees, NLP feature extraction.

✧ **M. Jaya Krishna Sai** - Backend & System Architect
   - Django setup, MySQL integration, API design.

✧ **T. Amarnath Goud** - Data & Pipeline Enginee
   - Dataset preprocessing (NSL-KDD, UNSW-NB15), entropy analysis.
   
✧ **Md. Ali Ahmad Khurshid** - Frontend & Visualization
   - UI design (HTML/CSS/JS), chart rendering (graphs/spline).
