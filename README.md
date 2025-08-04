# Daily-Briefing-n8n-Workflow
🗞️ Daily Briefing — n8n Workflow
This project provides an automated Daily Briefing using n8n, which fetches top news headlines and the latest currency exchange rate (USD to PKR). It is a great starting point for building personalized daily updates and automating news and financial info gathering.

**Demo Video**
https://drive.google.com/file/d/1E9y9ac0vXDoWQ3PiPWGiUmv53sJ6UHYR/view?usp=sharing
https://drive.google.com/file/d/1uI647U4kPMAjwCdHdRi-_Zzcdj5loIvo/view?usp=sharing

📌 Overview
This workflow is triggered manually and then performs the following actions:
Retrieves top news headlines from the United States.
Fetches the current USD to PKR currency exchange rate.
Presents the data in a detailed format.

🧩 Workflow Details
Node	Description
When clicking ‘Execute workflow’	Manual trigger node to start the workflow on click.
Daily Briefing	Custom node (using dailyBriefingApi) that fetches detailed news and currency exchange information.

⚙️ Configuration
Prerequisites
An active n8n instance (cloud or self-hosted).
A valid API key for the Daily Briefing API (custom credential configured in n8n).

Setup Steps
Clone this repo or import the workflow JSON directly into your n8n instance.

Create credentials:
Name: Daily Briefing APIs account
Type: Custom API key or OAuth2 (based on your API provider)

Adjust any parameters as needed:
newsCountry: Default is us.
baseCurrency: Default is USD.
targetCurrency: Default is PKR.
newsFormat: Default is detailed.

🚀 Running the Workflow
Open your n8n instance.
Import or create the workflow using the provided JSON.
Click "Execute Workflow".
You’ll get a detailed daily briefing including:
Top news headlines (from the specified country).
Current exchange rate from USD to PKR.

📦 Example Output
json
Copy
Edit
{
  "news": [
    {
      "title": "Tech stocks rally as market opens",
      "source": "CNN",
      "url": "https://cnn.com/article/..."
    },
    ...
  ],
  "currencyExchange": {
    "base": "USD",
    "target": "PKR",
    "rate": "290.45"
  }
}
🛠️ Customization
You can expand this workflow to:

Add weather updates.

Include stock prices or crypto rates.

Push summaries to Slack, Telegram, or email.

Schedule daily execution using a cron trigger instead of manual trigger.

🤝 Contributions
Feel free to fork the repo and open a pull request for improvements, bug fixes, or additional features.

📝 License
This project is open-source under the MIT License.
