## Inspiration
As both sophomore undergraduates recently thrust upon the SWE recruiting world for summer internships, we realized many of our accomplished and technically skilled peers were often screened away after the initial resume screen without being given an opportunity to demonstrate any of their skills. Furthermore, we noticed that the current pipeline of going from resume screen to coding assessment often lacked insight on the actual skill of the user; the current industry metric is simply how many test cases one passes, and often times can be a coin toss as to whether applicants have seen the algorithm or not. At the same time, a formal interview is a significant investment for the hiring company, as it inherently limits the number of applicants which the company can search from to determine an optimal choice. AlgoScout helps address these issues.


## What it does
Users are given a problem and periodically have their code analyzed by our backend. Upon discovering an error in logic or syntax, our helper ai bot provides a hint. They also have their speech recorded which is analyzed alongside a log of these hints in order to provide a more holistic perspective of the skills of the user.
Additionally, interviewers can upload their own problems for interviewees to the playground for the above analysis. 

## How we built it
We used React and Next.js for the frontend and utilized Flask for the backend server. We build distinct  pipelines for hints, error checking, and for the final feedback, fine tuning each to appropriately limit the relevant information (i.e. hints towards logic errors but not explicitly giving the answers to problems). 

## Challenges we ran into
A key challenge was producing GPT output for hints which were both helpful but also did not reveal too much regarding the solution. To address this, we compartmentalized tasks for each individual API call to minimize the bounds in which GPT would respond,  and chained these tasks together. Thanks to Andrew's suggestion, we also took a few shot approach of logging previous hints, suggestions, code states and feeding this material as additional context when determining targeted and personalized overall feedback for a given problem at the end of submission.

## Accomplishments that we're proud of
We're particularly proud of integrating voice-analysis into our application; although at first unsure whether it would work, we noticed that it helped provide a crucial dimension which I believe provides a dimension of significant value add for interviewers wanting to gain insight on the skills and thought processes of their applicants.

## What we learned
We learned quite a bit regarding working with GPT and fine tuning products.


## What's next for Interview Assistant
As hinted by our upload hope to expand this into a full suite with 