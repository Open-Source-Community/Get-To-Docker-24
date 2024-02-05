# Task 3

## How to deliver the task

1. Make a directory (folder) with the name of the session (ex: Session 0, Session 2, etc...).

2. Create a markdown file wth the name `task3.md`:
   - `(Question 1 and 2)`: Write the command you used to solve each question in the file.
   - `(Question 3)`: Paste in the file a screen shot of the output of the command you used to solve the question
   - `(Question 4)`: Write in the list the IP V4 address of each container

---

## Questions

1. Create a new container named `db1` from a `postgres` image with environment variables `POSTGRES_PASSWORD=pass1234`

   - The container should be running in the background
   - You have to make the data presistent between the contaienr and the host using `two` different methods
   - We need to be able to connect to the container on port `5432` without **port mapping**
   - We want to specifiy the max memory usage for the container to be `500MB`

2. Create `4` contaienrs `c1`, `c2`, `c3`, and `c4` from the `alpine` image where

   - `c1` should be able to connect to send request to `c2` via its container name `(and you should show example when c1 sends a request to c2)`

   - `c3` and `c4` should be able to send requests to each other via their `ip addresses` only `(and you should show example when c3 sends a request to c4)`

3. Print the current state of all of your docker networks in your host machine

4. Print the the `IP V4` address of each container `db1`, `c1`, `c2`, `c3`, and `c4`
