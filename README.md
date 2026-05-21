## Building

### Using VS Code Build Task (Recommended)
Press **`Ctrl + Shift + B`** to compile both `test_subscriber.c` and `test_publisher.c`.

Alternatively, use **`Ctrl + Shift + P`** → search for "Run Build Task" → select:
- **Compile Both** (default) - compiles both files
- **Compile Subscriber** - compiles only test_subscriber.c
- **Compile Publisher** - compiles only test_publisher.c

### Using Command Line
```powershell
# Compile both files
gcc -std=c99 -Wall -Wextra -o test_subscriber test_subscriber.c -lmosquitto
gcc -std=c99 -Wall -Wextra -o test_publisher test_publisher.c -lmosquitto

# Or use Makefile (requires make installed)
make
```

## Running

### In VS Code Terminal
Open terminal with **`Ctrl + J`**, then split it with the split icon.

**Terminal 1 (Subscriber):**
```powershell
.\test_subscriber.exe
```

**Terminal 2 (Publisher):**
```powershell
.\test_publisher.exe
```

The subscriber will listen for messages on `mqtt-lab/test/sensor` and the publisher will send test messages.

### Workflow
1. Edit `.c` files
2. Press `Ctrl + Shift + B` to recompile
3. Run both executables in separate terminal windows to test
