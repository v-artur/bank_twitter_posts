# bank_twitter_posts

Supplementary data for the paper *insert paper name later*

## How to Cite

```
@article{gombos2024bank,
  title={},
  author={Gombos, Nóra Julianna and Biró Szigeti, Szilvia and Molontay, Roland and Vlaszov, Artúr},
  journal={},
  volume={},
  number={},
  pages={},
  year={2024},
  publisher={}
}
```
## Remarks for the graphs

The words "popular" and "non-popular" refer to the binary label of the tweet that we defined in the paper. Shortly: a tweet of a certain account is labelled "popular", if the amount of likes on it is in the top 5% of the amounts of likes from the prior 50 and subsequent 50 tweets of the same account. All other tweets are labeled "non-popular".

In order to reduce heterogeneity, we decided to also repeat the analyses on a *reduced dataset*. We reduced the dataset to only contain the tweets of the 4 most followed accounts (belonging to 3 banks, Bank of America having two separate accounts in the list), which were uploaded between 2020-01-01 and 2022-12-31.

The graphs are based on 4 different slices of the full dataset:
- "all tweets": all of the scraped tweets
- "tweets with images": the tweets from which we could succesfully acquire the image(s)
- "top 4 accounts, all tweets": all tweets from the *reduced dataset* as described above
- "top 4 accounts, tweets with images": same as "tweets with images", except from the *reduced dataset* as described above

## Description and explanation for each graph
- 

## Source

The data is scraped using a [snscrape API](https://github.com/JustAnotherArchivist/snscrape), and it consists of all posts starting from January 1st, 2012 to December 31st, 2022 posted by the following 31 Twitter pages of NA banks:
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


## Summary of Data

| Feature | Type | Description |
|----------------------|-------------------------------|--------------------------------------------------------|
| sample | sample | sample |
