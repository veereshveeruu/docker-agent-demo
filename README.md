# Jenkins Distributed Architecture Setup

## Configuring Jenkins
- Provision 2 ubuntu instances on AWS, please add key while launching instances. 
- Navigate to ManageJenkins--> Security--> Agent
- Enable TCP port for inbound agents
- Select Fixed, and give port value as 50000
- Naivate to ManageJenkins--> Node
- Choose permanate and follow instruction to add a new Node
- Choose Launch by connecting to controller
- Click on new added node

 ## Connecting Slave with Master
  - Install Java
  - run command displayed on master node page
  - keep the process running, so not terminate process
