load('ext://kubebuilder', 'kubebuilder') 

docker_build('dtr.thefacebook.com/k8s/aqueduct', '.', 
    dockerfile='Dockerfile')

yaml = kustomize('config/default/')
k8s_yaml(yaml) 

k8s_resource('aqueduct-controller-manager',
    port_forwards=8000)
