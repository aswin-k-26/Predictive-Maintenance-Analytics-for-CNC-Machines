# Predictive Maintenance Analytics for CNC Machines (S.P.O.T – Fix-It-Bot)

An IoT + AI based predictive maintenance assistant designed to monitor CNC machines in real-time using an ESP32 microcontroller and multiple sensors. The system detects anomalies and predicts possible failures to enable proactive maintenance, reducing downtime and improving productivity.

---

## 🚀 Project Overview
**S.P.O.T (Fix-It-Bot)** continuously captures key machine health parameters such as:
- Temperature
- Vibration
- Sound levels
- Current consumption

These signals are transmitted to the cloud for logging and real-time visualization, while a **Random Forest ML model** analyzes the sensor patterns to identify faults and predict failure probability.

✅ Real-time alerts via dashboard + UI  
✅ Local alert system using buzzer + LEDs  
✅ Scalable and cost-effective predictive maintenance solution  

---

## 🎯 Problem Statement
In industrial CNC environments, unexpected breakdowns cause:
- High downtime
- Production delays
- Increased maintenance cost

This project predicts failures early using IoT sensor data and machine learning, helping operators take preventive actions before breakdown occurs.

---

## ✅ Key Features
- Real-time monitoring of CNC machine health
- Multi-sensor data acquisition using ESP32
- Cloud logging with timestamped data
- Visualization of sensor trends and machine health %
- Random Forest based anomaly detection & fault prediction
- Alerts using:
  - Mobile dashboard / UI
  - Buzzer & LEDs (local alerts)

---

## 🛠️ Hardware Components
| Component | Purpose |
|----------|---------|
| ESP32 | Main microcontroller |
| DS18B20 | Temperature monitoring |
| ADXL345 | Vibration monitoring |
| LM393 Sound Sensor | Acoustic anomaly detection |
| ACS712 | Current monitoring |
| Stepper Motor + Scrap DVD | CNC machine prototype model |
| LEDs + Buzzer | Real-time local alerts |

---

## 💻 Software Components
- **Arduino IDE** – ESP32 programming
- **Google Colab** – Dataset preprocessing + model training
- **Random Forest Model** – ML algorithm for anomaly detection
- **ThingSpeak** – Cloud dashboard for visualization
- **Google Sheets + Apps Script** – Data logging & timestamping
- **Firebase** – Storage + mobile dashboard integration

---

## 📊 System Architecture / Block Diagram (Flow)
1. Sensors collect CNC health parameters (temp, vibration, sound, current)
2. ESP32 formats the data and transmits it
3. Data is logged into Google Sheets using Apps Script
4. Random Forest model analyzes data for anomalies
5. Dashboard shows graphs + machine health status
6. Buzzer & LEDs alert operators in real time

---

## ⚙️ Working
1. **Data Acquisition:** ESP32 reads sensor values continuously  
2. **Cloud Upload:** JSON payload sent to Google Sheets  
3. **ML Analysis:** Random Forest model trained using historical patterns  
4. **Prediction:** Detects anomalies such as vibration spikes, load rise, temperature increase  
5. **Alerts + Visualization:**  
   - ThingSpeak dashboard displays real-time graphs  
   - LEDs + buzzer give on-site alert  

---

## 🤖 Machine Learning Model
**Algorithm:** Random Forest (Ensemble Learning)

**Input Features:**
- Vibration values
- Spindle load/current levels
- Temperature
- Acoustic/sound levels

**Output:**
- Fault probability
- Machine condition (Normal / Warning / Fault)

### Why Random Forest?
- High accuracy in classification tasks
- Reduced overfitting
- Works well with industrial multi-sensor data
- Reliable prediction for diverse conditions

---

## 📌 Applications
- Predictive maintenance in CNC / industrial machines
- Tool health monitoring
- Remote monitoring for manufacturing units
- Data-driven maintenance planning
- Educational & research use for IoT + AI systems

---

## 🌟 Future Enhancements
- Add edge ML inference directly on ESP32
- Train with larger real industrial dataset
- SMS/Email alerts for faults
- Predict failure location/tool wear classification
- Deploy model using TensorFlow Lite (TinyML)
