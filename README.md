# Event-Tracking-System
A simple Campus Event Reporting System using Flask + MySQL. It lets students register, mark attendance, give feedback, and generates reports like event popularity, participation, attendance %, and average feedback.


1.Project overview:
>It is a small backend system for Campus event management reporting.
>It lets the College Staff organize the events,students register to the events and after the event feedback will be collected.
>generates reports on event popularity,student participation,attendence percentage and Average feedback and top 3 Active students

2.Technology used:
>Python 3
>Flask (for APIs)
>MYSQL(for Database)

3.Setup Instructions:
1st step:"pip install flask mysql-connector-python" (Command to Connect your Database with Flask Application)
2nd step:Create database in MySQL:

 CREATE DATABASE campusdb;
 USE campusdb;

3rd step:Run "schema.sql" to create all tables.
4th step:Open app.py → update your MySQL username & password.


4.Run the Project:
>Start the Flask app:
"python app.py" run this command in terminal
>if everything works then it will run on the server:
"http://127.0.0.1:5000" and it will say "Campus event management API is running".


5.API EndPoints:


Students & Events:

POST /students → add a student

POST /events → create event

Participation:

POST /register → register student to event

POST /attendance → mark attendance

POST /feedback → submit feedback (1–5 rating)

Reports:

GET /reports/popularity → total registrations per event

GET /reports/participation → student participation

GET /reports/attendance → attendance % per event

GET /reports/feedback → average feedback score

GET /reports/top-students → top 3 most active students


6.Testing:
> Use Browser or PostMan to Test EndPoints.
> GET APIs → can be opened directly in browser (JSON output).


7.Reports/Sample Outputs:
Popularity → events sorted by registrations.

Participation → how many events each student attended.

Attendance % → present vs registered.

Feedback → average rating per event.

Top Students → top 3 active attendees.


8.My Understandings:
> if the tables are separate the data is clean like student,participation etc.
> Unique Constraints will stop duplicate Registrations or feedbacks
> With this data we can maximize the scale
>Flask actually provides clean APIs that can later connect to student or admin portal


9.Testing URLs for Endpoints(paste it in browser):

http://127.0.0.1:5000/reports/popularity

http://127.0.0.1:5000/reports/participation

http://127.0.0.1:5000/reports/attendance

http://127.0.0.1:5000/reports/feedback







