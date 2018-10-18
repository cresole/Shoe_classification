Problem Statement and EDA of Capstone

Problem Statement: People have different foot shapes but shoe manufacturers don’t have a standard to categorize their products for people to understand and choose easily.  Many people wear shoes those are not comfortable to them due to this or have to return their online purchases frequently which cost a lot of hassle in this busy working world. This project tries to categorize shoes based on their shapes for people with different foot shapes.

Strategy: 
Shoes websites often provide pictures from different sides of shoes and we can use the sole picture to identify if the shoes have a high probability of fitting a person’s feet. Based on this, we can make recommendations  to clients to save their search time.

Methodology:
Get the shoe sole pictures for shoes in a certain category(for example, women boots, size 5.5), compare them with our sample pictures of shoe shapes and classify them using neural network algorithm.

Assumptions:
We simplify the foot shapes to 4 ~ 5 categories while in reality, there could be more.
Need to mark pictures of shoe soles based on personal experience to make it a supervised machine learning problem, which may not be completely accurate.

Metrics:
Accuracy >  95% 
Balance false positives and false negatives.

Future Work:
Create an algorithm if we can classify the shoe box is able to handle upturned big toe.
Extend this problem to more merchandise, like clothes based on their own characteristics, for example, the shape of a dress for different body shapes.

Progress:
Extracted 3420 shoe sole pictures from 6pm.com with “boots” category in size 5.5 and saved them to folders with Pandas DataFrame to mark them. (This takes about 1.5 hours for python). The picture qualities are acceptable. But 6pm.com seems to have used some compression algorithms which I don’t have. Each picture is about 1~2 KB.
Find sample foot shapes online. This is extremely hard to find. I might need to draw them.



