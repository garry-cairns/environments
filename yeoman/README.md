## Directions for use

Build the container by navigation to the directory in which you've house the Dockerfile and running:

    sudo docker build -t your-username/yeoman ./

Once it's built (warning, takes a while) you run it with

    sudo docker run -p 9000:9000 -itv /path/to/your/empty/project/dir:/home/yeoman your-username/yeoman /bin/bash

That will give you a shell in the container in which you can start an ember or angular project with, for example, `yo angular --coffee`. Once your project is build edit the Gruntfile to change the localhost to 0.0.0.0 where the comment indicates to do so. You can now develop, test and build your project in a container, then just drop the `/dist/` directory into your server when you're ready to deploy. Whether you see any benefit in this over local installation is up to your personal taste but if, like me, you often have to work on different machines this will save you a lot of boring setup work. 
