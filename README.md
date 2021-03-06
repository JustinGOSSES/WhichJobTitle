# WhichJobTitle
A brief notebook to answer the question:
## "Which job title am I actually doing in my current position"
<i>A quick weekend-scale data exploration of:</i> <b>Data Scientist vs. Software Engineer?</b>

## <a href="http://nbviewer.jupyter.org/github/JustinGOSSES/WhichJobTitle/blob/master/Which_Job_Title_Are_You-PartI.ipynb">Part 1</a>: Data Harvest, Data cleaning, and Visualization
## <a href="http://nbviewer.jupyter.org/github/JustinGOSSES/WhichJobTitle/blob/master/Which_Job_Title_Are_You-PartII.ipynb">Part 2</a>: Vectorization, Machine-learning, and Prediction

2018-01 Justin Gosses

## Background
Who is a data scientist isn't exactly an easy question to answer. There are multiple reasons for this. Partly, the confusion comes from the fact that the position hasn't existed, at least in its current form, until quite recently. Managers may not have employed one before and more and more people want to be one. <a href="https://hbr.org/2012/10/data-scientist-the-sexiest-job-of-the-21st-century">Sexiest job of the 21st century</a> and all that malarkey. Additionally, like many jobs, responsibilities vary depending on the size and type of employer. Responsbilities may or may not be divided up between data scientistis, software engineers, data engineers, data visualization engineers, data analysts, etc.
Premise

One source of truth for who is a data scientist is the people hiring data scientists. Of course, there is an argument made against this approach, especially as many of them might be hiring data scientists for the first time. However, they've been helpful enough to provide relatively public descriptions of what skills they think data scientists vs. software engineers have in job advertisements, which makes them a handy if potentially questionable source of truth.

## Basic Process
Normally when trying to do text classification, you might follow an approach like <a href="http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html#training-a-classifier">this</a> or even something else more advanced using NLP specific toolsets. Document similarity is often done on larger documents and larger datasets than my toy examples of a handful of job descriptions, so I opted for a different and more simplistic approach. I might go back and use a larger dataset and more standard NLP approach in future, but this was a weekend project.
- Get a set of several hundred job skils.
- Find which of those skills were in different job descriptions.
- Visualization of skill counts.
- Turn said counts into vectors of features.
- Use job title categories as lables.
- Do quick ExtraTrees classification model to see if the distribution of skill words is predictive of job titles.
- Put my resume run in the model and see whether it predicts I'm a data scientist or a software engineer.

### Optional part B (haven't done this yet):
Port model to JavaScript using <a href="https://github.com/nok/sklearn-porter">sklearn-porter</a> and have it all running live on the front-end so others can throw their resumes in there and see how they are clasified.

# Basic question re-phrased:
What distribution of skills in job descriptions are associated data scientist vs. associated with software engineers?

# Should you use this to evaluate resumes?
### Absolutely not! 
First, it is based on a tiny dataset, which probably doesn't generalize super well. Second, you're optimizing for job descriptions but judging resumes, which have a different format. Third, job skills, meaning your features, change over time. They also vary significantly between jobs. Fourth, although keyword counts are an easy way to not have to look at a lot of applications, they likely weed out many qualified people and let through unqualified people. This type of system is easily gamed by just listing words. Awareness of NLP counts the same as delivered twelve different NLP projects. Someone could also use different words to describe the same thing and have that skill not counted at all, especially if they are describing actual accomplishments.

I work on a team of data scientists. We can get over a hundred intern applications per semester. We anonymize them, and we read them. We could create a word count system. We don't. The only way I would use something like that is if we had a list of skills or experiences we felt strongly were necessary and we gave applicants the exact phrasing to use. 
