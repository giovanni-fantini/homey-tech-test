# README

Questions:
- User requirements, auth and admin functionality
Simplistic user model based on email / password auth and with no permission limitations. No admin functionality. Login not required to view resources but to update
- Projects should be owned by a user?
No, projects are independent entity and a user can access / modify any project
- What are the available statuses for Projects and are there invalid transitions of status?
Assume statuses are 'Not started', 'In progress', 'Done' and there are no invalid transitions


TODO
- add before action authenticate user