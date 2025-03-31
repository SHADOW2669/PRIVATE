# Java Seminar on StringBuffer and StringBuilder

## Introduction
Java provides several classes for handling strings efficiently. Among them, `StringBuffer` and `StringBuilder` are widely used when mutable strings are required. This seminar covers additional methods introduced in `StringBuffer` with J2SE 5 and explains the key differences between `StringBuffer` and `StringBuilder`.

---

## StringBuffer Methods (J2SE 5 Additions)
Several new methods were introduced in `StringBuffer` with J2SE 5, which include:

1. **appendCodePoint(int ch)**: Appends a Unicode code point to the invoking object.
2. **codePointAt(int i)**: Returns the Unicode code point at the specified index `i`.
3. **codePointBefore(int i)**: Returns the Unicode code point before the specified index `i`.
4. **codePointCount(int start, int end)**: Returns the number of Unicode code points between `start` and `end`.
5. **indexOf(String str)**: Searches for a string and returns its index or `-1` if not found.
6. **indexOf(String str, int startIndex)**: Searches for a string starting from `startIndex`.
7. **lastIndexOf(String str)**: Searches for the last occurrence of a string.
8. **lastIndexOf(String str, int startIndex)**: Searches for the last occurrence of a string starting from `startIndex`.
9. **offsetByCodePoints(int start, int num)**: Returns the index of the string offset by `num` code points from `start`.
10. **subSequence(int startIndex, int stopIndex)**: Returns a substring as a `CharSequence`.
11. **trimToSize()**: Reduces the size of the `StringBuffer` to match the current contents.

---

## Example Code
Here is an example demonstrating `indexOf()` and `lastIndexOf()`:

```java
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
```
**Output:**
```
First index: 0
Last index: 8
```

---

## StringBuffer vs. StringBuilder
J2SE 5 introduced `StringBuilder`, which is similar to `StringBuffer` but differs in the following way:
- **StringBuffer** is **synchronized** and thread-safe, making it suitable for multi-threaded environments.
- **StringBuilder** is **not synchronized**, making it faster but not thread-safe.

### When to Use?
- Use `StringBuffer` when working with multiple threads.
- Use `StringBuilder` for better performance in single-threaded applications.

---

## Conclusion
The enhancements in `StringBuffer` introduced in J2SE 5 make it more powerful for string manipulation. Understanding the differences between `StringBuffer` and `StringBuilder` helps in choosing the right class based on application needs.

Thank you!

