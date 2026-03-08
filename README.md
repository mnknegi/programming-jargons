# programming-jargons

## Scaffolding: 
Process of quickly generating the boilerplate folder structure, manifest files, and initial source code for a project.

```
mkdir MyAwesomeLibrary
cd MyAwesomeLibrary
swift package init --type library  # Options: library, executable, tool, macro
```
**What it scaffolds for you**:
- Package.swift: The manifest file where you define targets and dependencies.
- Sources/ folder: A sub-folder named after your package for your logic.
- Tests/ folder: A pre-configured XCTest or Swift Testing target.
- .gitignore: Automatically set up for Swift projects.

**To scaffold an App**: Select "App" under the iOS or macOS tab. Xcode will generate your App.swift and initial ContentView.swift.
**To scaffold a Package**: Select the Multiplatform tab and choose Library or Empty.

**New in Xcode 26.3 (AI Scaffolding)**:
With the integration of `Claude/OpenAI` Agents, you can now use "Natural Language Scaffolding." You can open the Assistant and say:

> Scaffold a networking layer using Clean Architecture with a Repository pattern and a Mock URLSession.

Xcode will then generate multiple files, folders, and protocols based on that "vibe," rather than just giving you a single empty file.
