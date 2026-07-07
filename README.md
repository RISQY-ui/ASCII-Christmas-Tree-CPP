# 🌲 Learning Nested Loop C++ - Creating ASCII Christmas Tree

---

## 📌 Introduction

This program uses nested loops to create a tree shape using the `*` character.

### Complete Code

```cpp
#include <iostream>
using namespace std;

int main() {
    for(int i = 1; i <= 13; i++) {

        for(int s = 1; s <= 13 - i; s++)
            cout << " ";

        for(int j = 1; j <= i; j++)
            cout << "**";

        cout << endl;
    }

    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;

    return 0;
}
```

---

## 🔍 How the Program Works

The program consists of three main parts.

---

### 1. Outer Loop ("i")

```cpp
for(int i = 1; i <= 13; i++)
```

| Purpose | Description |
|---------|-------------|
| **Determines** | Number of tree canopy rows |
| **Limit** | 13 (so the tree has 13 levels) |
| **Increment** | Each iteration creates one row |

---

### 2. Space Loop ("s")

```cpp
for(int s = 1; s <= 13 - i; s++)
    cout << " ";
```

| Purpose | Print spaces in front of `*` characters |
|---------|----------------------------------------|
| **Goal** | Center the tree canopy |
| **Logic** | `13 - i` spaces decrease as `i` increases |

#### Example

| When i = | Calculation | Spaces | Result |
|----------|-------------|--------|--------|
| 1 | 13 - 1 | 12 | Program prints 12 spaces |
| 2 | 13 - 2 | 11 | Program prints 11 spaces |
| 10 | 13 - 10 | 3 | Program prints only 3 spaces |
| 13 | 13 - 13 | 0 | No spaces (fully left) |

**Pattern:** The larger the value of `i`, the fewer spaces are printed.

---

### 3. Leaf Loop ("j")

```cpp
for(int j = 1; j <= i; j++)
    cout << "**";
```

| Purpose | Print the tree leaves |
|---------|----------------------|
| **Why `**`** | To make the tree look wider and more proportional |
| **Pattern** | As `i` increases, more `**` are printed |

#### Example

| i Value | Loop Iterations | Output | Total Characters |
|---------|-----------------|--------|------------------|
| 1 | 1 time | `**` | 2 |
| 2 | 2 times | `****` | 4 |
| 5 | 5 times | `**********` | 10 |
| 13 | 13 times | `**************************` | 26 |

**Pattern:** The larger the value of `i`, the wider the tree canopy becomes.

---

### 4. Tree Trunk

After all leaves are printed, the program creates the tree trunk.

```cpp
cout << "\t    | |" << endl;
```

This line is repeated 5 times so the trunk appears elongated.

#### Output

```
      | |
      | |
      | |
      | |
      | |
```

| Element | Description |
|---------|-------------|
| `\t` | Tab character for indentation |
| `    ` | 4 spaces for positioning |
| `\| \|` | Trunk sides |

---

## 🌳 Final Output

The program produces the following shape:

```
            **
           ****
          ******
         ********
        **********
       ************
      **************
     ****************
    ******************
   ********************
  **********************
 ************************
**************************
           | |
           | |
           | |
           | |
           | |
```

---

## 📊 Summary Table

| Element | Description | Pattern |
|---------|-------------|---------|
| **"i" (Outer Loop)** | Determines the height of the tree | From 1 to 13 |
| **"s" (Space Loop)** | Determines the number of spaces to center | Decreases (13-i) |
| **"j" (Leaf Loop)** | Determines the number of `**` printed | Increases (equal to i) |
| **Spaces** | Position the tree | Decrease as i increases |
| **Leaves** | Tree canopy width | Increase as i increases |
| **Trunk** | Tree base | Fixed output, repeated 5x |

---

## 💡 How Nested Loops Work Together

```
i = 1  → 12 spaces + 1x"**" + newline
i = 2  → 11 spaces + 2x"**" + newline
i = 3  → 10 spaces + 3x"**" + newline
...
i = 13 → 0 spaces + 13x"**" + newline
```

**Each value of `i` triggers:**
1. Space loop → prints centered position
2. Leaf loop → prints tree width
3. Newline → moves to next row

---

## 🧮 Step-by-Step Execution (First Few Iterations)

### Iteration i = 1

```cpp
for(int s = 1; s <= 12; s++)    // Print 12 spaces
    cout << " ";

for(int j = 1; j <= 1; j++)     // Print 1x"**"
    cout << "**";

cout << endl;                   // New line
```

**Output:**
```
            **
```

### Iteration i = 2

```cpp
for(int s = 1; s <= 11; s++)    // Print 11 spaces
    cout << " ";

for(int j = 1; j <= 2; j++)     // Print 2x"**"
    cout << "**";

cout << endl;                   // New line
```

**Output:**
```
           ****
```

### Iteration i = 3

```cpp
for(int s = 1; s <= 10; s++)    // Print 10 spaces
    cout << " ";

for(int j = 1; j <= 3; j++)     // Print 3x"**"
    cout << "**";

cout << endl;                   // New line
```

**Output:**
```
          ******
```

---

## 🚀 How to Compile & Run

### Linux/Mac

```bash
# Compile
g++ -o ascii_tree ascii_tree.cpp

# Run
./ascii_tree
```

### Windows

```bash
# Compile
g++ -o ascii_tree.exe ascii_tree.cpp

# Run
ascii_tree.exe
```

### Termux (Android)

```bash
# Compile
g++ -o ascii_tree ascii_tree.cpp

# Run
./ascii_tree
```

---

## ✅ Learning Outcome

This exercise is excellent for understanding nested loops because each loop has a different task:

| Loop | Task |
|------|------|
| **Outer Loop (i)** | Controls the height of the tree |
| **Space Loop (s)** | Controls the horizontal position (centering) |
| **Leaf Loop (j)** | Controls the width of the tree canopy |

**Key Insight:** Nested loops allow you to solve complex problems by breaking them into smaller, manageable tasks.

---

## 🎨 Variations to Try

### Variation 1: Larger Tree

```cpp
for(int i = 1; i <= 20; i++)  // Change 13 to 20
```

### Variation 2: Different Width Character

```cpp
cout << "* ";  // Single asterisk with space
```

### Variation 3: Different Trunk

```cpp
cout << "\t   |***|" << endl;  // Different trunk style
```

### Variation 4: Multiple Trees

```cpp
for(int tree = 0; tree < 3; tree++) {
    // Your tree code here
}
```

---

## 📌 Important Concepts Tested

| Concept | Where It's Used |
|---------|-----------------|
| **Nested Loops** | Three loops inside each other |
| **Loop Variables** | i, s, j track their own iterations |
| **Increment** | i++, s++, j++ advance each loop |
| **Conditions** | `<=` determines loop limits |
| **String Output** | cout prints spaces and asterisks |
| **Formatting** | `\t` and `endl` for layout |

---

## 📈 Complexity Analysis

| Aspect | Complexity |
|--------|-----------|
| **Time** | O(n²) where n = 13 |
| **Space** | O(1) constant space |
| **Operations** | ~13×13 = 169 print operations |

---

**Last Updated:** June 2026

**Difficulty Level:** Beginner to Intermediate
