# apiDoc
### Prompt 
Create API documentation for calling the following method. Provide some feedback for the java developer. Assume the audience is an experienced java developer.

### API
For this method you must provide an array of strings ( needles ) and a string ( haystack ). This method acts as a counter; it counts how many times each string in needles appears in the string haystack. Once the all words have been counted the method prints the word and word count to standard output. 

<p align="center">
<img width="520" height="350" src="javaCode.png">
</p>


### Coding Comments / Feedback 
Here's a list of some feedback on your code. 
1. Line 10 creates **words[]** multiple times. To optimize space complexity it would be better to create a string array that contains all the words in **haystack** only once on line 7, i.e., create **words[]** outside of the for loop. 

2. In addition to my first suggestion, it would be helpful to create a a dictionary from **words[]**. Your key, value pair would be of type String, Integer. The String key would be for each unique word represented in **words[]** and the Integer would count every time the word was in **words[]**. Doing this would allow you to delete **countArray** on line 6. This would also allow you to use a single for loop, instead of three. This loop could include the print statement from line 19. 

3. As the code is now, there are no checks or restrictions for how long **words[]** can be. It seems imprudent to loop through an array of size n at most five times on line 12. Which is why I made my previous suggestion. 
