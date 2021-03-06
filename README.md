# CodeGrade Jest Config

How to create a simple, auto-tested CodeGrade assignment using Jest.

## Create an assignment with Jest tests

1. Go to Populi > Assignments
2. Create new assignment
3. Set Type to External LTI Tool
4. Set LTI Tool to CodeGrade
5. Create the assignment, go to it's CodeGrade link
6. Go to the Rubric tab
7. Add a category
    * Set it as Continuous
    * Give it some points
    * Call it Jest Tests
9. Go to the AutoTest tab
10. Upload fixtures
    * main.test.js (your tests)
    * jest.config.js (found in this repo)
11. Set Global setup script to `cg-jest install`
12. Set Per-student setup script to `mv $FIXTURES/*.js $STUDENT`
13. Add a Level
    * Make it a Unit Test
    * Set 'Unit Test Framework' to `Custom`
    * Set 'Program to test' to `cg-jest run ${STUDENT}main.test.js`
    * Link it to the Rubric category we made
    * Give it a weight of 100
    * Name it Jesting Testing
14. Config is done but **IMPORTANT**: don't forget to start the tests up at the top!
15. Go to the General tab
16. Go to "Upload Submission" at the bottom right, and check the box that says "Test Submission"
17. Using a completed version of the assignment, upload main.js
18. Go back to the AutoTest Tab. You should see the results for Test Student. If it's 100/100, it worked!
19. Done!
