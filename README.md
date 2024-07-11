# Report for Assignment 1 resit


## Project chosen


Name: Public APIs


URL: https://github.com/DeninLunja/public-apisSEP


Number of lines of code and the tool used to count it: 1429 lizard
  
![Screenshot of the count](screenshots/Screenshot1.png)

Programming language: Python


## Coverage measurement with existing tool


The tool used to check the coverage of the project was Coverage.py.

![Screenshot of the tool](screenshots/Screenshot2.png)

Commands used to generate the coverage report:
coverage run -m pytest scripts/tests
coverage report


## Coverage improvement


### Individual tests


Function test_find_link_in_text_with_invalid_argument
https://github.com/DeninLunja/public-apisSEP/commit/599712d945d21d50f0d3b56ba0431c171cfb406f


Old function coverage was 50%:
![Screenshot 1 of the function1](screenshots/Screenshot3.png)

![Screenshot 2 of the function1](screenshots/Screenshot4.png)

![Screenshot 3 of the function1](screenshots/Screenshot5.png)

New function coverage is 100%:
![Screenshot 4 of the function1](screenshots/Screenshot6.png)

![Screenshot 5 of the function1](screenshots/Screenshot7.png)

![Screenshot 6 of the function1](screenshots/Screenshot8.png)

This function has been improved. The coverage that was earlier 98% in the test_validate_links.py was increased by 2%. Now, since this is a small increase the overall coverage doesn’t change that much. The coverage improved due to 2 lines that weren't being properly executed in the test.

![Screenshot 7 of the function1](screenshots/Screenshot9.png)

This was fixed by asserting TypeError to each of find_links_in_text in the following way

![Screenshot 8 of the function1](screenshots/Screenshot10.png)


Function test_main_function


https://github.com/DeninLunja/public-apisSEP/commit/7177b6fbaf857fdc37feebb19fff818133868036


Old function coverage was 0%:
![Screenshot 1 of the function2](screenshots/Screenshot11.png)

![Screenshot 2 of the function2](screenshots/Screenshot12.png)

![Screenshot 3 of the function2](screenshots/Screenshot13.png)

New function coverage is 57%:
![Screenshot 4 of the function2](screenshots/Screenshot14.png)

![Screenshot 5 of the function2](screenshots/Screenshot15.png)

![Screenshot 6 of the function2](screenshots/Screenshot16.png)

This is a new test in test_validate_format.py which checks the main function in format.py. The coverage of main was increased by 57%. This function itself also increased the coverage of format.py by 3% (it was 91% before, now it is 94%). This also led to an increase of overall coverage by 1%. It improved because it is testing the main function which there were no test cases for.


### Overall


Overall old coverage:
![Screenshot of the overall old coverage](screenshots/Screenshot17.png)


Overall new coverage:
![Screenshot of the overall new coverage](screenshots/Screenshot18.png)