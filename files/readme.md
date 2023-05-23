The main file containing all the functional code is Chatter.ipynb. Later we will refactor and repackage the code in a way that provides a better overview, as well as provide proper documentation for usage.
In order to run the model, you will need to replace the empty string with an API key inside apikey.py, as this is imported and saved as a environment variable for security reasons.

CalPy is an attempt at utilizing OOP (Object Oriented Programming) in our script. However, due to issues with using the functions in conjunction with our agent chain, we have chosen a more simplistic approach with dictionaries and separate functions. In the future Chatter.ipynb will ideally be using the imported class objects we have defined in CalPy.ipynb.
This means that for now, CalPy.ipynb can be disregarded as it is not being used, and for the project hand-in it most likely will not be part of the package.

Current issues with project:
- check events tool is not a valid tool. This seems to be due to inconsistent inputs from the LLM chain.
- General inconsistency - Sometimes the model doesn't correctly save an event to dictionary, causing the calendar variable as well as 'events.json' to be output as empty.
- add_event_from_string functions does work properly, however the LLM model has issues with usage of quotation marks. By default it wraps a string with single quotation, which causes an input if it attempts to use an apostrophe mid sentence/word. For example; correct input = 'doctors appointment, 12-06-01-12-00', wrong input = 'doctor's appointment, 12-06-01-12-00'. 
