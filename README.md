# SQL Tutorial 
In this Tutorial I will be showcasing basic fundamentals and usage of SQL! I will try my best to make this as user friendly as possible!
<h2>What is SQL?</h2>
SQL stands for Structured Query Language which is a language and tool that is designed specifically for interacting with databases. It allows you to perform various tasks including querying data, inserting and deleting current records. When you think of the Usage of SQL, think of CRUD. (Create, Read, Update, Delete)
<br />
<h2>What is a Database?</h2>
A database a digital storage that stores and organized your Organizations information. Each table in the database will store different information. For example- Usernames, Passwords, email addresses, etc. There are multiple platforms that organizations may use in order to facilitate these databases that are called Database Management System. For example- Microsoft SQL Server, My SQL, Oracle, etc.

<h2>Languages, OS, and Applications Used</h2>

- <b>MySQL</b>
- <b>Ubuntu OS</b>
- <b>Terminal</b>

<h2>Skills</h2>

- <b>Linux Command line</b>
- <b>SQL - Creating tables</b>
- <b>SQL - Creating Rows</b>
- <b>SQL - Searching Data</b>


<h2>Step 1: Setting Up MySQL</h2>
In this step, we will be creating a Resource Group for the Company. A resource group is a container that groups related resources for your cloud solution. You would make Resource groups for each different department, application, or project for concerns of seperation.

1. First things first, lets prepare our Ubuntu for the installation of MySQL. Open your terminal and run the command <b>"sudo apt update"</b>.

    >**Note:**<b> This updates our repository for the machine.</b>

![step 1](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/454d972a-afcb-470c-9b42-42d27b6e1753)


2. Next, we are going to install MySQL Server. Run the command <b>"sudo apt install mysql-server"</b>. Select <b>"Yes"</b> for install

![step 2](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/1f67a1e7-727e-4a36-870f-14c63adcb857)

   
3. We can check if the installation was successful and running with the following command <b>"sudo systemctl status mysql"</b>

![step 3](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/bebbb72b-383b-4ce8-8432-be3c4d470e6f)


## Step 2: Accessing and Creating in MySQL

In this step, We will be diving into the application and taking a look around!

1. Time to access MySQL! Run the following command <b>"sudo mysql"</b>

1. Now that we have MySQL running, Lets check what databases are already established. To do that type "show databases;".
   >**Heads up:** <b>when running commands in mysql, always end your command with ";" if you are finished with the command.</b>

![step 4](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/992be7ac-3b2e-42a1-ad79-019e6f94a195)

3. You should see the following default database.

![step 5](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/ff00b7b8-d109-4697-a0da-e4776c2e2065)


5. Next, let's create our own database. type the following command <b>"create database lv_team;"</b>.
   >**Note:** You can name the database whatever you wish. I chose lv_team because i'm a naruto fan and it stands for leaf village 🍃 🥷

![step 6](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/e67fd5bd-8860-4bc5-94cc-ebabe5764f23)


6. Let's check <b>"show databases;"</b> again to see if our new database is showing.

![step 7](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/04f4f3ac-362d-4eac-8409-e283cd00d13e)


8. Perfect our database is available! Now let's select our database for usage. Run the command <b>"use lv_team;"</b>

![step 8](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/ead97105-406b-45f3-bb5e-4f3e5e7948db)

### Step 3: Updating Tables

Our tables won't have anything.. so let's start adding data!

1. It's time to start creating and naming our columns. Run the following command "create table leaf_village ( team int, name varchar(20), nin_rank varchar(20));
    >**Note:** <b> int: number value will be place. varchar(%): character value will be placed. (%) signifies the max amount of characters allowed for the name.</b>

![step 9](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/d7d0b44b-fcfc-495a-890e-9796b366eaca)


2. Now let's check to confirm our table has been created. Run <b>"show tables;"</b>

![step 10](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/efdbf3eb-4878-4950-9ea7-7de7b6a64d92)



### Step 4: Creating Rows

It is time to start creating the rows for our table

1. Let's insert our 1st row to our table. Run the command <b>"insert into leaf_village values (7, "Naruto", "Genin");</b>
    >**Note:** <b>It is important to enter the values of the row just as specified in the prior steps when we created the table. (team, name, nin_rank)</b>
    

![step 11](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/d9639427-15b0-4b59-ae2a-8a8d082ac303)


2. Let's check the table to make sure we entered it correctly. Run the command <b>"select * from leaf_village;"<b/>
    >**Note:** <b>The "*" allows us to pull all data from the selected table specified.</b>
    

 ![step 12](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/ed0a1c30-c0ff-4f95-b6a1-4b846b88bd03)
 

3. Now that we have created our 1st row, let's add some more!
        >**Challenge!:** <b>Add 4 more rows to your current table</b>


4. Now lets check our work. Go ahead and run <b>"select * from leaf_village;"</b>


![step 13](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/0e5c4c76-fd7c-4f5a-8c2d-a193b13e36b1)


5. Now that we have more entries on our table, Let's learn to remove a row. Let's remove Sasuke since he went rogue on our team. Run the command <b>"delete from leaf_village where name = "Sasuke";"</b>. We can confirm that the entry was removed by running <b>"select * from leaf_village;"</b>

![step 14](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/329c428f-e3d0-4a98-a271-c5c0f0f5aeda)


6. Looks like Naruto passed his Chuunin exams Finally! Let's update his nin_rank. To change an entry in our table, run the command <b>"update leaf_village set nin_rank = "Chuunin" where name = "Naruto";"</b>. Go ahead and verify that this has been updated as well.

![step 15](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/19c56110-332b-4895-9468-882cfb09eb91)


7. Last thing for this lesson, let's add one more column to the table for missions. To do that, run the following command <b>"alter table leaf_village add missions varchar(20);"</b>. If done correctly, your table should look like the one below.

![step 16](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/3a30bcb7-8096-4568-bf60-2c342e50f04f)


  >**Challenge!:** <b>Now that we added another column, go ahead and update the data in the column!</b>
  

8. Data should look like this by the end of the challenge!

![step 17](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/8eb99db8-29d4-4bd9-bde0-1694a8655e79)



### Congrats!

Congrats on taking the 1st steps of learning SQL and making it this far in my tutorial. I hope this was helpful and insightful in your journey of furthering your skills! I will be creating another Tutorial on creating Joins and Views to unlock the full capacity of SQL!
Please feel free to follow and share if this was easy to follow and have a focused future!

![naruto](https://github.com/loddysworld/Managing-Microsoft-Entra-ID-Identities/assets/134660738/b57a6f70-2e50-4588-880b-fcf6f3465229)


<p align="center">

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
