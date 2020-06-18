## Testing

TODO: Add motivation

### Code

All projects should attempt to do as much unit testing as possible.
At minimum aim to at least have tests for mission critical algorithms and functions.
Unit tests inside each module cover this nicely but the implementation is dependent on the programming language and environment. 


### Web

A huge part of the web is portability and accessibility, so making sure your website works on all major devices and platforms is very important.


#### Browsers

When testing your website keep in mind the demographic that will be using the site, what devices they are using (mobile vs. desktop), and which browsers.
Preferebly test each deplpoyment on these devices and browsers.
You can see browsers usage statistics [here](https://en.wikipedia.org/wiki/Usage_share_of_web_browsers#Summary_tables) to decide what browsers to test.

Major browsers on desktop are:

- Chrome, 
- Firefox, 
- Safari, and 
- Edge

For mobile, 
- Chrome, 
- Safari. and 
- Samsung Internet

[Caniuse.com](https://caniuse.com/) is helpful if you are unsure about browsers support for specific features.

If for some specific and clear reason a specific browser is needed make sure it is clearly stated on the page.
You can use the [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent) HTTP header to display warnings to all unsopported browsers.


#### Suggested strategy

Keep two entiernly seperate deployments up and running, staging and production.
Deploy all changes first to the staging environment (this can be done automatically).

Preferably have multiple users test all major changes on the staging deployment before deploying to production.
This part could be done automatically but is often time consuming and difficlut to keep up to date.
Suggested tools for automated testing: [Selenium with Python](https://selenium-python.readthedocs.io/index.html) and (Cucumber)[https://github.com/cucumber/cucumber]


## User testing

User testing is a great way to see how the users interact with your product. 
However, user testing is difficult to do well. When doing user tests keep the following points in mind.

#### User tests should only be used if you have planned time to make adjustments

There is no reason to spend time user testing if the results won't be used to make adjustments and improve the product.

#### User testing should focus on a specific task

Focusing on a specific scope or task helps to keep the user focusing on what is important.
This does not mean the same user can not test different tasks, only that each task you give the users should be clearly defined.

#### Up to 4 people for tests

Asking too many users to do the same tests will only result in more of the same responses.
Every users experience matters and should be taken into account.
If you have more users to test think about trying to test different things or do another round when adjustments have been made from the first one.

#### Testing prototypes often gives no useful information 

Users will most likely point out things that you know are missing and are less likely to give the feedback you are looking for.
This can be reduced somewhat by targetting very specific tasks early in the development, see point about specific tasks.
