## Impact of Elon Musk quotes on Tesla's stock


### Abstract

Elon Musk is the world's richest person and is famous for gaining attention for his tweets that according to him half are generated while sitting on his toilet. During the recent years his tweets have gathered much attention by their impact on markets which has left investors worried. From jumping the value of cryptocurrencies such as bitcoin and dogecoin to small companies such as Gamestop Elon Musk's tweets have undeniably played a huge impact on moving stock prices of companies. 

It has been claimed that Elon Musk's twitter account could be Tesla's primary marketing tool since Tesla does not invest in marketing at all. The hypothesis of our analysis definately backs this theory. (Add something here)

During our analysis we are going to try to find answers to the question 'What was the most signifficant event that affected the stock price?', 'Did the usage of certain words have a significant impact on the stock price?' and 'How accurate is our new machine learning model in predicting Tesla's stock price?'. This observation will tell us just how much Elon has managed to move Tesla's stock with one post. 



### The data and preprocessing

The data we used are datasets imported from Yahoo Finance which consist of stock prices from 2015 to 2020. From these datasets we filtered the ones that were mentioned by the man the myth the legend Mr Elon Musk himself. In addition to the quotes we imported the stock prices of Tesla from the same years. From the stock prices we were able to generate the daily returns for one stock. 



<img width="424" alt="Screenshot 2021-12-15 at 13 49 10" src="https://user-images.githubusercontent.com/92207222/146181293-b78e70e5-1aeb-4aec-bc48-7bff0c6743ec.png">

***Figure 1:*** Tesla's stock price graph



### Methods used for research

On each five datasets we first check which quotes belong to Elon Musk and write them in a new file. In our datastory, we focused on a major phenomena: what kind of correlation exists between Elon Musk quotes and the Tesla stock price? 
We will analyse this phenomena by studying the quotes made and see how Tesla's stock was impacted from a specific kind of post. The post quality will be examined by parsing each quote into separate words and analyse which words played a signifficant role in shifting the stock market price. In addition, another factor that we believe impacts the stock price of Tesla is the volume of posts made by Musk each day he posted.

![Screenshot 2021-12-16 at 12 51 25](https://user-images.githubusercontent.com/92207222/146358193-db438f2d-9e85-464b-9c4a-8af4fbd1d26f.png)

***Picture 1:*** The process of the data handling

For the analysis we used two different pre-trained machine learning methods of sentiment analysis, which were Valder and Textblob sentiment analysis models. The programming portion of our project consisted of three primary steps: data filtering, performing sentiment analysis to the filtered data, and creating a correlation from Tesla's stock price data. Additionally, we wanted to create a model that can predict future stock price based on quotes. 

![Screenshot 2021-12-15 at 19 49 17](https://user-images.githubusercontent.com/92207222/146238725-f41d59f1-624e-43cb-b37c-31b133ec6fbb.png)

***Picture 2:*** The Vader method

The Vader sentimental analysis model returns the compound score that informs if the quote is positive (compound>=0.05), neutral(-0.5>compound>0.05) or negative(compound >= -0.05). It is a great open-source tool designed to sentiments expressed in social media. It has a MIT License. In our project we specifically used the Vader tool to analyse the text from the quotes. The tool can recognise typical negations, such as "Tesla is not good" or "Model S wasn't very good". In addition, it spots punctuations such as exclamation marks and is thus capable. ofgiving these words more sentiment intesity. An example could the following "Tesla is Good!!!". The Vader tool can also recognize words written with caps lock to give them more sentimental intesity.

![Screenshot 2021-12-15 at 21 05 53](https://user-images.githubusercontent.com/92207222/146249209-00a8754e-a9d2-41c8-9826-02dca00f1ef6.png)

***Picture 3:*** The Textblob method

For the second model, we used TextBlob, another pretrained model to do the sentiment analysis. This model returns two values : the polarity (ie how much a quote is positive or negative) in a range between -1 and 1, and the subjectivity (ie how much the content of a quote is objective or not) in a range between 0 and 1.


### Data in numbers

Since the stock market is closed during weekends we had to take this in account on our data pre-processing. We moved the quotes from weekends to the next Monday.

<img width="924" alt="Screenshot 2021-12-14 at 16 49 36" src="https://user-images.githubusercontent.com/92207222/146021223-c579bade-a3e1-46d7-a1e8-3c6f36700448.png">
***Figure 2:*** The number of Elon Musk quotes in respective to time. 

<img width="787" alt="Screenshot 2021-12-16 at 0 53 33" src="https://user-images.githubusercontent.com/92207222/146277634-dd383f9b-d49d-4fb2-9280-5216e70996ac.png">

***Figure 3:*** Classification results of the quotes

The quotes were split into separate words and each word was classified using the Textblob pre-trained model that can give them a value between [1, -1] based on their objectivity or subjectivity. If the value is in range [1, 0] the word had a subjective nature and if the value generated from Texblob is in between [0, -1] it has a more objective nature. This tokenizing method is needed in further analysis, because it enables us to give weight to different words that Elon Musk used in quotes. Because of this we can now summarize a value for each quote that consists of words with different integer values from -1 to 1.

### The volume of quotes between 2015 - 2020

<img width="1579" alt="Screenshot 2021-12-16 at 19 04 40" src="https://user-images.githubusercontent.com/92207222/146416358-69a99360-e441-4c43-88d0-ea69deb5b80c.png">

***Figure : *** Quotes during 2015

<img width="1577" alt="Screenshot 2021-12-16 at 19 05 27" src="https://user-images.githubusercontent.com/92207222/146416487-f608c156-134c-4cac-aa06-d77f095162c6.png">

***Figure :*** Quotes during 2016

<img width="1573" alt="Screenshot 2021-12-16 at 19 06 19" src="https://user-images.githubusercontent.com/92207222/146416629-e780794d-3fe3-4bc4-a7a8-8dde9d3416da.png">

***Figure :*** Quotes during 2017


<img width="1575" alt="Screenshot 2021-12-16 at 19 07 27" src="https://user-images.githubusercontent.com/92207222/146416771-2b8ca55f-7682-40b2-b9cc-5e117c6ddf24.png">

***Figure :*** Quotes during 2018

<img width="1573" alt="Screenshot 2021-12-16 at 19 08 14" src="https://user-images.githubusercontent.com/92207222/146416877-d06ba6a5-fdfe-4355-9319-48490bd9ee13.png">

***Figure :*** Quotes during 2019





### Comparison between Textblob and Vader


<img width="1661" alt="Screenshot 2021-12-16 at 11 16 07" src="https://user-images.githubusercontent.com/92207222/146342895-e4ce48b8-0772-40a5-a414-9d50ddaffce6.png">

***Figure 4:*** Comparison results between the two pre-trained models Textblob and Vader


We can see that both analysis indicate similar results. The quotes consisted mostly of positive words (words that have a value above zero), but we should keep in mind that roughly 70% of the positive quotes are close to the value zero. This means that majority of the quotes contain words that are neutrally positive rather than over positive. 

### The impact of the quotes on the stock price



*** "I was always crazy on Twitter" - Elon Musk ***

https://www.dontdiewondering.com/elon-musks-most-controversial-tweets/

<img width="1616" alt="Screenshot 2021-12-16 at 12 17 18" src="https://user-images.githubusercontent.com/92207222/146352961-00c2a1e3-08fd-418a-982a-a03dad7e3141.png">

***Figure 5:*** Correlation between the stock price and words used by Elon Musk


Generally speaking we can see that when the quotes had a value of -0.2 to 0.4 the returns had a general turnover rate between -0.05 and 0.05. We could state that while the quotes were on a neutral level, the impact on the returns of the stocks was also on a controlled level. However some interesting exceptions linger in the correlation. For example, the stock price didn't ever drop signifficantly when the quote consisted of majourly of negative quotes. The chart can be easily misleading if we don't keep in mind the fact that each negative quote only tells the average of the score of words that it consisted of. This does not necessarily mean that something bad was said about Tesla. However, as picture 4 indicates, Elon Musk has provenly been giving quotes with a negative ringing which have inreturn impacted negatively on the stock price.



![Screenshot 2021-12-16 at 14 29 54](https://user-images.githubusercontent.com/92207222/146372340-16b61c55-e632-4c43-a91e-799d91153ac6.png)
***Picture 4:*** The impact of Elon Musk's quotes on the stock price of Tesla






### Conclusion




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

