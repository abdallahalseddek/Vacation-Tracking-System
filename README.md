# Vacation Tracking System
## System Idea :
### The system has a potential to save time and money mostly in HR department
### هناخد القواعد من قسم الموارد البشرية نأسس عليها النظام وموظف الموارد البشرية هيبقي مسئول عن ادخال وتحديث اوقات وتواريخ الاجازات للموظفين علي النظام
## system features :
1. Impl a flexible rules for validating and verifying leave time requests.
2. Enable manager approval.
3. Provide access for the previous 12Months and the next 6 Months.
4. Use email notification to notify the manger when found a new request and the employee after response.
5. Enable th HR and System Admin to override all actions restricted by rules with logging of those overrides.
6. Allow managers to directly award personal leave time with system limits.
7. provide a UI gave the employee a vacation request summary.

### Use Case Actors:
1. Employee 
   1. manage time 
2. Manager   
   1. Approve or refuse Request
   2. Award time
3. HR Clerk   
   1. Edit Employee Records 
   2. Manage Locations 
   3. Manage leave Categories
   4. Override Leave Records
4. System Admin
   1. Back Up system Logs

### Use Case Scenarios :
1. Manage Time [create new Request, Edit pending request, withdraw request, cancel Approved Request]
2. Award Time
3. Edit Employee Record
4. Manage Locations
5. Manage Leave categories
6. Override Leave records
7. Backup system Logs

### Main flow:
#### preconditions : The employee is authenticated to access  the vacation System with privileges to manage his vacation dashboard
1. The employee clicking on the link to access the vacation system.
2. The system use Employee credentials to look Up the current status of the employee previous 12M and next 6 months vacations
3. The employee choose to create a new vacation request.
4. The system ask the employee which data and time he wanted for the vacation
> The employee should have access to a **visual calendar** to help select and compare chosen dates.
5. The employee selects the desired dates and hours per data with short title and description. Then submits the request.
6. If the submitted information incomplete or incorrect or doesn't pass the validation, the app displayed the request again with errors highlighted and documented
7. At this point, the employee can edit any info or cancel the request and remove all info.
8. if the request submitted:
   * the employee is returned to the homepage which contain a vacation request summary.
   * If the employee’s vacation time requests require manager approval, an e-mail is immediately sent to the manager(s) authorized to approve the employee’s requests.
9. The request status should be updated to **pending**.
10. The manager responds to the e-mail by clicking on a link embedded in the e-mail or by explicitly logging into the System
11. The manager may be required to supply necessary authentication credentials to gain the access
12. The System home page lists the manager’s own vacation time requests and outstanding balances but also has a separate section listing requests pending approval by subordinate employees <b>The manager selects each of these one at a time to individually approve or deny.

<p align="center">
    <img src="img/request_validation_flow.png">
</p>
<p style="text-align: center">A Communication Diagram Describing a Request Validation Collaborationt</p>
<p align="center">
    <img src="img/DB_Design.png">
</p>
<p style="text-align: center">Data-Base Design</p>
