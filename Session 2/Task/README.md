### How to deliver tasks (Please read first) 


1. Make a directory (folder) with the name of the session (ex: Session 0, Session 2, etc...).

2. Inside the folder, make 2 folders called `A` and `B`

3. In each folder upload the `Dockerfile` (in case of question `A` create a new folder for each image and place its Dockerfile in the folder)

---

## Task 2

### A

#### We will create two images here

* First one is called `alpine-gcc`:
  1) We will use `alpine` as base image.
  2) We want to install the C++ compiler, the command to install it is `apk add gcc`.

* Second one is called `alpine-hello-world`:
  1) We will use the previously created `alpine-gcc` image as a base.
  2) Download the `main.cpp` file in this folder and copy it to `/usr/hello-world` directory in the container.
  3) Change to the directory you copied `main.cpp` to.
  4) Compile it using `g++ -o Main main.cpp`.
  5) When the container starts we want to run the compiled file, to do so we need to run.

---

### B

#### Please download the `server` folder 

* The Dockerfile in the `server` folder is incorrect, there are 3 faults.

  1) Correct the Dockerfile
  2) Build the image and start a new container from it (the server runs on port `3000`)
  3) Access the server using `localhost:<port_number>/tasks/` and take a screenshot, and upload it in the `B` folder.
   
   
