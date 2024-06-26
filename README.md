# Education Website Project

## Table of Contents
- [Requirements](#Requirements)
- [Project Tools](#Project-Tools)
- [Core Features](#Core-Features)
- [Best Practices](#Best-Practices)


## Requirements


1. **Upcoming Meetings**: Display upcoming courses with dynamic content.
2. **Course Visits**: Track and display the number of visits for each course.
3. **Dynamic Navigation**: Clicking on a course in the menu dynamically navigates to the course details page with appropriate tags.
4. **Course Detail Page**: Display dynamic course names and details based on the selected course.

### Sorting and Filtering
- Implement sorting and filtering based on various categories for excellent user experience.
- Implement pagination for easy navigation through courses.

### Dashboard
- **Home and Meetings Details**: Display a dashboard with home and meetings details.
- **Reservation Management**: Manage reservations with active/inactive status.

### User Management
- **User Login**: After logging in, redirect to the dashboard.
- **Retrieve User Name**: Display the user's name on the dashboard.
- **Edit Profile**: Allow users to edit their profile information, with the option to keep the password unchanged.

### Course Management
- **Course Details**: Add a new column to represent the number of visits.
- **Delete Category Check**: Display an alert before deleting a category. Ensure a category cannot be deleted if it contains courses (implemented through join relations in the database).

### Best Practices
- Implement component-based architecture for maintainability and scalability.
- Usage of Query Parameter and PHP functionalities.
- Implementation of all CURD operations of database management.

## Project Tools

- Web browser (latest version recommended)
- XMAPP (PHP, Apache server)
- Database(MySQL Admin)
- Frontend templet(HTML, CSS, JS)
- CSS framework(Bootstrap)


# Admin Panel

## User managements
- Sign Up ✅
- Log in ✅
- Add User ✅
- Edit User ✅
- Displaying the name of the logged in user ✅


For better mainatince, I have seperated the login page from the sign-up page. Upon successful login, users are redirected to the dashboard.
Retrieve User Name: Displays the logged-in user's name on the dashboard for a personalized experience.
Edit Profile: Enables users to update their profile information, including an option to change or retain their current password.



<img width="755" alt="image" src="https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/2c268d6a-15f9-4d74-82d2-097c7a3f7292">

<img width="956" alt="image" src="https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/59e947e1-2c81-4dcb-94e2-94ade9ecb647">

## Categories  Managements
- Add Categories 
- Manage Categories 
- Listing categories
- Deleting not used category
- Deleting used category

![image](https://github.com/astral-fate/Project_r10/assets/63984422/c50f0a90-a958-4b19-b996-768480d9087b)

![image](https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/218feba8-6b2b-4cf3-90cd-4796670e4d70)

![image](https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/4dcfad97-760a-4de1-8ab3-89764c8c1d79)

![image](https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/c6d55187-3b86-4b0a-bea4-1bfbfd86b02e)

![image](https://github.com/astral-fate/Project_r10/assets/63984422/08881d78-0625-4774-934f-09f5b48c5fea)


## Meetings  managements
- Add Meetings ✅
- Manage Meetings ✅

![image](https://github.com/astral-fate/UN-Women-Back-End-Scholarship/assets/63984422/37bcc383-a3fa-4513-a203-5ea588e1c361)
![image](https://github.com/astral-fate/Project_r10/assets/63984422/ecc22d1b-bb57-4067-84d3-1daaab79f381)

## Education Home Page
- Adding admin to the navigation bar
- Showing categories
- Navigate to categories
- Course Details Page
- Meetings page


I have used query parameter to pass the id of the category and filter using it, so the url apperas as

``` http://localhost/project_r10/index.php?category_id=8 ```

![image](https://github.com/astral-fate/Project_r10/assets/63984422/3be512a1-cbbc-47c9-b3ef-745d60a2946f)

I have also updated the   SQL query to only retive 5 result in each page, making use of pagination.

![image](https://github.com/astral-fate/Project_r10/assets/63984422/27723201-d8e2-4fe6-874d-cb66abb9c674)
![image](https://github.com/astral-fate/Project_r10/assets/63984422/5038db75-2452-4dff-9c31-8316b3d591a2)

![image](https://github.com/astral-fate/Project_r10/assets/63984422/d4fa4b4f-5bf8-49d9-ba1a-7eb90c7ce08f)

For the visit counters, I have modifed the SQL statment to increase the counter each time the title of the course is clicked.


```
ALTER TABLE courses ADD COLUMN click_count INT DEFAULT 0;
```

![image](https://github.com/astral-fate/Project_r10/assets/63984422/fe9ad731-4c61-405b-bdd2-d5ef941eb71b)



For better mainatince and redability, I have sepearted each section within the HTML as a coponents, and I included it in the main script using ```'include_once'```. This aims to reduce the number of lines.

![image](https://github.com/astral-fate/Project_r10/assets/63984422/7e5b9d2a-b8af-43a4-be0a-05354f61e5d2)

![image](https://github.com/astral-fate/Project_r10/assets/63984422/db325bdd-f608-47e2-8072-05c261184bb6)


