# ingredientsgenerator
This project takes 150 dessert recipes from foodnetwork.com and uses a character-based RNN to generate new ingredients lists

Given the URLs for 150 dessert recipes, this code scrapes the websites for the ingredients list, cleans and preprocesses the data, and then uses a character-based RNN to generate new ingredients lists. 
The preprocessing is comprised of several steps, including tagging the words in the ingredients as a cardinal "CD" (e.g. two), a unit "UNT" (e.g. teaspoon), a preparation "PRP" (e.g. chopped), or an ingredient "ING" (e.g. sugar), and using the tags to simplify lines of ingredients (e.g. 2 cups plus 2 tablespoons sugar --> 2.125 cups sugar).
The character-based RNN is implemented using Tensorflow, and is built off of the sample RNN publicly available here: https://www.tensorflow.org/tutorials/text/text_generation .

There are four supporting CSV files for this code: cardDict.csv, unitDict.csv, prepDict.csv, and ingrDict.csv, all of which are used to identify words for tagging.
