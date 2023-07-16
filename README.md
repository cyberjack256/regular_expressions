# Regular Expressions for Triage: A Primer in Regular Expressions for Incident Responders

## Lesson Overview

In this lesson, we aim to expand our incident response triage skill set by utilizing regular expressions for the initial analysis of datasets. We will parse logs, analyze datasets, and onboard logs into a data aggregation tool (Splunk Enterprise) using regular expressions.

## Lesson Objectives

By the end of this class, you should be able to:

- Parse, interpret, and analyze data using fundamental Regular Expressions (Regex) syntax.
- Leverage the power of Regex to navigate logs using the grep command.
- Conduct field extraction and transformation of log files within Splunk Enterprise using Regex.
- Identify references that will aid you in exploring additional Regular Expression Engines.

## Slide Show

The slides for today's lesson can be found on GitHub: [Slides](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/regular_expressions_for_triage_primer.pdf).

---

## 01. A Background in Regular Expressions

Regular expressions have their roots in multiple fields of science. In 1943, American neurophysiologist and cybernetician Walter Pitts of the University of Illinois at Chicago, and self-taught logician and cognitive psychologist, published [A Logical Calculus of the Ideas Imminent in Nervous Activity](https://www.cse.chalmers.se/~coquand/AUTOMATA/mcp.pdf). In 1956, Mathematician Stephen Kleene developed a model of nerve nets and finite automata in a simple algebra, introducing sets and regular events into the field. In 1968, Unix Pioneer and programmer Ken Thompson published "Regular Expression Search Algorithm" using Kleene's notation in the QED editor. It became so cumbersome that it necessitated the release of a standalone program, and in 1973 he published grep (global search/regular expressions/print screen). In 1987, Larry Wall's Perl programming language helped Regular Expressions become mainstream. From there, Regular expressions have diverged into more than 30 regular expression engines that are in active production and/or active use.

### Use Cases for Regular Expressions

Regular expressions are used for pattern matching. The range of uses in modern computing environments is so far-reaching that it would be impossible to list all of the use cases in this course, or any course. For example, regular expressions can check for the existence of specific patterns in:

- URLs (Uniform Resource Locator)
- Date/Time
- IP Addresses
- Email Addresses
- Social Security Numbers
- Credit Card Numbers

### Regular Expression Demonstrations

- [Finding Credit Card Numbers with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/unsolved/credit_card_number.md) (Group Activity)
- [Parsing Logs in grep with Regular Expressions 1](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/1http.log)
- [Parsing Logs in grep with Regular Expressions 2](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/2http.log) (Bonus as time permits)
- [Parsing Logs in grep with Regular Expressions 3](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/computer_sid_objects.csv) (Bonus as time permits)
- [Parsing logs in Splunk with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/windows_event.log) (Unstructured Data Sets)

Please navigate to [Regex101](https://regex101.com) and follow the instructions of the activity along with the instructor.

## Regular Expression Syntax Patterns

Regular expressions use a variety of syntax patterns for matching. Here are some of the fundamental patterns:

### Single Characters

- `x` : The character x
- `\\` : The backslash character
- `\\0n` : The character with octal value 0n (0 <= n <= 7)
- `\\xhh` : The character with hexadecimal value 0xhh
- `\\t` : The tab character
- `\\n` : The newline character

### Character Classes

- `[abc]` : a, b, or c (simple class)
- `[^abc]` : Not a, b, or c (negated class)
- `[a-zA-Z]` : a through z or A through Z, inclusive (range)

### Predefined Character Classes

- `.` : Any character except newline (unless given flag d)
- `\\d` : A digit: [0-9]
- `\\D` : A non-digit: [^0-9]
- `\\s` : A whitespace character
- `\\S` : A non-whitespace character
- `\\w` : A word character: [a-zA-Z_0-9]
- `\\W` : A non-word character (inverse of above, equivalent to [^a-zA-Z_0-9])

### Quantifiers

- `X?` : X, once or not at all
- `X*` : X, zero or more times
- `X+` : X, one or more times
- `X{n}` : X, exactly n times
- `X{n,}` : X, at least n times
- `X{n,m}` : X, at least n times but not more than m times

### Logical Operators

- `XY` : X followed by Y
- `X|Y` : Either X or Y

**Note:** To match special characters like the `.`, use the `\` to escape the character to avoid interpretation.

## References

These references are used throughout the course and should be helpful for following along with the demonstrations.

1. [Regex101](https://regex101.com/) - Web application for testing regular expressions in multiple regular expression engines.
2. [Debuggex Cheat-sheet](https://www.debuggex.com/cheatsheet/regex/pcre) - Cheat-sheet for PCRE regular expression engine.
3. [ExplainShell](https://explainshell.com) - Simplified explanation of Linux bash command line.
4. [Debuggex](https://www.debuggex.com/) - Logic diagramming and testing of regular expressions in multiple regular expression engines.
5. [Ascii Table](https://www.asciitable.com/) - Ascii table.
6. [List of Unicode Characters](https://en.wikipedia.org/wiki/List_of_Unicode_characters) - Unicode table(s).
