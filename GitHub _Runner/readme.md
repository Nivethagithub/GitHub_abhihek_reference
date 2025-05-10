Github action can be configured with self hosted runners and github runner itself. 

Self host runners can be EC2/VM/Containers. 

## When to use github runners
* It provides free resources, you can utilize for open source/public projects.

## When to use self hosted runners
* If your project is private and enterprise level.
* It has lot of artifacts to be built and deployed, in case github runners can fail due to resource limitations required to handle the cicd workloads.
* When security is very essential and it isn't a open source project.

  ## Configure self host runners

  ### Step1:
  **Create EC2 instance**
  1 . Update the security group in EC2.
       * Add inbound rules. Add HTTP **rule**, **source type** (anywhere IPV4 / My IP) . If **source type** is My IP, then include your IP address of github in **Source** option, else choose 0.0.0.0/0.
       * Add another rules. Add HTTPS  **rule**, **source type** (anywhere IPV4 / My IP) . If **source type** is My IP, then include your IP address of github in **Source** option, else choose 0.0.0.0/0.
       * Save the inbound rule.
       * Do the same for the outbound, add http and https rules. Save it.
   
  ### Step 2
  Configure the self hosted runners
  1.  Go to **setting** in github.
  2.  Select **Actions**, then click on **runners** in the left corner.
  3.  Click on the **new self-hosted runners** option in the right corner
  4.  Add the details of the runners here.  NOTE: Select the architecure correctly, if you are using your laptop, ensure to use the corrct architecture type.
  5.  Runner the ccommands as mentioned in the notes.
  6.  Connect to the agent with github using  ./run.sh
  7.  You can see the message in the terminal ---> **_listening for jobs_**.
  8.  Modify the github actions file. Go to github --> workflows --> <configuration>.yml file --> Add the below command.

```
jobs:
 build:
   runs-on: self-hosted
```

### How to store the secrets securely
We can use secrets and variables in Github.

### How to create CI in github. 
Create a folder called github/workflows --> create a yaml file (Define the runners, action (push or push, pull request) explain all the stages included.

### Compare with Jenkins and Github. 
Jenkins has lot of plugins, in-built integrations. It has good orchestration as well  --> **use when your project is a private one.** 
GitHub offers free resources to execute the process. The workflow is also simple to write code and use. --> **use when your project is public.** 
  
