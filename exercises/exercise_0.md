# Exercise 0 - PydanticAI and OpenRouter

In this exercise, you get to work with data validation using Pydantic v2 and PydanticAI. Output in general from LLMs are unstructured and hard to work with, to get any value from it you need to structure the output and validate its contents. This can be done with Pydantic.

## 0. Summarize job ads

In the data folder, there are a few job ads taken from arbetsförmedlingen.se.

a) Read all the jobs ads into python

b) Create a function that uses PydanticAI agent to summarize a job ad. This function should take in an ad as its parameter and return a summary.

c) Now create and export markdown files for each job ad and its corresponding summary.

d) Try to take other job ads from arbetsförmedlingen.se and see how well your function performs.

e) Make the output structured using a pydantic model together with PydanticAI agent. The output from the agent should have the following fields: 
- job_title
- description 
- summary 
- responsibilities 
- words_in_article

## 1. Product extractor

In this task you will based on product descriptions, be able to extract out relevant information into structured format using pydantic model together with PydanticAI agent.  

a) Read the `products.json` and store all of its descriptions into a list 

b) Loop through this list and extract structured output from each of the descriptions. The structure should have the fields: name, price, category, in_stock and description 

c) Now try to validate programmatically if the output fields are correct. 

> [!NOTE] 
> some of the fields might be straightforward as some others might require the use of another LLM agent




## 2. Theory questions

DESCRIPTION

&nbsp; a)

&nbsp; b)

&nbsp; c)

## Glossary

Fill in this table either by copying this into your own markdown file or copy it into a spreadsheet if you feel that is easier to work with.

| terminology | explanation |
| ----------- | ----------- |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
|             |             |
