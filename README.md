# 🔤 SSD Week 2 Lab: Interfaces in Java & Git Branching
**Software Systems Development (CRN 12391) · Level 5**  
**The British College (Leeds Beckett University)**

```
Progress: [████████████░░░░░░] Step 2 of 3 (In Progress)
```

---

## 🎉 Step 1 Completed! Welcome to Step 2

Great job! You have verified the `Counter` interface contract and successfully used Git branches.

---

## 🌿 Step 2: Create Your Next Feature Branch

As always, start by creating a dedicated branch for Step 2:

```bash
# 1. Ensure you have the latest updates on main
git checkout main
git pull origin main

# 2. Create and switch to the Step 2 feature branch
git checkout -b feature/step2-wordprocessor
```

---

## 📝 Step 2 Task: Implement `WordProcessor.java`

Open [`src/main/java/counter/WordProcessor.java`](src/main/java/counter/WordProcessor.java) in your IDE.

Notice the class header:
```java
public class WordProcessor implements Counter
```
By using the **`implements`** keyword, `WordProcessor` promises to provide a concrete implementation for every method declared in `Counter`.

### Your Tasks:

1. **Implement `countWords(String sentence)`:**
   * Split the sentence on single spaces `" "`.
   * Hint: `return sentence.split(" ").length;`
   * Handle empty string: if `sentence.isEmpty()`, return `0`.

2. **Implement `countLetters(String sentence)`:**
   * Loop through each character of the sentence.
   * Use `Character.isLetter(ch)` to count alphabetic letters only.
   * Spaces, digits (`0-9`), and punctuation symbols (`!`, `?`, `.`, `@`) must **not** be counted.

3. **Implement `getLength(String sentence)`:**
   * Return the total character count: `return sentence.length();`
   * Spaces and punctuation are included in total length.

---

## 🧪 Verify Step 2 Locally

Run both Step 1 and Step 2 tests:

```bash
mvn test -Dtest=Step1CounterTest,Step2WordProcessorTest
```

Expected output:
```
[INFO] Running counter.Step1CounterTest
[INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[INFO] Running counter.Step2WordProcessorTest
[INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
[INFO] BUILD SUCCESS
```

---

## 🚀 Commit, Merge & Advance to Step 3

```bash
# 1. Commit your changes on feature/step2-wordprocessor
git add src/main/java/counter/WordProcessor.java
git commit -m "feat(wordprocessor): implement sentence analysis methods"

# 2. Push your feature branch
git push -u origin feature/step2-wordprocessor

# 3. Merge into main
git checkout main
git merge feature/step2-wordprocessor

# 4. Push main to advance the lab!
git push origin main
```

> 💡 **Next:** Run `git pull origin main` to unlock **Step 3: Encapsulation & Fallback State**!
