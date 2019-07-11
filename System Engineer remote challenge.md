System Engineer remote challenge
Thanks for doing our challenge!

We currently have one big user-facing web app ( https://med******.com website & APIs that are
used by mobile apps) in 7 European countries. We are using AWS servers. At peak times we
have around 1000 requests per minute (website and app requests combined). We are using
nginx that forwards application requests to the Rails app via unicorn.
The web application mostly does read-only API requests for Drug data.
Mobile apps have Drug data in a local database so they mostly do read-only API requests for
latest news, ads and medical tools, but also some user-related read/write API requests
(registration, login, changing user profile). Analytics on mobile apps are collected via a 3rd party
service.

Task 1) Web app deployment and scaling
- Describe a plan on how to deploy a Rails app with nginx to a cloud computing service (using
containers/automation/deployment tools of your choice).
- Describe how you will scale this app once request rate grows beyond the unicorn queue of a
single server instance.
- How would you test the deployment process (without testing in production)?
- What approaches do you propose for maintaining security on the API server? We already had
issues with competitors in certain countries crawling our APIs for latest drug data.

Task 2) Event aggregation and data warehouse
Our mobile apps currently generate about 15M events monthly, split over 7 countries and a few
hundred different events.
These are events like "App opened", "Story X opened", "Story Y opened", "Tool N opened". For
purposes of reporting to clients but also for internal analytics, we need to do fast queries over
these events, mostly of the form "Event X in country Y in the period from July 2018 to Dec 2018:
how many times was it done? By how many unique users?"
Describe how you would go about handling this.
- How would you aggregate data from raw (JSON) events?
- What kind of data store would you use?
You're not limited to a particular technology, but have in mind that we're a startup and open
source oriented, so expensive enterprise database solutions are most likely not a good answer.
Altogether, the challenge should take you a few hours, so nothing too crazy. We’d like to see
you send in the results within a week, so you can work on it in your own pace. If you have other
obligations that prevent you from doing the challenge in the next days, do let us know, and we’ll
figure something out.
Best,
Backend team at Med******