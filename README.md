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
    * Link it to the Rubric category we made
    * The testing command should be `cg-jest run ${STUDENT}main.test.js`
14. Config is done but **IMPORTANT**: don't forget to start the tests up at the top!
15. Done!
