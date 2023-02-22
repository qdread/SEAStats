---
layout: default
title: Frequently Asked Questions
---

On this page, I answer FAQs that many scientists have asked me. If you have a question that isn't answered here, please feel free to email me or send me a Teams message!

*This document is a work in progress! Last edited 2023-02-22.*

## How can I ask you for help?

Please contact me by email (quentin dot read at usda dot gov) or Microsoft Teams message. I will do my best to get back to you as soon as possible!

## What information should I provide in a help request?

I can provide you a better answer if I know what the goals of your research are, and if I know what your data look like. I would greatly appreciate it if your help request would include at least a few sentences describing the research, including the goal of the research and what specific research questions you are exploring/hypotheses you are testing. Also, if you can provide at least a sample of your raw data so that I can see what format it is in and what kind of variables we will be working with, that's very helpful too. If you have anything like a field map or spreadsheet of treatment assignments that helps clarify the experimental design, that's also helpful for me to look at. 

With all of that said, don't worry too much about providing every single possible piece of information. But if I have the info I need to help you ahead of time, it can make our consultation meetings much more efficient and productive!

## What kinds of statistical analyses can you help with?

- **Power analysis and experimental design**: The old adage is that the best time to consult a statistician is before you start the experiment. I certainly agree, and I am happy to help you determine whether your experimental design is sound and what kind of sample size you will need.
- **Data science (visualization, data cleaning)**: I can help you turn your raw data into a format that you can feed into a statistical model, or help you make graphs and tables to explore patterns in your data.
- **Analyzing experimental and observational data**: This is my bread and butter. I can help you with many different kinds of statistical models from all kinds of studies, whether it is a designed experiment or observational dataset. This ranges from a simple ANOVA design to complex generalized linear mixed models with weird error structures and response distributions.
- **Geospatial data/statistics**: I can help you make maps of your spatial data and fit statistical models that take the spatial pattern in the data into account.
- **Time series**: Though I'm not an expert on time series, I'm learning more every day. I can help you with repeated measures models, forecasting techniques like ARIMA, and GAM models.
- **Machine learning**: Again, I am not an expert but I am constantly trying to learn new machine learning techniques. I can help you with models like random forest and other multivariate clustering techniques.
- **And more ...**: Feel free to ask me about any kind of model or analysis. If I can't help you I will try my best to find people or resources that can give you the help you need.

## What does the help you provide "look like"?

It ranges the whole gamut from a quick email or 10-minute conversation, to a collaboration that can last for months or years. I can answer questions you have, help point you toward resources that can help you learn about the stats or models you need, or review code or text you've written to make sure it's correct. If needed, I can do some analysis for you, or even take the lead on the entire data manipulation, analysis, and presentation workflow. It really depends on your needs. Every project is different! But no matter what, it is a "co-creation" process where we will work together to use your data to tell the story you want to tell.

## Do you have any favorite methods or approaches?

I am a big proponent of Bayesian methods. They are more flexible and allow us to fit models that classical statistical approaches just can't handle. Also, philosophically it's a better way to approach science: classical statistics tries to reject or not reject a null hypothesis, which gives the false impression that the world is black and white and there are "yes or no" answers to our hypotheses about the world. Bayesian statistics is more about estimating the size of the effects and being honest about the level of uncertainty we have for any claim we make about the world. Of course, I know many people haven't been trained in that approach, so I am happy to work with you to learn more about it. Even if you don't become a Bayesian, it's important to at least be familiar with the terminology and the ideas behind it because you will start to see it more and more in the literature as time goes on.

Whether we're working with Bayesian or classical models, I really like GLMMs (generalized linear mixed models). They are a very flexible kind of model that allow us to work with data with all kinds of non-independence in space and time, and all kinds of distributions. 

Bayesian stats and GLMMs are best for "small data" or medium-sized data. When it comes to big data, we have to move to machine learning approaches. As I said above, I am not an expert in those but I am excited to learn with you!

## What statistical programming languages do you use?

I primarily use R. If I do an analysis "from scratch" for a scientist, I usually do the analysis in R and write it up as an RMarkdown notebook. That's a document that includes code, output, figures, and explanatory text all in one place. I find that this is the best way to share my work with scientists. What R packages do I usually use? I do most data manipulation using tidyverse but also use data.table for larger datasets. I use the lme4 or nlme packages for classical statistical analyses, and Stan software coupled with the R packages brms and tidybayes for Bayesian analyses. emmeans and easystats are great packages for supporting all kinds of analyses. For geospatial data stuff, I use the sf package in R as well as occasionally using GDAL and GEOS on the command line.

I am also somewhat experienced with SAS and capable of helping you with your SAS code, as well as Python to a lesser extent. I can also help you with your JMP analysis. But I encourage ARS scientists to use R or at least to familiarize yourselves with it.

## Can you help me with SciNet?

Yes, I have some experience using SciNet and other high-performance computing clusters, and I can probably provide you some help. But for more involved requests, I'd recommend getting in touch with folks from GBRU or asking your question on the SciNet forums.

## How fast can you get something back to me?

I have a lot of ongoing commitments to help out scientists at any given time. I work on a first-come, first-served basis. But I do want to make regular progress on all the projects. So what I do is cycle through all my currently active projects and work on each one for a chunk of time. Currently I'm able to work on each project roughly every 1-2 weeks. Ideally, I would make enough progress each time to send you an update. But typically I will only be able to devote a small percent of time to a specific project in any one week. But you can feel free to email me at any time with questions or clarifications; again I'll address those on a first-come first-served basis as they come in.

Of course, I am willing to make exceptions if there is a rush deadline. The sooner you can let me know, the better, so that I can plan accordingly.

## How do I give you credit for assisting with my analysis?

I do not have a formal publication quota, but I am informally evaluated in part based on the publications and presentations I co-author. Of course, my contribution will vary a lot from project to project. Please consider adding me as a co-author on any paper or other product where I've made a meaningful contribution to the analysis, presentation, and/or writing. If I am a co-author, I promise to hold up my end of the bargain and write any sections for which I am responsible as well as review other parts of the manuscript, including text, figures, and tables. But if my contribution to your project is just a quick consultation or question-and-answer session, co-authorship is not necessary. An informal acknowledgment would be great! 

## Can you help me make my science open and reproducible?

Yes! I am passionate about promoting open and reproducible science in ARS. It's especially important now that the White House has mandated we make all our data publicly available. That should also include the code that turns raw data into a final product with the results of an analysis. I encourage the use of GitHub. I will help you create a private GitHub repository where we can share code and collaborate on our project. When it is time to publish the manuscript, I will help you archive the code from the repository as well as the raw data on [Ag Data Commons](data.nal.usda.gov), the USDA's own data repository. This will ensure that the code and data we produce at USDA provide the biggest possible benefit to society. Soon, it will be a requirement to file a 115 for Ag Data Commons entries; this will help us get credit for the additional work that it takes to make our science open and reproducible.

## What about reviewing my five-year project plan?

I am officially responsible for reviewing all 5-year CRIS project plans for the Southeast Area. The program analysts send me the preplans for each review cycle and I provide comments and feedback, primarily focusing on the experimental design, proposed statistical analyses, and data analysis/management parts of the plans. But if you want to get a head start on the process, I can help at an earlier stage if you send me questions about specific elements of your plan such as experimental design or power calculations.

Incidentally, it isn't necessary to list me as a collaborator on your preplan as I am always available to provide statistical support to SEA scientists whether or not my name appears on your plan.

## Quentin, it's great that you're there to help, but I see there is only one of you for hundreds of scientists. How can I learn to do my own stats?

Learning stats is a journey and a process. You can't learn it overnight. However, I would recommend starting at my [SEAStats training page](/SEAStats) for a gentle introduction to both the statistical models and the tools in R you will need to work with them. On that page I also have links to other helpful tutorials and learning resources. Also, check out the [free online training page on SciNet](https://scinet.usda.gov/training/free-online-training) that my area statistician colleagues Sara and Kathy put together with tons of resources!