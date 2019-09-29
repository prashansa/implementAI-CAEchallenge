# implementAI-CAEchallenge
**The Goal** 
The dataset contains of a maneuver being performed by various pilots. Under this maneuver, 10 features like velocity, altitudes etc are measured over time creating a time series for each. Each pilot is then tagged for being competent or incompetent. We were to find patterns in this multi-dimensional dataset that revealed soft skills dependence. This was a challenge, since I had never worked on such a dataset before. It was also amazing because this is the kind of dataset that can exist in any industry and therefore the skills I learn will be much more widely applicable. 

**What I Did**
While no concrete model could be built, many approaches to look at the data were tried. 

Starting with a little data processing: the data was parsed from a .csv file, NaN values taken care of etc in order to make data workable.

I then tried to visualize the data by plotting different features separately, looking for correlations that could speak for the kind of label that it had. for example, I looked at skew and kurtosis of the time series for each feature, and plotted them. Implicitly, I was looking to find clusters within uncertainities, so that I could use kMeans and the clusters would speak of the label. 

Then, I started with a simple linear regression fit which would reduce the dimensionality of each pilot's data into significantly fewer variables obtained from the similarity criteria. 

Then RandomForest method was tried which could help predict the label when passing the ten flight parameters into the algorithm.

Then Gaussian Process Classifier was attempted. The training data set contained about 600 data points in the time series of any given feature for any given pilot. So it could be assumed that the values come from a Gaussian, and I tried to fit the time series using Gaussian Processes. Thinking that the loglikelihood values could somehow correlate with the given label. I then tried PCA, where I blindly applied PCA to the entire dataset for a given Pilot, obtained the first main component and tried to classify that for 0 or 1 label, but that was also not successful, since the first main component would always have nearly the same value. 

Then I thought of modelling using a neural network. We cannot directly feed the entire dataset into the network, but we could use one more step before like the PCA or Regression that fits for the label. I could fit for the weights for each parameter! 

**Challenges I faced**
This entire exercise was new to me. So was definitely a challenge to think about such a dataset. The number of methods applicable could be numerous, but each have their own caveat which needs to be taken care of while implementing. Understanding uncertainities was definitely one big challenge. 

**What I Learned**
When I first looked at the challenge, my immediate response was to look at one straight method that could answer the question, but ofcourse I quickly learned that I cannot aspire for those in real life problems. Then even with the methods at my disposal, I could not estimate error bars on the data which I think would be important for determining trends. 
I learned that I was actually having fun doing this entire exercise and that I should explore more of this! 

I am glad this will be a good starting point of my journey :D 
