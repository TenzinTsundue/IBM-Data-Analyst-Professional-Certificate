### WEEK 5

* Simple APIs
* Rest APIs, Webscrapping, and working with files
* Final Exam

*Simple APIs*

*What is an API*
> API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to talk to each other.

*REST APIs*: Representational State Transfer APIs
* REST APIs are used to interact with web services, I.e., Applications that you call through the internet
* They have a set of Rules regarding:
	1. Communication
	2. Input or Request
	3. Output or Response

 *API Keys*: It’s a code used to identify and authenticate an application or user. 
*Endpoint*: Is the one end of the communication channel. When API interacts with another system, the touchpoint of this communication are considered endpoints.

*REST APIs & HTTP Requests*

HTTP: Hypertext Transfer Protocol
Request : You/Client -> Web Server
Response: Web Server -> You/Client  (Rescores)
URL:Uniform Resource Locator
`Scheme | Internet address or Base URL | Route`
`http:// | www.github.com | /tenzintsundue/project.html`

*3 parts to response message*
1. Status line
2. Header
3. Body

Status Code
HTTP Methods

Get request
Post request

*HTML for Webscraping*
>  

Beautiful soup abject

```python 
import request
from bs4 import BeautifulSoup

page = requests.get("http://websiteURL...).text

#Creat a BeaufifulSoup object
soup = BeautifulSoup(page, "html.parser")

# Pulls all instance of <a> tag
artists = soup.find_all('a')

#Clears data of all tags
for artist in artists:
    names = artist.contents[0]
    fullLink = artist.get('href')
    print(names)
    print(fullLink)
```

*Working with different file formats*
* csv:
```
import pandas as pd
file = "FileExample.csv"
df = pd.read_csv(file)
```  
* xml
```
import pandas as pd
import xml.etree.ElementTree as etree
tree = etree.parse("fileExample.xml")
root = tree.getroot()
columns = ["Name", "Phone Number", "Brthdat"]
df = pd.DataFrame(columns = columns)
```
* json:
```
import json
with open('fileSample.json', 'r') as openfile:
    json_object = json.load(openfile)
print(json_object)
```
* xlsx


