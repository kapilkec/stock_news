# IMPORT ALL THE REQUIRED LIBRARIES
from bs4 import BeautifulSoup as BS
import requests as req
symbol = input("Enter stock name to get news")
url = f"https://www.businesstoday.in/topic/{symbol}"
  
webpage = req.get(url)
trav = BS(webpage.content, "html.parser")

data = trav.find_all("div", class_ = "newcon-main")
# rows = data.find_all("li")
for i in data:
    a = i.find("a") 
    print("link:\n",a.get("href"))
    print("title:\n",a.get("title"))
    print('--------------------------\n\n\n')
