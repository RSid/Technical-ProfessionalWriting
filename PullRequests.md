
# Why do code reviews?
* Knowledge-sharing
* Code consistency and legibility
* Catching bugs
* Builds good culture around code quality & consensus
 
# How should we code review?
* I’d suggest that we code review everything, but do it asynchronously through a tool for most PRs and save live code reviews for bigger items 
* Gate merging to master on a single approval for most PRs, maybe require 2 for more major changes
* Use automated code review tool/linters like the Hound where possible, so humans can focus on functionality, not format

# What makes a good PR?
* Terse, descriptive title
* Focused around one narrow, well-defined feature/story
* Roughly 250 lines of code or less. For larger PRs, annotating any points you had doubts on (or alternatively trivial changes that are blowing up the diff like a var rename or file move) will help
* Screenshots of visual changes in PR description if they’re a significant part of the ticket

# What makes a good code review?
* Constructive, positive tone 
* Prefer ‘why did you do x’ or ‘won’t y happen in this scenario’ to ‘you’re wrong’ or ‘that sucks’
* Explicitly differentiate comments that are important to address from matters of taste (though still feel free to surface the latter + agreed up coding standards can still be the former)
* When suggesting refactors, providing code examples is great!
* Pulling down complex branches and exploring them locally 

Citations:
https://sback.it/publications/icse2018seip.pdf
https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/rigby2013convergent.pdf
