### Introduction
Android applications (apps for short) often need to display images. However, inefficient image displaying (IID) issues are pervasive in mobile apps, and can severely impact app performance and user experience.
RECIPE is a dynamic analyses tool for detecting IID issues in Android apps by harnessing the combined power of domain knowledge of IID issues and existing functional test cases. 
RECIPE reuses and mutates existing functional test cases to construct new test cases that can be used to exposed IID issues. 
We have applied RECIPE to real-world open-source Android apps, and RECIPE can effectively detect previous unknow IID issues.

### Motivating Example


### Approach Framework


### Approach Evaluation
We performed an empirical evaluation to investigate the effectiveness of RECIPE on detecting IID issues in real-world Android apps. 

#### Data set

##### Subjects
we selected 16 real world open-source Android apps as our evaluation subject.
Each selected Android app meets the following there selection criteria:
(1)Open-source: hosted on GitHub with an issue tracking system.
(2)Under maintenance}: having update operations within the last six months.
(3)Of realistic usage}: having over 10,000 downloads on the Google play market.

##### Functional test cases
For each selected Android app, we downloaded the latest version of it and gave a recruited tester (a post-graduate student whose research field is testing and analysis of Android apps) one hour to familiarize the app and manual construct typical replayable functional test cases.
The choice of constructing functional test cases manually is build on a fair intuition that humans are good at sketching the major functionalities of an Android app.


##### Results


Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.


## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/struggggle/RECIPE/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

