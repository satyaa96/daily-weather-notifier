# daily-weather-notifier

# ☁️ Daily Weather Notification System

A serverless application that sends personalized **daily weather updates via SMS** using **AWS Lambda**, **Amazon SNS**, and **EventBridge**, with real-time data fetched from the **OpenWeatherMap API**.

---

## 📌 Features

- ☀️ Retrieves current weather data for a given city
- 📱 Sends SMS notifications with temperature and conditions
- ⏰ Automatically runs every morning using scheduled AWS events
- 💡 Fully serverless — no infrastructure management
- 💰 Low-cost and free-tier friendly

---

## 🛠️ Built With

- **AWS Lambda** – Executes backend logic on demand
- **Amazon SNS** – Sends SMS messages to users
- **Amazon EventBridge** – Schedules daily execution
- **OpenWeatherMap API** – Provides real-time weather data
- **AWS IAM** – Handles secure access and permissions
- **Amazon CloudWatch** – Logs function activity for monitoring

---

## 📷 Screenshots

| Lambda Setup | Weather Notification |
|--------------|----------------------|
| ![Lambda](screenshots/lambda_setup.png) | ![SMS](screenshots/sms_received.png) |

---

## 📁 Project Structure


---

## ⚙️ Environment Variables

These variables must be set in your Lambda function configuration:

| Variable | Description |
|----------|-------------|
| `CITY` | City name (e.g., `Vijayawada`) |
| `PHONE_NUMBER` | Target phone number in E.164 format (e.g., `+919876543210`) |
| `WEATHER_API_KEY` | OpenWeatherMap API Key |

Use a `.env.example` to document your structure locally.

---

## 🚀 Deployment Steps

1. Create a Lambda function and name it `DailyWeatherNotifier`
2. Upload your `lambda_function.py` as a `.zip` file
3. Add required environment variables in configuration
4. Assign IAM role with:
   - `AmazonSNSFullAccess`
   - `CloudWatchLogsFullAccess`
5. Set up an **Amazon EventBridge** rule with a cron expression (e.g., `cron(30 1 * * ? *)` for 7:00 AM IST)
6. Test the function and receive SMS updates

---

## 🧠 Learnings

This project highlights:

- Real-world API integration
- Cloud automation with EventBridge
- Building event-driven, serverless apps
- Practical use of IAM and observability tools

---

## 🧩 Future Enhancements

- 🌍 Location-based dynamic city detection
- 📨 Email or push notification support
- 🌐 Multi-language message customization
- 🤖 Weather-based smart task automation

---

## 👨‍💻 Author

**P. Satya Sai Pavan Kumar**  
B.Tech CSE (Hons.), K L University  


---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
