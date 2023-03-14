# Lab report 5
---

My favorite lab is lab 3 and my favorite lab report is lab report 2. Because Debug is a very important and useful skill.
I picked `ArrayExample.java` and `ArrayTests.java` to Debug. 
---

## Details about the test
---

We first look at the code in `ArrayExample.java`, Understand the `purpose` and `role` of these codes.
Then we write test code in `ArrayTests.java` to try different inputs. 
This is to test the results returned by the code in different cases

For example:

```
@Test
  public void testAverageWithoutLowest1(){
    double[] input1 = {1, 2, 4};
    assertEquals(2.0, ArrayExamples.averageWithoutLowest(input1), 0.01);
  }
```

This is the test code to check `testAverageWithoutLowest1` method. I will also change some other test code to test the return results of other methods

And the output shows what the method should return and what results were actually returned. 
---

Use :

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ArrayTests
```

These two commands work well to compile and run the JUnit.
---

Then we can see the result like this: 
![Image](lab5-1.png)
---

It shows Test code with data bias with the expected value and actually value, then I can go back to `testAverageWithoutLowest1` to find the bug and fix it.
