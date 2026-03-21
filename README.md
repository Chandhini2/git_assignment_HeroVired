# git_assignment_HeroVired

This repository contains a simple Python project CalculatorPlus and Geometry Calculator, along with Git workflows such as branching, merging, Git LFS, and stash usage.


Q1: CalculatorPlus Application

Step 1: Create Repository

Command used:

git clone <repository_url>

Use case:
Downloads a project from GitHub to your local system so you can start working on it.

Step 2: Create dev Branch and Add Code

Commands used:

git checkout -b dev

Use case:
Creates a new branch called dev and switches to it.
Used to work on changes without affecting the main code.

Basic Calculator Code
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
Step 3: Add and Commit Code

Commands used:

git add .
git commit -m "Added calculator code"

Use case:

git add . → Selects all files to be saved
git commit → Saves changes permanently in Git
Step 4: Merge to Main & Release Version 1

Commands used:

git checkout main
git merge dev

Use case:
Combines changes from dev branch into main.

Step 5: Add Collaborator

Use case:Allows other people to access and contribute to the project.

Step 6: Create Feature Branch

Command used: git checkout -b feature/sqrt

Use case:Creates a separate branch to work on a new feature safely.

Step 7: Bug Fix in Divide Function

Fixed Code:
def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
Step 8: Keep Branch Updated

Commands used:

git checkout dev
git pull
git checkout feature/sqrt
git merge dev

Use case:

git pull → Gets latest updates from GitHub
git merge dev → Updates feature branch with latest fixes
Step 9: Push Changes

Command used:

git push origin feature/sqrt

Use case:
Uploads your branch to GitHub.

Step 10: Pull Request & Review

(No command – done in GitHub UI)

Use case:Used to request merging of code and get it reviewed.

Step 11: Merge and Release Version 2

Commands used:

git checkout dev
git merge feature/sqrt
git checkout main
git merge dev

Use case:
Final merging of all features into main branch.

Q2: Git LFS (Large File Storage)
Step 1: Create LFS Branch

Command used:

git checkout -b lfs

Use case:
Creates a branch to work with large files.

Step 2: Track Large Files

Command used:

git lfs track "*.zip"

Use case:
Tells Git to handle .zip files using LFS instead of normal Git.

Step 3: Add Attributes File

Command used:

git add .gitattributes

Use case:
Saves LFS tracking rules in the repository.

Step 4: Add and Commit Large File

Commands used:

git add .
git commit -m "Added large file"

Use case:
Adds and saves large file changes.

Step 5: Push to GitHub

Command used:

git push origin lfs

Use case:Uploads large files using Git LFS.

Step 6: Verify LFS Files

Command used:

git lfs ls-files

Use case:
Shows which files are managed by Git LFS.

Q3: Geometry Calculator
Base Code
import math

class GeometryCalculator:

    def calculate_circle_area(self, radius):
        return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width
Step 1: Create Circle Feature Branch

Command used:

git checkout -b feature/circle-area

Use case:
Creates a branch to work on circle area feature.

Step 2: Stash Work

Command used:

git stash

Use case:
Temporarily saves unfinished work without committing.

Step 3: Create Rectangle Feature Branch

Command used:

git checkout -b feature/rectangle-area

Use case:
Creates another branch for rectangle feature.

Step 4: Stash Again

Command used:

git stash

Use case:
Saves rectangle work temporarily.

Step 5: Retrieve Stash

Command used:

git stash pop

Use case:
Restores the last saved work.

Step 6: Commit and Push

Commands used:

git add .
git commit -m "Completed feature"
git push

Use case:
Saves and uploads completed work.

Step 7: Pull Requests

(No command – done in GitHub UI)

Use case:
Request to merge feature branches into dev.

Step 8: Final Merge

Commands used:

git checkout dev
git merge feature/circle-area
git merge feature/rectangle-area
git checkout main
git merge dev

Use case:
Combines all features into final project.

Final Outcome
Calculator with square root
Bug-free division
Large file support using Git LFS
Geometry calculator
Proper Git workflow (branching, merging, pull requests)
