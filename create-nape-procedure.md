# Your Role

You are an expert Python programmer. Your task is to create a very specific Python script that is one function.  Below you will find the specifications to meet with this function.

## Task Pre-Conditions

Please build a Python file with one condition.  This condition is you can only use libraries within the core Python library. Please DO NOT use any 3rd party libraries. 

I need you to create a one-method Python file.  The Python method is called "evaluate" and takes an argument of "evidence".  For your contenxt, this "evidence" argument is lines of document data that are created as an output from the following code in the main.py file: 

```python

with open(file_path, 'r') as f: evidence = f.readlines()

```

This main.py file will dynamically load the script you are creating, and invoke the execute(evidence) function.

## Function Arguments

This function will return a tuple of two types of data.  

The first element of the tuple is an outcome.  There are only four possible types of outcomes: pass, fail, inconclusive, and error. 

The second element is a reason.  This reason is extremely clear reason of why the pass, fail, inconclusive, or error exists for the outcome

### Tuple Return Tuple - The Outcome Specifications

- The "pass" outcome is provided when the data element is found within the evidence and meets the expected data.
- the "fail" outcome is provided when the data element the python function is found, and it does not exactly meet the expected data.
- the "inconclusive" outcome is provided when the data element cannot be found.
- the "error" outcome is provided when the code attempting to execute in the evaluate(evidence) method and there is a runtime error. Given there is a runtime error, please ensure the reason provides context to the error, and the exact error message.

### The Return Tuple - The Reason Specifications

The reason must be Clear, Unambiguous, and Understandable by a Disinterested 3rd party (CUUD3) who may have very little to zero knowledge of what the function is doing.

For example, if the function is evaluating whether a data field called "mgt_approved" has a status of "true" for an evidence file that is for a travel expense, the following are examples of what a reason that achieves CUUD3 expectations:

- Pass - "The Travel expense is approved because the field 'mgt-approved' is 'true'."
- Fail - "The Travel expense is NOT approved because the field 'mgt-approved is 'false'."
- Inconclusive ('mgt-approved' not found in evidence) - "It is inconclusive if the Travel expense is approved because the field 'mtg-approved' is not found in the evidence."
- Inconclusive ('mgt-approved' is neither true nor false, it has a value of 'test') - "It is inconclusive if the Travel expense is approved because the field 'mtg-approved' was expected to be true or false, but it is neither.  The current field vale is 'test'."
- Error - "An error occurred while evaluating whether the 'mgt-approved' field is true or false. The error is as follows: [The Error Goes Here]"

## Things to Consider For Function Implementation

Think of the CUUD3 approach a very specific form of defensive programming.  Any possible runtime error must be caught and turned into a value.  There should be no possible way that a runtime, or any other error, escapes and is bubbled up, or re-thrown, as an error.  Errors are always values for this appraoch

# An Example Evidence File

The evidence file is in the format of a standard [some file format] file, see the below section "Evidence File" for a sample of the evidence file.

The Python function you are going to write will look to assess the following:

- [Add here with a list for the things you want to assess]

## Requirements To Pass

The condition to pass is as follows:

- [ add the criteria here for a pass, and include how what the reason should be ]

## The Sample Evidence File

```[they type of files]

# Add add your evidence example here

```