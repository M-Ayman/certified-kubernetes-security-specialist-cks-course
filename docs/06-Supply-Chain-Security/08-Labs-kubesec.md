# Lab - Kubesec
  
  - Take me to [Lab](https://kodekloud.com/topic/labs-kubesec/)

Solution to Lab - Kubesec.

- What is the kubesec plugin used for?

    Answer: **`all of these`**


- To install kubesec plugin, Run

  Answer:

      wget https://github.com/controlplaneio/kubesec/releases/download/v2.11.0/kubesec_linux_amd64.tar.gz

      tar -xvf  kubesec_linux_amd64.tar.gz

      mv kubesec /usr/bin/


- **`Bash`** format is NOT supported by kubesec



- We have a pod definition template /root/node.yaml on controlplane host. Scan this template using kubesec and save the report in /root/kubesec_report.json file on controlplane host itself.

  Answer:
      kubesec scan /root/node.yaml  > /root/kubesec_report.json


- Look into the report generated by the previous scan and identify the final status of the scan.

  Look for the message in the report.

  Answer: FAILED


- kubesec scan failed for pod definition file /root/node.yaml . Fix the issues in this file as per the suggestions in the scan report and make sure that the final kubesec scan status is passed.

  Answer:

  In node.yaml template change privileged: true to privileged: false under securityContext:
