# Interview Prep

### Backend

* **What is a problem that you faced and how did you solve it?**
  * TEX Behaviour Analytics:
    * Staff needed to create analytics that could help them understand and share insights with customers as to how their users were engaging with features on the social platform
      * eg: How many sessions were people having?
      * eg: What were the most searched skills?
    * The first part of the problem was to research and find what a valuable but minimal data set would look like and how we would deliver it
    * The second part of the problem was to realise what the constraints were, do we build with what we have or research new tools \(eg: Segment\)
    * Time and risk were big factors, I needed to build the feature as quickly with minimum risk in order to gauge the value to customers, while still being able to migrate the solution away to something more permanent
    * I decided to use our existing database \(Firestore\) to build an aggregated data pattern, where metrics are tallied in real time with GCP Pub/Sub and serverless functions, I implemented an  API so that customers could fetch insight data about their team members as quickly as possible
    * GCP Cloud Storage was used to allow staff to generate on-demand reports that cover metrics across all customers for certain core features
    * We managed to find interested patterns, such as complete profiles would lead to more sessions booked for that individual
    * Customers loved the insights and we decided to implement a couple more core features to our data sets
* **What was the hardest bug you've faced?**
  * Regex Bottleneck
    * Noticed we were getting large request times with New Relic monitoring
    * Checked the logs for any timeouts or errors in application logs
    * Could not replicate locally
    * At the time we were using Platform.sh \(similar to Heroku\), so we didn't have a network tracing tool like AWS X-Ray
    * Try to bring the local environment closer to the production, used the production content API, was able to replicate
    * By profiling with Clinic.js Flame, was able to find a hot function that was performing a huge amount of CPU cycles
    * Function was performing a large amount of regular expressions that was growing exponentially, trying to parse header menu links to match them with application routes
    * Implemented a solution where links we pre-computed and cached on the backend
    * Actually made request times a lot faster
* **How did you resolve a conflict in your team?**
  * Ego
    * I had been working with our current stack for around a year and had become "attached" to one of our frameworks without realising
    * Time came for a new product, our team were deciding what the stack should look like
    * Debates were getting heated, we couldn't decide, discussion was going nowhere, not constructive
    * We decided to take a short break
    * Realised that thought needs to be objective, remove any ego or attachment to tools or frameworks
    * Spend less time worrying about things and more time thinking about actions you can take to get closer to your goals, then actually take action
    * Reformed with team to build a pros/cons list and a feature matrix to attempt to provide a clear path, involving all team members
    * Settled with a vote
    * After the decision, followed up individually after the meeting to apologise, empathise, let them know that their contribution is extremely valuable
* **Why do you want to work here?**
  * I love the product idea and it looks like it was made by people who really care
  * Finance can be inaccessible for many people, particularly younger generations or people without large disposable income, close the financial gap is extremely important
  * Voyager directly relates to my journey, I have been saving for a home deposit for years, I am currently invested in a mutual fund, I'm looking at even more options, which is how I found you
  * I find the problem exciting, how can I generate passive income without a ton of risk? I am even currently trying to build a portfolio dashboard myself, but finding it extremely difficult to get up to date and accurate ASX data
* **Why are you leaving your current role**
  * Growth!
  * I am extremely fascinated by the financial sector, especially since my father and both my brothers work in financial roles, a position at an exciting FinTech product would be a step in the right direction for my career
  * An opportunity to work with Go would be a huge win
  * I'm really keen to work with AWS, I'm taking my AWS certified developer exam in a couple of months
* **What is your greatest strength?**
  * My biggest strength is being able to collaborate with others for problem solving. I love to explore different ideas to try and find simple and effective solutions around constraints. I personally love to crack out my wacom tablet over a screen share and start forming ideas with my terrible illustrations, I find it's extremely effective to communicate ideas with others
* **What is your greatest weakness? \(How do you overcome it?\)**
  * Technology is fast paced and always changing, I can get lost in the excitement of new technologies, ideas and patterns. I find myself with a lot of enthusiasm to try new or different things that potentially might not work. Sometimes you have to separate yourself from the solution and really look at the problem. Not always a bad thing, you can have lot's of different solutions and angles for different problems.
* **Tell me about yourself**
  * I made my first table layout based website in Dreamweaver for a kebab shop when I was 16, I was paid in kebabs
  * Diploma of Graphic Design & Website Development
  * I started my career at **Rotapix** as a Wordpress Developer
    * SEO agency
    * I collaborated with SEO analysts to optimise WordPress websites and increase SE performance
    * I built an internal SEO first WordPress for new projects from lessons learned
  * Moved to **Digital Garden** as a Drupal Developer
    * Digital agency with a team of interface designers and developers
    * Designed and built content management solutions in sectors such as Government and Non-Profits, for organisations such as MSF and APRA
    * For MSF, I designed and implemented a multi-step donation system with automated recurring and one off payments payments
    * Collaborated with design and development team to build a pattern library and a containerised development environment to provide developers with standardised framework and UI elements across agency projects
    * Great team, worked there for four years
  * **Technocrat**
    * Started my contracting career at Technocrat
    * Worked with content team at APSC government agency to deliver a large-scale Drupal solution
    * Achieved WCAG AA accessibility rating
  * **Prosple**
    * Provides tools such as job boards, virtual internships and student reviews to help students, teachers and employers make recruiting decisions
    * Approached by former technical director of Digital Garden to refactor a monolithic multi-site Drupal solution to a microservice style architecture with MongoDB, Express.js, React and Node.js
    * Hadn't had the opportunity to work with React and GraphQL in production
    * Within a month, I had implemented a production ready faceted search solution, which is still used today and handles thousands of daily searches for over 60 tenants
    * Developed user profile solution UI and API with Next.js and GraphQL, collecting data such as education background, career objects, skills, now handling data for thousands of users
  * **TEX**
    * Social networking platform connecting individuals and organisations to share skills and experience
    * React, Express.js, Firebase \(NoSQL and serverless functions\), Algolia \(search\) on a GCP environment
    * Fast paced start up geared towards collaboration, rapid prototyping and experimentation
    * Developed a real time user behaviour analytics solution, providing aggregated metrics across core product features such as bookings and video sessions
    * I used an event based architecture to watch for database changes and aggregate them with Firestore NoSQL and GCP Pub/Sub
    * I've also spent a lot of time analysing and integrating third party software, solutions for social networking with GetStream.io, video sessions with Twilio Video and booking management with Cronofy

