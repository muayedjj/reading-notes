# Ten Thousand Game 1

## Random Module in Python
- Perhaps the most important thing about the random module is that it allows you to generate random numbers. Also, provides access to functions that support many operations. [1] 

### Randint
- If we want a random integer, we can use the randint function Randint **accepts two parameters: a lowest and a highest number**. 

- Example: Generate integers between 1,5. The first value should be less than the second.
`import random`
`print random.randint(0, 5)`
*This will output either 1, 2, 3, 4 or 5.*

### Random
- If we want a larger number, you can multiply it.

- Example: a random number between 0 and 100:
`import random`
`random.random() * 100`

### Choice
- Used to generate a random value from the sequence sequence.
- The choice function can often be used for choosing a random element from a list.

### Shuffle
- The shuffle function, shuffles the elements in list in place, so they are in a random order.

### Randrange
- Generate a randomly selected element from `range(start, stop, step)`.

_For more on the subject of *The Random Module* check this [article](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python) on pythonforbeginners.com_

# 

## Risk Analysis in Software Testing

> _The probability of any unwanted incident is defined as *Risk*._
> In Software Testing, *risk analysis* is the process of identifying the risks in applications or software that you built and prioritizing them to test. [2]

### Possible risks that one might encounter while developing software

1. Use of new hardware.

2. Use of new technology.

3. Use of new automation tool.

4. The sequence of code.

5. Availability of test resources for the application.

###  Unavoidable risks 
1. The time that you allocated for testing.

2. A defect leakage due to the complexity or size of the application.

3. Urgency from the clients to deliver the project.

4. Incomplete requirements.

### Measures that can be taken include
- Conduct Risk Assessment review meeting

- Use maximum resources to work on high-risk areas

- Create a Risk Assessment database for future use

- Identify and notice the risk magnitude indicators: high, medium, low.

### **Risk magnitude indicators**
1. High: means the effect of the risk would be very high and non-tolerable. The company might face loss.

2. Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

3. Low: it is tolerable. There lies little or no external exposure or no financial loss.

### Risk Identification
Sets of risks included in the risk identification process are:
1. Business Risks.
2. Testing Risks.
3. Premature Release Risk.
4. Software Risks.

### The perspective of Risk Assessment
There are three perspectives of Risk Assessment:

1. Effect

2. Cause

3. Likelihood

### How to perform Risk Analysis?
There are three steps:

Searching the risk

Analyzing the impact of each individual risk

Measures for the risk identified

# 

## Test Coverage

> Test coverage is a useful tool for finding untested parts of a codebase. Test coverage is of little use as a numeric statement of how good your tests are. [3]

If you make a certain level of coverage a target, people will try to attain it. The trouble is that high coverage numbers are too easy to reach with low quality testing. [3]
Note that _you are testing too much_ if you can remove tests while still having enough.
> TDD is a very useful, but certainly not sufficient, tool to help you get good tests.

**Sufficiency of testing** is much more complicated attribute than **coverage** can answer.
To know you are doing enough testing if the following is true:

- You rarely get bugs that escape into production, and
- You are rarely hesitant to change some code for fear it will cause production bugs.

Again the value of coverage analysis is that it helps you find which bits of your code aren't being tested.



[1]: https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python
[2]: https://www.edureka.co/blog/risk-analysis-in-software-testing/
[3]: https://martinfowler.com/bliki/TestCoverage.html