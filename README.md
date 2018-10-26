Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?

    Allow us to report and persist error and warning messages as well as info message to be analyzed later.

2.  Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']

    From the logging levels.

3.  What does Assertions.assertThrows do?

    Asserts that execution of the supplied executable throws an exception of the expectedType and returns the exception.
    If no exception is thrown, or if an exception of a different type is thrown, this method will fail.

4.  See TimerException and there are 3 questions
    1.  What is serialVersionUID and why do we need it? (please read on Internet)

        The serialization runtime associates with each serializable class a version number, called a serialVersionUID, which is used during deserialization to verify that the sender and receiver of a serialized object have loaded classes for that object that are compatible with respect to serialization.

    2.  Why do we need to override constructors?

        If the method has the same name, return type, and number of parameters, we use the override constructor to specify exactly what the method will be doing so that it will not perform its default behavior by calling the super() of its parent.

    3.  Why we did not override other Exception methods?
        We would get compile time errors.


5.  The Timer.java has a static block static {}, what does it do? (determine when called by debugger)

    Used for static initializations of the Class and called only once, either when an object of the class is initialized or when one of the members is accessed.

6.  What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)

    It is a markdown language file that is used to be a brief description or how to guide for using the software.

7.  Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)

    The test expects a TimerException but receives a NullPointerException. If we add an if() statement around the log.info output in the finally block with the condition that timeToWait >= 0 then the finally block will not execute the incorrect exception type.

8.  What is the actual issue here, what is the sequence of Exceptions and handlers (debug)

    It expects a TimerException but receives a NullPointerException because it executes the finally block which triggers the unexpected exception.

9.  Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel)



10.  Make a printScreen of your eclipse Maven test run, with console



11.  What category of Exceptions is TimerException and what is NullPointerException

    TimerException is a User-Defined Exception class and NullPointerException is a Built-In Exception class.

12.  Push the updated/fixed source code to your own repository.
