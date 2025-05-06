# Final Project User Management Documentation

This project is a User Management System API built using FastAPI, designed to handle core user operations such as registration, authentication, and user data management. It is structured for scalability and maintainability, making use of asynchronous programming with asyncpg for PostgreSQL interactions.

The application is containerized using Docker, ensuring consistent deployment across environments. A fully automated CI/CD pipeline is implemented using GitHub Actions.

## Issue Tracking and Resolution

### Issue 1: LinkedIn and GitHub URLs Null When Creating a User
In response to creating a user, the GitHub URL and LinkedIn URL are null; they should instead display the correctly entered URLs.
And The values are appropriately mapped, and the URLs are now accessible.
- code fix: https://github.com/psbpras/Final-Project/tree/1-the-linkedin-and-github-urls-are-null-when-creating-a-user

### Issue 2: UUID Missing from Email
The email verification lacks a UUID, preventing the link from confirming the email address. Ideally, clicking on the link should verify the email.
The problem occurred because the email was sent before the user was added to the database. Now that it's fixed, the link works as expected.
- code fix: https://github.com/psbpras/Final-Project/tree/3-uuid-missing-from-email

### Issue 3: Updation of Email ID
When attempting to update an email ID to one that already exists, the system is incorrectly returning a 200 response. The expected behavior is for an appropriate error message to be displayed.
Add a check based on an email address and return an error message stating that the email address already exists.
- code fix: https://github.com/psbpras/Final-Project/tree/5-updation-of-email-id

### Issue 4: Removing URL Fields Causes an Error
When attempting to set the profile_picture_url and linkedin_profile_url fields to an empty string to delete the URLs, an error occurs. The expected behavior is for the URLs to be removed and the fields set to null.
Fix: I created a validator to verify if the entered data is empty, and then set the value to None.
- code fix: https://github.com/psbpras/Final-Project/tree/7-removing-url-fields-is-causing-an-error

### Issue 5: Ensure Valid Image Extensions When Updating User Profiles
The user profile has been successfully updated even though the profile link does not contain a recognized image extension. It should only update if the file includes a valid extension.
Changes to the code have fixed the problem. Only jpeg, png, and jpg file formats are currently accepted.
- Codef fix: https://github.com/psbpras/Final-Project/tree/9-ensure-that-the-image-extensions-are-valid-when-updating-user-profiles 

### Docker Image Output
- [Docker Image Link] (https://hub.docker.com/repository/docker/lakshmiprasanna111/final_project_user_management/general)
  
This documentation details the resolutions and enhancements made during the development process, ensuring each feature operates as intended and enhances the overall functionality of the user management system.







