# How to find the shoes that fit your foot shape?

This project targeted the problem to find the shoes that fit your foot shape. The approach is to scrape the shoe sole images from websites like 6pm.com and classify them into 3 categories based on predefined shapes.

## Data Scraping from 6pm.com
Zappos.com is an online shoe and clothing retailer based in Las Vegas, Nevada. In July 2009, Amazon announced that it would acquire Zappos in an all-stock deal worth around $1.2 billion. And 6pm.com is a subsidary of Zappos.com with lower price ranges. In the process of scraping, I found that all Amazon.com shoe products share the same images with 6pm.com and Zappos.com. They probably have the largest and most complete stock of shoes online available in the world right now. So this project is applicable to a wider variety of situations. 

A selenium libary is used to scrape because 6pm.com coded their website to specific ip address and a cookie jar had to be used to capture the shoe sole images. 

There are two jupyter notebook files in the directory and the first one is the initial 3400 images scraping with women's size 5.5 and boot style. The latter is with women's size 7 and all styles to capture more samples to compensate for unblanced samples in the first notebook.


## EDA
The images are more blurry compared to online images shown to customers with size 78 * 106 * 3 but ideal for computational efficiency and good enough for classification.

3400 shoe sole images are initially downloaded for classification but after carefull examination, the data 
is quite unblanced between classes so another 20,000 images downloaded for picking a type 3 shoe sole images. Below is a typical image:

##add image here

Most images face the toe to the right and with rare exceptions facing to the left. The images are converted to numpy arrays and saved to csv for modeling. 

There are 3 jupyternotebooks in the EDA folder:
                EDA.ipynb             initial EDA corresponding to the first notebook in datascraping
  EDA-Adjust_labels.ipynb	          EDA corresponding to the second notebook in datascraping with swapped labels
EDA-Adjust_labels_2.ipynb	          EDA corresponding to the second notebook in datascraping with original swapped labels


## Neural Network Modeling
5 different architects are tested first on 3400 images and the conclusion is 2 layers of convolutional neural network with dropouts and 1 single Dense layer converges fastest. 

To optimize accuracy score, different labeling are tested but no obvious improvement showed. There is mainly because shoe manufacters try to "unfit" their shoes to fit more people which makes some shoes are between type 1 and type 2 and hard to classify.  

![NetworkX Force Directed Ego Graph](https://github.com/DataSnek/TwitterNLP/blob/master/Pics/force_ego.png)


## Future Work
To increase accuracy score, I want to try different strategies to classify type 1 and type 2. Here are a few thoughts:
1. Boosting the images to larger sample size.
2. Collect more data for classification, like from 4000 images to 20000 images.
3. Make more classes for "between class" shoes.
4. Different classification methods. There are several methods of classifying foot shapes online and maybe we can use a better metrics to label them.
5. Unsupervised learning. Let the computer decides!



