# Reading 6 - Game of Greed 1

## Random Module 

**Random module**- access to functions and support many operations. Also provides ability to generate random number.

**Randit**- accepts two parameters (high and low numbers)
-The output would be two random integers within those two numbers.
-First value should be less than the second

**Random**- output is a large random number.

**Choice**- generates random value from the sequence.

**Shuffle**- "shuffles" list elements so that the order is scrambled randomly.

**Randrange**- generates randomly selected element from range

## Risk Analysis

**Risk Analysis**- targeting the risks in apps or software and create tests to fix them.

### Why Risk Analysis

Risk analysis *highlists* potential code blockers

### Potential Risks

1.New Hardware
2.New technology
3.New automation tool
4.Sequence of code
5.Obtainable test resource

### Unavoidable Risks

1.Time to test
2."Leakage" from enlarge applications
3.Deadlines
4.Unfinished requirements

### Taking Care of Such Risks

1.*Risk Assessment* review meetings
2.Maximum resources work on high risk areas
3.Establish *Risk Assessment* database for future
4.Target *risk magnitude indicators*

### Risk Magnitude Indicators

**High**: risk effect = loss
**Medium**: tolerable but not desired = limited risk
**Low**: tolerable = little risk

### Risk Identification

1.Business Risks: risk from company you work for.
2.Testing Risks: become familiarized with programs and software that you are using.
3.Premature Release Risk- analyze risk that releasing untested software has.
4.Software Risks: software making has many risks.

### Risk Assessment

1.Effect: *determine* impact of risk
2.Cause: *finding* reasoning behind problem
3.Likelihood: *probability* that requirement won't be satisfied.

## Test Coverage

*Test Coverage* is very helpful in finding untested parts of code.

Test Coverage:

1.Be thoughtful in writing tests
2.In testing, you want a higher percentage coverage rate. It doesn't mean much if you are testing things just to please higher ups.

**Good Testing**:

1.Rarely obtain bugs
2.Rarely apprehensive to change code for fear of bugs.

**Test confidence**:

- The more tests the better; you can also comment the test out until you need it or it it is slowing you down. 

## Big O Notation

O(1)- constant time with respect to the size of input

O(n)- scales linearly with respect to the amount of input

### 4 Rules of Big O

1.Difference steps get added
  ie O(a)
     O(b)
     O(a+b)

2.Drop constants
  ie just drop numerical
  **NOT** O(2n) but *instead* O(n)

3.Different inputs -> different variables
  ie O must have meaning
     O(axb)

4.Drop non-dominant terms.

[<==BACK](README.md)
