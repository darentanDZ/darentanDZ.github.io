---
layout: post
title: How I Made The Data Visualization of Top 50 Comments on Facebook Post by the Crown Prince of Johor
description: The explanation of how I created the Data Visualization for Data Analysis on comments the Facebook Post by the Crown Prince of Johor
published: true
---

<style type="text/css">
 p {
  text-align: justify;
}

img {
    display: block;
    margin: auto;
}
</style>

![Top 50 Comments on Facebook Post by the Crown Prince of Johor Cover Photo](/images/11042018/cover_photo.png)

## Foreground/Motivation
Two days ago, I read this post by the Crown Prince of Johor on his official FB Page, JOHOR Southern Tigers where he occasionally posts his thoughts on current issues in Malaysia.

For the uninitiated, sultans and princes are remnants from the Malaysia's history where back then, the first 9 states of Malaysia were separate and ruled by 9 individual, traditional Malay rulers. The descendants of those rulers inherit the thrones and serve as symbolic rulers and are in charge of all matters pertaining to Islam in the country today.

Among the many states' monarchs, the sultan and prince of Johor particularly stand out and are revered by the Malaysian citizens for being vocal about the issues in the country and the plight of the common citizen by openly criticizing or hitting back at the ministers and government.

Back to the post , that particular post written by the prince sharing his opinion on the political situation in the country since the 14th General Election is looming in the corner. He makes an indirect attack on the former prime minister, Dr.Mahathir who is also the head of the opposition for the upcoming election by warning the citizens not to trust the 'forked tongue' man and also telling the citizens, to not rock the boat by changing government. He acknowledges the ship(the current government) is broken and advises to replacing the broken rudders instead changing the entire ship and that he will be the one bringing around the change. Essentially telling the citizens to continue voting for the current government and he will take care of the rest.

This piqued my curiousity as to what the other readers' opinions were on this post? Would the citizens agree or disagree with their beloved prince? Will his words bring a change the current sentiments of the people towards the government?

Hence, I set out to scrape the comments, perform data analysis and create this visualization.

{% include in-article-ads-1.html %}

## Methodology
1. Wrote Python script to scrape the comments of the original Facebook Status at JOHOR Southern Tigers using Facebook Graph API. Unfortunately, Graph API is down indefinitely while FB is making some changes to their policy(Thanks Cambridge Analytica!)
<br />
![Facebook Graph API down screenshot](/images/11042018/fb_graph_api_down.jpg)
<center>Screenshot of message returned by Facebook Graph API</center><br />
2. Manually scraped Top 50 comments(With highest reactions) from the post(aka Select, Copy+Paste).
3. Preprocess text using custom stopword list, removing punctuations, lower case etc.
<br />
![Stop words list preprocessing function](/images/11042018/preprocess_function.PNG)
<center>Screenshot of the preprocessing with the custom Malay stopwords list</center><br />
4. Perform word count.
5. Manually created and labelled the weights a 1183-word sentiment corpus based on the words in the comments
<br />
![Snippet of the Malay sentiment corpus](/images/11042018/malay_sentiment_corpus_snippet.jpg)
<center>Snippet of the Malay Words Sentiment Corpus with and without the neutral words</center><br />
6. Performed sentiment analysis using custom sentiment corpus to find out sentiment of each comment
7. Produced visualizations using wordcloud, matplotlib and Tableau
8. Compiled findings and designed infographic using Corel Draw X7
<br />
![Screenshot of finishined infographic in Corel Draw](/images/11042018/coreldraw_screenshot.png)
<center>Screenshot of finished infographic in Corel Draw X7</center><br />

## Main Findings
- 52% of the Top 50 comments on the post had negative sentiment with 30% positive and 18% neutral comments which indicates that a majority of the comments reacted negatively to the Crowned Prince's post.
<br />
![Comments Sentiment Pie Chart Visualization](/images/11042018/sentiment_pie_chart.png)
<center>Comments Sentiment Pie Chart Visualization</center><br />
- The Top 5 most mentioned words were politik, hidup, tun, kerajaan, najib with some prominent phrases such as: "nasib_kami", "saya_sokong", "rakyat_marhaen", "pandangan_peribadi" which is inline with this upcoming election which pits former 4th prime minister of Malaysian (Tun) Dr.Mahathir Mohamad against the current one, Dato' Sri Haji Mohammad Najib.
<br />
![Comments Word Cloud Visualization](/images/11042018/sentiment_word_cloud.jpg)
<center>Comments Wordcloud Visualization</center><br />


## Conclusion
Based on this analysis, it can be concluded that the rakyat disagrees with the prince. This contradicted with my initial belief that the Crown Prince's words would influence the rakyat.

## Note
* My knowledge of Malaysian history/sultans/princes is a little rusty. Any friends have anything to add on feel free.
* I plan to redo this analysis when the Facebook Graph API is restored. With more data, the results will become even more accurate.

## P/S
Am also a professional freelance developer. So hit me up if you need someone for web, mobile to big data/machine learning-related projects! :)

## The Infographic
<br />
![Data Visualization of Top 50 Comments on Facebook Post by the Crown Prince of Johor](/images/10042018/infographic4.png)
