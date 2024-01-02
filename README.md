# hello-world
This is my first real interaction with Github to set up a portfolio for projects that I have done.

---

## Devin S. Wolson 
CISSP | B.S. Cybersecurity at Champlain College.

---

### 13 March 2022

A few months into the Covid-19 Pandemic I lost my job in Automotive Sales of almost 10 years. I had just moved into a +230 year old stone cottage, in need of major renovations, with my wife and 1 year old child. This was a change that we had not forseen but it did not take me long to decide that I needed to make a career choice and within 2 weeks I applied to and was accepted into the Cybersecurity undergraguate program at Champlain College, Online. 

I always have had great interest in computers, coding and technology, in general, and yet never took a deliberate approach to making it the foundation for a career. Starting this journey was very exciting for me and nerve racking because I was only able to transfer in 30 credits of my Associate Degree and only had enough in savings to take me so far. 

I spoke with my academic advisor and schedualed 18credit hours per semester and planned on taking on a full schedule during the summer term as well. This pace would allow me to complete the 3 years of coursework needed for the degree program in 1.5years and finish near the end of my savings. 

This brings me to today, where I am halfway through my last semester of college with a 3.988 GPA, one 3 credit course and a capstone class left. With a sense of relief, disbelief and pride I realize that there is more work to be done to increase my marketability. I have spent so much time on my classes, family and side jobs that I had not taken a real moment to create a portfolio of some of the projects that I have worked on so now that I have a little more time in my schedule I have decided to populate this Github repository with what I have produced, been exposed to and am working on. This post was a great first step in becoming familiar with the *markdown sytax* while following along with the quickstart guide.

Thank you for reading my story and I look forward to sharing what I can. 

### 02 January 2024

Wow, Time flies when you are having fun, or struggling, or on days ending in 'y'. 

So its time for my weak blog attempt of a github page to become a weekly tool that I use to help grow my development abilites. Since my previous/first post so much has changed. I found a wonderful position with a fantastic team at Synack as a weekend ops engineer back in August of 2022. This last year and a third have been action packed with learning and growth in my professional and personal life. 

As you can see its now the second day of 2024.

My most recent professional development has been diving into learning Ruby on Rails by following along with a Free youtube tutorial, https://www.youtube.com/watch?v=fmyvWz5TUWg&t=8117s. This has been a great help in learning the framework and deploying an app locally. This video is a few years old and some of the content in the tutorial did not exactly match up with the latest verson or RoR but I appreciated the effort I needed to put forth to solve any of these misalignments. The biggest struggle I had was with the authorization sign_out routes using the Devise gem. In all of the documentation that I found and in a few tutorials what I had in my code/ routes/ syntax/ etc.. matched what should have worked but when I would attempt to signout a user the app would throw an error claiming that there was no route for [GET] users/signout#destory (or something like this... going from wrote here). I even found a few stakeoverflow posts with possible solutions that did not solve my issue and even Chat GPT was not offering any un attempted or relevant options. 

Then I found a single post where someone had this issue. The default http method used in devise to call the sign_out was set to DELETE (which, as stated, all docs supported) but this person who had the same issue changed this default to GET to match the error of the route and it worked. A 3 letter change solved a 3day runaround 🤡 oh well, now this is something I will not readily forget. 

Next up for me is usint github to version control my RoR project and maybe develop it into a fully functional app with a use case that solves a problem. Im thinking about a Pantry Invenory app that uses AI to scan receipts to take a persons total purchase and break it into individual items and quantites that then fills a .db. Maybe this app will have an option to take available inventory to give meal suggestions. Obviously the app will need a function to remove items from inventory when used/ expired and it should have aletrs for when times get low or run out.
