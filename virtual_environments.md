# **Virtual Environment**

## What is a Virtual Environment
This is simply a Self-Contained location that enables you to maintain separate and isolated Environmanes for your Python Projects.
This isolation helps you to manage Dependencies, versions, and packages without any conflicts accross different Projects.

**For Example:** when you work on a different python projects its likly some of them depend on different version of external libraries or even python itself.
whitout Virtual Environment if you were to install every Dependencies globally you might run into issues where one projects needs a different version of a library than another project.
This can lead to compatibility issues Vertual Environment solve this issue by allowing each project to have its own set of installed packages independent to what install globally in other Environments.

## How to create Virtual Environment 

* If you are on mac/linux open your terminal or if you're on windows open your command prompt/powershell.
* **Create a folder**
```
mkdir python_virtual_env
```
* **Then inside your Directory create a Virtual Environment**
```
python3 -m venv env
```
* **Then Activate Virtual Environment**
```
source env/bin/activate
```
Once you have activated the Environment you get prefix with the name of the Environment appearing before the normal life in your terminal.
If you see that you will know that your virtual Environment is working perfectly.

### **Output**
```
(env) laxman@laxman-X556UR:~/python_virtual_env$ 
```

* **How to Deactivate Virtual Environment**
Simply type Deactivate.
```
(env) laxman@laxman-X556UR:~/python_virtual_env$ deactivate

```
### **Output**
Now you can see below, Virtual Environment is Deactivated.
```
laxman@laxman-X556UR:~/python_virtual_env$ 
```

* **Reactivate with source comman again**

```
source env/bin/activate
```

## **Installing Packages**
**Now to do this we going to use PIP command(Preferred Installer Program)**
* Now if you want to see what are the current Packages in the Virtual Environment.
```
pip list
```

* Now we can install Packages.
```
pip install requests
```
* Now again you can see what Packages have installed.
``` 
pip list
```

## **Saving Dependencies**
If you done some intense Project or Development and you are ready to push it on Github or share a Project with someone else.

**Now in order to do this you have to create a requirement.txt file**
```
pip freeze > requirements.txt
```
Now you can see the requirements.txt file have created by list the files.
```
ls
```

Now if we want to check what are the Packages requirement.txt file has.
```
nano requirement.txt
```
Now you can see there, and if you want to get out simply press **(contol + x)**

## **Now we are going to see how we can use this requirement.txt file to install the various Packages**
* Simply Deactivate this Environment by typing **deactivate**.
```
deactivate
``` 
**Now think you are someone else**
* Create new one.
```
python3 -m venv my_env
```
* **Activate Virtual Environment**
```
source my_env/bin/activate
```
* If we do want to see those requirement in available or not.
```
pip list
```

* If we want to install require packages.
```
pip install -r requirements.txt
```
-r = 'r' stands for install from a file
## **Example**

```
(my_env) laxman@laxman-X556UR:~/python_virtual_env$ pip install -r requirements.txt
```
Then (pip) will find in the file requirement.txt and start installing Packages.
* Now if you will type command **(pip list)** this will show you all the Packages you have just installed.

# **Summary**
**You have learned:**
* Create an Environmnet
* Activate an Environment
* Install Individual Packages
* Install Packages from a File
* save Packages or Dependencies into a requirement.txt file

## **Common practices**
* It is a common practice to create Virtual Environmnet Folder inside of the Directory where your Python Files exist.
* Now I will Create a Virtual Environmnet inside this Directory so it's alongside of my Python File
* Now it is a common practice to call it **(env)** or **(venv)**
* If you don't need it anymore you can delete it anytime
