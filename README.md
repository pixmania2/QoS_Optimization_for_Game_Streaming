Name: HARDIK AGRAWAL
RA No.: RA2211027010007
Section: AD-1
Real-Time QoS Optimization in Game Streaming using Sentiment & Engagement Analysis

Project Overview
    As live game streaming platforms like Twitch and YouTube Gaming experience explosive growth, maintaining consistent Quality of Service (QoS) becomes increasingly challenging. Viewers experience issues like buffering, resolution drops, or latency—all of which can result in dissatisfaction and disengagement.

This project presents an AI-powered, data-driven solution that leverages:

    BERT-based sentiment classification of chat messages

    Engagement scoring based on chat behavior

    A QoS recommendation engine that suggests adaptive bitrate and buffer strategies in real-time

Objectives
    Dynamically understand viewer sentiment from live chats.

    Model viewer engagement beyond just stream metrics.

    Suggest QoS improvements based on real-time chat intelligence.

Dataset
    We used a publicly available dataset of Twitch chat logs, with fields including:

    user: Username of the commenter

    channel: Stream channel name

    message: Actual Twitch chat message (including emotes, slang, symbols)

    timestamp: When the message was posted

    The dataset was manually cleaned and expanded to ~2000 samples for training purposes.

Tech Stack
    Tool	                    Purpose
    Python	                    Core programming language
    HuggingFace Transformers	BERT-based sentiment modeling
    Scikit-learn	            Train-test split & metrics
    Matplotlib/Seaborn	        Data visualization
    Pandas	                    Data processing
    Google Colab	            Model training and notebook execution


Implementation Steps
    1. Preprocessing
        Converted Twitch emotes like PogChamp, LUL, and emojis into readable text.

        Removed URLs, special characters, and lowercased the text.

    2. Sentiment Labeling
        A rule-based keyword matching system was used to auto-label 2000 samples as positive, neutral, or negative.

    3. Sentiment Classification using BERT
        Fine-tuned bert-base-uncased on labeled chat data.

        Achieved high validation performance across 3 sentiment classes.

        Used HuggingFace's Trainer API for training.

    4. Engagement Scoring
        Designed a scoring metric combining:

        Word count

        Presence of emotes or uppercase tokens

        Message length

        Capped final score to a range of 0–10.

    5. QoS Suggestion Engine
        Used a rule-based engine for real-time recommendations:

        Increase Bitrate: Positive sentiment + high engagement

        Reduce Bitrate: Negative sentiment + low engagement

        Pre-buffer: Mixed signals

        Maintain: Stable conditions

Visualizations:
    Sentiment Distribution

    Engagement Score Histogram

    QoS Action Breakdown

These plots help in understanding user behavior trends during streaming.

Key Insights
    Real-time chat data can serve as a reliable proxy for stream experience.

    Combining NLP and behavioral signals gives a more holistic understanding of QoS needs.

    The rule-based engine can easily be replaced with a reinforcement learning system in future work.
