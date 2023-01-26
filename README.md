# Basic-API-Fuzzer-

 This is a very basic API fuzzer for anyone who is new and just wants a quick look. 
Its an application that finds vulnerabilites by sending random bits of code to the api.

 For the URL section, in the program enter the URL followed by /api to access the API itself.
exapmle       url = "http://example.com/api" <--- just palce the url in the quotes ending with /api

If you have any trouble importing modules just hover the bit, then click download. 

# define the API endpoint and a list of test inputs

import requests 

import random

url = "http://example.com/api"

inputs = [1, 2, "a", "b", "hello", "world"]

# send a request with a random input to the API endpoint

    for input in inputs:

    data = {"input": random.choice(inputs)}
    
    response = requests.post(url, json=data)
    
    print(response.status_code)
    
    print(response.text)
