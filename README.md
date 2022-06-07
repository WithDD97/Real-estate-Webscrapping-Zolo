# Real-estate-Webscrapping-Zolo
A relative was looking for buying a property but with the inflation, property prices were just crazy and too high for a certain budget. So we decided to have a clear idea of the property prices in general and per neighborhood in Toronto.

We web scraped Zolo and grabbed data for 827 houses, 1757 Condos, and 312 Town-Houses for sales ( each cart has 24 articles). The huge majority of :

- Houses: around 7oo k and 5.5M { Mean:  2.5 M}
    - Neighborhood with more properties: Scarborough Village, South Parkdale, Black Creek
    - N_ price under the mean: Yonge-St, North Riverdale, Regent Park, Henry Farm, Church Yonge Corridor …
    - Most expensive:  Niagara
- Condos: around 18o k and 2M { Mean: 1M}
    - Neighborhood with more: East York, Elms-Old Rexdale, Mount Dennis
    - N_ price under the mean: Most
    - Most expensive: Greenwood - Coxwell
- Townhouses: around 7oo k —> 4M {Mean: 1.7M}
    - Neighborhood with more: Woburn, Alderwood, Humberlea-Pelmo, Danforth
    - N_ price under the mean: Milliken, Hillcrest Village
    - Most expensive: Dorset Park

For the web scraping, we used ***Selenium*** mostly because Zolo is a dynamic Website. 

- We **set up a driver** with a specific for each kind of property
- Then **Sign up** through this driver: To sign up, you need to *write your email address* and then write *the access number* that they send you at this address. (Sleep  function to not being caught)
- Grab the information from each page (24 articles per page) and insert them in a dictionary
- Data Cleaning:
    - It wasn’t possible to grab directly the price, number of beds and bathrooms, and the size separately so we define a function for that.
    - Made a column call room = Number of bathrooms + number of beds
    - Put the size at the same format
* 
