This is my solution to the trackstreet Ebay Crawler challenge.

The crawler extracts the title, url, price and condition for each Ebay product from a given URL and stores it json files for each product that matches the user's conditions.

QUICKSTART:

1- Install the libraries in the 'requirements.txt' file;
    Example: pip install -r requirements.txt

2- Open the file 'ebay-crawler.py' and set the 'crawl_ebay()' parameters. 
    Ps.: If the user does not pass the 'condition_filter' or if its value is None, the crawler will save all products that it finds.
         To filter the desired condition, simply pass a value to 'condition_filter' and the crawler will only save the products that match the user's condition.
         Example: item_list = crawl_ebay(url, headers, condition_filter = "new")

3- Run the 'ebay-crawler.py' file

OUTPUT: 
The script will create a directory 'data' and save a json file for each crawled product inside of it.

Example Output: {
                    "title": "Samsung M393A4K40BB1-CRC4Q 32GB PC4-2400T 2Rx4 error-correcting C\u00f3digo Reg DDR4 19200",
                    "product_url": "https://www.ebay.com/itm/234177234445?epid=23032716228&itmmeta=01HVA60ARWBVK57SQ330DA11SY&hash=item36860d060d:g:3xkAAOSw2jRkHczT",
                    "price": "R$ 584,58",
                    "condition": "Seminovo"
                 }   