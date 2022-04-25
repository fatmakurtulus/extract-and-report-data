# extract-and-report-data
Application that will extract and report data according to the criteria entered from Imdb.com
# PYTHON FINAL PROJECT
Our project is an application that will retrieve and report data according to the 
criteria entered from IMDB.com. 
There is information that should be taken from IMDB. URL’s are individually 
defined based on the content of the movies. Request module is used for this 
operation.
In default version of this program gives the “Top Rated Movies” list. Top Rated 
Movies list are in descending order by the IMDB Rating. It gives the top rated 
first 250 movie.
The program gives user a choice to topic of movie. The user can see the list of 
topics from 1 to 15, the user writes the number of the topic user wants and can 
reach the Top Rated Movies list.
### There are 15 different topics about movies:
1. Action
2. Adventure
3. Animation 
4. Biography
5. Comedy
6. Crime
7. Drama
8. Family
9. Fantasy
10. History
11. Horror
12. Music
13. Romance
14. Sport
15. Western
### The Code Explanation
• The program gets the data of IMDB. However the data cannot be read so 
“soup” is defined and the data becomes readable in the program. For 
example we can see the soup for Comedy topic:
```
soup_Comedy = BeautifulSoup(im_Comedy_Url.content, "html.parser")
```
• Each website has different data. The program wants to get readable data 
from IMDB. After “soup” all datas can be read from IMDB. In “data” 
method the program wants to get all readable data in a tabular form. For 
example we can see data for Comedy topic:
```
data_Comedy = soup_Comedy.find_all("div", {"class": "lister-item modeadvanced"})
```
• A while loop is started and printed to see the topics that the user will 
select in this loop. For example we can see the print function for Comedy 
topic:
```
print("5 - Comedy")
```
• An if condition is opened. According to the topic selected by the user, it 
was selected and printed from the information tabulated with the "data" 
method. For example we can see this print function for Comedy topic:
```
elif select == 5:
 for films_Action in data_Comedy:
 filmTitles = films_Action.find_all("h3", {"class": "lister-itemheader"})
 filmRanking = films_Action.find_all("div", {"class": "inline-block 
ratings-imdb-rating"})
 print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
 print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", 
""))
 print("*" * 50)
 ```
• The program have to consider how user can exit the program. so that if 
user press 0 program will be shut down.
```
 if select == 0:
 break
 ```
• If the user does not press one of the numbers between 1 and 15. The 
program have to tell the user this is a wrong select.
```
else:
 print("Wrong select2.")
 i = 0
 ```
