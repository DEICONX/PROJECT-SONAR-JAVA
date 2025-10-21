# AWS-SERVER CONFIGURATION

> Give a name for instance and select image ubuntu

![](Screenshot%202025-10-21%20151155.png)

------

> Here while selecting instance type sonarqube needs minimum of 2 cpus and 4gb memory 

![](Screenshot%202025-10-21%20151221.png)

----

> Add inbound rule i.e default port number of sonarqube is 9000

![](Screenshot%202025-10-21%20151251.png)

-----

> SSH into terminal  
>
> Sonarqube needs Java so update and install Java as shown in the image:  
> `sudo apt -y update && sudo apt install openjdk-17-jre-headless -y`

![](Screenshot%202025-10-21%20152552.png)

------

> Install Maven using: `sudo apt install maven -y`

![](Screenshot%202025-10-21%20152632.png)

----

> Clone the GitHub repo: `git clone <repo url>` and `cd <foldername>` 

![](Screenshot%202025-10-21%20153035.png)

----

> Install SonarQube:  
> `sudo apt install wget unzip -y`  
> `sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip`  
> Unzip using: `sudo unzip sonarqube-10.6.0.92116.zip`   

![](Screenshot%202025-10-21%20153429.png)

----

> Modify permission as root: `sudo chown -R ubuntu:ubuntu <foldername>`  
> Now go to `cd sonarqube-version/bin/linux-x86-64/`  
> Start the server using the executable file: `./sonar.sh start`

![](Screenshot%202025-10-21%20153528.png)

-----

> Configure `sonar.properties` by allowing web access:  
> `cd sonarqube<version>/conf`  
> `sudo vi sonar.properties`

![](Screenshot%202025-10-21%20153758.png)

----

> Insert and add:  
>
> ```text
> sonar.web.host=0.0.0.0
> sonar.web.port=9000
> ```  
> and save

![](Screenshot%202025-10-21%20153910.png)

----

> Copy the IP address and open in a new tab:  
> `<your IP>:9000`

![](Screenshot%202025-10-21%20153622.png)

-----

> The SonarQube will ask you to login. Default username and password is `admin/admin`

![](Screenshot%202025-10-21%20155412.png)

------

> Co
