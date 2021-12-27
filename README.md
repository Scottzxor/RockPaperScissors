# RockPaperScissors
Using C# and TSQL to create a full stack rock paper scissors game, front end and back end.

/***********************************************
DATABASE NAME: RPS_DB

***********************************************/

Files should be run based on numerical sequence. 

i.e., files are in numerical order starting with 

Script #1_RPS_Project_Create_Tables. 

With this script, you may encounter 2 errors: 

You'll be unable to drop tblPlayers--whether existing or not--given that tblPlayers is 
referenced by the constraint in the creation of tblGames. This script can be run by temporarily
commenting out the drop table if you know for certain that you do not have this table in your database.
Or, you can temporarily remove the constraint, then reestablish it. Once the table has been dropped 
and recreated, the script will run fine.

The proceeding scripts should run easily, provided EXEC and SELECT have been granted priveleges.

If SELECT and EXEC privleges have not been granted to rps_user, Visual Basic code will only appear to add players,
but no actual connection will be made with the database.

Commands to do so are, ("GRANT SELECT/EXEC ON tableName TO userName/role") 

[There's also INSERT/DELETE[never use]/REFERENCE (create forign key into table), or ALTER

Script #2_RPS_Project_Create_Procedures, then

Script #3_RPS_Project_Create_Functions. 

Script #4_RPS_Project_Triggers

At this point, you may have to delete the loopback address manually, as sys admin, if you already have 
a loopback server running under that name.

The code to do this is: 

EXEC sp_dropserver 'loopback', 'droplogins';

Script #5_RPS_Project_Erratta

Basic account privileges for basic access are: 

User: rps_user 
Password: easy
