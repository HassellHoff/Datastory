## Impact of Elon Musk quotes on Tesla's stock


### Abstract

Elon Musk is the world's richest person and is famous for gaining attention for his tweets that according to him half are generated while sitting on his toilet. During the recent years his tweets have gathered much attention by their impact on markets which has left investors worried. From jumping the value of cryptocurrencies such as bitcoin and dogecoin to small companies such as Gamestop Elon Musk's tweets have undeniably played a huge impact on moving stock prices of companies. 

It has been claimed that Elon Musk's twitter account could be Tesla's primary marketing tool since Tesla does not invest in marketing at all. The hypothesis of our analysis definately backs this theory. (Add something here)

During our analysis we are going to try to find answers to the question 'What was the most signifficant event that affected the stock price?', 'Did the usage of certain words have a significant impact on the stock price?' and 'How accurate is our new machine learning model in predicting Tesla's stock price?'. This observation will tell us just how much Elon has managed to move Tesla's stock with one post. 



### The data and preprocessing

The data we used are datasets imported from Yahoo Finance which consist of quotes from 2015 to 2020. From these datasets we filtered the ones that were mentioned by the man the myth the legend Mr Elon Musk himself. In addition to the quotes we imported the stock prices of Tesla from the same years. From the stock prices we were able to generate the daily returns for one stock. 



<img width="424" alt="Screenshot 2021-12-15 at 13 49 10" src="https://user-images.githubusercontent.com/92207222/146181293-b78e70e5-1aeb-4aec-bc48-7bff0c6743ec.png">



### Methods used for research

On each five datasets we first check which quotes belong to Elon Musk and write them in a new file. In our datastory, we focused on a major phenomena: what kind of correlation exists between Elon Musk quotes and the Tesla stock price? 
We will analyse this phenomena by studying the quotes made and see how Tesla's stock was impacted from a specific kind of post. The post quality will be examined by parsing each quote into separate words and analyse which words played a signifficant role in shifting the stock market price. In addition, another factor that we believe impacts the stock price of Tesla is the volume of posts made by Musk each day he posted.

***Take away from blog: FinBERT, mentioning considering us studying the number of post that Elon made***

For the analysis we used three different pre-trained machine learning methods of sentiment analysis, which are FinBERT, Valder and Textblob sentiment analysis.

![Screenshot 2021-12-15 at 19 49 17](https://user-images.githubusercontent.com/92207222/146238725-f41d59f1-624e-43cb-b37c-31b133ec6fbb.png)

![Screenshot 2021-12-15 at 21 05 53](https://user-images.githubusercontent.com/92207222/146249209-00a8754e-a9d2-41c8-9826-02dca00f1ef6.png)




### Data in numbers

Since the stock market is closed during weekends we had to take this in account on our data pre-processing. We moved the quotes from weekends to the next Monday.

<img width="924" alt="Screenshot 2021-12-14 at 16 49 36" src="https://user-images.githubusercontent.com/92207222/146021223-c579bade-a3e1-46d7-a1e8-3c6f36700448.png">
***Figure 1:*** The number of Elon Musk quotes in respective to time. 

<img width="787" alt="Screenshot 2021-12-16 at 0 53 33" src="https://user-images.githubusercontent.com/92207222/146277634-dd383f9b-d49d-4fb2-9280-5216e70996ac.png">
***Figure 2:*** Classification results of the quotes

The quotes were split into separate words and each word was classified using the Textblob pre-trained model that can give them a value between [1, -1] based on their objectivity or subjectivity. If the value is in range [1, 0] the word had a subjective nature and if the value generated from Texblob is in between [0, -1] it has a more objective nature. This classification method is needed in further analysis, because it enables us to give weight to different words that Elon Musk used in quotes.

<img width="1661" alt="Screenshot 2021-12-16 at 11 16 07" src="https://user-images.githubusercontent.com/92207222/146342895-e4ce48b8-0772-40a5-a414-9d50ddaffce6.png">
***Figure 3:*** Comparison results between the two pre-trained models Textblob and Vader


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

