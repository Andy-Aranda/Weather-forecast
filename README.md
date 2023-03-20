# Weather forecast 🌤️
This is a Python program that uses a weather API to send daily hourly weather forecasts to your cellphone. The program is designed to send information for the city in which you are located.




<img src = "https://i.imgur.com/1OMDChQ.png" data-cannonical-src = "https://i.imgur.com/1OMDChQ.png" height="700" position="center"/>

## How it works 🤔
The program uses the [Weather API](https://www.weatherapi.com/) to obtain hourly weather forecasts for the city in which you are located. The information is extracted from the API and then filtered to obtain only the information that is to be sent. Then, [Twilio](https://www.twilio.com/) is used to send the information to the user's cellphone.

In addition, the program is set up to run daily. This is accomplished using [Amazon EC2](https://aws.amazon.com/), which allows scheduling the program execution at a specific time every day.

## Requirements 🚀
To use this program, you will need the following:
- A Twilio account to send text messages
- An Amazon EC2 account to schedule daily sending
- Python 3.6 or higher
- The following Python libraries:
    - twilio 7.14.0
    - pandas 1.3.4
    - requests 2.22.0
    - tqdm 4.62.3

## Setup ⚙️
Before you can use the program, you need to perform the following setup steps:

1. Obtain a Twilio account and set it up to send text messages.
2. Obtain an Amazon EC2 account and set it up to run the program daily.
3. Obtain an API key from the weather API you want to use.
4. Clone or download the GitHub repository and open the `twilio_config.py` file.
5. Set the `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, `TWILIO_PHONE_NUMBER`, `DESTINATION_PHONE_NUMBER` variables with your Twilio account values and source and destination phone numbers.
6. Set the `API_KEY` variable with your weather API key.
7. Set the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` variables with your Amazon EC2 account access keys.

## Usage 💻
Once you have completed the setup, you can run the program going to the folder in which is, using `python3 twilio_script.py` in MacOS or `py twilio_script.py` in Windows.

The program will send a text message with the hourly weather forecast for the city in which you are located. It will also automatically execute every day at the time you have scheduled in Amazon EC2.