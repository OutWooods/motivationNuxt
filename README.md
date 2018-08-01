# What??!

This is the second of the 2 nuxt projects.

This is one of two competeing repos of mine. They may all die, or be finished uncompleted. But they're all about just dipping into and playing about with vue, nuxt and some other libraries I thought looked cool. 

The reason I decided to approach it like this, is that I'm crazy prone to thinking of an idea, starting it. Setting it up. And then having a new idea the next day and abandoning it. So, I spent 3 weeks, writing down all the random ideas I had. Saw which I spent the most time thinking about, and then marked them as the big three that I would test out. 

The next three weeks (Edit until the end of August) I'm only allowed to do these two projects (I culled one as it was dead), but I can do whatever ones I want of them. And over time, hopefully, one will turn out to reign supreme.  --Currently leading is this one. 

### So whats this one?

This is a motivation, or target tracking site. Essentially, when you meet a target you get to fill in a pixl in a screen. 
Gradualy over time these build up and up as a measure of your success. So you get a satisfying image as you achieve. 
Hopefully also the pixels move and form a mini-universe, with sounds to make it even cooler. 

I felt this was a nice balance as its little enough that you don't just do it 'to get points' (as I find this works 
for a short period of time, but ineffective to build long term motivation to do habits) but also gives you a sense of pride 
over time. It also motivates me to log my goals, which I am not great at, and I know massively increases my ability to meet targets anyway. 

This was heavily influenced by the project (insert link here). As they produced a pretty awesome looking website. I also wanted to learn about gravity.js and javascript sound libraries. 

--- Edit --- 
I also decided structually to try out having an API backend using laravel. The main challenge here is authentication and I've decided to set up a separate MVP over there. You can see that. 

My reasoning for all these design principals, is primarily to further understand the tech that is used at work, but also I really like Vue and want to get to know it better. I also wanted the challenge of planning architecture. Going for an API backend was alsoa way ot opening up the opportunity to make a mobile app for this project too. If I really want it to be a useful productivity tool for me, than this would work well. 

Furthermore Laravel is great, and with the Resources options to send JSON data. It seemed a good choice, both for authentication (with passport) and for ease of use. Admitedly its a bit massive for just an API backend for a small project, but thats not a massive drawback and it leaves options open for how I want to take this project further. 

### Steps to MVP 
- [X] You can add squares of one colour and fill in the screen
- [X] You can add squares when you achieve one colour
- [x] You can add new targets, and choose corresponding colours (type in the 3 rgb values) or random 
- [ ] CSS and Refactor and tidy up of code (Ongoing)

Currently everything else is BLOCKED until the backend is working 

(BACKEND WORK)
- [ ] Setup a laravel project
- [ ] Setup MySQL DB with targets (targets have a colour and name)
- [ ] Be able to make requests from Nuxt to Laravel (v. basic)
- [ ] Route for getting all targets
 
-- From this point on, F and B mark what is front and backend work --
- [ ] F Can get targets from DB
- [ ] FB Can add new targets to DB
- [ ] FB Can delete targets 


- [ ] You can't use the same colour more than once 
- [ ] You can only meet a target once a day 
- [ ] You can only add one new target a day 


- [ ] Diagram structure
- [ ] Reflection - are there alternate designs that could have been done? 
- [ ] Write up two articles on how I got there
 
###  Next steps after 
- [ ] The Pixls have motion
- [ ] They hit each other 
- [ ] They make noises when they touch 
- [ ] Special shapes for stages (e.g. 10 days in a row) 
- [ ] You can click on one and see the timestamp
- [ ] You can click and see the goal
- [ ] You can add possitive notes
- [ ] You can see the notes randomly
- [ ] When you get a random note, the target is highlighted 
- [ ] You can only set five new goals a week 
- [ ] Reflection page 
- [ ] Goals you missed yesterday, you get a little pop up, where you can add a reflection 
- [ ] You can set a different time for reflections 

#### Random future ideas
- [ ] Multiple universes
- [ ] Merge dots together
- [ ] Center of gravity 
- [ ] Size affects speed
- [ ] Cool messafes 
- [ ] Timeline of your goals as balls of colour 
- [ ] Can mark a goal as 'special' as one you're particularly proud of (can only do one a day)

#### Learning 
Nuxt 
Tailwind
Vue 
Gravity.js (not used so far)
(potentially a music library in the future)

#### Tech
Nuxt 
Tailwind
Vue 

#### How to run

You will need node and npm installed before doing this.

- clone this repo ```git clone https://github.com/Tagrand/motivationNuxt.git```
- go inside ```cd motivationNuxt```
- run ```npm install```
- run ```nuxt```  (this starts your local server)
- go to localhost:3000
- Enjoy!


