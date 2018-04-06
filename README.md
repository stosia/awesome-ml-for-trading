# Awesome Machine Learning for Trading
A curated list of awesome application of machine learning in stock trading.

## Table of Contents

  * [Companies that Have Done It](#companies-that-have-done-it)
  * [Conferences, Summits](#conferences-summits)
  * [Books](#books)
  * [Papers](#papers-thesis)

## Companies that Have Done It

List of companies that have successfully applied machine learning or deep learning in stock trading.

* [Renaissance Technologies](https://en.wikipedia.org/wiki/Renaissance_Technologies) - Probably the most well known and successful hedge fund firm that specializes in systematic trading using quantitative models derived from mathematical and statistical analyses.
* [Numerai](https://numer.ai/) - An A.I hedge fund with crowd sourced algorithms. People can submit algorithm and get paid if it works. See the corporate introduction video [here](https://youtu.be/dhJnt0N497c), and longer interviews with the founder Richard Craib [here](https://www.youtube.com/watch?v=yY-Sg7KhRhU) and [here](https://www.youtube.com/watch?v=yY-Sg7KhRhU).
* [Alpaca](https://www.alpaca.ai/) - a platform where end users mark their trading entries/exits in the chart, and a deep learning platform figures out the model to detect such patterns. See their video presentation [here](https://youtu.be/FoQKCeDuPiY)
* [Binatix](http://www.binatix.com/) - there's nothing on their website, but you can read their coverage [Introducing Binatix: A Deep Learning Trading Firm That's Already Profitable](https://www.recode.net/2014/9/10/11630724/introducing-binatix-a-deep-learning-trading-firm-thats-already) (actually there's not much information here either).

 
## Conferences, Summits

* Deep Learning in Finance - See the videos of past events (some videos can be watched freely, but you need to pay $$ to access the full videos: [2017 (London)](http://videos.re-work.co/events/25-deep-learning-in-finance-summit-london-2017), [2017 (Singapore)](http://videos.re-work.co/events/22-deep-learning-in-finance-summit-singapore-2017), [2016 (London)](http://videos.re-work.co/events/8-deep-learning-in-finance-summit-london-2016), [2018 (event page)](https://www.re-work.co/events/deep-learning-in-finance-summit-london-2018)

## Books

* Marcos Lopez de Prado: [**_Advances in Financial Machine Learning_**](http://a.co/gKz8hpa) (2018). 

  This is a very good book describing how to structure the use of machine learning in finance. The [first chapter](https://poseidon01.ssrn.com/delivery.php?ID=521087021095126103013122009108119098033054052039028007076097107111067094069091074068054032007059016029043022070095121122119022016038095048036074098066064114066030068061049125122024004103070072091079107084089027065116124122101097090028025105007065020&EXT=pdf) is available online and it outlines the main ideas that will be taught in the rest of the books. This book is written by someone who knows both finance and machine learning subjects very well. The author is an expert in mathematical finance, has written many papers on machine learning and supercomputing, and has $13 billion fund under his management. He knows what he's talking about.
  
  In this book, he describes 1) why many failed to apply ML to finance, and 2) what it takes to succeed. And he argues that what it takes to succeed is first you must realize that there is no silver bullet, no magic ML model that will put you in the list of billionaires, and what you must do instead is to establish the infrastructure and process to facilitate the creation and development of these models.
  
  Be warned though that you won't find any state of the art ML techniques for finance in this book. No no no, that is just not going to happen with finance culture in this planet. As this book says, it won't tell you how to make a car, but how to make the car factory. 

## Papers, Thesis

### On End of Day Price Data

#### Using Multiple Techniques

* Mikelsen, Stian; Andersen, André Christoffer: "**_A Novel Algorithmic Trading Framework Applying Evolution and Machine Learning for Portfolio Optimization_**", Master's Thesis (2012) [[PDF](http://www.datascienceassn.org/sites/default/files/A%20Novel%20Algorithmic%20Trading%20Framework%20-%20Machine%20Learning%20for%20Portolio%20Optimization.pdf)] [[Google Scholar](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Andersen++A+Novel+Algorithmic+Trading+Framework+Applying+Evolution+and+Machine+Learning+for+Portfolio+Optimization&btnG=)]

  In this thesis, the authors present 14 trading systems based on technical techniques (RSI, MACD, follow the leader), machine learning (SVM, NN including RNN, and regression), and efficient frontier (EF), and evaluate them on EOD data on stocks on DOW and OBX indexes (Oslo Stock Exchange). The periods are 12 and 6 years for Dow and OBX, which are somewhat short. The paper concluded that Dow is highly efficient because it's hard to make profit using the models, whereas they can stil make some profit on OBX because it is less efficient.

#### Using DBN

* C. Zhu et al.: **_A Stock Decision Support System based on DBNs_**, Journal of Computational Information Systems 10: 2 883–893 (2014) [[PDF](http://or.nsfc.gov.cn/bitstream/00001903-5/324239/1/1000009681354.pdf)] [[Google Scholar](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Zhu+A+Stock+Decision+Support+System+based+on+DBNs&btnG=)]

    Using oscilation box indicator on EOD data as trading system. DBN is used for learning the data and predict box boundary. Buy if price breaks the upper bound, and vice versa. The model has 14 inputs (indicators) such as the standard HLOCV, MA, ROC, RSI, and MACD indicators. Each indicators are normalized and given different weights based on their influence on the price before they're given to DBN as input. Gray correlation degree is used to calculate these influence weights. Data are 400 stocks in S&P 500, with 1200 days and 400 days of EOD data for training and testing dataset respectively.
    
    The results look very good, the model can significantly outperform the benchmark in all four conditions: bull, bear, fluctuating bull, and fluctuating bear situations. However some careful decisions need to be done with regard to hyperparameter selections such as training data duration, the box window sizes, and transaction rate σ, and there is overfitting concern here.
    


#### Using Multi-agent Reinforcement Learning

* Lee J.W., O J. (2002) "**_A Multi-agent Q-learning Framework for Optimizing Stock Trading Systems_**". In: Hameurlain A., Cicchetti R., Traunmüller R. (eds) Database and Expert Systems Applications. DEXA 2002. Lecture Notes in Computer Science, vol 2453. Springer, Berlin, Heidelberg [[PDF](http://ftp10.us.freebsd.org/users/azhang/disc/springer/0558/papers/2453/24530153.pdf)] [[Google Scholar](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Lee+A+Multi-agent+Q-learning+Framework+for+Optimizing+Stock+Trading+Systems&btnG=)]

  The paper presents multi-agent RL architecture containing four agents: for generating buy signal, executing buy signal, generating sell signal, and executing sell signal. Each are running Q-learning. Operating on EOD data, with dataset from KOSPI 200 stocks from Jan 1999 to Oct 2001 (less than 3 years). Claimed good result on the test set (about 4 months period). This paper presents interesting multi-agent architecture, but the details are a bit unclear.    

### On Intraday Price Data

#### Using Neural Networks

* Dixon, M., Klabjan, D., & Bang, J. H. (2016). "**_Classification-based Financial Markets Prediction using Deep Neural Networks_**". Algorithmic Finance [[PDF](https://pdfs.semanticscholar.org/f4b5/c7059eaa43edf1fced2752c4570b76bf5950.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=14843145424555595400&hl=en&as_sdt=2005&sciodt=0,5)]

  This paper analyses the 5-minute interval price of 43 commodities and FX futures over 23 year period. It uses standard NN with four hidden layers of 1000, 900, 800, and 700 neurons and 129 output neurons (three signals (up, down, and neutral) for each of the 43 securities). The input is extended with additional indicators and correlation with other securities, making a total of 9895 input features for the network. Good results were claimed.  
  

### On Order Books

#### Theory

* Charles Cao & Oliver Hansch & Xiaoxin Wang, 2009. "**_The information content of an open limit‐order book,_**" Journal of Futures Markets, John Wiley & Sons, Ltd., vol. 29(1), pages 16-41 [[PDF](https://pdfs.semanticscholar.org/3234/ac395016bcd8b9907df6e2f7c49d56242f50.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=5312431820185241274&hl=en&as_sdt=0,5)]

#### Using RNN


### On News

#### Using CNN

* Xiao Ding, Yue Zhang, Ting Liu, and Junwen Duan. 2015. "**_Deep learning for event-driven stock prediction_**". In Proceedings of the 24th International Conference on Artificial Intelligence (IJCAI'15), Qiang Yang and Michael Wooldridge (Eds.). AAAI Press 2327-2333. [[PDF](http://www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/download/11031/10986)] [[Google Scholar](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Ding+Deep+learning+for+event-driven+stock+prediction&btnG=)]

   This paper analyzes the short, mid, and long term effects of news on stock price. It proposes two main ideas, i.e. the use of event embeddings to represent news events (as opposed to word embeddings or just bag of words methods), and the use of CNN (combined with a feed forward NN) to learn and predict the effect of these events to stock price movement. It concludes that using these two techniques gives better result than using either one. The result is about 65% accuracy, and this is about 6% better than previous state of the art work, and combined with a simple trading strategy it can give handsome profit.
   
   This is a very useful paper for those who want to perform news extraction and analyse the impact on stock price.

### Want to Read

* Matthew Dixon, "**_Sequence classification of the limit order book using recurrent neural networks_**", Journal of Computational Science, Volume 24, 2018, Pages 277-286, ISSN 1877-7503, [[URL](http://www.sciencedirect.com/science/article/pii/S1877750317309675)] [[PDF](https://www.sciencedirect.com/science/article/pii/S1877750317309675)] [[Google Scholar](https://scholar.google.com/scholar?cluster=11756832130786467866&hl=en&as_sdt=2005&sciodt=0,5)]

* Sirignano, Justin, "**_Deep Learning for Limit Order Books_**" (May 16, 2016). [[SSRN](https://ssrn.com/abstract=2710331)] [[PDF](http://www.smallake.kr/wp-content/uploads/2017/04/1601.01987.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=14762137393827403270&hl=en&as_sdt=2005&sciodt=0,5)]

* D. Palguna and I. Pollak, "**_Mid-Price Prediction in a Limit Order Book,_**" (December 31, 2014) [[SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2544361)] [[PDF](https://papers.ssrn.com/sol3/Delivery.cfm/SSRN_ID2544361_code1615147.pdf?abstractid=2544361&mirid=1)]  [[Google Scholar](https://scholar.google.com/scholar?cluster=10479489130084858948&hl=en&as_sdt=0,5)]

* B. Zheng, E. Moulines and F. Abergel, "**_Price Jump Prediction in a Limit Order Book,_**" _Journal of Mathematical Finance_, Vol. 3 No. 2, 2013, pp. 242-255 [[PDF](http://file.scirp.org/pdf/JMF_2013052414582995.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=8926587948972519125&hl=en&as_sdt=2005&sciodt=0,5)]

* Kearns, Michael, and Yuriy Nevmyvaka. "**_Machine learning for market microstructure and high frequency trading_**." High Frequency Trading: New Realities for Traders, Markets, and Regulators (2013). [[PDF](http://www.smallake.kr/wp-content/uploads/2014/01/KearnsNevmyvakaHFTRiskBooks.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=3674704136917952284&hl=en&as_sdt=0,5)]

* Rama Cont, Arseniy Kukanov, Sasha Stoikov. "**_The Price Impact of Order Book Events_**". 2010 [[PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.755.4233&rep=rep1&type=pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=15147414922236014366&hl=en&as_sdt=0,5)]

* Chordia, Tarun, Richard Roll, and Avanidhar Subrahmanyam. "**_Order imbalance, liquidity, and market returns._**" Journal of Financial economics 65.1 (2002): 111-130. [[PDF](http://www.cis.upenn.edu/~mkearns/finread/Chordia_buy-sell_orders.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=11113798686198861834&hl=en&as_sdt=0,5)]

* Lee, Charles, and Mark J. Ready. "**_Inferring trade direction from intraday data._**" The Journal of Finance 46.2 (1991): 733-746. [[PDF](https://www.acsu.buffalo.edu/~keechung/MGF743/Readings/Inferring%20trade%20direction%20from%20intraday%20data.pdf)] [[Google Scholar](https://scholar.google.com/scholar?cluster=11859816935661177512&hl=en&as_sdt=2005&sciodt=0,5)]


## Other Lists

* Greg Harris: "**_A Survey of Deep Learning Techniques Applied to Trading_**" (July 2016) [[URL](http://gregharris.info/a-survey-of-deep-learning-techniques-applied-to-trading/) (broken)] [[PDF](http://www.smallake.kr/wp-content/uploads/2017/04/Survey-1.pdf)].

  Note that many the content overlap with items on this page.

