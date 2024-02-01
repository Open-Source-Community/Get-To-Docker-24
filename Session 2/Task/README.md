### How to deliver tasks 


1. Make a directory (folder) with the name of the session (ex: Session 0, Session 2, etc...).

2. Inside the folder, make a text or markdown file.

3. In the file write each question's number and the command you used to solve it.

4. Some questions may require posting an screenshot, in this case take a screenshot of the required part and rename it to the question number (ex: Q1.png, Q4.png, etc...) and put it in the folder you created with the text or markdown file.

---

## Task 2

### A

#### We will create two images here

* First one is called `alpine-gcc`:
  1) We will use `alpine` as base image.
  2) We want to install the C++ compiler, the command to install it is `apk add gcc`.

* Second one is called `alpine-hello-world`:
  1) We will use the previously created `alpine-gcc` image as a base.
  2) Download the main.cpp file in this folder and copy it to `/usr/hello-world` directory in the container.
  3) Change to the directory you copied `main.cpp` to.
  4) Compile it using `g++ -o Main main.cpp`.
  5) When the container starts we want to run the compiled file, to do so we need to run.

---

### B

#### Please download the `server` folder 

* The Dockerfile in the `server` folder is incorrect, there are 3 faults.
