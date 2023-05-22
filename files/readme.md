Current issues with model (is also listed inside actual script for now):
- check events tool is not a valid tool. This seems to be due to inconsistent inputs from the LLM chain.
- General inconsistency - Sometimes the model doesn't correctly save an event to dictionary, causing the calendar variable as well as 'events.json' to be output as empty.
- add_event_from_string functions does work properly, however it has unnecessary code smell in terms of the try: except:. The exception error seems to always be thrown regardless of function input. Should be tested further to see if this is causing inconsistent performance.
