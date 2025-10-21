# AWS-SERVER CONFIGURATION

> Give a name for instance and select image ubuntu

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 151155.png)

------

> Here while selecting instance type sonarqube needs minimum of 2 cpus and 4gb memory 

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 151221.png)

----

> Add inbound rule i.e default port number of sonarqube is 9000

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 151251.png)

-----

> SSH into terminal 
>
> sonarqube needs java so update and install java as shown in the image use
>
> `sudo apt -y update && sudo apt install openjdk-17-jre-headless -y`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 152552.png)

------

> Install maven using `sudo apt install maven -y`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 152632.png)

----

> clone the github repo `git clone <repo url>` and `cd <foldername>` 

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153035.png)

----

> Install sonarqube using `sudo apt install wget unzip -y`
>
> `sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip `
>
> Unzip using `sudo unzip sonarqube-10.6.0.92116.zip`   

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153429.png)

----

> modify permission as root using `sudo chown -R ubuntu:ubuntu <foldername>`
>
> Now go to `cd sonarqube-version/bin/linux-x86-64/`
>
> Start the server you will find an executable file sonar.ch 
>
> start using `./sonar.ch start`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153528.png)

-----

> configure sonar.properties by adding world wide web(allow)
>
> Using `cd sonarqube<version>/conf` `sudo vi sonar.properties`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153758.png)

----

> insert and add 
>
> sonar.web.host=0.0.0.0
>
> sonar.web.port=9000 and save

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153910.png)

----

> Copy the Ip address and open new tab
>
> paste your ip along with port number `<your IP>:9000`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 153622.png)

-----

> The sonarqube will ask you to login default username and password is admin,admin

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155412.png)

------

> Configure New Password

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155605.png)

-----

> Now to generate token go to
>
> Administration

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155711.png)

----

> To generate token select security-->users

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155728.png)

-----

> select on three dots to update token

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155741.png)

----

> give a name and generate token (copy the token store in notepad)

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 155816.png)

-------

>  Now to test with sonarqube use the cmd`mvn clean verify sonar:sonar -Dsonar.host.url=http://13.221.134.199:9000 -Dsonar.login=squ_f07f413acf99fff40f16d40e801a02bfa605dc9b`

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 163534.png)

------

> Build success and now go to sonarqube website

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 163618.png)

-----

> Go to dashboard we can view our Java application name click on that

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 163641.png)

----

> Test is successful and we can view detailed bugs in issues

![](C:\Users\jagan\Downloads\JAVASONAR\Screenshot 2025-10-21 163702.png)



