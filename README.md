Discount Alert Bot
===================

Overview
--------
This bot sends instant notifications when products on supported e‑commerce sites drop to deep discount levels. Users can manage subscriptions directly from Telegram.

Features
--------
* Track multiple e‑commerce sites
* Real‑time price drop alerts
* Simple subscription commands

Local Setup
-----------
1. Install Python 3.11.
2. Clone the repository.
3. Create a virtual environment and install dependencies:
   pip install -r requirements.txt
4. Copy .env.example to .env and insert your bot token.
5. Run the bot:
   python main.py

Free Cloud Deployment (Render)
------------------------------
1. Sign up at render.com and create a new Web Service.
2. Connect your GitHub repository.
3. Set the build command to `pip install -r requirements.txt`.
4. Set the start command to `python main.py`.
5. Add an environment variable `BOT_TOKEN` with your token.
6. Deploy – the service will start automatically.

Free Cloud Deployment (Koyeb)
-----------------------------
1. Sign up at koyeb.com and create a new Service.
2. Choose "Git Repository" as source and link your repo.
3. Set the build command to `pip install -r requirements.txt`.
4. Set the run command to `python main.py`.
5. Add the environment variable `BOT_TOKEN`.
6. Deploy the service.

Usage
-----
* `/start` – welcome message and quick reply keyboard.
* `/help` – list of available commands.
* `/subscribe <site> <product url>` – add a product to watchlist.
* `/unsubscribe <site> <product url>` – remove a product.
* `/list` – show current subscriptions.

The bot stores data in a local SQLite database (`subscriptions.db`). It is lightweight and can be scaled by moving the database to a managed service.
