# Task 4: Jenkins Installation and Configuration

## Objective

In this Task4 was created kubernetes infrastructure based on k3s cluster and deployed Jenkins based on  HELM. 

## Steps

1. **Create k3s cluster**
   - Create cluster based on  k3s.
        - curl -sfL https://get.k3s.io | sh -
        - sudo k3s kubectl get node

2. **Install Helm**
   - Install Helm
        - curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3

3. **Install Jenkins**
   - Prepare configuration file to create environment for deploy Jenkins Helm  chart
        - create additional namespace for deploy Jenkins (kubectl create namespace jenkins)
        - create configuration  files for environment Jenkins (jenkins-sa.yaml,jenkins-volume.yaml)

4. **Install Jenkins from  Helm chart**
   - Install Helm for deploy Jenkins server
        - screen [helm](images/install_jenkins_helm.png)
   - Verify cluster.
        - screen [kubectl](images/create_jenkins_pod_svc_pv.png)
   - Create NodePort for access from Internet.
        - screen [expose NodePort](images/expose_nodeport_jenkins.png)
5. **Deploy a simplepipepline on  Jenkins**
   - Deploy a simple pipepline on  jenkins
       - screen [jenkins pipepline](images/jenkins_pipeline1.png)
       - screen [jenkins job](images/jenkins_1_job.png)
       - screen [jenkins gui](images/jenkins_1_job_finish.png)
6. **Additional task**
   - in progress...