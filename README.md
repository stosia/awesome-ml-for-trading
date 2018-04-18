# Awesome Machine Learning for Trading <sup>*)</sup>
A curated list of anything related to the application of machine learning in stock trading.

<sup>*)</sup> This work is sponsored by [Stocks Asia, berita saham Indonesia (stock news search engine)](https://stocks.asia) and [Stosia.ai](https://stosia.ai).

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

### Structuring Financial Machine Learning Company

* Marcos Lopez de Prado: [**_Advances in Financial Machine Learning_**](http://a.co/gKz8hpa). John Wiley & Sons, 2018. [[Google Scholar (2)](https://scholar.google.com/scholar?lookup=0&q=Advances+in+Financial+Machine+Learning&hl=en&as_sdt=0,5)] 

  This is a very good book describing how to structure the use of machine learning in finance. The [first chapter](https://poseidon01.ssrn.com/delivery.php?ID=521087021095126103013122009108119098033054052039028007076097107111067094069091074068054032007059016029043022070095121122119022016038095048036074098066064114066030068061049125122024004103070072091079107084089027065116124122101097090028025105007065020&EXT=pdf) is available online and it outlines the main ideas that will be taught in the rest of the books. This book is written by someone who knows both finance and machine learning subjects very well. The author is an expert in mathematical finance, has written many papers on machine learning and supercomputing, and has $13 billion fund under his management. He knows what he's talking about.
  
  In this book, he describes 1) why many failed to apply ML to finance, and 2) what it takes to succeed. And he argues that what it takes to succeed is first you must realize that there is no silver bullet, no magic ML model that will put you in the list of billionaires, and what you must do instead is to establish the infrastructure and process to facilitate the creation and development of these models.
  
  Be warned though that you won't find any state of the art ML techniques for finance in this book. No no no, that is just not going to happen with finance culture in this planet. As this book says, it won't tell you how to make a car, but how to make the car factory. 

### Market Microstructure

* Schmidt, Anatoly B. [**_Financial markets and trading: an introduction to market microstructure and trading strategies._**](http://a.co/fqw6BrI) Vol. 637. John Wiley & Sons, 2011. [[Google Scholar (28)](https://scholar.google.com/scholar?cluster=2144017200463163368&hl=en&as_sdt=0,5)]



## Papers, Thesis

### On End of Day Price Data

#### Using Multiple Techniques

* Mikelsen, Stian; Andersen,  André Christoffer: "**_A Novel Algorithmic Trading Framework Applying Evolution and Machine Learning for Portfolio Optimization_**", Master's Thesis (2012) [[PDF](http://www.datascienceassn.org/sites/default/files/A%20Novel%20Algorithmic%20Trading%20Framework%20-%20Machine%20Learning%20for%20Portolio%20Optimization.pdf)] [[Google Scholar (8)](https://scholar.google.com/scholar?cluster=10410656300975668672&hl=en&as_sdt=0,5)]

  In this thesis, the authors present 14 trading systems based on technical techniques (RSI, MACD, follow the leader), machine learning (SVM, NN including RNN, and regression), and efficient frontier (EF), and evaluate them on EOD data on stocks on DOW and OBX indexes (Oslo Stock Exchange). The periods are 12 and 6 years for Dow and OBX, which are somewhat short. The paper concluded that Dow is highly efficient because it's hard to make profit using the models, whereas they can stil make some profit on OBX because it is less efficient.

#### Using DBN

* C. Zhu et al.: **_A Stock Decision Support System based on DBNs_**, Journal of Computational Information Systems 10: 2 883-893 (2014) [[PDF](http://or.nsfc.gov.cn/bitstream/00001903-5/324239/1/1000009681354.pdf)] [[Google Scholar (10)](https://scholar.google.com/scholar?cluster=6680487426698004620&hl=en&as_sdt=0,5)]

    Using oscilation box indicator on EOD data as trading system. DBN is used for learning the data and predict box boundary. Buy if price breaks the upper bound, and vice versa. The model has 14 inputs (indicators) such as the standard HLOCV, MA, ROC, RSI, and MACD indicators. Each indicators are normalized and given different weights based on their influence on the price before they're given to DBN as input. Gray correlation degree is used to calculate these influence weights. Data are 400 stocks in S&P 500, with 1200 days and 400 days of EOD data for training and testing dataset respectively.
    
    The results look very good, the model can significantly outperform the benchmark in all four conditions: bull, bear, fluctuating bull, and fluctuating bear situations. However some careful decisions need to be done with regard to hyperparameter selections such as training data duration, the box window sizes, and transaction rate, and there is overfitting concern here.
    


#### Using Multi-agent Reinforcement Learning

* Lee, Jae Won, and O. Jangmin. "**_A multi-agent Q-learning framework for optimizing stock trading systems_**" International Conference on Database and Expert Systems Applications. Springer, Berlin, Heidelberg, 2002. [[PDF](http://ftp10.us.freebsd.org/users/azhang/disc/springer/0558/papers/2453/24530153.pdf)] [[Google Scholar (11)](https://scholar.google.com/scholar?cluster=12722630045314905670&hl=en&as_sdt=0,5)]

  The paper presents multi-agent RL architecture containing four agents: for generating buy signal, executing buy signal, generating sell signal, and executing sell signal. Each are running Q-learning. Operating on EOD data, with dataset from KOSPI 200 stocks from Jan 1999 to Oct 2001 (less than 3 years). Claimed good result on the test set (about 4 months period). This paper presents interesting multi-agent architecture, but the details are a bit unclear.    

### On Intraday Price Data

#### Using Neural Networks

* Dixon, M., Klabjan, D., & Bang, J. H. (2016). "**_Classification-based Financial Markets Prediction using Deep Neural Networks_**". Algorithmic Finance [[PDF](https://pdfs.semanticscholar.org/f4b5/c7059eaa43edf1fced2752c4570b76bf5950.pdf)] [[Google Scholar (21)](https://scholar.google.com/scholar?cluster=14843145424555595400&hl=en&as_sdt=2005&sciodt=0,5)]

  This paper analyses the 5-minute interval price of 43 commodities and FX futures over 23 year period. It uses standard NN with four hidden layers of 1000, 900, 800, and 700 neurons and 129 output neurons (three signals (up, down, and neutral) for each of the 43 securities). The input is extended with additional indicators and correlation with other securities, making a total of 9895 input features for the network. Good results were claimed.  
  

### On Market Microstructure

#### Theory

* Rama Cont, Arseniy Kukanov, Sasha Stoikov. "**_The Price Impact of Order Book Events_**". 2011 [[PDF](https://pdfs.semanticscholar.org/d064/5eb3d744f9e962ff09b8a5e9156f2147e983.pdf)] [[Google Scholar (194)](https://scholar.google.com/scholar?cluster=15147414922236014366&hl=en&as_sdt=0,5)]

  The authors study the price impact of order book events - limit orders, market orders and cancelations to equity price. They show that, over short time intervals, price changes are mainly driven by the order flow imbalance (OFI), defined as the imbalance between supply and demand at the best bid and ask prices. Further they show that there is a linear relation between OFI and price movement and argues that OFI captures other relationships such as between trade order imbalance or traded volume and price movement.

* Charles Cao & Oliver Hansch & Xiaoxin Wang, 2009. "**_The information content of an open limit order book,_**" Journal of Futures Markets, John Wiley & Sons, Ltd., vol. 29(1), pages 16-41 [[PDF](https://pdfs.semanticscholar.org/3234/ac395016bcd8b9907df6e2f7c49d56242f50.pdf)] [[Google Scholar (210)](https://scholar.google.com/scholar?cluster=5312431820185241274&hl=en&as_sdt=0,5)]

  The authors primarily investigate whether the orders behind the best bid and ask prices contribute to price discovery and contain information about short-term future price movements. There are two competing schools of thought on these. The first believes that private information is short-lived, and any imbalances of information will be reflected immediately using market orders. An informed trader who knows that the current market price is too high will expect the price to go downward in the future, especially when the other traders learn the same information, thus the likelihood of achieving execution for a limit sell order is relatively small in this situation.

  The second believes that private information is long-lived and the number of traders who may discover the private information is small. They believe submitting market orders signals impatience and reveals too much information. [Harris (1990)](https://scholar.google.co.id/scholar?cluster=9020206743718904491&hl=en&as_sdt=0,5) considered two types of limit-order traders: pre-committed
and value-motivated traders. The former submit limit orders to reduce trading costs, but will switch to using market orders if their orders remain unfilled for too long. The latter express their valuations of the asset through their choice of limit price. Both of these contribute to the reasons of price movements.
  
  The authors uses [Hasbrouck method](https://scholar.google.co.id/scholar?cluster=14497113078429292177&hl=en&as_sdt=0,5) to calculate the information share of three components: the MID price (mean between the best bid and ask price), the P price (i.e. last transaction price), and weighted price WP of order book steps up to ten steps (calculated from bid and ask price of the step scaled by the number of shares). Data is order book of 100 most active stocks in ASX for the month of March 2000, sampled every second. 
  
   The authors find that the order book is moderately informative; its contribution to price discovery is approximately 22%. The remaining 78% is from the best bid and offer prices on the book and the last transaction price. Furthermore, the authors find that order imbalances between the demand and supply schedules along the book are significantly related to future short-term returns, even after controlling for the autocorrelations in return, the inside spread, and the trade imbalance.

* Lee, Charles, and Mark J. Ready. "**_Inferring trade direction from intraday data._**" The Journal of Finance 46.2 (1991): 733-746. [[PDF](https://www.acsu.buffalo.edu/~keechung/MGF743/Readings/Inferring%20trade%20direction%20from%20intraday%20data.pdf)] [[Google Scholar (3021)](https://scholar.google.com/scholar?cluster=11859816935661177512&hl=en&as_sdt=2005&sciodt=0,5)]

   In this paper, the authors explains _tick test_, a technique to infers the direction of a trade by comparing its price to the price of the preceding trade(s), and proposes a hybrid method that combines it with _quote method_ to increase accuracy. The tick test classifies each trade into four categories: an uptick, a downtick, a zero-uptick, and a zero-downtick. A trade is an uptick (downtick) if the price is higher (lower) than the price of the previous trade. When the price is the same as the previous trade (a zero tick), if the last price change was an uptick, then the trade is a zero-uptick. Similarly, if the last price change was a downtick, then the trade is a zero-downtick. A trade is classified as a buy if it occurs on an uptick or a zero-uptick; otherwise it is classified as a sell.
   
   The accuracy of Lee and Ready hybrid method has been compared with other methods such as tick test and quote methods and it was found that while the accuracy in general is better than tick test (80.8% on average vs 77.2%), it is not as good as what Lee & Ready suggested (more than 90%). The summaries of the results are as follows [source: 'tick-test', private repository].
   
   |        Paper            |   Dataset   |Tick Test | Rev Tick Test | Quote | L & R |
   |-------------------------|-------------|:--------:|:-------------:|:-----:|:-----:|
   | Aitken and Frino [1996] | ASX         | 74.4%    |               |       |       |
   | Ellis, et al. [2000]    | Nasdaq      | 77.7%    |               | 76.4% | 81.0% |
   | Odders-White [2000]     | TORQ (NYSE) | 78.6%    |               | 74.9% | 85.0% |
   | Theissen [2001]         | Frankfurt SE| 72.2%    |               | 75.4% | 72.8% |
   | Finucane [2000]         | TORQ (NYSE) | 83.0%    | 72.1%         |       | 84.4% |
   | **Average**             |             | **77.2%** | **72.1%**    | **75.6%** | **80.8%** |
   
   References:
   
    * Aitken, Michael, and Alex Frino. "_**The accuracy of the tick test: Evidence from the Australian stock exchange.**_" 
      Journal of Banking & Finance 20.10 (1996): 1715-1729.
      [[Google Scholar (103)](https://scholar.google.co.id/scholar?cluster=11526285019126824797&hl=en&as_sdt=0,5)]
    * Ellis, Katrina, Roni Michaely, and Maureen O'Hara. "_**The accuracy of trade classification rules: Evidence from Nasdaq.**_" 
      Journal of Financial and Quantitative Analysis 35.4 (2000): 529-551.
      [[Google Scholar (467)](https://scholar.google.co.id/scholar?cluster=16725554999272992783&hl=en&as_sdt=0,5)]
    * Odders-White, Elizabeth R. "_**On the occurrence and consequences of inaccurate trade classification.**_" 
      Journal of Financial Markets 3.3 (2000): 259-286.
      [[Google Scholar (273)](https://scholar.google.co.id/scholar?cluster=1157070048670264356&hl=en&as_sdt=0,5)]
    * Theissen, Erik. "_**A test of the accuracy of the Lee/Ready trade classification algorithm.**_" 
      Journal of International Financial Markets, Institutions and Money 11.2 (2001): 147-165.
      [[Google Scholar (62)](https://scholar.google.co.id/scholar?cluster=12358541067434974138&hl=en&as_sdt=0,5)]
    * Finucane, Thomas J. "_**A direct test of methods for inferring trade direction from intra-day data.**_" 
      Journal of Financial and Quantitative Analysis 35.4 (2000): 553-576.
      [[Google Scholar (153)](https://scholar.google.co.id/scholar?cluster=1407349205202244755&hl=en&as_sdt=0,5)]
  
  

#### Using RNN


### On News

#### Using CNN

* Xiao Ding, Yue Zhang, Ting Liu, and Junwen Duan. 2015. "**_Deep learning for event-driven stock prediction_**". In Proceedings of the 24th International Conference on Artificial Intelligence (IJCAI'15), Qiang Yang and Michael Wooldridge (Eds.). AAAI Press 2327-2333. [[PDF](http://www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/download/11031/10986)] [[Google Scholar (62)](https://scholar.google.com/scholar?cluster=4450997871447409040&hl=en&as_sdt=0,5)]

   This paper analyzes the short, mid, and long term effects of news on stock price. It proposes two main ideas, i.e. the use of event embeddings to represent news events (as opposed to word embeddings or just bag of words methods), and the use of CNN (combined with a feed forward NN) to learn and predict the effect of these events to stock price movement. It concludes that using these two techniques gives better result than using either one. The result is about 65% accuracy, and this is about 6% better than previous state of the art work, and combined with a simple trading strategy it can give handsome profit.
   
   This is a very useful paper for those who want to perform news extraction and analyse the impact on stock price.

### Want to Read

#### General Machine Learning

* Lopez de Prado, Marcos. "**_The 10 Reasons Most Machine Learning Funds Fail._**" (2018). [[SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3104816)] [[Google Scholar (0)](https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=Prado+The+10+Reasons+Most+Machine+Learning+Funds+Fail&btnG=)]


#### Market Microstructure

* Matthew Dixon, "**_Sequence classification of the limit order book using recurrent neural networks_**", Journal of Computational Science, Volume 24, 2018, Pages 277-286, ISSN 1877-7503, [[URL](http://www.sciencedirect.com/science/article/pii/S1877750317309675)] [[PDF](https://www.sciencedirect.com/science/article/pii/S1877750317309675)] [[Google Scholar (7)](https://scholar.google.com/scholar?cluster=11756832130786467866&hl=en&as_sdt=2005&sciodt=0,5)]


* Sirignano, Justin, "**_Deep Learning for Limit Order Books_**" (May 16, 2016). [[SSRN](https://ssrn.com/abstract=2710331)] [[PDF](http://www.smallake.kr/wp-content/uploads/2017/04/1601.01987.pdf)] [[Google Scholar (14)](https://scholar.google.com/scholar?cluster=14762137393827403270&hl=en&as_sdt=2005&sciodt=0,5)]

  Interesting papers cited:
  
  * Cartea, Álvaro, Ryan Donnelly, and Sebastian Jaimungal. "**_Enhancing trading strategies with order book signals._**" Applied Mathematical Finance (2018): 1-35. [[PDF](http://www.smallake.kr/wp-content/uploads/2015/11/SSRN-id2668277.pdf)] [[Google Scholar (17)](https://scholar.google.com/scholar?cluster=3694311355214648861&hl=en&as_sdt=0,5)]

  * B. Zheng, E. Moulines and F. Abergel, "**_Price Jump Prediction in a Limit Order Book_**" _Journal of Mathematical Finance_, Vol. 3 No. 2, 2013, pp. 242-255 [[PDF](http://file.scirp.org/pdf/JMF_2013052414582995.pdf)] [[Google Scholar (20)](https://scholar.google.com/scholar?cluster=8926587948972519125&hl=en&as_sdt=2005&sciodt=0,5)]

  * Avellaneda, Marco, and Sasha Stoikov. "**_High-frequency trading in a limit order book._**" Quantitative Finance 8.3 (2008): 217-224. [[PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.464.5771&rep=rep1&type=pdf)] [[Google Scholar (270)](https://scholar.google.com/scholar?cluster=5527447623732412778&hl=en&as_sdt=0,5)]

  * Avellaneda, Marco, Josh Reed, and Sasha Stoikov. "**_Forecasting prices from Level-I quotes in the presence of hidden liquidity._**" Algorithmic Finance 1.1 (2011): 35-43. [[PDF](https://content.iospress.com/download/algorithmic-finance/af004?id=algorithmic-finance%2Faf004)] [[Google Scholar (35)](https://scholar.google.com/scholar?cluster=8343363853300442598&hl=en&as_sdt=0,5)]
  
* D. Palguna and I. Pollak, "**_Mid-Price Prediction in a Limit Order Book,_**" (December 31, 2014) [[SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2544361)] [[PDF](https://papers.ssrn.com/sol3/Delivery.cfm/SSRN_ID2544361_code1615147.pdf?abstractid=2544361&mirid=1)]  [[Google Scholar (6)](https://scholar.google.com/scholar?cluster=10479489130084858948&hl=en&as_sdt=0,5)]

* Kearns, Michael, and Yuriy Nevmyvaka. "**_Machine learning for market microstructure and high frequency trading_**." High Frequency Trading: New Realities for Traders, Markets, and Regulators (2013). [[PDF](http://www.smallake.kr/wp-content/uploads/2014/01/KearnsNevmyvakaHFTRiskBooks.pdf)] [[Google Scholar (22)](https://scholar.google.com/scholar?cluster=3674704136917952284&hl=en&as_sdt=0,5)]


* Rama Cont, Arseniy Kukanov, Sasha Stoikov. "**_The Price Impact of Order Book Events_**". 2011 [[PDF](https://pdfs.semanticscholar.org/d064/5eb3d744f9e962ff09b8a5e9156f2147e983.pdf)] [[Google Scholar (194)](https://scholar.google.com/scholar?cluster=15147414922236014366&hl=en&as_sdt=0,5)]

  The authors study the price impact of order book events - limit orders, market orders and cancelations to equity price, using the NYSE TAQ data for 50 U.S. stocks. They show that, over short time intervals, price changes are mainly driven by the order flow imbalance, defined as the imbalance between supply and demand at the best bid and ask prices.

  Interesting papers cited:
  * Eisler, Zoltan, Jean-Philippe Bouchaud, and Julien Kockelkoren. "The price impact of order book events: market orders, limit orders and cancellations." Quantitative Finance 12.9 (2012): 1395-1419. [[PDF](https://arxiv.org/pdf/0904.0900)] [[Google Scholar (105)](https://scholar.google.com/scholar?cluster=10991371471005487446&hl=en&as_sdt=0,5)]
  * Hautsch, Nikolaus, and Ruihong Huang. "The market impact of a limit order." Journal of Economic Dynamics and Control 36.4 (2012): 501-522. [[PDF](https://www.econstor.eu/bitstream/10419/39308/1/612287254.pdf)] [[Google Scholar (112)](https://scholar.google.com/scholar?cluster=14154850011786678034&hl=en&as_sdt=0,5)]
  * Avellaneda, Marco, Josh Reed, and Sasha Stoikov. "Forecasting prices from Level-I quotes in the presence of hidden liquidity." Algorithmic Finance 1.1 (2011): 35-43. [[PDF](https://content.iospress.com/download/algorithmic-finance/af004?id=algorithmic-finance%2Faf004)] [[Google Scholar (35)](https://scholar.google.com/scholar?cluster=8343363853300442598&hl=en&as_sdt=0,5)]
  * Hopman, Carl. "Do supply and demand drive stock prices?." Quantitative Finance 7.1 (2007): 37-53. [[Google Scholar (55)](https://scholar.google.com/scholar?cluster=5491481593115357299&hl=en&as_sdt=0,5)]
  * Weber, Philipp, and Bernd Rosenow*. "**_Order book approach to price impact_**" Quantitative Finance 5.4 (2005): 357-364. [[PDF](https://arxiv.org/pdf/cond-mat/0311457)] [[Google Scholar (157)](https://scholar.google.com/scholar?cluster=12995251003638085426&hl=en&as_sdt=0,5)]
  * Bouchaud, Jean-Philippe, et al. "**_Fluctuations and response in financial markets: the subtle nature of random price changes_**" Quantitative finance 4.2 (2004): 176-190. [[PDF](https://arxiv.org/pdf/cond-mat/0307332)] [[Google Scholar (400)](https://scholar.google.com/scholar?cluster=10344048419493002618&hl=en&as_sdt=0,5)]
  * Engle, Robert F., and Asger Lunde. "Trades and quotes: a bivariate point process." Journal of Financial Econometrics 1.2 (2003): 159-188. [[PDF](https://academic.oup.com/jfec/article-pdf/1/2/159/2444267/nbg011.pdf)] [[Google Scholar (163)](https://scholar.google.com/scholar?cluster=14029022516470199418&hl=en&as_sdt=0,5)]
  * Hasbrouck, Joel, and Duane J. Seppi. "Common factors in prices, order flows, and liquidity." Journal of financial Economics 59.3 (2001): 383-411. [[PDF](https://www.archive.nyu.edu/bitstream/2451/26848/2/wpa99011.pdf)] [[Google Scholar (1143)](https://scholar.google.com/scholar?cluster=15977843785483107545&hl=en&as_sdt=0,5)]
  * Knez, Peter J., and Mark J. Ready. "**_Estimating the profits from trading strategies._**" The Review of Financial Studies 9.4 (1996): 1121-1163. [[PDF](http://www.technicalanalysis.org.uk/reversal-patterns/KnRe96.pdf)] [[Google Scholar (162)](https://scholar.google.com/scholar?cluster=8722874810495216777&hl=en&as_sdt=0,5)]
  * Karpoff, Jonathan M. "The relation between price changes and trading volume: A survey." Journal of Financial and quantitative Analysis 22.1 (1987): 109-126. [[PDF](https://www.researchgate.net/profile/Jonathan_Karpoff/publication/227406040_The_Relation_Between_Price_Changes_and_Trading_Volume_A_Survey/links/53cecd5a0cf2fd75bc59a213/The-Relation-Between-Price-Changes-and-Trading-Volume-A-Survey.pdf)] [[Google Scholar (2873)](https://scholar.google.com/scholar?cluster=18087812455019644743&hl=en&as_sdt=0,5)]

* Krishnamurti, Chandrasekhar. "Introduction to market microstructure." Investment management. Springer, Berlin, Heidelberg, 2009. 13-29. [[PDF](http://www.springer.com/cda/content/document/cda_downloaddocument/9783540888017-c1.pdf)] [[Google Scholar (10)](https://scholar.google.com/scholar?cluster=4191178735967067647&hl=en&as_sdt=0,5)]

* Chordia, Tarun, Richard Roll, and Avanidhar Subrahmanyam. "**_Order imbalance, liquidity, and market returns._**" Journal of Financial economics 65.1 (2002): 111-130. [[PDF](http://www.cis.upenn.edu/~mkearns/finread/Chordia_buy-sell_orders.pdf)] [[Google Scholar (970)](https://scholar.google.com/scholar?cluster=11113798686198861834&hl=en&as_sdt=0,5)]

* Hasbrouck, Joel. "**_One security, many markets: Determining the contributions to price discovery._**" The journal of Finance 50.4 (1995): 1175-1199. [[Google Scholar (1477)](https://scholar.google.co.id/scholar?cluster=14497113078429292177&hl=en&as_sdt=0,5)]

#### News

* Andersen, Torben G., et al. "**_Real-time price discovery in global stock, bond and foreign exchange markets._**" Journal of international Economics 73.2 (2007): 251-277. [[PDF](https://www.econstor.eu/bitstream/10419/25442/1/515162655.PDF)] [[Google Scholar (952)](https://scholar.google.co.id/scholar?cluster=14790221890386887476&hl=en&as_sdt=0,5)]


## Other Lists 

* Greg Harris: "**_A Survey of Deep Learning Techniques Applied to Trading_**" (July 2016) [[URL](http://gregharris.info/a-survey-of-deep-learning-techniques-applied-to-trading/) (broken)] [[PDF](http://www.smallake.kr/wp-content/uploads/2017/04/Survey-1.pdf)].

  Note that many the content overlap with items on this page.

