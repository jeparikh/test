# Lab Report 2

## Three Code Changes

1. Code Change 1

![Change 1:](https://github.com/jemilparikh/Cse15L-LabReports/blob/b6a29a58ead5c1817537b90ae01c7759ee2a1d5b/Screen%20Shot%202022-04-25%20at%202.38.22%20AM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/b6a29a58ead5c1817537b90ae01c7759ee2a1d5b/Screen%20Shot%202022-04-25%20at%202.38.10%20AM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/b6a29a58ead5c1817537b90ae01c7759ee2a1d5b/Screen%20Shot%202022-04-25%20at%202.37.43%20AM.png)

Since there was a closeParen after the closing parenthesis of the URL, but no other brackets, openBracket at the start of the second cycle of loop became -1, but the loop still didn't end and currentIndex keep getting more and more negative. This was the bug, and the symptom was an infinite loop. The correction was to add a condition that if openBracket was ever -1, the loop breaks away.

2. Code Change 2

![Change 2:](https://github.com/jemilparikh/Cse15L-LabReports/blob/ae674e31eb28ceee9153a34e32d76886dfe5f357/Screen%20Shot%202022-04-25%20at%201.59.26%20AM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/3669717300f57892c1366de3b516ceda11f3c587/Screen%20Shot%202022-04-25%20at%201.56.43%20AM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/511894c1360f05506781654ba3695d8b922edfe7/Screen%20Shot%202022-04-25%20at%202.05.03%20AM.png)

The symptom was an infinite loop, which was caused by the bug that due to the [] brackets after the link at the end of the test-file2.md, which ensures openBracket is not -1 but closeParen remains -1 which causes currentIndex to keep decreasing and thus the loop keeps going on as currentIndex remains less than markdown.length. The correction was to break from the loop even if any one of openBracket, closeBracket, openParen or closeParen is -1.

3. Code Change 3

![Change 3:](https://github.com/jemilparikh/Cse15L-LabReports/blob/3a7ef813d2066f7fab894230a0847f5b8897bddc/Screen%20Shot%202022-04-25%20at%202.23.43%20AM.png)

![Failure-Inducing Input in Test File:](https://github.com/jemilparikh/Cse15L-LabReports/blob/3a7ef813d2066f7fab894230a0847f5b8897bddc/Screen%20Shot%202022-04-25%20at%202.24.04%20AM.png)

![Symptom:](https://github.com/jemilparikh/Cse15L-LabReports/blob/3734693c18ebf36076368f64bf5f382806a6df19/Screen%20Shot%202022-04-25%20at%202.21.58%20AM.png)

If there is no link, the output must simply should show '[]' without any indexes of the opening and closing brackets and parantheses. The symptom is that it shows the indexes, due the bug of printing them despite there being none of the brackets and parantheses, and it was corrected by ensuring the indexes don't get printed when there are no links in the test file.





