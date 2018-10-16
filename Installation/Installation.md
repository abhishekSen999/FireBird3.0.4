Here, we will define the steps needed to install FireBird 3.0.4 server of Windows 

## Step 1
Download the Firebird3.0.4 exe file for Windows x32/x64 from the specified link (https://www.firebirdsql.org/en/firebird-3-0/)

## Step 2
Execute the downloaded file and perform the tasks as shown in the images.

## Step 3
### Step 3.1
![Step 1](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%201.png)
### Step 3.2
![Step 2](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%202.png)
### Step 3.3
![Step 3](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%203.png)
### Step 3.4
![Step 4](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%204.png)
### Step 3.5
![Step 5](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%205.png)
### Step 3.6
![Step 6](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%206.png)
### Step 3.7
![Step 7](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%207.png)
### Step 3.8
![Step 8](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%208.png)
### Step 3.9
![Step 9](https://github.com/krishna1401/FireBird3.0.4/blob/master/Installation/Step%209.png)

## Step 4
We need to run the Firebird Management Service to use the isql and other command line features.
### Step 4.1
Run Command Line (as administrator) and move to the folder where you have installed FireBird.
### Step 4.2
Use command **instreg install**
![Step 1]()
> instreg install command is used to make all the necessary entries in the right places, and install everything required during service.
### Step 4.3
Use command **instsvc install -auto -name firebird3**
![Step 2]()
