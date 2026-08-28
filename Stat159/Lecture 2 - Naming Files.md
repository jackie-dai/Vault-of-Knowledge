
## Project Structure
![[Pasted image 20260828101822.png]]

## Use of Delimeters
With intentional file naming, we can use it to easily search through our files

```
list.files(pattern = "2026-05")
```
This returns all the files with the given pattern


### Regex Refresher

```
list.files(pattern = "\\w+(-\\w+)\\.csv$")
```
The regex components mean:
- `\\w+`
    - `\w` matches a “word character”: letters, numbers, or `_`
    - `+` means “one or more”
    - Example: `grades`, `data1`, `student_records`
- `(-\\w+)`
    - `-` matches a literal hyphen
    - `\\w+` matches one or more word characters
    - Parentheses group this part together
    - Example: `-final`, `-2026`, `-student_data`
- `\\.csv`
    - `\\.` matches a literal period. A plain `.` in regex means “any character.”
    - `csv` matches the exact letters `csv`
- `$`
    - Requires `.csv` to appear at the end of the filename