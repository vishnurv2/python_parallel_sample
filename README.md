# Parallel Testing on LambdaTest

This project contains 3 files. Each of the files is described below.

`browsers.json` - This file specifies the browser capabilites for the tests. Here, each test would be run in these two browsers. 

    [
      {
        "platform" : "Windows 10",
         "browserName" : "Chrome",
         "version" : "91.0"
      },
      {
        "platform" : "MacOS Big sur",
        "browserName" : "Safari",
        "version" : "14.0"
      },
    ]


`test.py <browsers.json> <capability id>` - This file contains the selenium test which would be run in each of the browsers specificed by "browsers.json". 

`run_parallel_tests.py <test.py> <browsers.json>` - This is the runner which runs the tests in parallel.  

To run the tests in parallel execute the following command:

```sh
python3 run_parallel_tests.py test.py browsers.json
```
