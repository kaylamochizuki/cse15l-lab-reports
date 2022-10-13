Kayla Mochizuki 

# WEEK 3 LAB REPORT 2

---

## Part 1

---

## Part 2

Bug 1 From ArrayExamples: method reverseInPlace

Failure inducing input:
```
int[] input1 = {1,2,3};
```
Symptom(actual output):  
```
{3,2,3}
```
Expected: 
```
{3,2,1}
```
Bug: The for loop is trying to change the elements one at a time. I had to make it where the elements on opposite sides would switch with each, so I would be changing two elements at a time.
Correlation: Once the for loop tried to change the later half of the array, the first halves elements are already changed, so the later halves elements will stay the same. This means that instead of the values flipping, only one side is changing it's value.

---

Bug 2 From ListExamples: method merge

Failure inducing inputs:  
```
List<String> input1 = Arrays.asList("a", "b", "d"); 
List<String> input2 = Arrays.asList("c", "e"); 
```
Symptom(actual output): Java heap space
Expected:
```
["a","b","c","d","e"]
```
Bug: The index1 count was counting in places it shouldn't be. In the 3rd while loop in the code it should've been adding 1 to index2 but was instead adding 1 to index1.
Correlation: Because index2 was not being added, the while loop countinued running because it never reached the condition for it to end.



