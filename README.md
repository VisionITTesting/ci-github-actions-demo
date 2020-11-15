# CI implementation for Test Automation using GitHub Actions

Author
---

This Tutorial is created by Akash Tyagi.
You can reach out to me at: akashdktyagi@gmail.com 

Introduction
---
This demo is about how to use Git Hub Actions to create CI and CD pipeline. 
As a part of this demo we will implement git hub actions to build the maven project and trigger the test cases.

### Steps to Do 

* Create a Java Maven Project
* Add Junit dependency in POM file
* Create a test class and then add add two test cases.

```aidl
public class RunTest {

    @Test
    public void t_01_test_case_is_failed(){
        System.out.println("This test case is supposed to be failed.");
        Assert.assertEquals("Test assertion is failed", true,false);
    }

    @Test
    public void t_02_test_case_is_passed(){
        System.out.println("This test case is supposed to be passed.");
        Assert.assertEquals("Test assertion is passed", true,true);
    }
}
```
* Run the tests using command: ```mvn clean install```
* One test will pass and other will fail. That is how we have created these test cases, so that we can check the same behaviour in the github pipeline.
* Commit the project in a GitHub Repo