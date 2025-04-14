# HOW TO USE TIMER(S) IN VS2022

VS2022 supports multiple timers (definitely). You just need to give each timer a unique number ID. All the timers will triigger the 'WM_TIMER' event, use 'wParam' to distinguish them.

## HOW IT WORKS?

```C
#define IDT_TIMER_1  1
#define IDT_TIMER_2  2

// Set two timers in your initialization code (e.g., in InitInstance or WM_CREATE)
SetTimer(hwnd, IDT_TIMER_1, 50, NULL);   // 50ms timer
SetTimer(hwnd, IDT_TIMER_2, 1000, NULL); // 1000ms (1 second) timer

```

In WndProc()
```c

case WM_TIMER:
{
    switch (wParam)
    {
    case IDT_TIMER_1:
        // Handle 50ms timer
        OutputDebugString(L"Timer 1 (50ms) ticked\n");
        break;

    case IDT_TIMER_2:
        // Handle 1000ms timer
        OutputDebugString(L"Timer 2 (1s) ticked\n");
        break;
    }
}
break;

case WM_DESTROY:
    KillTimer(hwnd, IDT_TIMER_1);
    KillTimer(hwnd, IDT_TIMER_2);
    break;

```