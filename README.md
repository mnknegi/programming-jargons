# programming-jargons

## Table of Content
- [Vibe Coding](#vibe-coding)
- [Scaffolding](#scaffolding)
- [Domain Specific Language](#domain-specific-language)
- [Semantic Versioning](#semantic-versioning)

## Vibe Coding:
Coined by AI researcher *_Andrej Karpathy_* in early 2025. It is a way of building software where you `fully give in to the vibes` and let AI handle the implementation. Instead of writing syntax line-by-line, you describe your vision in natural language, iterate based on what "feels" right, and essentially treat the underlying code as a steerable draft that you don't necessarily need to read or fully understand.

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

## Domain Specific Language
A DSL is essentially a "mini-language" designed to solve a very specific problem. **SwiftUI**, which is a Domain-Specific Language built right on top of Swift. Similarly, in the context of a `Package.swift` file (the manifest for a Swift Package), saying that `PackageDescription` is Apple's DSL means that you are using a specialized "mini-language" to describe your project's structure, but that mini-language is written entirely using standard Swift syntax.

## Semantic Versioning
Also known as SemVer is a standard convention for naming software versions so that developers and users know exactly what kind of changes are in a new release just by looking at the numbers.

SemVer uses a three-part format:
> MAJOR.MINOR.PATCH

**MAJOR**: When you make breaking changes (incompatible API changes). Existing code might break.

**MINOR**: When you add functionality in a backward-compatible manner. New features are available, but your old code still works.

**PATCH**: When you make backward-compatible bug fixes. No new features, just stability and security improvements.
