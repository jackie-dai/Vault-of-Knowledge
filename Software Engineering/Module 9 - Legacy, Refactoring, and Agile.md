

## **Legacy Code**:
A codebase that is not understood because it's original developers are gone.

**Steps to understanding legacy app**
1. Check out the scratch branch to run the app in a development environment 
2. Learn and replicate the user stories (understanding the user perspective when using the app)
3. Examine the database schema and the relationships among the most important classes.
4. Skim all the code to quantify code quality and test coverage

### Class Responsibility Collaborator (CRC)
Create a card for each class object, defining the
- Knows (what instance variables it has)
- The instance methods
- What classes it belongs to


## Spotting Problems in your code
### Code Metrics

## Code Smells

**SOFA**
- **S**hort
- do only **O**ne thing
- take **F**ew arguments
- maintain a consistent level of **A**bstraction

**Long Method**: when a method get too long in terms of lines of code. It is a sign we should refactor the code

Refactoring methods
- Extract method
- Decompose conditional
	- Situation: when a conditional becomes nested two deep or more
	- Solution: replace each arm of the conditional with a extracted method

**Technical debt**: when a emergency arises, clean code goes out the window and fast working code is prioritized. This creates technical debt that the maintenance team needs to refactor and write documentation for. 