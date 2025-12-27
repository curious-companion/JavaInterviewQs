# 5️⃣ Exception Handling

## 🔹 Checked vs Unchecked Exceptions
- **Checked Exceptions**
  - Checked at compile-time
  - Must be handled using `try-catch` or `throws`
  - Example: `IOException`, `SQLException`

- **Unchecked Exceptions**
  - Occur at runtime
  - Not mandatory to handle
  - Example: `NullPointerException`, `ArrayIndexOutOfBoundsException`

---

## 🔹 Can We Have Multiple Catch Blocks?
Yes.  
Multiple `catch` blocks are allowed, but they **must be ordered from child to parent** exception.

```java
catch (NullPointerException e) {}
catch (Exception e) {}