
### Use Case Table: Register Support Manager

| **Use Case ID** | **Use Case Name**        | **Actors**   | **Description**                                                 | **Preconditions**                    | **Postconditions**                                  | **Main Flow**                                                                                            | **Alternate Flow** |
|-----------------|--------------------------|--------------|-----------------------------------------------------------------|--------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|--------------------|
| UC1             | Register Support Manager | Company support Manager | Manually register a Support Manager using a DB script at system startup. | System is initialized and running.   | Support Manager is registered and can log in to the system. | 1. System Admin executes the DB script.<br>2. Support Manager details are added to the database.           | N/A                |

### 1.1 Register Support Manager Wireframe
Manually register a Support Manager using a DB script at system.

### Use Case Table: Register External Client

| **Use Case ID** | **Use Case Name**        | **Actors**      | **Description**                                                                                 | **Preconditions**              | **Postconditions**                                                | **Main Flow**                                                                                                                           | **Alternate Flow**                                                                                                      |
|-----------------|--------------------------|-----------------|------------------------------------------------------------------------------------------------|--------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| UC2             | Register External Client | External Client | Allow External Clients to register through a client registration link available on the login page. | System is initialized and running. | External Client is registered and can log in to the system.    | 1. External Client accesses the login page.<br>2. External Client clicks on the registration link.<br>3. External Client fills in the registration form.<br>4. System validates the information and registers the client. | 1. If registration fails due to validation errors, prompt the user to correct the information.<br>2. If registration fails due to system error, display an appropriate error message. |

### 1.2 Register External Client Wireframe
<img width="262" alt="image" src="https://github.com/user-attachments/assets/bdb08602-46e0-4633-938e-d6e9279d3484">

### Use Case Table: Add Support Team Member

| **Use Case ID** | **Use Case Name**        | **Actors**        | **Description**                                                                     | **Preconditions**              | **Postconditions**                                             | **Main Flow**                                                                                                     | **Alternate Flow** |
|-----------------|--------------------------|-------------------|------------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|
| UC3             | Add Support Team Member  | Support Manager   | Allow Support Manager to add Support Team members from inside the system.           | Support Manager is logged in.  | Support Team Member is registered and can log in to the system. | 1. Support Manager logs into the system.<br>2. Support Manager navigates to the team management section.<br>3. Support Manager fills in the registration form.<br>4. System validates the information and registers the team member. | N/A                |

### 1.3 Add Support Team Member
<img width="234" alt="image" src="https://github.com/user-attachments/assets/5869f470-7b45-42f6-9c40-803e3f42d961">

### Use Case Table: Login

| **Use Case ID** | **Use Case Name** | **Actors**                  | **Description**                                                                                     | **Preconditions**                    | **Postconditions**                                           | **Main Flow**                                                                                      | **Alternate Flow**                                                                                                     |
|-----------------|-------------------|-----------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| UC4             | Login             | Support Manager, Support Team Member, External Client | Allow users to log in using their username or email and password.                                   | User is registered in the system.    | User is logged in and can access the system.                 | 1. User navigates to the login page.<br>2. User enters username/email and password.<br>3. System validates credentials.<br>4. User is granted access to the system. | 1. If credentials are invalid, prompt the user to re-enter credentials.<br>2. If there is a system error, display an appropriate error message. |

### 1.4 Login Wireframe
<img width="385" alt="image" src="https://github.com/user-attachments/assets/c75d2a8a-c6ac-4463-9d9e-f73d314be207">

### Use Case Table: Support Manager Workflow

| **Use Case ID** | **Use Case Name**          | **Actors**        | **Description**                                                                                                 | **Preconditions**                      | **Postconditions**                                                  | **Main Flow**                                                                                                                                                                                                                 | **Alternate Flow**                                                                                                      |
|-----------------|----------------------------|-------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| UC5             | Support Manager Workflow   | Support Manager   | Allow Support Manager to manage support employees and external clients, assign tickets, and view dashboard stats. | Support Manager is logged in.          | Support employees and clients are managed; tickets are assigned.  | 1. Support Manager logs into the system.<br>2. Support Manager navigates to employee/client management.<br>3. Support Manager performs actions such as add/edit/view/deactivate employees/clients.<br>4. Support Manager navigates to the ticket management section.<br>5. Support Manager assigns tickets to support employees.<br>6. Support Manager views dashboard stats and reports. | 1. If there is an error in any management action, display an appropriate error message.<br>2. If ticket assignment fails, allow re-assignment. |

### 1.5 Support Manager Wireframes
#### 1.5.1  Add Client/Employee
<img width="231" alt="image" src="https://github.com/user-attachments/assets/fa5acf4e-5eb8-461f-9364-0827ff71ff1f">
<img width="231" alt="image" src="https://github.com/user-attachments/assets/73060b71-58d8-4108-906f-635466139ac0">

#### 1.5.2 Edit Clint/Employee
<img width="231" alt="image" src="https://github.com/user-attachments/assets/eeaefec2-9cb7-4229-ab0c-1131c5248447">

<img width="231" alt="image" src="https://github.com/user-attachments/assets/2c219b67-a43c-40a8-aff8-f5f11945acf9">

#### 1.5.3 View/Deactivate/Activiate Clint/Employee

<img width="231" alt="image" src="https://github.com/user-attachments/assets/d4709dce-743e-4646-8e7a-b39f0bcfad40">

#### 1.5.6 Views Dashboard Stats and Reports.

<img width="231" alt="image" src="https://github.com/user-attachments/assets/9df45ae3-6a3b-4cba-a78f-28c92594e01d">

### Use Case Table: External Client Ticket Management

| **Use Case ID** | **Use Case Name**            | **Actors**         | **Description**                                                                            | **Preconditions**                 | **Postconditions**                                               | **Main Flow**                                                                                                      | **Alternate Flow** |
|-----------------|------------------------------|--------------------|-------------------------------------------------------------------------------------------|-----------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|--------------------|
| UC6             | External Client Ticket Management | External Client | Allow External Client to log in, view, add, and edit their support tickets.                 | External Client is logged in.     | External Client's tickets are managed.                                     | 1. External Client logs into the system.<br>2. External Client navigates to the ticket management section.<br>3. External Client views the list of their tickets.<br>4. External Client adds/edits tickets as needed.<br>5. External Client submits tickets, which get the status 'New'. | N/A                |

### 1.6 External Client Ticket Management Wireframe
![Uploading image.png…]()

### Use Case Table: Ticket Assignment

| **Use Case ID** | **Use Case Name**         | **Actors**        | **Description**                                                                        | **Preconditions**                | **Postconditions**                                           | **Main Flow**                                                                                              | **Alternate Flow**                                                                                                     |
|-----------------|---------------------------|-------------------|---------------------------------------------------------------------------------------|----------------------------------|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| UC7             | Ticket Assignment         | Support Manager   | Allow Support Manager to assign new tickets to support team members.                    | Support Manager is logged in.   | Tickets are assigned to specific support team members.     | 1. Support Manager logs into the system.<br>2. Support Manager navigates to the ticket management section.<br>3. Support Manager views the list of new tickets.<br>4. Support Manager assigns tickets to support team members. | 1. If assignment fails, display an appropriate error message and allow re-assignment.    2. If Support Manager try to assign pre-assigned ticket display an appropriate error message and prevent completeing  |


#### 1.7 Assigns Tickets to Support Employees
<img width="231" alt="image" src="https://github.com/user-attachments/assets/5655d913-5490-4717-936d-39044e7363f4">

### Use Case Table: Support Employee Ticket Management

| **Use Case ID** | **Use Case Name**            | **Actors**            | **Description**                                                                                               | **Preconditions**                     | **Postconditions**                                                      | **Main Flow**                                                                                                                                                   | **Alternate Flow**                                                                                                      |
|-----------------|------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|---------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| UC8             | Support Employee Ticket Management | Support Team Member | Allow Support Team Member to view, comment, and close assigned tickets.                                       | Support Team Member is logged in.     | Support tickets are managed and resolved.                                        | 1. Support Team Member logs into the system.<br>2. Support Team Member navigates to the ticket management section.<br>3. Support Team Member views the list of assigned tickets.<br>4. Support Team Member adds comments to tickets.<br>5. Support Team Member closes tickets after client confirmation. | 1. If there is an error in ticket management, display an appropriate error message.<br>2. If closing a ticket fails, prompt the user to retry or escalate. |

