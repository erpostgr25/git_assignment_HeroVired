# git_assignment_HeroVired

// This repository is created for the assignment shared by Herovired on Git and GitHub.
// Due Date: 17 Aug 2025.
## Question 1
Step By Step Procedure:
1) Create Github Repository
   Name: git_assignment_HeroVired
2) Create & switch to dev branch:
   git checkout -b dev
3) Add python Code (CalculatorPlus.py):
  import math
  class Calculator:
      def add(self, a, b):
          return a + b
      def subtract(self, a, b):
          return a - b
      def multiply(self, a, b):
          return a * b
      def divide(self, a, b):
          return a / b
       def square_root(self, x):
          return math.sqrt(x)
  if __name__ == "__main__":
      calculator = Calculator()
      num1 = 16
      num2 = 4
      print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
      print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
      print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
      print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")
      num3 = 25
      print(f"The square root of {num3} = {calculator.square_root(num3)}")
4) Commit & push:
   a) git add .
   b) git commit -m "Calculator with sqrt"
   c) git push origin dev
5) Merge this branch into main and create version 1 release
   a) git checkout main
   b) git merge dev
   c) git tag v1.0
   d) git push origin main --tags
6) Add collaborators
   Settings → Collaborators → Add your classmate
7) Create new branch for feature: feature/sqrt
   git checkout -b feature/sqrt dev (This command will take the copy directly from dev and login into feature/sqrt branch to start working straight way)
8) Add the sqrt code
   num3 = 36
   print(f"The square root of {num3} = {calculator.square_root(num3)}")
9) Fix critical bug in divide function (in dev branch)
   a) git checkout dev
   b) Add code below:-
     def divide(self, a, b):
      if b == 0:
          raise ValueError("Cannot divide by zero.")
      return a / b
10) Commit fix:
    git commit -am "Fix divide by zero bug"
11) Update feature/sqrt branch with the fix:
    a) git checkout feature/sqrt
    b) git merge dev
12) Create Pull Request targeting
    git push origin feature/sqrt
13) Request Code Review
14) After approval
    a) git checkout dev
    b) git merge feature/sqrt
15) Merge into main:
    a) git checkout main
    b) git merge dev
    c) git tag v2.0
    d) git push origin main --tags
## Question 2
Result
<img width="1061" height="418" alt="image" src="https://github.com/user-attachments/assets/7001d5d7-619f-47ab-b8cd-eacd59141069" />
<img width="1068" height="752" alt="image" src="https://github.com/user-attachments/assets/999f6603-7693-40fa-b541-bf57de5e4576" />
## Question 3
Step By Step Procedure
1) Create the geometry-calculator branch
   a) git checkout -b geometry-calculator
2) Add the initial file and push the branch
   a) git add geometry_calculator.py
   b) git commit -m "<your input>"
   c) git push -u origin geometry-calculator
3) Create feature branch for circle area
   a) git checkout -b feature/circle-area geometry-calculator
4) Stash the incomplete circle work
   a) git stash push -m "Work In Progress: circle area"
   b) git stash list
   c) git status
5) Create feature branch for rectangle area
   a) git checkout geometry-calculator
   b) git checkout -b feature/rectangle-area geometry-calculator
6) Make partial edits for rectangle area
   a) git stash push -m "Work In Progress: rectangle area"
   b) git stash list
   c) git status
7) Return to feature/circle-area
   a) git checkout feature/circle-area
   b) git stash list
8) Apply the circle stash:
   a) git stash pop "stash@{1}"
9) Finish implementing
   a) git add geometry_calculator.py
   b) git commit -m "<your message>"
   c) git push -u origin feature/circle-area
10) Switch to feature/rectangle-area
   a) git checkout feature/rectangle-area
   b) git stash list
   c) git stash pop "stash@{0}"
11) Finish rectangle code
   a) git add geometry_calculator.py
   b) git commit -m "<your message>"
   c) git push -u origin feature/rectangle-area
12) Create Pull Requests to dev
   a) On GitHub: go to your repo.
   b) For branch feature/circle-area click Compare & pull request.
   c) Set base to dev.
   d) Add title + description, request reviewer, create PR.
13) Repeat for feature/rectangle-area.
14) After Review approved merge to dev branch
15) Later merge dev -> main (Add tag v3.0)
