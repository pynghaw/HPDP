# Real-Time Sentiment Analysis of Malaysian E-Wallet Reviews

---
## 🚀 Project Overview

This project implements a **real-time sentiment analysis pipeline** for user reviews of popular Malaysian e-wallet and e-commerce applications (Touch 'n Go, Boost, Grab, Setel, Shopee) from the Google Play Store. Leveraging the power of **Apache Kafka** for data ingestion and **Apache Spark Streaming** for real-time processing and sentiment prediction, the system provides immediate insights into public opinion. The results are visualized through an interactive **Streamlit dashboard**.

The primary goal is to extract, process, analyze, and visualize sentiments from digital media in real-time, enabling organizations to make data-driven decisions swiftly.

---

## 📂 Project Documentation
<div align="center">



| Document Type          | Link |
|------------------------|------|
| 📄 **Final Report**     | [<img src="https://cdn-icons-png.flaticon.com/512/337/337946.png" width="40" alt="PDF"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/final_report.pdf) |
| 📄 **Final Report (Turnitin)**     | [<img src="https://cdn-icons-png.flaticon.com/512/337/337946.png" width="40" alt="PDF"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/Turnitin_FinalProject_DataDrillers.pdf) |
| 📊 **Presentation Slides** | [<img src="https://cdn-icons-png.flaticon.com/512/888/888882.png" width="40" alt="PPTX"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/presentation_slides.pptx) |
| 🎬 **Presentation Video** | [<img src="https://cdn-icons-png.flaticon.com/512/3670/3670147.png" width="40" alt="YouTube"/>](https://youtu.be/7pEr9hx8oP4) |
| 📂 **Raw Data**         | [<img src="https://github.com/user-attachments/assets/3ee1c27e-9bd6-4b2e-b54b-7fd597879591" width="40" alt="Excel CSV"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/data/e_wallet_reviews.zip) |
| 🧹 **Cleaned Data**     | [<img src="https://github.com/user-attachments/assets/3ee1c27e-9bd6-4b2e-b54b-7fd597879591" width="40" alt="Excel CSV"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/data/cleaned_reviews.csv) |
| ⚙️ **Preprocessing**    | [<img src="https://cdn-icons-png.flaticon.com/512/5968/5968350.png" width="40" alt="Colab"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/notebooks/preprocessing.ipynb) |
| 🤖 **Model Training**   | [<img src="https://cdn-icons-png.flaticon.com/512/5968/5968350.png" width="40" alt="Colab"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/notebooks/model_training.ipynb) |
| ⚡ **Kafka & Spark Pipeline** | [<img src="https://cdn-icons-png.flaticon.com/512/1006/1006363.png" width="40" alt="Pipeline"/>](https://github.com/drshahizan/HPDP/tree/main/2425/project/p2/DataDrillers/kafka_spark_pipeline) |
| 📊 **Dashboard**        | [<img src="https://streamlit.io/images/brand/streamlit-mark-color.png" width="40" alt="Streamlit"/>](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/dashboard/streamlit_dashboard.py) |


</div>

---

## 👥 Group B - Data Drillers

| No | Name                           | Matric No   |
|----|--------------------------------|-------------|
| 1  | Muhammad Anas Bin Mohd Pikri   | A21SC0464   |
| 2  | Mulyani Binti Saripuddin       | A22EC0223   |
| 3  | Aliatul Izzah Binti Jasman     | A22EC0136   |
| 4  | Thevan Raju A/L Jeganath       | A22EC0286   |

---

## ✨ Key Features

- ✅ **Live review scraping in Bahasa Melayu**
- ✅ **Streams reviews to Kafka every 60 seconds**
- ✅ **Uses pre-trained LSTM model to classify sentiment**:
  - Positive 😊
  - Neutral 😐
  - Negative 😠
- ✅ **Real-time interactive dashboard with**:
  - 📊 **Pie chart for sentiment distribution**
  - 📈 **Line chart showing sentiment over time**
  - ☁️ **Word cloud per sentiment**
  - 📋 **Table with latest 20 reviews**
  - 🔍 **Filters by app, sentiment and date**
---


## 🎯 Target Applications

The sentiment analysis focuses on user reviews for the following popular Malaysian e-wallet and e-commerce applications:

| App Name     | Package Name                |
| :----------- | :-------------------------- |
| Touch 'n Go  | `my.com.tngdigital.ewallet` |
| Boost        | `my.com.myboost`            |
| Grab         | `com.grabtaxi.passenger`    |
| Setel        | `com.setel.mobile`          |
| Shopee Pay   | `com.shopeepay.my`          |

---

## 🧠 Project Architecture
<div align="center">
   
![Architecture Diagram](https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/ArchitectureDiagram.png)<br>
*The architecture diagram illustrates the real-time data flow from Google Play reviews through Kafka and Spark to a live dashboard.*

</div>

---

## 🧰 Technologies Used

| Technology             | Description                                       |
|------------------------|---------------------------------------------------|
| Apache Kafka       | Real-time streaming platform                      |
| Apache Spark       | Structured streaming for processing data         |
| TensorFlow (LSTM)  | Pre-trained model for sentiment classification    |
| **Google Play Scraper**| Tool for scraping app reviews                     |
| Streamlit          | Web-based dashboard to visualize live analytics   |
| Python             | Programming language used for all components      |

---

## ⚙️ System Architecture

The pipeline consists of three main stages:

1.  **Data Acquisition (Kafka Producers)**: A Python script continuously scrapes new reviews from the Google Play Store and publishes them as JSON messages to a Kafka topic.
2.  **Real-Time Processing (Spark Streaming)**: An Apache Spark Structured Streaming application consumes messages from Kafka, preprocesses the review text, applies the trained LSTM sentiment model, and outputs the classified sentiments.
3.  **Visualization (Streamlit Dashboard)**: An interactive Streamlit application reads the processed sentiment data and displays real-time metrics, charts, and the latest reviews.



---

## 🚀 Getting Started

Follow these steps to set up and run the Real-Time Sentiment Analysis pipeline.

### Prerequisites

* **Java Development Kit (JDK 8 or newer)**: Required for Kafka and Spark.
    * [Download OpenJDK](https://openjdk.org/install/)
* **Apache Kafka**: Download the latest stable release.
    * [Download Kafka](https://kafka.apache.org/downloads) (Choose a binary download).
* **Apache Spark**: Download a pre-built package for Hadoop 3.3 or similar.
    * [Download Spark](https://spark.apache.org/downloads.html)
* **Python 3.7+**:
    * [Download Python](https://www.python.org/downloads/)
* **Python Libraries**:
    ```bash
    pip install kafka-python google-play-scraper tensorflow pandas scikit-learn numpy streamlit plotly nltk emoji regex
    ```
    (Ensure you download NLTK stopwords: `python -c "import nltk; nltk.download('stopwords')"`)

### Setup Steps

1.  **Extract Apache Kafka & Spark**:
    Unzip the downloaded Kafka and Spark archives to your desired directories (e.g., `C:\kafka`, `C:\spark` on Windows, or `/opt/kafka`, `/opt/spark` on Linux/macOS).

2.  **Set Environment Variables**:
    * Set `JAVA_HOME` to your JDK installation path.
    * Set `KAFKA_HOME` to your Kafka installation path.
    * Set `SPARK_HOME` to your Spark installation path (e.g., `C:\spark\spark-3.5.1-bin-hadoop3`).
    * Add `%KAFKA_HOME%\bin\windows` (Windows) or `$KAFKA_HOME/bin` (Linux/macOS) to your system's `PATH`.
    * Add `%SPARK_HOME%\bin` (Windows) or `$SPARK_HOME/bin` (Linux/macOS) to your system's `PATH`.
    * **Windows Specific**: If on Windows, you might need `winutils.exe` for Hadoop compatibility with Spark. Download it and place it in a `bin` folder (e.g., `C:\hadoop\bin`) and set `HADOOP_HOME` to `C:\hadoop`.

3.  **Download Model Artifacts**:
    Ensure you have the trained model artifacts (`sentiment_lstm_model.h5`, `tokenizer.pkl`, `label_encoder.pkl`) in your project's `models/` directory or ensure `spark_kafka_consumer.py` points to their correct local path. These are generated from `model_training.ipynb`.

### Running the Pipeline

1.  **Start Zookeeper (Kafka Prerequisite)**:
    Open a new terminal/command prompt, navigate to your Kafka directory, and run:
    * **Windows**: `.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties`
    * **Linux/macOS**: `bin/zookeeper-server-start.sh config/zookeeper.properties`

2.  **Start Kafka Broker**:
    Open *another* new terminal/command prompt, navigate to your Kafka directory, and run:
    * **Windows**: `.\bin\windows\kafka-server-start.bat .\config\server.properties`
    * **Linux/macOS**: `bin/kafka-server-start.sh config/server.properties`

3.  **Create Kafka Topic**:
    Open *another* new terminal/command prompt, navigate to your Kafka directory, and run to create the `review_topic`:
    * **Windows**: `.\bin\windows\kafka-topics.bat --create --topic review_topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1`
    * **Linux/macOS**: `bin/kafka-topics.sh --create --topic review_topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1`

4.  **Run the Full Pipeline Orchestrator**:
    Open your project's root directory in a new terminal/command prompt and run:
    ```bash
    python src/run_all_pipeline.py
    ```
    This script will sequentially launch:
    * The Kafka Live Producer (`kafka_live_producer.py`) to start scraping and sending reviews.
    * The Spark Kafka Consumer (`spark_kafka_consumer.py`) to process the stream.
    * The Streamlit Dashboard (`streamlit_dashboard.py`) for visualization.

    **Note**: There are `time.sleep()` calls in `run_all_pipeline.py` to allow components to start up properly.

---

## 📊 Dashboard Visualization

<div align="center" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">

<div style="width: 45%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/dashboard1.jpg" width="60%"><br>
<em>Interactive dashboard interface with sentiment distribution and trend analysis components.</em>
</div>

<div style="width: 45%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/dashboard2.png" width="60%"><br>
<em>Detailed metrics view displaying key performance indicators and review statistics.</em>
</div>

<div style="width: 45%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/dashboardshopee.png" width="60%"><br>
<em>The comprehensive dashboard provides real-time sentiment analysis.</em>
</div>

<div style="width: 30%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/positiveshopee.png" width="60%"><br>
<em>Positive sentiment analysis</em>
</div>

<div style="width: 30%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/neutralshopee.png" width="60%"><br>
<em>Neutral sentiment analysis</em>
</div>

<div style="width: 30%;">
<img src="https://github.com/drshahizan/HPDP/blob/main/2425/project/p2/DataDrillers/reports/images/negativeshopee.png" width="60%"><br>
<em>Negative sentiment analysis</em>
</div>

</div>

### 🖥️ Dashboard Usage
Once `run_all_pipeline.py` is executed, the Streamlit dashboard will automatically open in your web browser (usually at `http://localhost:8501`).

- Use the **sidebar filters** to select specific applications or date ranges
- View **Key Sentiment Measures** for quantitative insights
- Examine **Sentiment Distribution** via interactive pie chart
- Track **Sentiment Trends** with time-series visualization
- Explore **Latest Reviews** for qualitative feedback

---

## 📈 Optimization & Future Work

We've explored several areas for improvement:

### Sentiment Model Enhancements

* **N-grams & Lexicon-based Features**: For Naive Bayes, capturing multi-word expressions and leveraging sentiment lexicons.
* **Hyperparameter Tuning & Advanced Embeddings**: For LSTM, refining `maxlen`, LSTM units, dropout rates, and exploring pre-trained word embeddings (e.g., Word2Vec, GloVe, FastText, or even Malay-specific BERT models) for richer contextual understanding.
* **Model Quantization**: To reduce model size and inference time for real-time deployment.

### Architecture Improvements

* **Kafka Optimization**: Increased topic partitioning, fine-tuning producer settings (e.g., `linger.ms`, `batch.size`), and ensuring adequate replication factors.
* **Spark Streaming Tuning**: Optimizing resource allocation (`spark.executor.memory`, `spark.executor.cores`, `spark.executor.instances`, `spark.default.parallelism`), adjusting micro-batching intervals, and exploring **Pandas UDFs** for vectorized operations.
* **Advanced Output Sinks**: Transitioning from console/CSV output to **Elasticsearch** or **Apache Druid** for true real-time indexing, querying, and dashboarding.
* **Fault Tolerance & Scalability**: Implementing robust checkpointing in Spark, horizontal scaling of Kafka brokers and Spark workers, and considering distributed NoSQL databases for data persistence.

### Broader Future Directions

* **Increased Data Sources**: Incorporating data from other social media platforms (X/Twitter, Facebook, local forums).
* **Multimodal Sentiment Analysis**: Integrating non-textual cues like emojis or image content.
* **Advanced Dashboard Capabilities**: Adding predictive analytics, anomaly detection with alerting, and more interactive drill-down features.
* **Aspect-Based Sentiment Analysis**: Delving deeper into what specific features of the e-wallets users are expressing sentiment about.

---

