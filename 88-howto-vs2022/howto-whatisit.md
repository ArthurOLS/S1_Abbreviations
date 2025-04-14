# WHAT CAN VS2022/GDI DO IN THE ELEVATOR SIMULATOR

## What Can GDI do for my Elevator Program

| Feature                        | Use in Elevator Program              | GDI Function / Concept                   |
| ------------------------------ | ------------------------------------ | ---------------------------------------- |
| **Draw elevator shaft/floors** | Show static floor structure          | `Rectangle()`, `MoveToEx()` + `LineTo()` |
| **Draw elevator car (moving)** | Animate the car moving up/down       | `Rectangle()`, `InvalidateRect()`        |
| **Draw buttons, lights**       | Simulate call buttons and indicators | `Ellipse()`, `TextOut()`                 |
| **Draw labels, numbers**       | Show floor number, height, speed     | `TextOut()`, `DrawText()`                |
| **Color coding**               | Color car, floors, call buttons      | `CreateSolidBrush()`, `SelectObject()`   |
| **Custom fonts**               | Make text easier to read or stylized | `CreateFont()`                           |
| **Double buffering**           | Reduce flicker during animation      | Memory DC: `CreateCompatibleDC()`        |