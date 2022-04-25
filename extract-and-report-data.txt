import requests
from bs4 import BeautifulSoup

im_Url = requests.get("https://www.imdb.com/chart/top/")
im_Action_Url = requests.get("https://www.imdb.com/search/title/?genres=action&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_1")
im_Adventure_Url = requests.get("https://www.imdb.com/search/title/?genres=adventure&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_2")
im_Animation_Url = requests.get("https://www.imdb.com/search/title/?genres=animation&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_3")
im_Biography_Url = requests.get("https://www.imdb.com/search/title/?genres=biography&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_4")
im_Comedy_Url = requests.get("https://www.imdb.com/search/title/?genres=comedy&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_5")
im_Crime_Url = requests.get("https://www.imdb.com/search/title/?genres=crime&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_6")
im_Drama_Url = requests.get("https://www.imdb.com/search/title/?genres=drama&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_7")
im_Family_Url = requests.get("https://www.imdb.com/search/title/?genres=family&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_8")
im_Fantasy_Url = requests.get("https://www.imdb.com/search/title/?genres=fantasy&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_9")
im_History_Url = requests.get("https://www.imdb.com/search/title/?genres=history&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_11")
im_Horror_Url = requests.get("https://www.imdb.com/search/title/?genres=horror&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_12")
im_Music_Url = requests.get("https://www.imdb.com/search/title/?genres=music&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_13")
im_Romance_Url = requests.get("https://www.imdb.com/search/title/?genres=romance&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_16")
im_Sport_Url = requests.get("https://www.imdb.com/search/title/?genres=sport&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_18")
im_Western_Url = requests.get("https://www.imdb.com/search/title/?genres=western&sort=user_rating,desc&title_type=feature&num_votes=25000,&pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=5aab685f-35eb-40f3-95f7-c53f09d542c3&pf_rd_r=HCK85MK228XRD3WTXAM8&pf_rd_s=right-6&pf_rd_t=15506&pf_rd_i=top&ref_=chttp_gnr_21")

soup = BeautifulSoup(im_Url.content, "html.parser")
soup_Action = BeautifulSoup(im_Action_Url.content, "html.parser")
soup_Adventure = BeautifulSoup(im_Adventure_Url.content, "html.parser")
soup_Animation = BeautifulSoup(im_Animation_Url.content, "html.parser")
soup_Biography = BeautifulSoup(im_Biography_Url.content, "html.parser")
soup_Comedy = BeautifulSoup(im_Comedy_Url.content, "html.parser")
soup_Crime = BeautifulSoup(im_Crime_Url.content, "html.parser")
soup_Drama = BeautifulSoup(im_Drama_Url.content, "html.parser")
soup_Family = BeautifulSoup(im_Family_Url.content, "html.parser")
soup_Fantasy = BeautifulSoup(im_Fantasy_Url.content, "html.parser")
soup_History = BeautifulSoup(im_History_Url.content, "html.parser")
soup_Horror = BeautifulSoup(im_Horror_Url.content, "html.parser")
soup_Music = BeautifulSoup(im_Music_Url.content, "html.parser")
soup_Romance = BeautifulSoup(im_Romance_Url.content, "html.parser")
soup_Sport = BeautifulSoup(im_Sport_Url.content, "html.parser")
soup_Western = BeautifulSoup(im_Western_Url.content, "html.parser")

data = soup.find_all("table", {"class": "chart full-width"})
data_Action = soup_Action.find_all("div", {"class": "lister-item mode-advanced"})
data_Adventure = soup_Adventure.find_all("div", {"class": "lister-item mode-advanced"})
data_Animation = soup_Animation.find_all("div", {"class": "lister-item mode-advanced"})
data_Biography = soup_Biography.find_all("div", {"class": "lister-item mode-advanced"})
data_Comedy = soup_Comedy.find_all("div", {"class": "lister-item mode-advanced"})
data_Crime = soup_Crime.find_all("div", {"class": "lister-item mode-advanced"})
data_Drama = soup_Drama.find_all("div", {"class": "lister-item mode-advanced"})
data_Family = soup_Family.find_all("div", {"class": "lister-item mode-advanced"})
data_Fantasy = soup_Fantasy.find_all("div", {"class": "lister-item mode-advanced"})
data_History = soup_History.find_all("div", {"class": "lister-item mode-advanced"})
data_Horror = soup_Horror.find_all("div", {"class": "lister-item mode-advanced"})
data_Music = soup_Music.find_all("div", {"class": "lister-item mode-advanced"})
data_Romance = soup_Romance.find_all("div", {"class": "lister-item mode-advanced"})
data_Sport = soup_Sport.find_all("div", {"class": "lister-item mode-advanced"})
data_Western = soup_Western.find_all("div", {"class": "lister-item mode-advanced"})

filmTable = data[0].contents[len(data[0].contents) - 2]
filmTable = filmTable.find_all("tr")

print("*" * 50)
for films in filmTable:
    filmTitles = films.find_all("td", {"class": "titleColumn"})
    filmRanking = films.find_all("td", {"class": "ratingColumn imdbRating"})
    print("Film Title: " + filmTitles[0].text.replace("\n", ""))
    print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
    print("*" * 50)

i = 0

while i < 1:
    try:
        print("0 - Exit")
        print("1 - Action")
        print("2 - Adventure")
        print("3 - Animation")
        print("4 - Biography")
        print("5 - Comedy")
        print("6 - Crime")
        print("7 - Drama")
        print("8 - Family")
        print("9 - Fantasy")
        print("10 - History")
        print("11 - Horror")
        print("12 - Music")
        print("13 - Romance")
        print("14 - Sport")
        print("15 - Western")
        select = int(input("Select: "))
        if select == 0:
            break

        elif select == 1:
            for films_Action in data_Action:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 2:
            for films_Action in data_Adventure:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 3:
            for films_Action in data_Animation:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 4:
            for films_Action in data_Biography:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 5:
            for films_Action in data_Comedy:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 6:
            for films_Action in data_Crime:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 7:
            for films_Action in data_Drama:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 8:
            for films_Action in data_Family:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 9:
            for films_Action in data_Fantasy:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 10:
            for films_Action in data_History:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 11:
            for films_Action in data_Horror:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 12:
            for films_Action in data_Music:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 13:
            for films_Action in data_Romance:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 14:
            for films_Action in data_Sport:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        elif select == 15:
            for films_Action in data_Western:
                filmTitles = films_Action.find_all("h3", {"class": "lister-item-header"})
                filmRanking = films_Action.find_all("div", {"class": "inline-block ratings-imdb-rating"})
                print("Film Title: \t\t" + filmTitles[0].text.replace("\n", ""))
                print("Film IMDb Rating: \t\t\t" + filmRanking[0].text.replace("\n", ""))
                print("*" * 50)

        else:
            print("Wrong select2.")
            i = 0
    except ValueError:
        print("Wrong select.")
        i = 0

