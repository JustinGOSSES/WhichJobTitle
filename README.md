# WhichJobTitle
A brief notebook to answer the question:
## "Which job title am I actually doing in my current position"
<i>A quick data exploration of:</i> <b>Data Scientist vs. Software Engineer?</b>

## <a href="http://nbviewer.jupyter.org/github/JustinGOSSES/WhichJobTitle/blob/master/Which_Job_Title_Are_You-PartI.ipynb">Part 1</a>: Data Harvert, Data cleaning, and Visualization

2018-01 Justin Gosses

## Background
Who is a data scientist isn't exactly an easy question to answer. There are multiple reasons for this. Partly, the confusion comes from the fact that the position hasn't existed, at least in its current form, until quite recently. Managers may not have employed one before and more and more people want to be one. Sexiest job of the 21st century and all that malarkey. Additionally, like many jobs, responsibilities vary depending on the size and type of employer. Responsbilities may or may not be divided up between data scientistis, software engineers, data engineers, data visualization engineers, data analysts, etc.
Premise

One source of truth for who is a data scientist is the people hiring data scientists. Of course, there is an argument made against this approach, especially as many of them might be hiring data scientists for the first time. However, they've been helpful enough to provide relatively public descriptions of what skills they think data scientists vs. software engineers have in job advertisements, which makes them a handy if potentially questionable source of truth.

## Basic Process
Normally when trying to do text classification, you might follow an approach like this or even something else more advanced using NLP specific toolsets. Document similarity is often done on larger documents and larger datasets than my toy examples of a handful of job descriptions, so I opted for a different and more simplistic approach. I might go back and use a larger dataset and more standard NLP approach in future, but this was a weekend project.
- Get a set of several hundred job skils.
- Find which of those skills were in different job descriptions.
- Visualization of skill counts.
- Turn said counts into vectors of features.
- Use job title categories as lables.
- Do quick random forest and Support Vector Machine models to see if the distribution of skill words is predictive of job titles.
- Put my resume run in the model and see whether it predicts I'm a data scientist or a software engineer.

### Optional part B (haven't done this yet):
Port model to JavaScript using sklearn-porter and have it all running live on the front-end so others can throw their resumes in there and see how they are clasified.

# Basic question re-phrased:
What distribution of skills in job descriptions are associated data scientist vs. associated with software engineers?
