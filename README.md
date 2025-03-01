# git_assignment_HeroVired## 🚀 (Question 1) - Step-by-Step Guide

#### 📝 1. Create a GitHub Repository  
- Log in to GitHub

##### Go to [GitHub](https://github.com/) and sign in.
- Create a New Repository
1. Click on the **"+"** sign in the top right corner.  
2. Select **"New repository"** from the dropdown. 
##### Enter Repository Details  
- **📂 Repository Name:** `git_assignment_HeroVired`  
- **📝 Description (Optional):** Add a short description if needed.  
- **🔒 Visibility:** Set to **Private** (only you and collaborators can see it).

##### Initialize the Repository  
✅ **Check** the box for **"Add a README file"** _(optional but recommended)_.  
✅ **Optionally,** add a `.gitignore` file if needed.
##### Create the Repository  
💾 Click **"Create repository"** to finalize the setup.  

#### 🌿 2. Clone the Repository  
```sh
git clone https://github.com/sboddapati/git_assignment_HeroVired.git
cd git_assignment_HeroVired
```

#### 🔀 3. Create and Switch to the dev Branch
```sh
git checkout -b dev
```

#### 📂 4. Add Your Code to the Repository
- Create `calculator.py` file & add code or modify a file.
```py
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

if __name__ == "__main__":
    calculator = Calculator()

    num1 = 16
    num2 = 4
    
    print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
    print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
    print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
    print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")
```
- Add your changes:
```sh
git add .
```
- Commit the changes:
```sh
git commit -m "Added initial code to dev branch"
```

#### 🚀 5. Push the dev Branch to the Remote Repository
```sh
git push origin dev
```

#### 🔀 6. Merge `dev` into `main` and Release Version 1
```bash
git checkout main
git merge dev
git push origin main
git tag v1.0
git push origin v1.0
```

### 🚀 Add a Classmate as a Collaborator on GitHub

#### 🛠️ 1. Open the Repository Settings
- Navigate to your repository.
- In the **top-right corner**, click on the **⚙️ Settings** tab.
- In the **left sidebar**, scroll down and click on **👥 Collaborators** under the **Access** section.

#### ➕ 2. Add a Collaborator
- Click on the **🔹 "Add people"** button.
- In the search box, type your classmate’s **GitHub username, email, or name**.
- Select their **GitHub profile** from the list.
- Click **✅ "Add"** to invite them.

#### 📩 3. Wait for Acceptance
- Your classmate will receive an **email invitation** to join the repository.
- They must **accept the invitation** before they can access the repository.

#### 🔍 4. Verify Access
- Once they accept, their name will appear under the **Collaborators** list.
- They can now **push, pull, and contribute** to your repository. 🎉

### 🚀 **Implementing a Square Root Feature in Git**  

#### 🌿 **Create a New Branch for the Feature**  
Before making changes to the project, it's a best practice to create a new branch. This ensures that the main branch remains stable while you develop new features.  

#### 🛠 **Command:**  
```bash  
git checkout -b feature/sqrt  
```
#### 🔢 **Implement the Square Root Feature**  
Now that you have a dedicated branch, modify the your calculator file (or an equivalent module in your project) to add a square root function.

##### 📝 **Modify your calculator:**  
```py 
import math  

class Calculator:  
    def square_root(self, x):  
        """Returns the square root of a given number."""  
        return math.sqrt(x)

    num3 = 25
    print(f"The square root of {num3} = {calculator.square_root(num3)}")
```

#### 📌 **Commit and Push the Changes:**  
After making modifications, commit and push the changes to the feature branch.

```bash  
git add .
git commit -m "✨ Implement square root function"  
git push origin feature/sqrt  
```
#### 🛠️ Fix a Critical Bug in `dev` Branch
Switch back to `dev` and pull the latest changes:

```bash
git checkout dev
git pull origin dev
```

Modify your calculator file to handle division by zero properly:

```py
def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
```

Commit and push the fix:

```bash
git add .
git commit -m "🐞 Fix divide by zero bug"
git push origin dev
```

#### 🔄 Keep `feature/sqrt` Branch Updated
```bash
git checkout feature/sqrt
git merge dev
git push origin feature/sqrt
```

#### 🔀 Create a Pull Request

1. Go to **GitHub → Pull Requests → New Pull Request**
2. Select `feature/sqrt` as the source branch and `dev` as the target branch.
3. Review the changes and ensure that everything is correct.
4. Add a meaningful title and description explaining the changes.
5. Click **Create Pull Request** to submit it for review.
6. Wait for feedback, make any necessary changes, and merge once approved.

#### 👀 Request Code Review and Address Feedback
1. Tag a team member for a code review.
2. Wait for feedback and suggestions.
3. Make necessary improvements based on the review.
4. Push the updated changes if required.
5. Once all feedback is addressed, proceed with merging the pull request.


#### 🔂 Merge `feature/sqrt` into `dev`

After approval:

```bash
git checkout dev
git merge feature/sqrt
git push origin dev
```

#### ✅ Final Testing in `dev` and Merge to `main`
```bash
git checkout main
git merge dev
git push origin main
git tag v2.0
git push origin v2.0
```
#### 🎉 Version 2 Released!



---





## 📦 **(Question 2) - Using Git LFS for Large Files in a Repository**

### 🚀 **Step 1: Install Git LFS**
If Git LFS is not installed, install it using the following commands:

##### 🖥 **For Windows:**
```sh
git lfs install
```

##### 🐧 **For Ubuntu/Linux:**
```sh
sudo apt install git-lfs
git lfs install
```

#### 🌿 **Step 2: Clone the Repository and Create a New Branch**
Clone the repository and create a new branch named **lfs**.

```sh
git clone https://github.com/sboddapati/git_assignment_HeroVired.git
cd git_assignment_HeroVired
git checkout -b lfs
```

#### 🔧 **Step 3: Configure Git LFS and Track Large Files**
Initialize Git LFS in your repository.

```sh
git lfs install
```

Track large binary files (e.g., `.zip`, `.mp4`, `.iso`, `.exe`, etc.).

```sh
git lfs track ".\VirtualBox-7.1.6-167084-Win.exe"
```

This will create a `.gitattributes` file in the repository.

#### 📂 **Step 4: Upload a Large File**
- Copy or move a **117MB+** file into the repository.
- Add the file to Git.

```sh
git add .gitattributes
git add .
```

Commit the changes.

```sh
git commit -m "Added large file using Git LFS"
```

#### 📤 **Step 5: Push the Large File to the Repository**
Push the `lfs` branch to GitHub.

```sh
git push origin lfs
```

Git LFS will automatically handle the large file upload.

#### 🔍 **Step 6: Verify by Cloning on Another Machine**
On another system, clone the repository and checkout the **lfs** branch.

```sh
git clone https://github.com/sboddapati/git_assignment_HeroVired.git
cd git_assignment_HeroVired
git checkout lfs
git lfs pull
```

This will download the large file correctly from Git LFS storage.

#### ✅ **Verification**
To check if Git LFS is handling your file properly, run:

```sh
git lfs ls-files
```
You should see your large file listed.



---




### 📌 **(Question 3) - Geometry Calculator Git Workflow**
This document outlines the Git workflow for implementing the **Geometry Calculator**, which calculates the area of a **circle** and a **rectangle** using a structured branching strategy.

### 🌜 **Workflow Steps**

#### 🔹 **Clone the Repository & Create a Main Feature Branch**
```sh
# Clone the repository
git clone https://github.com/sboddapati/git_assignment_HeroVired.git
cd git_assignment_HeroVired

git checkout main

# Create a new branch for the geometry calculator
git checkout -b geometry-calculator
```
- Create a new file named `geometry_calculator.py` and add the code.

```py
import math

class GeometryCalculator:

    def calculate_circle_area(self, radius):
        return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

if __name__ == "__main__":

    calculator = GeometryCalculator()
```
#### 🔹**Create a Branch for the Circle Area Feature**
```sh
# Create a new branch for circle area calculation
git checkout -b feature/circle-area
```
👨‍💻 **Modify the `geometry_calculator.py` file**:
```py
radius = 5
print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")
```

🚀 **Save incomplete changes using Git stash**:
```sh
git stash
```

✅ **Verify clean working directory**:
```sh
git status
```

#### 🔹**Create a Branch for the Rectangle Area Feature**
```sh
# Switch to a new branch for rectangle area calculation
git checkout -b feature/rectangle-area
```

👨‍💻 **Modify the `geometry_calculator.py` file**:
```py
length = 10
width = 6
print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")
```

🚀 **Save incomplete changes using Git stash**:
```sh
git stash
```

✅ **Verify clean working directory**:
```sh
git status
```

#### 🔹 **Switch Back to the Circle Area Branch & Complete It**
```sh
# Switch to the circle area branch
git checkout feature/circle-area

# Retrieve stashed changes
git stash pop "stash@{1}"
```

📉 **Commit and push the changes**:
```sh
git add .
git commit -m "Added circle area calculation"
git push origin feature/circle-area
```
#### 🔹 **Switch Back to the Rectangle Area Branch & Complete It**
```sh
# Switch to the rectangle area branch
git checkout feature/rectangle-area

# Retrieve stashed changes
git stash pop "stash@{0}"
```

📉 **Commit and push the changes**:
```sh
git add .
git commit -m "Added rectangle area calculation"
git push origin feature/rectangle-area
```
#### 🔹 **Create Pull Requests**
📌 **Go to GitHub and create pull requests**:

1️⃣ Create a **Pull Request** from `feature/circle-area` → `dev` branch.  
2️⃣ Create another **Pull Request** from `feature/rectangle-area` → `dev` branch. 

**Note:  If you are merging a branch into the dev branch, ensure that any conflicts are resolved.**

#### 🔹**Review & Merge**
👀 **Code Review**:
- Request a **team member** to review your PRs.
- Fix any requested changes.

✅ **Merge the PRs into `dev` branch**.

#### 🔹 **Merge Into `main`**
📌 Once the features are **tested & verified** in `dev`:
1️⃣ Create a **final pull request** from `dev` → `main`.  
2️⃣ Merge the changes after review.  

**Note:  If you are merging a branch into the dev branch, ensure that any conflicts are resolved.**

---

## 🎯 **Final Git Workflow Summary**
| Step | Command |
|------|---------|
| Clone the repository | `git clone https://github.com/sboddapati/git_assignment_HeroVired.git` |
| Create a new branch | `git checkout -b geometry-calculator` |
| Create a branch for the circle feature | `git checkout -b feature/circle-area` |
| Stash circle feature changes | `git stash` |
| Create a branch for the rectangle feature | `git checkout -b feature/rectangle-area` |
| Stash rectangle feature changes | `git stash` |
| Switch back to `feature/circle-area` | `git checkout feature/circle-area` |
| Retrieve stashed changes for the circle feature | `git stash pop "stash@{0}"` |
| Commit and push circle feature | `git add . && git commit -m "Added circle area calculation"` <br> `git push origin feature/circle-area` |
| Switch to `feature/rectangle-area` | `git checkout feature/rectangle-area` |
| Retrieve stashed changes for the rectangle feature | `git stash pop "stash@{1}"` |
| Commit and push rectangle feature | `git add . && git commit -m "Added rectangle area calculation"` <br> `git push origin feature/rectangle-area` |
| Create pull requests on GitHub | PR from `feature/circle-area` → `dev` <br> PR from `feature/rectangle-area` → `dev` |
| Merge into `dev` | After approval, merge PRs |
| Merge `dev` into `main` | Final merge after testing |

## 🌟 **Expected Output**
After running the Python script:
```sh
The area of the circle with radius 5 = 78.53981633974483
The area of the rectangle with length 10 and width 6 = 60
```