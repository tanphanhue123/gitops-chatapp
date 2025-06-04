# Helm Charts for GitOps ChatApp

This folder contains Helm charts for deploying various components of the GitOps ChatApp. These charts are managed using an ArgoCD ApplicationSet for automated GitOps deployment.

## Folder Structure

- **application/**  
  Helm chart for the main application logic.
  
- **database/**  
  Helm chart for the database service.
  
- **reverb/**  
  Helm chart for the reverb service.
  
- **scheduler/**  
  Helm chart for the scheduler service.
  
- **worker/**  
  Helm chart for the worker service.

## How to Use with ArgoCD ApplicationSet

1. **Ensure ArgoCD and ApplicationSet Controller are Installed**  
   Install ArgoCD and the ApplicationSet controller in your Kubernetes cluster.  
   [ArgoCD Installation Guide](https://argo-cd.readthedocs.io/en/stable/getting_started/)

2. **Configure ApplicationSet**  
   Use the `argocd/application-set.yaml` file to define an ApplicationSet that automatically scans the `helmchart/` folder and creates ArgoCD Applications for each chart.

3. **Apply the ApplicationSet Configuration**  
   Run the following command to apply the ApplicationSet:

   ```sh
   kubectl apply -f argocd/application-set.yaml
   ```

4. **Automatic Deployment**  
   - ArgoCD will automatically detect all Helm charts in the `helmchart/` folder.
   - Each chart will be deployed as a separate application in the Kubernetes cluster.
   - The `values-dev.yaml` file in each chart folder will be used for configuration.

## Customization

- **Add or Remove Applications**  
  To add or remove applications, simply add or delete folders in the `helmchart/` directory. The ApplicationSet will automatically update.

- **Override Values**  
 # Helm Charts for GitOps ChatApp

This folder contains Helm charts for deploying various components of the GitOps ChatApp. These charts are managed using an ArgoCD ApplicationSet for automated GitOps deployment.

## Folder Structure

- **application/**  
  Helm chart for the main application logic.
  
- **database/**  
  Helm chart for the database service.
  
- **reverb/**  
  Helm chart for the reverb service.
  
- **scheduler/**  
  Helm chart for the scheduler service.
  
- **worker/**  
  Helm chart for the worker service.

## How to Use with ArgoCD ApplicationSet

1. **Ensure ArgoCD and ApplicationSet Controller are Installed**  
   Install ArgoCD and the ApplicationSet controller in your Kubernetes cluster.  
   [ArgoCD Installation Guide](https://argo-cd.readthedocs.io/en/stable/getting_started/)

2. **Configure ApplicationSet**  
   Use the `argocd/application-set.yaml` file to define an ApplicationSet that automatically scans the `helmchart/` folder and creates ArgoCD Applications for each chart.

3. **Apply the ApplicationSet Configuration**  
   Run the following command to apply the ApplicationSet:

   ```sh
   kubectl apply -f argocd/application-set.yaml
   ```

4. **Automatic Deployment**  
   - ArgoCD will automatically detect all Helm charts in the `helmchart/` folder.
   - Each chart will be deployed as a separate application in the Kubernetes cluster.
   - The `values-dev.yaml` file in each chart folder will be used for configuration.

## Customization

- **Add or Remove Applications**  
  To add or remove applications, simply add or delete folders in the `helmchart/` directory. The ApplicationSet will automatically update.

- **Override Values**  
 