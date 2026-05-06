# Module 3 — String Formatting in C#

## What This Module Is About
This module is about how to format and combine strings in C#. You learn how to add special characters like new lines and tabs, display file paths correctly, and combine strings in two different ways.

---

## Character Escape Sequences

A backslash `\` followed by a character gives a special instruction to the compiler.

| Sequence | Effect |
|---|---|
| `\n` | New line |
| `\t` | Tab |
| `\"` | Double quote inside a string |
| `\\` | Single backslash |
| `\u` | Unicode character (4-digit code) |

### Examples
```csharp
Console.WriteLine("Hello\nWorld!");     // new line
Console.WriteLine("Hello\tWorld!");     // tab
Console.WriteLine("Hello \"World\"!");  // double quotes
Console.WriteLine("c:\\source\\repos"); // backslash
```

Output:
```
Hello
World!
Hello   World!
Hello "World"!
c:\source\repos
```

---

## Verbatim String Literal `@`

Use `@` before a string to keep backslashes and whitespace exactly as written — no escaping needed.

```csharp
Console.WriteLine(@"c:\source\repos");

Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)");
```

Output:
```
c:\source\repos
    c:\source\repos    
        (this is where your code goes)
```

---

## Unicode Characters `\u`

Add characters from any language using `\u` + 4-digit code.

```csharp
// Kon'nichiwa World (Japanese)
Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!");
```

> ⚠️ Not all consoles support Unicode display.

---

## Full Escape Sequence Example

```csharp
Console.WriteLine("Generating invoices for customer \"Contoso Corp\" ... \n");
Console.WriteLine("Invoice: 1021\t\tComplete!");
Console.WriteLine("Invoice: 1022\t\tComplete!");
Console.Write("\nOutput Directory:\t");
Console.Write(@"c:\invoices");
```

Output:
```
Generating invoices for customer "Contoso Corp" ...

Invoice: 1021           Complete!
Invoice: 1022           Complete!

Output Directory:       c:\invoices
```

---

## String Concatenation `+`

Combining two or more strings using the `+` operator.

```csharp
string firstName = "Bob";
string greeting = "Hello";
Console.WriteLine(greeting + " " + firstName + "!");
```

Output:
```
Hello Bob!
```

> Avoid creating extra variables if they don't make the code clearer.

---

## String Interpolation `$`

Cleaner way to combine strings — like f-strings in Python.
Prefix the string with `$` and put variables inside `{}`.

```csharp
string firstName = "Bob";
string greeting = "Hello";
Console.WriteLine($"{greeting} {firstName}!");
```

Output:
```
Hello Bob!
```

### With multiple variables
```csharp
int version = 11;
string updateText = "Update to Windows";
Console.WriteLine($"{updateText} {version}!");
```

Output:
```
Update to Windows 11!
```

---

## Combining `$` and `@` Together

Use both when you need variables AND backslashes in the same string.

```csharp
string projectName = "First-Project";
Console.WriteLine($@"C:\Output\{projectName}\Data");
```

Output:
```
C:\Output\First-Project\Data
```

---

## Concatenation vs Interpolation

| Method | Example | Best For |
|---|---|---|
| Concatenation `+` | `"Hello " + name` | Simple, few values |
| Interpolation `$` | `$"Hello {name}"` | Cleaner, multiple values |

---

## Challenge Solution

```csharp
string projectName = "ACME";
string englishLocation = $@"c:\Exercise\{projectName}\data.txt";
Console.WriteLine($"View English output:\n\t{englishLocation}\n");

string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434";
string russianLocation = $@"c:\Exercise\{projectName}\ru-RU\data.txt";
Console.WriteLine($"{russianMessage}:\n\t{russianLocation}\n");
```

Output:
```
View English output:
    c:\Exercise\ACME\data.txt

Посмотреть русский вывод:
    c:\Exercise\ACME\ru-RU\data.txt
```

---

