# README

Questions:
- User requirements, auth and admin functionality
Simplistic user model based on email / password auth and with no permission limitations. No admin functionality. Login not required to view resources but to update
- Projects should be owned by a user?
No, projects are independent entity and a user can access / modify any project
- What are the available statuses for Projects and are there invalid transitions of status?
Assume statuses are 'Not started', 'In progress', 'Done' and there are no invalid transitions


TODO
- request tests
- tailwind formatting
- readme writing
- git history and migrations time changes

CONSIDERATIONS
- statuschange auditing has been manually created to simplify but PaperTrail better option
- indexing only added on project foreign keys as user not currently present in queries
- avoid tautological tests like associations. Prefer testing behaviour over implementation
- project controller uses two queries + in memory sorting. in case of large data sets this should be refactored to be performed all in one SQL query or through an STI table (interactions)
- error handling / displaying in views