## Impact of Elon Musk quotes on Tesla's stock


### Abstract

Elon Musk is the world's richest person and is famous for gaining attention for his tweets that according to him half are generated while sitting on his toilet. During the recent years his tweets have gathered much attention by their impact on markets which has left investors worried. From jumping the value of cryptocurrencies such as bitcoin and dogecoin to small companies such as Gamestop Elon Musk's tweets have undeniably played a huge impact on moving stock prices of companies. 

It has been claimed that Elon Musk's twitter account could be Tesla's primary marketing tool since Tesla does not invest in marketing at all. The hypothesis of our analysis definately backs this theory. (Add something here)

During our analysis we are going to try to find answers to the question 'What was the most signifficant event that affected the stock price?'. This observation will tell us just how much Elon has managed to move Tesla's stock with one simple Twitter post. 




### The data and preprocessing

The data we used are datasets imported from Yahoo Finance which consist of Twitter quotes from 2015 to 2020. From these datasets we filtered the ones that were mentioned by the man the myth the legend Mr Elon Musk himself. In addition to the quotes we imported the stock prices of Tesla from the same years. From the stock prices we were able to generate the daily returns for one stock. 



<img width="424" alt="Screenshot 2021-12-15 at 13 49 10" src="https://user-images.githubusercontent.com/92207222/146181293-b78e70e5-1aeb-4aec-bc48-7bff0c6743ec.png">



### Methods

On each five datasets we first check which quotes belong to Elon Musk and write them in a new file. In our datastory, we focused on a major phenomena: what kind of correlation exists between Elon Musk quotes on Twitter and the Tesla stock price? 
We will analyse this phenomena by studying the quotes made and see how Tesla's stock was impacted from a specific kind of post. The post quality will be examined by parsing each quote into separate words and analyse which words played a signifficant role in shifting the stock market price. In addition, another factor that we believe impacts the stock price of Tesla is the volume of posts made by Musk each day he posted.

For the analysis we used three different pre-trained machine learning methods of sentiment analysis, which are FinBERT, Valder and Textblob sentiment analysis.

![Screenshot 2021-12-15 at 19 31 55](https://user-images.githubusercontent.com/92207222/146238236-aa712615-b579-4867-a547-ffa52d9326a6.png)

![Screenshot 2021-12-15 at 19 42 02](https://user-images.githubusercontent.com/92207222/146238250-e6baa816-bc2f-480f-9254-be7005959b06.png)


### Data in numbers

(insert pictures and graohs) and analyse them

<img width="924" alt="Screenshot 2021-12-14 at 16 49 36" src="https://user-images.githubusercontent.com/92207222/146021223-c579bade-a3e1-46d7-a1e8-3c6f36700448.png">





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

