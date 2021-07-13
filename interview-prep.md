# Interview Prep

### Backend

* What is a problem that you faced and how did you solve it?
  * TEX Behaviour Analytics:
    * Staff needed to create analytics that could help them understand and share insights with customers as to how their users were engaging with features on the social platform
      * eg: How many sessions were people having?
      * eg: What were the most searched skills?
    * The first part of the problem was to research and find what a valuable but minimal data set would look like and how we would deliver it
    * The second part of the problem was to realise what the constraints were, do we build with what we have or research new tools \(eg: Segment\)
    * Time and risk were big favors, I needed to build the feature as quickly with minimum risk in order to gauge the value to customers, while still being able to migrate the solution away to something more permanent
    * I decided to use our existing database \(Firestore\) to build an aggregated data pattern, where metrics are tallied in real time in order to provide an API that can respond with customer insight data as quickly as possible
    * GCP Pub/Sub and GCP Cloud Storage was used to allow staff to generate on-demand reports that cover metrics across all customers for certain core features
    * Customers loved the insights and we decided to implement a couple more core feature insights
* What was the hardest bug you've faced?
  * Regex Bottleneck
    * Noticed we were getting large request times with New Relic
    * Checked the logs for any timeouts or errors in application logs
    * Could not replicate locally
    * Try to bring the local environment closer to the production, used the production API endpoint, was able to replicate
    * By profiling with Clinic.js Flame, was able to find a hot function that was performing a huge amount of CPU cycles
    * Function was performing a large amount of regular expressions that was growing exponentially, trying to parse header menu links to match them with application routes
    * Implemented a solution where links we pre-computed and cached on the backend
* How did you resolve a conflict in your team?
  * Ego Stabliser
    * 
* Why do you want to work here?
* Tell me about yourself
  * Should conform to the narrative
  * See "Behaviora Questions" in "Cracking the Code Interview"
    * Current role, education, post education, current role details, relevant outside of work, wrap up - why your here"
  * Mention if you were "headhunted"
  * Mention awards or success
* Why are you leaving your current role
* What is your greatest strength?
* What is your greatest weakness? \(How do you overcome it?\)
  * Make the weakness your strength

