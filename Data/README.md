# Data for the MSAI6320 Unit 4 lab

`train.csv`, `dev.csv` and `test_public.csv` come from **Twitter US Airline Sentiment**
(Crowdflower / Figure Eight, Feb 2015), via
https://huggingface.co/datasets/osanseviero/twitter-airline-sentiment, listed there under
CC BY-NC-SA 4.0. Changes: duplicates removed, new random ids, only `text` and `label` kept,
stratified 70/15/15 split with seed 42. These files are shared under the same license.

`sentiment_lexicon.csv` is a small word list written for this lab.
