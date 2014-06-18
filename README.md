RobotX
======

Instructions
------------

**Let all your robot Framework test cases fly!**

The RobotX is a tool set for automation development with [Robot Framework][Robot Framework].  

The Newest version (since version 0.2.1) can automatically, intelligently and dynamically partition all automated tests into multiple pcs, and each one of which can be executed in parallel.
The execution can happen on different physical/virtual machines.
More the partitions, less tests executed on each one.
That means that if you have multiple pcs you can use them for a combined test run.

And since all of the partitions start almost at the same time overall test-execution time 
gets divided by the number of partitions you make.
for the usage examples of distributed execution, refer to following docs.

* [Jenkins configure about distributed run][jenkins dist run]   
* [Usage of parallel run tests in Jenkins][parallel run in jenkins]  
* [Usage of parallel run tests in cmd][parallel run in cmd]   

It includes the following tools:
* Runner
* Generator
* Debugger
* Checker
* Expander

RobtX Runner is pretty powerful
* It can be integrated into Jenkins.  
* It can be used in command line.   
* It can be used to run tests in parallel (since version 0.2.1).  
* Get and filter tests from Test Case Management System.
* Executed tests can be filtered and collected from Test Case Management System.  
* The tests result can be updated to Test Case Management System in real-time.


Installation
------------
    $ pip install robotx
    or
    $ easy_install robotx

Usage
-----
[RobotX Usage Doc][RobotX Usage]

Build & Config Jenkins
----------------------
[Build and Config Jenkins Doc][Build Config Jenkins]


Robot Framework Best Practices
------------------------------
[Robot Framework Best Practices Doc][Best Practice]

Test Case Management System
---------------------------
### Default TCMS Client   
Currently, RobotX uses [Nitrate][Nitrate] as default TCMS(Test Case Management System). 
If your TCMS is not Nitrate(such as TestLink), you need write a new client and replace the 
[default TCMS client of RobotX][nitrate client].

### Configure TCMS Client   
* Copy [config template file][tcms config] to /etc/, and name it as tcms.conf.
* Open tcms.conf, and change all values to yours.


[Robot Framework]: http://robotframework.org/
[RobotX Usage]: https://github.com/idumpling/robotx/blob/master/docs/USAGE.md
[Build Config Jenkins]: https://github.com/idumpling/robotx/blob/master/docs/JENKINS_CONFIG.md
[Best Practice]: https://github.com/idumpling/robotx/blob/master/docs/ROBOT_BEST_PRACTICE.md
[Nitrate]: https://fedorahosted.org/nitrate/
[nitrate client]: https://github.com/idumpling/robotx/blob/master/robotx/core/nitrateclient.py
[tcms config]: https://github.com/idumpling/robotx/blob/master/robotx/conf/tcms.conf
[jenkins dist run]: https://github.com/idumpling/robotx/blob/master/docs/JENKINS_CONFIG.md#Parameters-for-running-as-distributed  
[parallel run in jenkins]: https://github.com/idumpling/robotx/blob/master/docs/JENKINS_CONFIG.md#Parallel-run-tests-on-more-than-one-PC
[parallel run in cmd]: https://github.com/idumpling/robotx/blob/master/docs/USAGE.md#Parallel-run-tests-on-more-than-one-PC

