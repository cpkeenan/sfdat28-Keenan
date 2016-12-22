For my project, I decided to use a DrivenData competition dataset with the goal of determining the functionality of water wells in Tanzania. Using the provided training set, I should be able to predict whether the well is functioning, non functioning, or functioning but needs repairs based on a variety of factors including water quality, current quantity, latitude, longitude, and last year of construction. I have three goals for this project. One to complete the project and in so doing pass the class. The second goal is to be able to claim a spot on the competition leaderboard. The current leader in the competition has a projected prediction rate of around 82%. I would like to use the techniques I’ve learned in this class to match or exceed that success rate. The third goal is to make the project business relevant for my company. The goal now becomes to succinctly describe how I achieved each step in the process.

*Cleaning*

After analyzing the data, I determined that several columns needed to be dropped from the overall dataset but they did not have any real significance after continued analysis so I did not see this as a problem. I merged my two datasets together to make a training set and I grouped the response values (status_group) into 2 categories (functional and non functional) from 3 categories (the third being functional but in need of repairs). I thought that if the well is still functional and needs repairs, it is still considered functional and could be combined with that group to improve the dataset.

*EDA*

I produced several visuals that you will be able to see in my code and tried to determine any relationship between the variables. Construction year, water type, and latitude and longitude all seemed to have potential. My main visualization was plotting the location of the wells using latitude and longitude and the response with Tableau as well as plotting by GPS height to determine if geography might play any part. The analysis was inconclusive from the map but I am looking forward to exploring it further. A heatmap of the other variables allowed me to pick several values that seemed to show relationships between the responses so I decided to keep two sets of features: one set that seemed intuitive and one that I generated from feature selection using EDA.

*Modeling*

When it came to modeling the data, the simpler the model I used, the more successful the result. I claim that this is more to do with overfitting and competency but I was pleased that I got a result in the first place for each model. Between my two datasets, my KNN model achieved around 89% accuracy, which is more than enough to post on the leaderboard for DrivenData so with some more tuning I will consider posting on their site.

Using the two datasets, logistic regression was able to achieve about 68% accuracy after testing. I was pleased that it was competitive but I think that I have to reanalyze what features are most important in my EDA if I were to continue tuning this model.

My decision tree displayed that the most important variable I had chosen in each set of features was Quantity. The worst part about that is that I realized I had included Quantity in each set of features. However, I was able to find some relatively pure nodes that would allow me to use the tree for several degrees of certainty. To remedy the initial issue I found, I’ll have to go back to the drawing board similar to my logistic regression model.

My random forest optimum displayed an 80% true positive to 40% false positive using ROC AUC. I thought this was a reasonable because I would choose a high true positive because the false positive rate wouldn’t be considered a waste of resources if the repair team was deployed to the well site. The worst that could happen is that the team would survey the well and find that it did not actually need repairs. I did not find this to be an issue so I was pleased with the result.
Using this as a basis for addressing Goal #2, I am proud that I achieved a KNN accuracy score that would challenge the leaders in the competition. I am fairly confident the model is overfit but happy to have beaten the null and the competition to achieve my second goal.

*Business Relevance*

The task of making this project business relevant was eluding me until I changed roles at my current employer. I was tempted to use our massive amounts of logistics data to put together a project that would benefit the company from an efficiency standpoint. When wrangling the data became too complicated, I moved to the above stated dataset and decided to devise a reason why this series of models would matter to Clorox and its Sales teams. It struck me that Clorox has two businesses involved in access to clean water: our bleach business and Brita. This allowed me to conclude that those two business would be interested in learning if they could use data to aid in access to clean water or ways to determine places that might need access to sanitization stations for safe drinking water so I proceeded to develop my models through the lens that my models would be sponsored by my company and deployed to aid communities with limited access to fresh and safe water. Goal #3 complete.

*Conclusion*

Goal #1 is still up in the air, but I think that with the creation of my models, my supporting materials, this paper, and a wicked PechaKucha, again, I have faith that I have done enough(?) to at least get a pass and continue to benefit from being given the keys to the kingdom of data science. Now it’s time to put some of this knowledge to good use and make some money.


