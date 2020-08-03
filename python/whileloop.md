Python Format String %s %d
Python Day 18
It is convenient to be able to output different strings freely while printing the text. Such as assigning different values to the "name" variable or various height to the "height" variable according to the context needs.
Format String: %s, %d
%s is used as a placeholder for string/character values
%d is used as a placeholder for numeric/decimal values
Simple Numeric and String Variables

print ("%s is %d cm" %("yibo", 179))
yibo is 179 cm
name="Yibo"
height=179
print("%s is %d cm" %(name, height))
Yibo is 179 cm
Multiple variables

print ("%s %s %s %d" %("Today", "is", "May", 20))
Today is May 20
Alternative Solution:
f"{name!r} is {height!r} cm"
"'Yibo' is 175 cm"
Happy Studying!
Reference:
https://drive.google.com/file/d/0B-hV1HrMP8j1OWpEWXBXbUJsNms/view
https://stackoverflow.com/questions/4288973/whats-the-difference-between-s-and-d-in-python-string-formatting
