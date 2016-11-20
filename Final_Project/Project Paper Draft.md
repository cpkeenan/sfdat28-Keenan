For my project, I decided use a DrivenData competition dataset with the goal to determine the functionality of water wells in Tanzania. Using the provided training set, I should be able to predict whether the well is functioning or non-functioning based on a variety of factors including water quality, current quantity, latitude, longitude, and several factors that I have still yet to determine how viable they are. The current leader in the competition has a projected prediction rate of around 82%. I would like to use the techniques I’ve learned in this class to match or exceed that success rate.
 
I am still exploring how to clean the dataset. I grouped the y variable (status_group) into 2 categories (functional and non functional) from 3 categories (the third being functional but in need of repairs) and changed that to a numerical response. I also grouped the functional but needs repairs group into the functional group. I have yet to determine how to replace null values. I think that if I drop certain columns that have the majority of null values, I’ll also lose the majority of my data so I have to determine a workaround.

I have produced several visuals and tried to determine correlation between any of the variables. Construction year, water type, and latitude and longitude all seem to have potential. I still have to continue to explore the other features.

My major visualization is plotting the location of the wells using latitiude and longitude with basemap. I am exploring other visualization packages to make a more aesthetically pleasing map. Also looking to incorporate the response into the map using marker color as well as introducing topography because the dataset provides the GPS height of the well. I think the visualization will really help determine what variable to consider.

My initial plan was to use KNN to model the prediction, but I will also try to use a basic decision tree, a random forest, several of the newer models we just recently demoed including PCA, and then trying to pipe several together to get a faster and more successful result.


