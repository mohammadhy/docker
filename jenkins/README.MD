# Jenkins & jenkins-agent
## To Have Jenkins server And Run your pipeline on Agent.

## Prerequisites
1. install docker & docker-compose:
    ```bash
    https://docs.docker.com/engine/install/
    ```

## Usage
1. Need To Have ssh-key with command 
   ``` bash 
    ssh-keygen
    ```
2. Copy publickey into composefile agent
    ``` bash
    environment:
    - JENKINS_AGENT_SSH_PUBKEY=<public-key here>
    ```
3. Run composefile
    ``` bash
    docker compose up -d
    ```
4. Install plugins **ssh build agent**
5. Add New Node 
   ```
   1) Enter Name
   2) Enter Root Directory: /home/jenkins/agent
   3) Enter Labels That You Want Call in Your Pipeline
   4) Select Launch agents via ssh
   4.1) Enter Host
   4.2) Enter Private-Key Into Credentials
   4.3) Select Host-key verification To Non Verifying Verification
   ```
