# skillTest_dev

usecase 1: fetch data

The scheduler flow which is created can be used to fetch the staff data on timely bases . In the current code the scheduled will be running once in 24 hours and will be calling system api's get endpoint to fetch data from HR system.  We can schedule the api to run in particular time using cron expression

usecase 2: update 

The Patch end point is used to update the records.  In the code we are using "empId" that can be passed as a uri parameter to uniquely identify the record that needs to be updated. This endpoint will be calling the patch endpoint os system api to update the records

usecase 3: create and offboard/delete

The post endpoint is used to create employee record and the delete endpoint is used to delete or offboard the employee
Here we are passing role in headers and it accepts only two values(HR, recruiter). only these two roles have access to create or delete record. and these two endpoints are secured by basic authentication
