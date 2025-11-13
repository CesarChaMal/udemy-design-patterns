# CLAUDE.md - Design Patterns Repository Guide

## Repository Overview

This is an educational Java repository containing implementations of **23 Gang of Four (GoF) Design Patterns** from a Udemy course ([Experience Design Patterns](https://www.udemy.com/course/experience-design-patterns)). The repository contains **243 Java files** demonstrating creational, structural, and behavioral design patterns with both basic and improved implementations.

**Key Characteristics:**
- Pure Java educational codebase (no build tools like Maven/Gradle)
- Each pattern demonstrates problem → solution evolution
- Includes comprehensive PDF documentation for all pattern categories
- Case studies showing real-world applications

## Directory Structure

```
udemy-design-patterns/
├── docs/                              # Pattern documentation (PDFs)
│   ├── Design-Patterns-Introduction.pdf
│   ├── Design-Patterns-Creational-Patterns.pdf
│   ├── Design-Patterns-Structural-Patterns.pdf
│   ├── Design-Patterns-Behavioral-Patterns.pdf
│   └── Design-Patterns-Case-Study.pdf
└── src/
    ├── creational/                    # 5 Creational Patterns
    │   ├── singleton/
    │   ├── factorymethod/
    │   ├── abstractfactory/
    │   ├── builder/
    │   └── prototype/
    ├── structural/                    # 7 Structural Patterns
    │   ├── adapter/
    │   ├── bridge/
    │   ├── composite/
    │   ├── decorator/
    │   ├── facade/
    │   ├── flyweight/
    │   └── proxy/
    ├── behavioral/                    # 11 Behavioral Patterns
    │   ├── chainofresponsibility/
    │   ├── command/
    │   ├── interpreter/
    │   ├── iterator/
    │   ├── mediator/
    │   ├── memento/
    │   ├── observer/
    │   ├── state/
    │   ├── strategy/
    │   ├── templatemethod/
    │   └── visitor/
    ├── casestudy/                     # Real-world applications
    │   ├── documentstructure/
    │   ├── multiplatform/
    │   ├── rendering/
    │   └── useractions/
    └── additional/                    # Additional concepts
        ├── dto/                       # Data Transfer Object
        └── ioc/                       # Inversion of Control
```

## Pattern Implementation Structure

Each design pattern follows a consistent structure:

### Standard Pattern Layout
```
pattern-name/
├── [Base implementation files]    # Problem demonstration
│   ├── SomeClass.java
│   ├── AnotherClass.java
│   └── Client.java               # Usage example
└── improved/                      # Proper pattern implementation
    ├── SomeClass.java
    ├── AnotherClass.java
    └── Client.java
```

### Key Files in Each Pattern
- **Base implementation**: Shows the problem or naive approach
- **improved/**: Contains the proper design pattern implementation
- **Client.java**: Demonstrates how to use the pattern (found in most patterns)

## Coding Conventions

### Package Naming
- Pattern packages: `category.patternname`
- Improved implementations: `category.patternname.improved`
- Examples:
  - `creational.singleton`
  - `creational.singleton.improved`
  - `behavioral.observer.improved`
  - `structural.adapter.improved`

### Code Style
- **Access Modifiers**: Follows standard Java encapsulation (private fields, public methods)
- **Comments**: Minimal inline comments; some patterns have JavaDoc-style comments
- **Naming**: Descriptive class names (e.g., `TransportFactory`, `Button`, `Observer`)
- **Simplicity**: Code is intentionally simple for educational purposes
- **No Dependencies**: Pure Java SE with no external libraries

### Common Classes
- **Client.java**: Entry point with `main()` method demonstrating pattern usage
- **Interface/Abstract classes**: Define contracts for pattern participants
- **Concrete implementations**: Specific implementations of patterns

## Design Patterns Catalog

### Creational Patterns (Object Creation)
| Pattern | Purpose | Location |
|---------|---------|----------|
| **Singleton** | Ensure only one instance exists | `src/creational/singleton/` |
| **Factory Method** | Define interface for object creation | `src/creational/factorymethod/` |
| **Abstract Factory** | Create families of related objects | `src/creational/abstractfactory/` |
| **Builder** | Construct complex objects step-by-step | `src/creational/builder/` |
| **Prototype** | Clone objects instead of creating new | `src/creational/prototype/` |

### Structural Patterns (Object Composition)
| Pattern | Purpose | Location |
|---------|---------|----------|
| **Adapter** | Convert interface to another expected interface | `src/structural/adapter/` |
| **Bridge** | Separate abstraction from implementation | `src/structural/bridge/` |
| **Composite** | Treat individual and composite objects uniformly | `src/structural/composite/` |
| **Decorator** | Add responsibilities dynamically | `src/structural/decorator/` |
| **Facade** | Provide simplified interface to subsystem | `src/structural/facade/` |
| **Flyweight** | Share objects to support large quantities efficiently | `src/structural/flyweight/` |
| **Proxy** | Provide surrogate/placeholder for another object | `src/structural/proxy/` |

### Behavioral Patterns (Object Interaction)
| Pattern | Purpose | Location |
|---------|---------|----------|
| **Chain of Responsibility** | Pass requests along chain of handlers | `src/behavioral/chainofresponsibility/` |
| **Command** | Encapsulate requests as objects | `src/behavioral/command/` |
| **Interpreter** | Define grammar and interpret sentences | `src/behavioral/interpreter/` |
| **Iterator** | Access elements sequentially | `src/behavioral/iterator/` |
| **Mediator** | Define object interaction in a mediator | `src/behavioral/mediator/` |
| **Memento** | Capture and restore object state | `src/behavioral/memento/` |
| **Observer** | Define one-to-many dependency | `src/behavioral/observer/` |
| **State** | Alter behavior when state changes | `src/behavioral/state/` |
| **Strategy** | Define family of algorithms | `src/behavioral/strategy/` |
| **Template Method** | Define skeleton, defer steps to subclasses | `src/behavioral/templatemethod/` |
| **Visitor** | Define new operations without changing classes | `src/behavioral/visitor/` |

### Additional Concepts
- **DTO (Data Transfer Object)**: `src/additional/dto/` - Object for transferring data between layers
- **IoC (Inversion of Control)**: `src/additional/ioc/` - Dependency injection concept

### Case Studies
- **Document Structure**: `src/casestudy/documentstructure/` - Document composition patterns
- **Multiplatform**: `src/casestudy/multiplatform/` - Cross-platform UI implementations
- **Rendering**: `src/casestudy/rendering/` - Graphics rendering systems
- **User Actions**: `src/casestudy/useractions/` - User interaction handling

## Development Workflows

### Compiling Code
Since this repository has no build tool configuration, compile manually:

```bash
# Compile a specific pattern (from repository root)
javac src/creational/singleton/improved/*.java

# Compile all Java files in a pattern
javac src/behavioral/observer/improved/*.java

# Compile with explicit classpath if needed
javac -cp src src/creational/factorymethod/improved/*.java
```

### Running Examples
```bash
# Run from repository root (adjust classpath as needed)
java -cp src creational.singleton.improved.Client

# Run behavioral pattern
java -cp src behavioral.observer.improved.Client

# Run structural pattern
java -cp src structural.adapter.improved.Client
```

### Common Commands
```bash
# Count all Java files
find src -name "*.java" | wc -l

# List all Client.java files (entry points)
find src -name "Client.java"

# Find all improved implementations
find src -path "*/improved/*.java"

# Search for specific pattern usage
grep -r "Observer" src/behavioral/observer/improved/
```

## Working with This Repository

### For AI Assistants (Claude Code)

#### When Adding New Patterns
1. **Follow existing structure**: Create base implementation + `improved/` subdirectory
2. **Package naming**: Use `category.patternname.improved` convention
3. **Include Client.java**: Always provide a runnable example
4. **Keep it simple**: Educational code should be clear, not production-ready
5. **No external dependencies**: Use only Java SE standard library

#### When Modifying Patterns
1. **Read both versions**: Check base implementation and improved version
2. **Preserve teaching intent**: Don't over-engineer educational examples
3. **Test compilability**: Ensure code compiles with plain `javac`
4. **Maintain consistency**: Follow existing code style and structure

#### When Explaining Patterns
1. **Reference both versions**: Show problem (base) vs solution (improved)
2. **Use Client.java**: Demonstrate pattern usage with the provided Client
3. **Point to documentation**: Reference PDF files in `docs/` folder
4. **Compare patterns**: Explain when to use one pattern vs another

#### Best Practices for Code Changes
- **Always compile-test** after changes using `javac`
- **Maintain educational clarity** over production-readiness
- **Preserve package structure** - don't refactor package names
- **Keep examples self-contained** - each pattern should work independently
- **Don't add build tools** unless explicitly requested
- **Document any new patterns** following existing conventions

### File Editing Guidelines
1. **Read before editing**: Always read the file first to understand context
2. **Preserve formatting**: Maintain consistent indentation (tabs in this repo)
3. **Keep imports minimal**: Only import what's needed
4. **Match existing style**: Follow the pattern's existing code style
5. **Test Client.java**: Ensure the Client class still runs after changes

### Common Tasks

#### Adding a New Pattern
```bash
# 1. Create directories
mkdir -p src/category/newpattern/improved

# 2. Create base implementation files
# - Write problem demonstration
# - Include Client.java

# 3. Create improved implementation
# - Write proper pattern implementation
# - Include Client.java showing usage

# 4. Test compilation
javac src/category/newpattern/*.java
javac src/category/newpattern/improved/*.java
```

#### Comparing Implementations
```bash
# View both versions side-by-side
diff src/creational/singleton/Preferences.java \
     src/creational/singleton/improved/Preferences.java
```

#### Finding Pattern Usage
```bash
# Find all Observer pattern implementations
find src -path "*observer*" -name "*.java"

# Search for Factory pattern usage
grep -r "Factory" src/creational/
```

## Git Workflow

### Branch Strategy
- **Development branch**: `claude/claude-md-mhy0jshugrd67loj-01Umqk6BEEK9VDQysozzseFd`
- All changes should be committed to this branch
- Use descriptive commit messages

### Commit Guidelines
```bash
# Stage changes
git add [files]

# Commit with descriptive message
git commit -m "Add [pattern-name] pattern implementation"
git commit -m "Fix [issue] in [pattern-name] improved version"
git commit -m "Update documentation for [pattern-name]"

# Push to feature branch
git push -u origin claude/claude-md-mhy0jshugrd67loj-01Umqk6BEEK9VDQysozzseFd
```

### What to Commit
- Java source files (`.java`)
- Documentation updates (`.md`, PDFs if needed)
- Updated `.gitignore` if adding new patterns

### What NOT to Commit (see `.gitignore`)
- Compiled class files (`*.class`)
- IDE-specific files (`.idea`, `.project`, `.classpath`, `*.iml`)
- Build outputs (`/build`, `/target`, `/classes`)
- Log files (`*.log`)

## Troubleshooting

### Compilation Errors
**Problem**: `package X does not exist`
```bash
# Solution: Compile with proper classpath
javac -cp src src/path/to/File.java
```

**Problem**: `class X is public, should be declared in a file named X.java`
```bash
# Solution: Ensure class name matches filename
# Rename file or class to match
```

### Runtime Errors
**Problem**: `Could not find or load main class`
```bash
# Solution: Run with proper classpath and fully qualified class name
java -cp src package.name.ClassName
```

### Finding Pattern Examples
**Problem**: Not sure which pattern to use
```bash
# Solution 1: Check PDF documentation in docs/
# Solution 2: Look at Client.java files for examples
find src -name "Client.java" | xargs grep -l "keyword"
```

## Quick Reference

### Repository Stats
- **Total Java Files**: 243
- **Creational Patterns**: 5
- **Structural Patterns**: 7
- **Behavioral Patterns**: 11
- **Case Studies**: 4
- **Additional Concepts**: 2

### Key Directories
- `src/` - All source code
- `docs/` - PDF documentation
- `improved/` - Proper pattern implementations (in each pattern directory)

### Important Files
- `README.md` - Basic repository information
- `.gitignore` - Git ignore rules
- `Client.java` - Pattern usage examples (in each pattern directory)

## Learning Path Recommendations

### For Understanding This Codebase
1. **Start with Creational Patterns** - Simplest to understand
   - Begin with Singleton (`src/creational/singleton/`)
   - Move to Factory Method (`src/creational/factorymethod/`)

2. **Progress to Structural Patterns** - Object composition
   - Start with Adapter (`src/structural/adapter/`)
   - Explore Decorator (`src/structural/decorator/`)

3. **Study Behavioral Patterns** - Object interaction
   - Begin with Observer (`src/behavioral/observer/`)
   - Explore Strategy (`src/behavioral/strategy/`)

4. **Review Case Studies** - Real-world applications
   - See how patterns combine in practice

### For Each Pattern
1. Read base implementation (shows the problem)
2. Read improved implementation (shows the solution)
3. Run Client.java to see it in action
4. Refer to PDF documentation for theory

## Additional Resources

- **Course URL**: https://www.udemy.com/course/experience-design-patterns
- **Documentation**: See `docs/` folder for comprehensive PDFs
- **Design Patterns**: Gang of Four (GoF) Design Patterns

## Notes for AI Assistants

### Context Awareness
- This is an **educational repository** - prioritize clarity over complexity
- Code is **intentionally simple** - don't over-optimize
- **No testing framework** - manual testing via Client.java
- **No build system** - compile with javac, run with java

### Response Guidelines
1. **Always check both base and improved versions** when analyzing a pattern
2. **Compile test suggestions** before recommending changes
3. **Maintain educational value** - explain why, not just how
4. **Reference specific files** with line numbers when explaining
5. **Suggest running Client.java** to demonstrate pattern behavior

### Common Requests
- "Explain pattern X" → Read base + improved + Client.java, then explain
- "Add new pattern Y" → Follow directory structure, create improved/ version
- "Fix compilation error" → Check package names and classpath
- "Compare patterns X and Y" → Analyze use cases and trade-offs

---

**Last Updated**: 2025-11-13
**Repository**: udemy-design-patterns
**Purpose**: Educational Design Patterns Implementation
