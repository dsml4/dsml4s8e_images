# dsml4s8e_images

Images for the machine learning system development life cycle.  
Images notation: 
The prefix means the base image.

jds - base image from https://jupyter-docker-stacks.readthedocs.io/en/latest/

powershell commands:
```
cd jupyter-docker-stacks
dockre build -t jds_dsml4s8e .  
docker create --name jds_dsml4s8e -p 8899:8888 -v C:\Users\$env:UserName\education\work:/home/jovyan/work jds_dsml4s8e 
```

Docker in VS Coded
https://code.visualstudio.com/docs/containers/overview 
Build Image...

VS Code extension:
Remote - Containers https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers
Docker for Visual Studio Code https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker

VS Code extension inside container:
pylance https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance