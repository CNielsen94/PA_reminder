The main file containing all the functional code is Chatter.ipynb. Later we will refactor and repackage the code in a way that provides a better overview, as well as provide proper documentation for usage.

CalPy is an attempt at utilizing OOP (Object Oriented Programming) in our script. However, due to issues with using the functions in conjunction with our agent chain, we have chosen a more simplistic approach with dictionaries and separate functions. In the future Chatter.ipynb will ideally be using the imported class objects we have defined in CalPy.ipynb.
This means that for now, CalPy.ipynb can be disregarded as it is not being used, and for the project hand-in it most likely will not be part of the package.

Current issues with model (is also listed inside actual script for now):
- check events tool is not a valid tool. This seems to be due to inconsistent inputs from the LLM chain.
- General inconsistency - Sometimes the model doesn't correctly save an event to dictionary, causing the calendar variable as well as 'events.json' to be output as empty.
- add_event_from_string functions does work properly, however it has unnecessary code smell in terms of the try: except:. The exception error seems to always be thrown regardless of function input. Should be tested further to see if this is causing inconsistent performance.
