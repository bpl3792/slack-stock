### Bot to report stock price to any Slack channel 
Runs on Google App Engine

Steps to configure:

1. Create Google App Engine project: `https://https://console.developers.google.com`
1. Call it whatever you want. Your integration point for slack would be `http://<project-id>.appspot.com/price/<ticker>`
1. Clone this repository
1. Run `pip install -r requirements.txt -t lib/ in app subdirectory`
1. Run `deploy.sh`
1. Test with curl: `curl -X POST -H "Content-Length: 0" http://<project-id>.appspot.com/price/AAPL`
1. Go to Integrations configuration in your Slack account
1. Configure the above URL as Outgoing Webhook
