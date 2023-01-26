# Basic-API-Fuzzer-

// This is a very basic API fuzzer for anyone who is new and just wants a quick look. 
ITs an application that find vulnerabilites by sending random bit of code.

//Also for the URL section in the code ass the URL followed by /api to access the API itself 
exapmle       url = "http://example.com/api" <--- just palce the url in the quotes ending with /api


import requests
import random

# define the API endpoint and a list of test inputs
url = "http://example.com/api"
inputs = [1, 2, "a", "b", "hello", "world"]

# send a request with a random input to the API endpoint
for input in inputs:
    data = {"input": random.choice(inputs)}
    response = requests.post(url, json=data)
    print(response.status_code)
    print(response.text)
