The main file containing all the functional code is Chatter.ipynb. Later we will refactor and repackage the code in a way that provides a better overview, as well as provide proper documentation for usage.
In order to run the model, you will need to replace the empty string with an API key inside apikey.py, as this is imported and saved as a environment variable for security reasons.

CalPy is an attempt at utilizing OOP (Object Oriented Programming) in our script. However, due to issues with using the functions in conjunction with our agent chain, we have chosen a more simplistic approach with dictionaries and separate functions. In the future Chatter.ipynb will ideally be using the imported class objects from the CalPy script.
This means that for now, CalPy.ipynb can be disregarded as it is not being used, and for the project hand-in it most likely will not be part of the package.

Current issues with project:
- A tool that can create recurrent events needs to be added, as this is necessary for scheduling when medicine or other reacurring events should happen.
- It is lacking a reminder functionality. As for right now, the model can correctly tell you about the scheduled calendar, as well as plan and cancel events within, but this only happens when the model is being called directly. This functionality should not have to be a tool for the agent-chain, but rather a separate function that checks the current date within the calendar, and if an event exists on current date, it should return those events and timestamps.
