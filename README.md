
# 🌲 Learning Nested Loop C++ - Creating ASCII Christmas Tree

---

# 📌 Introduction

This program uses nested loops to create a tree shape using the "*" character.

Code:

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

🔍 How the Program Works

The program consists of three main parts.

---

1. Outer Loop ("i")

```cpp
for(int i = 1; i <= 13; i++)
```

This loop determines the number of tree canopy rows.

Since the limit is "13", the tree has 13 levels.

---

2. Space Loop ("s")

```cpp
for(int s = 1; s <= 13 - i; s++)
    cout << " ";
```

This loop prints spaces in front of the "*" characters.

The goal is to center the tree canopy.

Example:

When i = 1 → 13 - 1 = 12 → Program prints 12 spaces.

When i = 10 → 13 - 10 = 3 → Program prints only 3 spaces.

The larger the value of "i", the fewer spaces are printed.

---

3. Leaf Loop ("j")

```cpp
for(int j = 1; j <= i; j++)
    cout << "**";
```

This loop prints the tree leaves.

Why use ""?**

To make the tree look wider and more proportional.

Example:

i Value Output
1 **
2 ****
5 **********

The larger the value of "i", the wider the tree canopy becomes.

---

Tree Trunk

After all leaves are printed, the program creates the tree trunk.

```cpp
cout << "\t    | |" << endl;
```

This line is repeated several times so the trunk appears elongated.

Output:

```
      | |
      | |
      | |
      | |
      | |
```

---

🌳 Final Shape

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

📊 Summary

Element Description
"i" Determines the height of the tree
"s" Determines the number of spaces to center the tree
"j" Determines the number of leaves ("**") printed
Spaces As "i" increases, spaces decrease
Leaves As "i" increases, leaves increase
Trunk Created after all leaves using multiple cout statements

---

💡 Learning Outcome

This exercise is excellent for understanding nested loops because each loop has a different task:

· One controls the height
· One controls the position
· One controls the width

---

🚀 How to Compile & Run

```bash
# Compile
g++ -o ascii_tree ascii_tree.cpp

# Run
./ascii_tree          # Linux/Mac
ascii_tree.exe        # Windows
```

---

📌 Sample Output

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
