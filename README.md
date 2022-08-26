# Regular Expressions for Triage : A primer in regular expressions for incident responders

### Lesson Overview

Today we expand our incident response triage skill set by utilizing regular expressions in our initial analysis of datasets.  In this lesson, we will parse logs, analyze data sets, and onboard logs into a data aggregation tool (Splunk Enterprise) using regular expressions.

### Lesson Objectives

By the end of class you should be able to:

- Parse, Interpret, and analyze data with fundamental Regular Expressions (Regex) syntax

- Leverage the power of Regex to navigate logs using the grep command

- Conduct field extraction and transformation of log files within Splunk Enterprise using Regex

- Identify references that will aid  you in exploring additional Regular Expression Engines


### Slide Show

The slides for today can be found in Github: [Slides](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/regular_expressions_for_triage_primer.pdf).


---

### 01. A Background in Regular Expressions

Regular expressions have their roots in multiple fields of science. In 1943 American neurophysiologist and cybernetician of the University of Illinois at Chicago and self-taught logician and cognitive psychologist Walter Pitts published [A Logical Calculus of the ideas Imminent in Nervous Activity](https://www.cse.chalmers.se/~coquand/AUTOMATA/mcp.pdf). In 1956, Mathematician Stephen Kleene developed a model of nerve nets and finite automata in a simple algebra: introducing sets and regular events into the field. In 1968, Unix Pioneer and programmer Ken Thompson published "Regular Expression Search Algorithm" using Kleene's notation in the QED editor, it became so cumbersome necessitating the release of a stand alone program and in 1973 he published grep (global search/regular expressions/print screen). In 1987, Larry Wall's perl programming language helped Regular Expressions become mainstream. From there Regular expressions have diverged into more than 30 regular expression engines that are in active production and/or active use.

#### Use Cases for Regular Expressions

Regular expressions are used for pattern matching. The range of uses in modern computing environments is so far reaching that it would be impossible to list all of the the use cases in this course, or any course.

  - For example, regular expressions can check for the existence of specific patterns in:
    - (Uniform Resource Locator) URLs
    - Date/Time
    - IP Addresses
    - Email Addresses
    - Social Security Numbers
    - Credit Card Numbers


#### Regular Expression Demonstrations

[Finding Credit Card Numbers with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/unsolved/credit_card_number.md) (Group Activity)

[Parsing Logs in grep with Regular Expressions 1](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/1http.log)
[Parsing Logs in grep with Regular Expressions 2](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/2http.log) (bonus as time permits)  
[Parsing Logs in grep with Regular Expressions 3](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/computer_sid_objects.csv) (bonus as time permits)

[Parsing logs in Splunk with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/windows_event.log) (Unstructured Data Sets)

Navigate to [Regex101](https://regex101.com). Follow the instructions of the activity along with the instructor.

**Classes:**
- `[0-9a-zA-Z]` : All letters and numbers
- `[a-zA-Z]` : All letters
- `[\s]`	: Spaces and tabs
- `[0-9]` : Digits 0 to 9
- `[a-z]` : Lowercase letters

**Quantifiers:**

- `*`	: Zero or more matches (greedy)
- `?`	: Zero or one match (lazy)
- `+`	: One or more matches (greedy)
- `{n}` : n matches
- `{n,}` : n or more matches
- `{,m}` : Up to m matches
- `{n,m}` : From n up to m matches

**Note:** To match special characters like the `.`, use the `\` to escape the character to avoid interpretation.

###References

These references are used throughout the course and should be helpful for following along with the demonstrations.

1. https://regex101.com/ <- Web application for testing regular expressions in multiple regular expression engines

2. https://www.debuggex.com/cheatsheet/regex/pcre <- Cheat-sheet for PCRE regular expression engine

3. https://explainshell.com <- Simplified explination of linux bash command line

4. https://www.debuggex.com/ <- Logic diagramming and testing of regular expressions in multiple regular expression engines

5. https://www.asciitable.com/ <- Ascii table

6. https://en.wikipedia.org/wiki/List_of_Unicode_characters <- Unicode table(s)

