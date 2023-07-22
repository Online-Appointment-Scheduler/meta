# meta
## Description
A REST API that must be called by a telegram bot which will be used as front end for the application. The app itself has to be designed in the way that there will be 2 roles: a manager (someone who will manage timetable and accept someones' else requested to attend the appointment) and a user (someone who will browse through existing time table managed by the manager and decide when to come to the appointment in a request form that can be accepted or denied)

- Microservice architecture
- openID

## Stack
Django Rest Framework, Redis/RabbitMQ(?), db(?PostgreSQL), Telegram API, OAuth2, Celery, AWS, React

## Functional requirmenets
 - CRUD appointment windows (time when a user can attend the appointment) (Manager)
 - Add title, description, make appointment windows reocurring until some time (Manager)
 - Accept/Deny attend request (Manager)
 - Read the details (author, name, note) of the request (Manager, User(author))
 - Read the ap. windows details, including manager's info (User)
 - Authorization
 - CRUD lobbies (Manager)
 - Invite to the lobby with code (Manager)
 - Accept/Deny join lobby request without invitation (Manager)
 - Add to the Blacklist (Manager)
 - Update profile information (Manager, User)
 - View all members of a lobby (Manager, User)
 - List members of all manager's lobbies filtered by lobby names and users' statuses (e.g. class group name, faculty and etc.) (Manager)
 - Update status (User)
 - Get updates when the appointment window is deleted, created (User)
 - Get updates when request is sent, unsent, cancelled (Manager)
 - Get updates when request is cancelled (User)
 - Get updates when requst is accepted/denied (User(author))
 - Get tech support
 - CRUD entities on the admin panel (Admin)

## Non-functional requirements
