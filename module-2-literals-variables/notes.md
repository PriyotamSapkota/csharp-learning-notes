# Module 2 — Store and Retrieve Data (Literals & Variables)
## Literal Values
A **literal** is a hard-coded constant value that never changes.
---
## Data Types
| Type | Example | Notes |
|---|---|---|
| string | "Hello" | Double quotes, for words/text |
| char | 'A' | Single quotes, ONE character only |
| int | 123 | Whole numbers, no quotes needed |
| float | 0.25F | Decimals — least precise, needs F suffix |
| double | 2.625 | Decimals — default when no suffix |
| decimal | 12.39m | Decimals — most precise, needs m suffix |
| bool | true / false | Lowercase only |
### Precision Comparison
| Type | Precision |
|---|---|
| float | ~6-9 digits |
| double | ~15-17 digits |
| decimal | 28-29 digits |
---
## Examples
csharp
Console.WriteLine("Hello");       // string
Console.WriteLine('A');           // char
Console.WriteLine(123);           // int
Console.WriteLine(0.25F);         // float
Console.WriteLine(2.625);         // double
Console.WriteLine(12.39m);        // decimal
Console.WriteLine(true);          // bool
Console.WriteLine(false);         // bool

---
## Variables
A **variable** is a container for storing a value that can change.
### Declare → Assign → Use
csharp
string firstName;         // declare
firstName = "Bob";        // assign
Console.WriteLine(firstName);  // use

### Best Practice — Initialize on one line
csharp
string firstName = "Bob";
Console.WriteLine(firstName);

### Reassigning Variables
csharp
string firstName = "Bob";
Console.WriteLine(firstName);  // Bob
firstName = "Liem";
Console.WriteLine(firstName);  // Liem

---
## Variable Naming Rules
| Rule | Example |
|---|---|
| Letters, numbers, underscore only | game_score ✅ |
| Must start with letter or _ | 1score ❌ |
| Case-sensitive | firstName ≠ FirstName |
| No C# keywords | string ❌ as a name |
| Use camelCase | gameScore ✅ |
| Be descriptive | x ❌ → userAge ✅ |
### Good Variable Names
csharp
string firstName;
char userOption;
int gameScore;
decimal particlesPerMillion;
bool processedCustomer;

---
## Common Errors
| Mistake | Error |
|---|---|
| "Bob" = firstName | CS0131: Left-hand side must be a variable |
| Assign wrong type int x = "Bob" | CS0029: Cannot convert string to int |
| Use before assigning | CS0165: Use of unassigned local variable |
---
## var Keyword
var lets the compiler **figure out the data type** from the value you give it.
csharp
var message = "Hello!";   // compiler sees string
var score = 100;           // compiler sees int
var temp = 34.4;           // compiler sees double

### Rules for var
- Type is **locked** once set — cannot change it later
- Must be **initialized immediately** — var message; alone gives error
- Use actual data types when possible — var is for convenience
### Example — what NOT to do
csharp
var message = "Hello World!";
message = 10.703m;  // ❌ Error: cannot convert decimal to string

---
## Full Example
csharp
var name = "Bob";
var messages = 3;
var temperature = 34.4;
Console.Write("Hello, ");
Console.Write(name);
Console.Write(". You have ");
Console.Write(messages);
Console.Write(" messages. Temperature is ");
Console.Write(temperature);
Console.Write(" degrees celsius.");

Output:
```
Hello, Bob. You have 3 messages. Temperature is 34.4 degrees celsius.
