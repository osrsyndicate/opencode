
# Problem Statement: Build an Online Open Code Editor Platform

## Description
You are tasked with implementing the core logic of an online open code editor platform used to evaluate a candidate’s programming skills under time-restricted and controlled conditions.

The platform supports two primary user roles: **Admin** and **Candidate**.

## Your Task
Implement a simulation for the Candidate and Admin workflows with the following behaviors:

---

### Candidate Workflow (Simulated)

1. **Landing Page**  
   - Displays test instructions (if any) and a Start Test button. (Refer to mockups for finalized details).  
   - This page sets the context for the test and may include guidelines or disclaimers.  
   - On clicking 'Start Test', the countdown timer is initiated and the candidate is taken to the test interface.  

2. **Editor/Test Page**  
   - Show a problem statement in markdown format (non-editable).  
     - Ensures the candidate cannot alter or manipulate the problem definition during the test.  
   - Provide a code editor:  
     - Supports manual code typing and proper indentation.  
     - Disables clipboard paste events to prevent copying from external sources, encouraging originality.  
     - Tracks tab/window changes and logs them to detect focus shifts which may suggest cheating attempts.  
   - Provide a console to:  
     - Run the code against predefined test cases on the server.  
     - Display output, errors, and pass/fail status of test cases.  
   - A countdown timer enforces the test duration strictly.  
     - Once time expires, the code editor and console are locked.  
   - Auto-submits the candidate's code and records final results once the timer ends.  

3. **Finished Page**  
   - Displays a “Thank you” message to indicate the end of the test.  
   - All interactions are disabled, and the user can no longer view or edit their code.

---

### Admin Workflow (Simulated)

1. **Login Panel**  
   - Admin logs in securely to access the admin panel for test management.  
   - Authentication ensures only authorized personnel can modify test content or access candidate data.  

2. **Admin Panel**  
   - Admin can perform the following actions:  
     - **Create a new test** with configurable options:  
       - A clearly written problem statement in Markdown for formatting flexibility and readability.  
       - A configurable test duration (e.g., 15, 30, 45 minutes).  
       - Input/output test cases including both sample (visible to the candidate) and hidden (used for final evaluation) in JSON(preferably).
     - **Monitor candidate activity logs**:  
       - Logs include tab switches, code run events, and auto-submission time to track behaviors.  
     - **Access results after test completion**:  
       - Review submitted code and output from candidates.  
       - Generate reports if needed.(Optional)  
     - **Manage language support**:  
       - Enable or disable supported programming languages (e.g., Python, Java, Go) as required.
