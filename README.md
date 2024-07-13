# Regular Expressions for Triage: A Primer for Incident Responders

## Lesson Overview

Welcome to an exciting journey into the world of regular expressions! In this lesson, we'll supercharge your incident response triage skills by using regular expressions to analyze datasets. Get ready to parse logs, scrutinize datasets, and onboard logs into Splunk Enterprise like a pro.

## Lesson Objectives

By the end of this class, you'll be able to:

- Parse, interpret, and analyze data using fundamental Regular Expressions (Regex) syntax.
- Harness the power of Regex to navigate logs with the `grep` command.
- Perform field extraction and transformation of log files in Splunk Enterprise using Regex.
- Identify resources to explore additional Regular Expression engines.

## Slide Show

Dive into today's lesson with our slides on GitHub: [Slides](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/regular_expressions_for_triage_primer.pdf).

---

## 01. A Background in Regular Expressions

Regular expressions have fascinating roots in science. In 1943, Walter Pitts, an American neurophysiologist and cybernetician, co-authored [A Logical Calculus of the Ideas Immanent in Nervous Activity](https://www.cse.chalmers.se/~coquand/AUTOMATA/mcp.pdf). Fast forward to 1956, when mathematician Stephen Kleene introduced regular events into the field. Unix pioneer Ken Thompson took it further in 1968 with his "Regular Expression Search Algorithm," leading to the creation of `grep` in 1973. By 1987, Larry Wall's Perl programming language had brought Regular Expressions into the mainstream. Today, regular expressions power over 30 engines in active use.

### Use Cases for Regular Expressions

Regular expressions are the Swiss Army knife of pattern matching. Their applications are boundless, including:

- URLs (Uniform Resource Locator)
- Dates/Times
- IP Addresses
- Email Addresses
- Social Security Numbers
- Credit Card Numbers

### Regular Expression Demonstrations

- [Finding Credit Card Numbers with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/student_files/unsolved/credit_card_number.md) (Group Activity)
- [Parsing Logs in `grep` with Regular Expressions 1](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/1http.log)
- [Parsing Logs in `grep` with Regular Expressions 2](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/2http.log) (Bonus if time permits)
- [Parsing Logs in `grep` with Regular Expressions 3](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/computer_sid_objects.csv) (Bonus if time permits)
- [Parsing logs in Splunk with Regular Expressions](https://github.com/cyberjack256/regular_expressions/blob/main/log_samples/windows_event.log) (Unstructured Data Sets)

Jump over to [Regex101](https://regex101.com) and follow along with the instructor for hands-on activities.

## Regular Expression Syntax Patterns

Regular expressions are all about patterns. Here's a quick guide to some fundamental patterns:

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

**Pro Tip:** To match special characters like the `.`, use the `\` to escape the character and avoid interpretation.

## References

These references will be your best friends throughout the course:

1. [Regex101](https://regex101.com/) - A web app for testing regular expressions in multiple engines.
2. [Debuggex Cheat-sheet](https://www.debuggex.com/cheatsheet/regex/pcre) - A handy cheat-sheet for the PCRE engine.
3. [ExplainShell](https://explainshell.com) - Simplifies Linux bash command line explanations.
4. [Debuggex](https://www.debuggex.com/) - Logic diagramming and testing of regular expressions.
5. [Ascii Table](https://www.asciitable.com/) - The classic ASCII table.
6. [List of Unicode Characters](https://en.wikipedia.org/wiki/List_of_Unicode_characters) - Comprehensive Unicode tables.
7. [RegexOne](https://regexone.com/) - Interactive tutorials for learning regular expressions.

---

Dive into the world of regular expressions with confidence, and let's make data wrangling fun and efficient! 🌐💻✨