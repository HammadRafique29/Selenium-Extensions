## Instructions

Here is how to load a chrome extension into chrome Selenium Python

Date = 20-12-19
Chrome version = 79.0.3945.88

The new version of Chrome support crx.crx (crx3) and if you use crx it will throw an error.
If you are using chrome version 73 or above then only follow this step


1> Crate a crx3 file.
1. Go to Chrome web store and search you Extension, copy the link of the extension. Screen shot
2. Go to this site and paste the link and download crx file for your Chrome extension.
3. Go to this GitHub page and download the module which will convert your crx file to crx3 or crx.crx.
4. Now you have your crx.crx or (crx3) file

**2> Python Code to Add chrome extension in selenium**
1. Put your extension.crx.crx file in the same folder as your code or give the path
2. You can copy-paste this code and just change the file crx.crx name at `chrome_options.add_extension(' YOUR - EXTENSION - NAME ')`

import os
    from selenium import webdriver
    from selenium.webdriver.chrome.options import Options
    
    
    executable_path = "/webdrivers"
    os.environ["webdriver.chrome.driver"] = executable_path
    
    chrome_options = Options()

    chrome_options.add_extension('  YOUR - EXTIONTION  - NAME    ')
    
    driver = webdriver.Chrome(chrome_options=chrome_options)
    driver.get("http://stackoverflow.com")