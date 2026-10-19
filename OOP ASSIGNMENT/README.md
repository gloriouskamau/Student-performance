# Student Performance Analysis System

Files: `student_performance.py` (source), `students.csv` (dataset).
Run: `python student_performance.py` (keep both files in the same folder).

## Polymorphism and method overriding (Task 5)
`describe()` is defined in `Student` and overridden in `ScholarshipStudent`.
All students are stored in one list and `describe()` is called in a loop.
Python picks the version belonging to each object's actual class at run time:
`AIUStudent` gives the basic summary, `ScholarshipStudent` calls
`super().describe()` and adds scholarship status and amount. The same applies to
the abstract `student_type()` method, implemented in `AIUStudent` and overridden in `ScholarshipStudent`.

## Flexible interface (Task 6)
Python has no overloading by signature, so `Student.calculate_average(*marks)`
uses variable-length arguments. It accepts three marks, any other number of
marks, or an unpacked list (`*marks_list`). It validates that at least one mark
is given, that each is numeric, and that each is between 0 and 100.
