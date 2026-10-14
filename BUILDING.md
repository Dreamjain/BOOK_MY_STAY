# Java Build & Validation

## Requirements

- JDK 17 or newer
- Git (to clone the repository)

## Run the starter use cases

From the repository root, compile the entry-point and room-initialization examples:

```bash
javac UseCase1HotelBookingApp.java UseCase2RoomInitialization.java
java UseCase1HotelBookingApp
java UseCase2RoomInitialization
```

## Run the full source set

Several use-case files define domain classes with the same names, so compile each use case separately rather than compiling every `.java` file in one command. For example:

```bash
javac UseCase11ConcurrentBookingSimulation.java
java UseCase11ConcurrentBookingSimulation
```

To compile another use case, substitute its source filename and corresponding public class name.

## Clean generated artifacts

Compiled `.class` files are build outputs, not source files. Remove generated classes before committing them:

```bash
# macOS / Linux / Git Bash
find . -name '*.class' -type f -delete

# Windows PowerShell
Get-ChildItem -Recurse -Filter *.class | Remove-Item
```

The repository's `.gitignore` excludes `.class` files for future untracked builds. Files that are already tracked must also be removed from Git's index through a normal `git rm` commit.
