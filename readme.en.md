# Course warm-up exercises

This repository contains Java exercises that help you review the contents of the Ohjelmointi 1 course and get familiar with how the exercises of this follow-up course work. The topics are strings, collections, and classes and objects. Detailed instructions for each method and class are in the comments of the Java classes in the template.

## Starting the exercise

First fork this repository into your own GitHub repository with GitHub's **Fork** button, and only then clone your fork to your computer:

```sh
git clone https://github.com/<your-github-username>/2-warming-up.git
```

Open the cloned project in your code editor.

## Testing

The parts of the exercise have ready-made [JUnit](https://junit.org/) unit tests in the [src/test/java](./src/test/java/) directory. Each part tells which test class grades it. You can run the tests with your code editor's testing tool ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)) or with [Gradle](https://docs.gradle.org/current/userguide/java_testing.html), for example:

```
./gradlew test --tests StringBasicsTest        # unix
.\gradlew.bat test --tests StringBasicsTest    # windows
```

Add `--info` to the end of the command for more details about failing tests. You do not need to study how the tests are implemented, and you can also try your solution with your own `main` method. You may write more tests of your own, but do not change or remove the given tests.

Do not change the names, parameters or return types of the given classes, methods and constructors, because the tests will then not compile. You get the original version of a file back with `git restore <path to file>` or with the **Palauta lähtökoodi** (restore starter code) function of the course system.

## Submitting and points

Each part of the exercise has its own page in the course system (https://jtjuslin.kapsi.fi/java), and its code fields contain the part's starter code. Copy your solution into the code fields or write it there directly. **Testaa ilman palautusta** (test without submitting) runs the part's tests without saving points, and **Lähetä** (submit) submits your solution. Each test class is accepted only if all of its tests pass, and the points are divided according to the accepted test classes.

**Points in two stages**

1. When your solution passes in the course system, you get **half of the points** for the part.
2. Finally, push everything to your public GitHub repository. Then press the **Lähetä tarkistettavaksi** (submit for checking) button on the part's page. When the tests pass, you get **full points** for the part. The repository may remain public.

There is no grading YAML workflow (GitHub Actions) on GitHub, and `git push` does not start any grading. When you press **Lähetä tarkistettavaksi**, the course system's bot fetches your code from your repository and checks it with the same tests. Both stages must be completed before the chapter deadline. You can submit as many times as you need, and your best result is kept.


## Part 1: strings *(recap, 30 %)*

The Java class [StringBasics](./src/main/java/part01/StringBasics.java) has methods, some of which contain bugs and some of which are not implemented. Fix and complete the methods according to their comments. `centerMultiLine` is an optional extra task: if it returns `null`, its test is skipped.

Graded with the test class [StringBasicsTest](./src/test/java/part01/StringBasicsTest.java).

💡 *The message of a failing test tells what was expected. For example, `expected: <He> but was: <Hello>` means that the test expected He, but your method returned Hello.*


## Part 2: collections *(recap, 30 %)*

Implement the methods of the [CollectionsBasics](./src/main/java/part02/CollectionsBasics.java) class according to their comments. The methods handle lists: the largest value, sum, multiplication, a range of numbers, joining strings, lengths and occurrences of a substring.

Graded with the test class [CollectionsBasicsTest](./src/test/java/part02/CollectionsBasicsTest.java).

🚀 *During the course, you will learn new ways to implement these methods. You can come back to them later and think about how you would implement them with streams, for example.*


## Part 3: classes and objects *(recap, 20 % + 20 %)*

Complete two Java classes:

* [Person](./src/main/java/part03/Person.java) models a person with a name and an age. Implement its instance variables, constructor and getters according to the comments of the class and its methods.
* The method of the [ObjectExercise](./src/main/java/part03/ObjectExercise.java) class handles a list of `Person` objects and joins the names into one string. The detailed rules are in the method's comments.

Graded with the test classes [PersonTest](./src/test/java/part03/PersonTest.java) (half of the points) and [ObjectExerciseTest](./src/test/java/part03/ObjectExerciseTest.java) (half of the points).


## License and authors

This exercise was developed by Teemu Havulinna and Jukka Juslin, and it is licensed under the [Creative Commons BY-NC-SA license](https://creativecommons.org/licenses/by-nc-sa/4.0/). ChatGPT 3.5 and GitHub Copilot were used in creating the assignment, the source code and the tests.
