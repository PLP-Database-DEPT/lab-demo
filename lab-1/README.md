### Lab 1: Installing and Verifying MySQL

#### Scenario
You have been hired as a Junior Data Assistant at a small company called BrightMart Ltd.
The company stores customer and sales information in a MySQL database.

Before you can view or work with any data, your manager asks you to install MySQL on your computer and confirm that it is working properly.

This lab represents your first task on the job.

**Lab Duration:**
60 minutes

#### Learning Objectives
By the end of this lab, you will be able to:
- Understand what MySQL is and why it is used
- Install MySQL Server on their computer
- Access MySQL using a command-line client
- Confirm that MySQL is running correctly

#### System Requirements
- Windows 10/11 or Linux
- Internet connection
- Administrator (Windows) or sudo (Linux) access

#### Tools to Be Installed
- [ ] MySQL Server
- [ ] MySQL Command-Line Client
- [ ] MySQL Workbench – visual tool

**Task 1: Check Your Computer Is Ready**

Open Command Prompt (Windows) or Terminal (Linux).
Type:
```bash
whoami
```
**Task 2: Download MySQL**
Open a web browser.
- Search for MySQL Community Server.
- Download the installer for your operating system.
- Start the installation.
- Confirm you can run commands without errors.

**Task 3: Install MySQL Server**
During installation:
- Choose Developer Default or Server Only
- Set a root password
- Write it down
- Do not forget it
- Use default port 3306
- Complete the installation

Important:
_The root user is the administrator of the database._

**Task 4: Verify MySQL Installation**

Open Command Prompt or Terminal.
Type:
```bash
mysql --version
```
_If installed correctly, you will see a version number._

**Task 5: Log Into MySQL**
In the terminal, type:
```sh
mysql -u root -p
```
Press Enter
Enter the root password you created
If successful, you will see:
```bash
mysql>
```
This means:
**MySQL is running**
You are connected to the database

#### Validation Checklist
- [x] MySQL installed successfully
- [x] Can run mysql --version
- [x] Can log in using root user
- [x] Can see existing databases
