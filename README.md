# Data-Wrangling-for-WeRateDogs
This is the assignment for Data Wrangling module of Udacity's Data Analyst Nanodegree Programme.

The dataset used in this assignment is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

My goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

## The Data
In this project, I will work on the following three datasets.
1. Enhanced Twitter Archive: The WeRateDogs Twitter archive provided by Udacity which was extracted programmatically.
2. Additional Data via the Twitter API: The information like retweet count and favorite count which were omitted in Enhanced Twitter Archive can be gathered by Twitter's API.
3. Image Predictions File: every image in the WeRateDogs Twitter archive was run through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).
![image](https://user-images.githubusercontent.com/72946315/218456687-954f56e9-4a2e-47dd-a8a6-cae0c5b738bc.png)

So for the last row in that table:

- `tweet_id` is the last part of the tweet URL after "status/" → https://twitter.com/dog_rates/status/889531135344209921
- `p1` is the algorithm's #1 prediction for the image in the tweet → **golden retriever**
- `p1_conf` is how confident the algorithm is in its #1 prediction → 95%
`p1_dog` is whether or not the #1 prediction is a breed of dog → **TRUE**
- `p2` is the algorithm's second most likely prediction → **Labrador retriever**
- `p2_conf` is how confident the algorithm is in its #2 prediction → 1%
`p2_dog` is whether or not the #2 prediction is a breed of dog → **TRUE**
- etc.

And the #1 prediction for the image in that tweet was spot on:
![image.png](attachment:image.png)

This is a golden retriever named Stuart.

So that's all fun and good. But all of this additional data will need to be gathered, assessed, and cleaned. This is where I come in.
