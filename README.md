Ansible-master 
--------------

                 AWS CLOUD
                     |
          +----------------------+
          |   Ansible Master     |
          |   Ubuntu EC2         |
          |----------------------|
          | ansible.cfg          |
          | Inventory            |
          | group_vars/all.yaml  |
          | Playbooks            |
          | Jinja2 Templates     |
          +----------+-----------+
                     |
               SSH Connection
                 (Port 22)
                     |
          +----------+-----------+
          |          |           |
          v          v           v
      Target 1   Target 2    Target 3
      Ubuntu     Ubuntu      Ubuntu
      EC2        EC2         EC2
          |          |           |
          +----------+-----------+
                     |
              Collect Metrics
                     |
          +----------------------+
          | CPU Utilization      |
          | Memory Utilization   |
          | Disk Utilization     |
          | Server Status        |
          +----------+-----------+
                     |
                     v
             Ansible Master
                     |
                     v
             Jinja2 HTML Template
              (.html.j2)
                     |
                     v
             Generate HTML Report
                     |
                     v
               Email Reporting


=======================================================================================


- I have practiced how to connect ansible master to target node by using SSH connection.
- Approach
- I manually created instances in local  machine.
- then connect with by using SSH connection in platform of mobaxterm.
- Now, start - in ansible-master instance to install  requirements means ansible, python3 , AWS CLI
- And write the some scripting's for automation.
- then manually  checking usage of CPU, RAM, Memory

- Finally, creates a collection metrics and send report to email by using SMTP port 

Here,  Troubleshooting
------------------------
- To connect the SSH port missing -- trouble shooting -add the port in ansible instance
- scripting errors - indentation -- go back to file check which line is incorrect or indentation
- whenever I executed  email sent it through SMTP but inside a mail there is no  metrics -- is there issue with send report file

- 














 
















               
