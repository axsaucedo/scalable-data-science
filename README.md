# Scaling Data Science Capabilities with Python

## [View Live Presentation](https://axsauze.github.io/scalable-data-science/#/)

Scalable Data Science in Python

## Running Presentation

You can also run the presentation on a local web server. Clone this repository and run the presentation like so:

```
npm install
grunt serve
```

The presentation can now be accessed on `localhost:8080`. Note that this web application is configured to bind to hostname `0.0.0.0`, which means that once the Grunt server is running, it will be accessible from external hosts as well (using the current host's public IP address).

# Presentation Index

# Overview
* Introduction
* Motivations for talk / examples of why scalable data science is necessary
    * Team deploying one model is not bad
    * Having 3-4 models running in production starts getting complicated
    * As data science team grows, a lot of implications arise
    * Several models are running in production
    * Complexity increases for deploying containers
    * When something goes wrong it's hard to trace back the reason why
    * It's also hard to fix the issue because of lack of understanding of issues
    * It becomes hard to have reproducibility when something goes wrong
    * And this becomes an issue for compliance, as it's required to know what goes in where
* Breaking down the scalability issues into buckets
    * Deployment - Release a new model
        * Continuous integration & continuous deployment
        * Monitoring - Want to track a model
            * Monitoring for model bias
            * Monitoring for anomalities
    * Reproducibility
        * Versioning - Want to revert back
        * Compliance - Something goes wrong
        * Development - People wanting to use their own technologies (TF, Spark, sklearn, etc)
        * Data storage/standardisation
        * Orchestration of Dataflows


# Breakdown topic

* In this talk I want to focus on two things:
    * The concepts available 
    * The tools out there
    * A practical example building our own
* Often the conversation is foucsed on 
    * Model development
    * Model serving
* When we only have a small team of data scientists
    * It all works relatively well
    * There is a relatively small number of models to maintain
    * Development and deployment may work as all knowledge lives on people's heads
* As the data science team grows however...
    * Increasing number of models are being developed and deployed to production
    * Complexity increases for deploying containers
    * When something goes wrong it's hard to trace back the reason why (DSs blame SEs and vice-versa)
    * It's also hard to fix the issue because of lack of understanding of issues
    * It becomes hard to have reproducibility when something goes wrong
    * And this becomes an issue for compliance, as it's required to know what goes in where
* It becomes a wider challenge beyond simple building/deploying
    * But thankfully this is a challenge that many people have been facing for a long time
    * There are a lot of tools out there - so many it can be overwhelming
    * But that's why we're going to do a deep dive 
* To reduce complexity, we will still break these down into development and production
    * There is some ambiguity as some actually are relevant in both sides, but we'll separate them for the sake of simplicity
    * Model Development 
        * This encompasses all the phases around discovery, including exploration of data ingestion, data cleaning, 
        * Versioning - Want to revert back
        * Development - People wanting to use their own technologies (TF, Spark, sklearn, etc)
        * Data storage/standardisation
        * Continuous Integration

    * Model Serving 
        * Continuous Deployment 
        * Compliance - Something goes wrong
            * Storing data from inputs / outputs
        * Monitoring - Want to track a model
            * Monitoring for model bias
            * Monitoring for anomalities
        * Orchestration of DataFlows
            * ETL / Data pipelines
            * Data streams

    




