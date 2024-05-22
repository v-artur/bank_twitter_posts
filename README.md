# bank_twitter_posts

Supplementary data for the paper *insert paper name later*

## How to Cite

## Remarks for the graphs

The words "popular" and "non-popular" refer to the binary label of the tweet that we defined in the paper. Shortly: a tweet of a certain account is labelled "popular", if the amount of likes on it is greater than the mean plus two standard deviations of the amount of likes from the prior 50 and subsequent 50 tweets of the same account. All other tweets are labeled "non-popular".
The other variant of target variable is referred to as the "continuous target variable" or "continuous label", and is calculated similarly, except instead of checking whether the amount of likes is greater than the mean plus the double of the standard deviation, we measure "how many standard deviations away" the number of likes on the post is from the average in the 50-50 window.

In order to reduce heterogeneity, we decided to also repeat the analyses on a *reduced dataset*. We reduced the dataset to only contain the tweets of the 4 most followed accounts (belonging to 3 banks, Bank of America having two separate accounts in the list), which were uploaded between 2020-01-01 and 2022-12-31.

The graphs are based on 4 different slices of the full dataset:
- "all tweets": all of the scraped tweets
- "tweets with images": the tweets from which we could succesfully acquire the image(s)
- "top 4 accounts, all tweets": all tweets from the *reduced dataset* as described above
- "top 4 accounts, tweets with images": same as "tweets with images", except from the *reduced dataset* as described above

## Description and explanation for each graph
- **NA_daily_freq_of_tws**: each dot represents the amount of tweets posted on a certain day by all of the banks. The color of the dot represents whether the tweet was posted on a weekday or on the weekend.
- **OCR_caption_object_illustration**: this image illustrates the result of the OCR (optical character recognition), image captioning, color retrieving and object detection, including the image output with the bounding boxes. We listed the detected objects with their confidence score, printed the generated caption and the detected words below the image, along with the color class ratios received from the masking with the appropriate HSV ranges. In this case the OCR was slightly confused by the unique font and design of the small text in the bottom-right corner.
- **OCR_caption_object_illustration_2**: this is just another illustration of the same operations, except it also illustrates the accuracy of Keras-OCR in case of a more structured text.
- **Sentiments and topics**: this image illustrates the topic- and sentiment analysis results on 3 tweets, specifically chosen to showcase all of the 3 sentiments and different topics. The first example illustrates the "nature" of posts that are labeled negative really well, specifically here the bank warns users about scam methods.
- **all_mi_b_norm**: this graph shows the normalized mutual information between the common variables of all tweets and the binary popularity label.
- **all_mi_c**: this graph shows the estimated (not normalized) mutual information between the common variables of all tweets and the continuous target variable.
- **bank_daily_activity**: the top graph shows the amount of posts that were posted by each bank on each day of the week in the whole time interval. The bottom graph shows the median amount of likes received for the posts posted on certain weekdays by the banks. The banks are ordered from left to right based on their follower count in a descending way.
- **colors_likes_rt_reply**: this graph shows the mean and median amount of likes, replies and retweets depending on the dominant color in the image attached to the tweet. The bars of specific colors represent the mean and median values of interactions among the posts where the ratio of the specific color was the highest.
- **dominant_colors_in_sentimens**: this graph shows the distribution of the dominant colors among posts of the specific sentiment. A bar represents how many tweets with the appropriate sentiment had the highest ratio of the color of the bar.
- **img_mi_b_norm**: same as *all_mi_b_norm*, except for tweets with images.
- **img_mi_c**: same as *all_mi_c*, except for tweets with images.
- **media_type_emoji_amount_per_bank**: for each bank, the first 3 bars show the amount of tweets they posted with no media, only image(s) and only video(s) respectively. The fourth bar shows the amount of tweets where the bank used an emoji. The banks are once again sorted in the order of their follower count decreasing.
- **monthly_bank_activity**: on this graph each bank has a separate line of dots, where the size of the dot depends on the amount of tweets that the bank posted in that given month. The larger the dot, the more tweets were posted in that specific month by the bank.
- **nmf_word_distr**: this graph shows the top 10 key words for each topic with the height of the bar representing the number of the word's appearances within the topic. The one odd subgraph in the beginning of the second row shows the amount of tweets in each topic, in a decreasing order.
- **sent_amount_per_bank**: this graph shows the amount of posts with each sentiment from each bank. The banks are in the usual order.
- **sent_distr_bars**: the subgraphs on the top show the amount of tweets with each sentiment posted in each year, the top-right subgraph including only the tweets labeled popular. The bottom row shows the "normalized" variants of the top row, that is, the ratio of tweets with the different sentiments in each year.
- **sent_ratio_per_bank**: this graph shows the ratio of the different sentiments in the tweets posted by each bank.
- **stat_all_length_hist**: this graph shows the empirical histograms of the raw lengths of all tweets (popular on the left, non-popular on the right subgraph), with 10 bins.
- **stat_all_sent_hist**: this graph shows the empirical distribution of the sentiments among all tweets (popular on the left, non-popular on the right subgraph).
- **stat_all_topic_hist**: this graph shows the empirical distribution of the topics among all tweets (popular on the left, non-popular on the right subgraph).
- **stat_img_length_hist**: the same as *stat_all_length_hist* except for tweets with images.
- **stat_img_sent_dist**: the same as *stat_all_sent_hist* except for tweets with images.
- **stat_img_topic_dist**: the same as *stat_all_topic_hist* except for tweets with images.
- **stat_top4_all_length_hist**: the same as *stat_all_length_hist* except for all tweets on the *reduced dataset*.
- **stat_top4_all_sent_hist**: the same as *stat_all_sent_hist* except for all tweets on the *reduced dataset*.
- **stat_top4_all_topic_hist**: the same as *stat_all_topic_hist* except for all tweets on the *reduced dataset*.
- **stat_top4_img_length_hist**: the same as *stat_img_length_hist* except for tweets with images on the *reduced dataset*.
- **stat_top4_img_sent_hist**: the same as *stat_img_sent_dist* except for tweets with images on the *reduced dataset*.
- **stat_top4_img_topic_hist**: the same as *stat_img_topic_dist* except for tweets with images on the *reduced dataset*.
- **top4_all_mi_b_norm**: the same as *all_mi_b_norm* except for all tweets on the *reduced dataset*.
- **top4_all_mi_c**: the same as *all_mi_c* except for all tweets on the *reduced dataset*.
- **top4_img_mi_b_norm**: the same as *img_mi_b_norm* except for tweets with images on the *reduced dataset*.
- **top4_img_mi_c**: the same as *img_mi_c* except for tweets with images on the *reduced dataset*.

## Summary table of statistical tests - "stat tests summary.xlsx"

In this large table we collected 4 summary tables of all statistical tests.

The first table contains the results of two tests, Welch t-tests regarding the mean of the continuous target depending on the category of a variable, and the correlation tests of continuous variables with the same target. These two cases are collected together, because they both measure the effect of a variable on the value of the continuous target. For a continuous variable, the correlation shows whether an increase in its value increases or decreases the target value. For categorical features, we check for each category, whether the mean of the target is greater or smaller among the tweets labeled with that category, versus among all other tweets. For binary features we obviously checked the case when the value is 1. The rows are colored depending on the significance of the test statistics. A row is colored green, if the test statistic is significant both on the full- and the reduced dataset. It is blue if only the full dataset case is significant, magenta if only the reduced case is significant. The row is white if neither of the cases showed significant connection.
The different columns are:

- **var (category)**: name of the continuous variable or in case of categorical features, the name of the variable combined with the specific category.
- **data slice**: whether the feature is tested on all tweets or just the tweets with images.
- **var type**: type of the variable (continuous, binary, categorical).
- **category size**: number of tweets with the specific category in the given variable, or number of all tweets in case of cont. features.
- **top4 category size**: same as the previous, except only for the *reduced dataset*.
- **cardinality**: the number of different categories for the original feature, or in case of continuous variables, the number of tweets.
- **top4 cardinality**: same as the previous, except only for the *reduced dataset*.
- **mean of cont. target by category**: mean of the continuous target among tweets belonging to the specific category.
- **top4 mean of cont. target by category**: same as the previous, except only for the *reduced dataset*.
- **cont. target mean of the rest/ correlation with cont. target**: mean of the continuous target among the rest of the tweets or in case of continuous variables the correlation between the variable and the target.
- **top4 cont. target mean of the rest/ correlation with cont. target**: same as the previous, except only for the *reduced dataset*.
- **is the mean greater in the category? / is the correlation positive?**: binary indicator of whether the mean is greater in the specific category, or in case of continuous variables, whether the correlation is positive.
- **top4 is the mean greater in the category? / is the correlation positive?**: same as the previous, except only for the *reduced dataset*.
- **Welch/corr. test p_value**: p-value of the appropriate test.
- **top4 Welch/corr. test p_value**: same as the previous, except only for the *reduced dataset*.
- **significant difference in target mean/correlation**: indicator, whether the p-value is less or equal to 0.05.
- **top4 significant difference in target mean/correlation**: same as the previous, except only for the *reduced dataset*.


## Data scraping and the accounts of the 31 banks

The data was scraped using a [snscrape API](https://github.com/JustAnotherArchivist/snscrape) (doesn't work anymore unfortunately), and it consists of all posts starting from January 1st, 2012 to December 31st, 2022 posted by the 31 Twitter pages of North American banks listed below. We only included organic tweets, that is, we excluded the tweets which were either simple retweets or were quoted by the bank.
- @BankFAB: https://twitter.com/BankFAB
- @PCFinancial: https://twitter.com/PCFinancial
- @TDBank_US: https://twitter.com/TDBank_US
- @BankofAmerica: https://twitter.com/BankofAmerica
- @Citibank: https://twitter.com/Citibank
- @BofA_News: https://twitter.com/BofA_News
- @CitizensBank: https://twitter.com/CitizensBank
- @fvbankus: https://twitter.com/fvbankus
- @usbank: https://twitter.com/usbank
- @FifthThird: https://twitter.com/FifthThird
- @RegionsBank: https://twitter.com/RegionsBank
- @Chase: https://twitter.com/Chase
- @TruistNews: https://twitter.com/TruistNews
- @USAA: https://twitter.com/USAA
- @BNYMellon: https://twitter.com/BNYMellon
- @Ally: https://twitter.com/Ally
- @BMO: https://twitter.com/BMO
- @GoldmanSachs: https://twitter.com/GoldmanSachs
- @MandT_Bank: https://twitter.com/MandT_Bank
- @WellsFargo: https://twitter.com/WellsFargo
- @Netspend: https://twitter.com/Netspend
- @TangerineBank: https://twitter.com/TangerineBank
- @fidelitybankplc: https://twitter.com/fidelitybankplc
- @SVB_Financial: https://twitter.com/SVB_Financial
- @CapitalOne: https://twitter.com/CapitalOne
- @SallieMae: https://twitter.com/SallieMae
- @RBC: https://twitter.com/RBC
- @FrostBank: https://twitter.com/FrostBank
- @CreditOneBank: https://twitter.com/CreditOneBank
- @cibc, https://twitter.com/cibc
- @TD_Canada: https://twitter.com/TD_Canada
