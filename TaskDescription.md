# Sentiment Analysis For Smartphones

Hello,

As founding partner and SVP, I would like to personally welcome you to Alert Analytics. I’m excited to have you join the team. You will be working on a challenging project to analyze sentiment on the web toward a number of smart phones for Helio, a smart phone and tablet app developer. You will be taking over this project from Amy Gorman, one of our most experienced analysts. She has made significant progress, but there is still a lot left to do. Before we dig into the details of what I will need you to do, let me give you some background on our client, what they are trying to accomplish, our general approach to the project, and what Amy has accomplished so far.

Project Background

Helio is working with a government health agency to create a suite of smart phone medical apps for use by aid workers in developing countries. This suite of apps will enable the aid workers to manage local health conditions by facilitating communication with medical professionals located elsewhere. The government agency requires that the app suite be bundled with one model of smart phone. The Helio project manager called me yesterday with some new developments. The initial discussions with Apple and Samsung have progressed over the last few weeks. At this point, they would like us to prioritize—and of course speed up if we can—our sentiment analysis of the iPhone and the Galaxy over the other handsets in the short list. To help Helio narrow their list down to one device, they have asked us to examine the prevalence of positive and negative attitudes toward these devices on the web. The goal of this project is to provide our client with a report that contains an analysis of sentiment toward the target devices, as well as a description of the methods and processes we used to arrive at our conclusions.

Our Approach to the Project

Although there are a number of ways to capture sentiment from text documents, our general approach to this project is to count words associated with sentiment toward these devices within relevant documents on the web. We then leverage this data and machine learning methods to look for patterns in the documents that enable us to label each of these documents with a value that represents the level of positive or negative sentiment toward each of these devices. We then analyze and compare the frequency and distribution of the sentiment for each of these devices.

In order to really gauge the sentiment toward these devices, we must do this on a very large scale. To that end, we use the cloud computing platform provided by Amazon Web Services (AWS) to conduct the analysis. The data sets we analyze will come from Common Crawl. Common Crawl is an open repository of web crawl data (over 5 billion pages so far) that is stored on Amazon’s Public Data Sets.

Progress to Date

The first thing Amy did was to figure out what data to collect from each document in Common Crawl that would enable us to determine if the document was relevant to our analysis. As you can imagine, only a very small fraction of the billions of webpages are going to be expressing useful sentiment about the devices we are interested in. Then she determined what data to collect from each webpage to enable us to assess if the review was strongly positive, strongly negative, or somewhere in between. Next, she wrote Python mapper, reducer, and output aggregator programs to efficiently collect and compile this data across the billions of documents on the Common Crawl. She then put this data into a matrix that contains approximately 12,000 entries (we call it the small data matrix).

I have forwarded an email from Amy that includes the small data matrix she developed. Please look it over. We are in the process of manually labeling this subset of documents with a sentiment rating that you will use later in the process to develop machine learning models capable of determining web page sentiment automatically. You’ll then use those models to review a much larger set of web pages and build a data matrix at least an order of magnitude larger for the complete analysis.

Your Job on the Project

Your job during the course of this project is to collect and develop a data matrix in the range of 20 thousand instances (called the large data matrix) of relevant web documents from the Common Crawl. Using Amy’s labeled small matrices, you will create models in R that understand the sentiment patterns within the data. Then you will apply your models to the large matrices you collected to understand their sentiment scores. Lastly you will analyze this large labeled data matrix and report descriptive statistics to the client on the level of sentiment toward the handsets.

Immediate Next Steps

You will need to quickly setup and become familiar Amazon Web Services. The specific AWS services that you will be employing include Elastic Compute Cloud (EC2), Elastic MapReduce (EMR), and Simple Storage Service (S3), where you will process the Common Crawl data to develop the large data matrix. Common Crawl is stored on Amazon’s Public Data Sets, so you will be able to access it directly for map-reducing processing.

Glad to have you onboard!

Michael

Michael Ortiz
Senior Vice-President
Alert! Analytics

Source: University of Texas Data Analytics Certificate Program
