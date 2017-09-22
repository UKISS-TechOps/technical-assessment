# UKISS-TechOps Technical Assessment

### Info

The technical-assessment uses a number of open source projects to work properly:

* [VirtualBox] - Virtualization tool
* [Git] - Version Control
* [Vagrant] - The development environment build tool.
* [ansible/ansible] - The automation platform.
* [laravel/framework] - The PHP framework for the project.

Before starting, you must have installed in your local machine [Vagrant], [VirtualBox] and [Git].

### Local Installation

The technical-assessment is very easy to install locally using Vagrant and Ansible.

By default, Vagrant will create the `candidate` user and expose port 8000.

Run the below commands to set up the project.

```sh
git clone https://github.com/UKISS-TechOps/technical-assessment.git
cd technical-assessment
vagrant up
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
http://127.0.0.1:8000/TechnicalAssessment
```

### Assessment

Follow the instructions on the home page of the web app and complete the exercise.

Submit a pull request to this repo with your work.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job.)

   [VirtualBox]: <https://www.virtualbox.org/>
   [Git]: <https://git-scm.com/>
   [Vagrant]: <https://www.vagrantup.com/>
   [ansible/ansible]: <https://github.com/ansible/ansible>
   [laravel/framework]: <https://github.com/laravel/framework>
