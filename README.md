<h1>Filtering SQL Queries</h1>

<h2>Description</h2>
In this lab, we will further filter SQL queries to access specific information contained within the database. We will utilize the <em><strong>SELECT</strong></em>, <em><strong>FROM</strong></em> and <em><strong>WHERE</strong></em> commands. We will also take it a step further and add operators in the queries to apply more filters. Additionally, we apply the <em><strong>AND</strong></em>, <em><strong>OR</strong></em>, <em><strong>NOT</strong></em>, and <em><strong>LIKE</strong></em> filters to our queries. SQL will be accessed through the Linux command line by typing the command <em><strong>sqlite3</strong></em> in the command line.
<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL</b>

<h2>Environments Used </h2>

- <b>SQL</b>
- <b>Linux Bash Shell</b>

<h2>Program Walk-Through:</h2>

<h3>Filtering Using <em><strong>WHERE</em></strong></h3>

<p align="center">
First, list all organization machines and their operating systems from the "machines" table, only highlighting the "device_id" and "operating_system" columns: <br/>
<img src="https://i.imgur.com/MfPLwfJ.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Now, filter the table to list all the machines with the operating system of "OS 2" using the <em><strong>WHERE</strong></em> command:  <br/>
<img src="https://i.imgur.com/NRXhvh1.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Next, we will retrieve a list of all the employees in the Finance and Sales departments to obtain their office numbers: <br/>
<img src="https://i.imgur.com/hLDotbI.png" height="100%" width="100%" alt="Query Filtering"/> <br/>
<br />
<img src="https://i.imgur.com/Tg6SlNK.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
A machine in 'South-109' has been identified as having an issue. In order to send the correct employee an alert, we must find which employee uses that machine. Focus on the "office" column of the "employees" table:  <br/>
<img src="https://i.imgur.com/yYIcjOU.png" height="100%" width="100%" alt="Query Filtering"/>
</p>
<br />
<br />

<h3>Filtering with <em><strong>OPERATORS</em></strong></h3>

<p align="center">
We need to ivestigate a recent security incident and must gather information on login attempts made after a certain date. The first step is to run a query on the "log_in_attempts" table for login attempts made after '2022-05-09':  <br/>
<img src="https://i.imgur.com/sMO9Ka5.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
It was decided that we should also include '2022-05-09' in our query results as well:  <br/>
<img src="https://i.imgur.com/u4Ut0pb.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Now we need to narrow the focus of the search; login attempts made after '2022-05-11' shouldn't be included in the results. This can be acheived by using the <em><strong>BETWEEN</strong></em> and <em><strong>AND</strong></em> operators:  <br/>
<img src="https://i.imgur.com/DUINaNB.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Next, we need to investigate logins that were made before working hours. Typical work hours begin at 07:00:00:  <br/>
<img src="https://i.imgur.com/mai4Fce.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
The previous query produced too many results, so we will narrow it by focusing on logins <em><strong>BETWEEN</strong></em> '06:00:00' <em><strong>AND</strong></em> '07:00:00':  <br/>
<img src="https://i.imgur.com/cAo5KTY.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Now, we want to investigate login attempts that have an event ID number greater than or equal to 100. We can do this by returning only the "event_id", "username", and "login_date" columns from the "log_in_attempts" table:  <br/>
<img src="https://i.imgur.com/uocsRnF.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Lastly, we want to narrow the results further by only focusing on event ID numbers <em><strong>BETWEEN</strong></em> 100 <em><strong>AND</strong></em> 150:  <br/>
<img src="https://i.imgur.com/NgpS0Ms.png" height="100%" width="100%" alt="Query Filtering"/>
</p>
<br />
<br />

<h3>Additional Filtering Commands</h3>

<p align="center">
We are now investigating failed login attempts that were made after business hours, which ends at '18:00:00'. We can search multiple conditions that need to be met by using the <em><strong>AND</strong></em> operator:  <br/>
<img src="https://i.imgur.com/UzspmJ7.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Next, we are investigating a suspicious event that occurred on '2022-05-09'. We want to query for all login attempts made that day and the day before, which can be done using the <em><strong>OR</strong></em> operator:  <br/>
<img src="https://i.imgur.com/2tTyU4A.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Now, we must focus on logins that did not originate in Mexico. We can do this by using the <em><strong>NOT</strong></em> and <em><strong>LIKE</strong></em> operators:  <br/>
<img src="https://i.imgur.com/PNjoLLf.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Next, we need to update employee machines and we need information on employees in the "Marketing" department who are located in all offices in the "East" building:  <br/>
<img src="https://i.imgur.com/iQsvWUD.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Now, we need to perform a different update to all the machines of all employees in the "Finance" and "Sales" department:  <br/>
<img src="https://i.imgur.com/6ZNdxeA.png" height="100%" width="100%" alt="Query Filtering"/>
<br />
<br />
Lastly, we need to make an update on all machines to employees who are not in IT (the update was already installed on employee computers in the IT department):  <br/>
<img src="https://i.imgur.com/Cmi45sJ.png" height="100%" width="100%" alt="Query Filtering"/>
</p>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
