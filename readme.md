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

The following log file (xml/application_test.09-17.log) is artificially generated but represents similar logs that we regularly work with. We often need to cross-reference data from application logs with databases or other data sets.

Your task is to extract data from the XML contained in the log.

You should extract the following fields in this order, this represents the CSV header.

Timestamp,authIdentifier,indexType,IndexName,sandwich

You should be able to explain how your system works.

The xml contained in the example log file MAY NOT be valid XML.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job.)

   [VirtualBox]: <https://www.virtualbox.org/>
   [Git]: <https://git-scm.com/>
   [Vagrant]: <https://www.vagrantup.com/>
   [ansible/ansible]: <https://github.com/ansible/ansible>
   [laravel/framework]: <https://github.com/laravel/framework>
