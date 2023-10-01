# DContainer
This project is a container structure to use to program inside the container with the helix editor in different language, each in a different isolated container.

## Usage
As long as the command-line app is not done, you can only use the containers manually.
To use this project you need to install `podman`.
Then you must follow the steps:
1. Build the Container in the common directory  
  `podman build -t dev:common ./common/`  
2. Build the other container you need  
  `podman build -t dev:<lang> ./<lang>`  
3. Run the container containing your desired repsoitory  
  `podman run -it -v /path/to/repository:/src --name crypto dev:<lang> /bin/bash`  

The first step is only needed to do once. After that you can start with step 2  

The build and run process is going to be automated in the future!