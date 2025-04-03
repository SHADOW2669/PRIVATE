StringBuffer Methods in Java

Overview

The StringBuffer class in Java provides various methods to manipulate and handle strings efficiently. This document covers additional StringBuffer methods introduced in J2SE 5 and explains them with examples.


---

List of Methods

1. appendCodePoint(int ch)

Description: Appends a Unicode code point to the end of the invoking StringBuffer object.

Returns: A reference to the object.

Example:

StringBuffer sb = new StringBuffer("Hello");
sb.appendCodePoint(33); // Appends '!'
System.out.println(sb); // Output: Hello!



---

2. int codePointAt(int i)

Description: Returns the Unicode code point at the specified index i.

Returns: Unicode code point as an integer.

Example:

StringBuffer sb = new StringBuffer("Java");
System.out.println(sb.codePointAt(1)); // Output: 97 ('a')



---

3. int codePointBefore(int i)

Description: Returns the Unicode code point at the location preceding the specified index i.

Returns: Unicode code point as an integer.

Example:

StringBuffer sb = new StringBuffer("Java");
System.out.println(sb.codePointBefore(2)); // Output: 97 ('a')



---

4. int codePointCount(int start, int end)

Description: Returns the number of Unicode code points between start and end-1.

Returns: The number of code points.

Example:

StringBuffer sb = new StringBuffer("Hello");
System.out.println(sb.codePointCount(1, 4)); // Output: 3



---

5. int indexOf(String str)

Description: Searches for the first occurrence of str and returns its index, or -1 if not found.

Example:

StringBuffer sb = new StringBuffer("one two one");
System.out.println(sb.indexOf("one")); // Output: 0



---

6. int indexOf(String str, int startIndex)

Description: Searches for str starting from startIndex.

Example:

StringBuffer sb = new StringBuffer("one two one");
System.out.println(sb.indexOf("one", 2)); // Output: 8



---

7. int lastIndexOf(String str)

Description: Searches for the last occurrence of str and returns its index, or -1 if not found.

Example:

StringBuffer sb = new StringBuffer("one two one");
System.out.println(sb.lastIndexOf("one")); // Output: 8



---

8. int lastIndexOf(String str, int startIndex)

Description: Searches for str starting backward from startIndex.

Example:

StringBuffer sb = new StringBuffer("one two one");
System.out.println(sb.lastIndexOf("one", 7)); // Output: 0



---

9. int offsetByCodePoints(int start, int num)

Description: Returns the index num code points beyond the specified start index.

Example:

StringBuffer sb = new StringBuffer("Hello");
System.out.println(sb.offsetByCodePoints(1, 2)); // Output: 3



---

10. CharSequence subSequence(int startIndex, int stopIndex)

Description: Returns a substring from startIndex to stopIndex.

Example:

StringBuffer sb = new StringBuffer("Hello World");
System.out.println(sb.subSequence(0, 5)); // Output: Hello



---

11. void trimToSize()

Description: Reduces the capacity of the StringBuffer to fit its content size exactly.

Example:

StringBuffer sb = new StringBuffer(50);
sb.append("Java");
sb.trimToSize();



---

StringBuilder vs StringBuffer

StringBuffer is synchronized (thread-safe) but slower.

StringBuilder is not synchronized but faster.

If multithreading is required, use StringBuffer, otherwise use StringBuilder.



---

Example Program

class IndexOfDemo {
    public static void main(String args[]) {
        StringBuffer sb = new StringBuffer("one two one");
        int i;

        i = sb.indexOf("one");
        System.out.println("First index: " + i);

        i = sb.lastIndexOf("one");
        System.out.println("Last index: " + i);
    }
}

Output:

First index: 0
Last index: 8

Explanation

1. StringBuffer Initialization:

A StringBuffer object sb is created with the value "one two one".



2. Finding the First Occurrence (indexOf)

Searches for the first occurrence of "one".

Found at index 0.



3. Finding the Last Occurrence (lastIndexOf)

Searches for the last occurrence of "one".

Found at index 8.



4. Printing the Results

Outputs:

First index: 0
Last index: 8





---

Conclusion

These methods enhance the functionality of StringBuffer in Java, making string manipulation more powerful and efficient.

