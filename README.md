## Some Docker cmd using in this project
 Build img: docker build -t todo-app:v1.0 .
-> docker build -t {project-name}:{tag-version} . 
    -t stands for tag, alow to tag img version

 Create container: docker run -dp 3000:3000 todo-app
-> docker run -dp {hostPort}:{containerPort} todo-app
    -d: detached mode
    -p: port mapping
    Without the -d flag, the container would run in the foreground and show you the container's logs directly in your terminal. Without the -p flag, you wouldn't be able to access the application from outside the container.

 Stop and delete container: docker rm -f 7de74b95face
-> docker rm -f {container-id}
    -f: force stop

 Docker compose: 
    docker-compose up
    docker-compose down

 List all active container: docker ps

 Assign tag to push img: docker image tag todo-app clemy1004/todo-app-2:v1.0
-> docker image tag {project-name} clemy1004/{proj-name}:{tag-version}

 Push img to docker hub: docker push clemy1004/todo-app:v1.0
-> docker push clemy1004/{img-tag}

 Pull img to local docker: docker pull clemy1004/todo-app:v1.0
-> docker pull clemy1004/{img-tag}

## Some k8s cmd using in this project
 Get pods/services/node/deployments: kubectl get {pods/services/node/deployments} -o wide
 Get detailed: kubectl describe {pods/services}
 Get services: kubectl get services
 Deploy: kubectl apply -f deployment.yaml
 Delete deployment: kubectl delete deployment {deployment-name} -n {namespace}
 Get deployment status: kubectl rollout status {deployment-name}
 Get deployment log: kubectl logs {deployment-id}