# 🚀 Semi-Supervised Machine Learning Approach for DDoS Detection


## 📌 Project Overview
This project implements a **Semi-Supervised Machine Learning** approach to detect **Distributed Denial-of-Service (DDoS) attacks** efficiently. By leveraging both labeled and unlabeled data, the model improves its accuracy while reducing dependency on fully labeled datasets.

## 🔥 Key Features
✅ **Semi-Supervised Learning** - Uses both labeled and unlabeled data for better detection accuracy.  
✅ **Anomaly Detection** - Identifies abnormal network traffic patterns.  
✅ **Real-time Analysis** - Processes incoming traffic in real-time.  
✅ **Scalable & Efficient** - Works with large-scale network datasets.  
✅ **Robust Against Evasion** - Adaptable to evolving attack patterns.  

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
   Place the datasets (NSL-KDD, UNSW-NB15, UNBISCXIDS2012) in a folder like data/ (update paths in code if needed).
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
🔹 **Integration with Deep Learning models** for improved detection accuracy.  
🔹 **Real-time deployment** in network security environments.  
🔹 **Adaptive Learning** to counter evolving attack patterns.  

## 🤝 Contributions
Contributions are welcome! Feel free to fork this repo, submit pull requests, or report issues. Let's collaborate to improve DDoS detection. 😊
