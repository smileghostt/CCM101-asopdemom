# Reflection 💭
The following mission felt like a fun break from the rest. A majority of it being a way to analyze it gave me the time to have some fun the whole thing.

Anyways, time to answer questions. Why is it even importat to check the host's resources? Well, this one is relatively simple. Even if the containers are running perfectly, your host system has to provide power to run these containers. If your system's specifications are on the lower end, it can cause some problems for the containers (can include crashes).

Docker logs can easily help point towards the issue at hand. If a user complains about being unable to log into a web application, usually the logs would be able to provide information on what has happened.

Monitoring logs moreso monitors the actions happening within the web application. Monitoring metrics however is focused on the performance of the application rather than the actions within an application.

I believe that large companies run visualizations and such of the containers. Usually this is something integrated within the infrastructure of their system, as thats where the thousands upon thousands of applications reside in. Essentially, they'd have a proper dashboard they use for analytics.

My overall ability to troubleshoot Linux environments did somewhat improve by this alone. Most of this allowed me to understand how to use and log whatever is happening within an environment, however, this can come in handy as I used to be less mindful of logging and analysis.