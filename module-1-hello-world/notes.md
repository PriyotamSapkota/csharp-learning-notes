# Module 1 — Write Your First C# Code

## What is C#?
C# is used to build:
- Business apps (capture, analyze, process data)
- Web applications
- Games (2D and 3D)
- Financial and scientific apps
- Cloud-based and mobile apps

---

## First Line of Code

```csharp
Console.WriteLine("Hello World!");
```

Output:
```
Hello World!
```

---

## Key Rules

- C# is **case-sensitive** — `console` ≠ `Console`
- Use **double quotes** for strings — `"Hello"` ✅ not `'Hello'` ❌
- Every statement ends with a **semicolon** `;`
- `//` makes a comment (compiler ignores it)

---

## Console.Write vs Console.WriteLine

| Method | Behavior |
|---|---|
| `Console.WriteLine()` | Prints then moves to next line |
| `Console.Write()` | Prints and stays on same line |

### Example
```csharp
Console.Write("Hello ");
Console.Write("World!");
```
Output:
```
Hello World!
```

---

## How C# Works (Compilation)

1. You write **source code** (human-readable)
2. The **compiler** converts it to computer language
3. The computer **executes** it

> C# must be compiled before it can run — unlike Python which runs directly.

---

## Anatomy of a Line

```csharp
Console.WriteLine("Hello World!");
```

| Part | Name | Role |
|---|---|---|
| `Console` | Class | Represents an object |
| `.` | Member access operator | Connects class to method |
| `WriteLine()` | Method | Writes a line to output |
| `"Hello World!"` | Input parameter | The data passed in |
| `;` | End of statement | Marks command as finished |

---

## Common Errors

| Mistake | Error |
|---|---|
| `console.WriteLine()` | `CS0103: 'console' does not exist` |
| `'Hello World!'` single quotes | `CS1012: Too many characters in character literal` |
| Missing `;` | Syntax error |
