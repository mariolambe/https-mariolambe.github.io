Python is becoming one of the most popular programming languages when it comes to SEO tasks automation.

People use Python for many different purposes and here you can find a good tutorial if you want to learn more about it.

With this post I will teach you how to extract keywords from Google autocomplete using Python for Keyword Research Opportunities. 

You can run Python from your terminal or cloud-based alternatives such as:

Jupyter Notebooks.
Google Colab.
If you need to share the script with colleagues or friend I would then recommend Google Colab.

The python code is ready to be used, you only need to add as many keywords as you want in the list_a following the same structure.

Example:

```
import requests
import string
import xml.etree.ElementTree as ET


list_a = ["hotel berlin", "hotel new york"]
list_b = [" ", "a", "b", "c", "d", "e", "f", "g", "h", "i", "l", "m", "n", "o", "p", "q", "r", "s", "t", "v", "z",
           "ü", "ä", "ö", "y", "w", "x"] 
list_c = [f"{i} {j}" for i in list_a for j in list_b]
               
for x in list_c:
    apiurl = "http://suggestqueries.google.com/complete/search?output=toolbar&hl=de&q=" + x
    r = requests.get(apiurl)
    tree = ET.fromstring(r.text)
    
    
    for child in tree.iter('suggestion'):
        print(child.attrib['data'])
        ```
