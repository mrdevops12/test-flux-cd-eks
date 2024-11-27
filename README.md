Assume you have alredy AWS EKS Clsuter , in that cluster if you want install FluxCD 

Login into your kubectl server/system and follwo below steps 

Install and Bootstrap Flux CD:

     curl -s https://fluxcd.io/install.sh | sudo bash

Bootstrap Flux CD:
    Bootstrap to GitHub/GitLab/BitBucket repository:

            flux bootstrap github \
                --owner=<github-username> \
                --repository=<repo-name> \
                --branch=main \
                --path=./clusters/my-cluster \
                --personal

    example: https://github.com/mrdevops12/test-flux-cd-eks/edit/main/README.md   in this URL 
             Owner: mrdevops12
             Repo: test-flux-cd-eks


Verify Flux CD Installation
    Confirm flux-system namespace is created:

      kubectl get ns flux-system
      kubectl get pods -n flux-system


      






      


   
