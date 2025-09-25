# Campus Course & Records Manager (CCRM)

## Project overview
Small console-based Java SE application to manage students, courses, enrollments, grades, and export/backup utilities.

## How to run (macOS)
- JDK: Java 17 (Temurin recommended)
- Build:
  ```bash
  find src -name "*.java" > sources.txt
  javac -d out @sources.txt
  java -cp out edu.ccrm.cli.Main
  ```
- Or run packaged JAR:
  ```bash
  java -jar CCRM.jar
  ```

## Deliverables (what I included)
- Source code under `src/edu/ccrm/...`
- `screenshots/` folder (java -version, IDE run, exports/backups)
- `test-data/` small CSV files for import
- `USAGE.md` with sample import commands

## Evolution of Java (short bullets)
- 1995: Java 1.0 — initial release  
- 2004: Java 5 — generics, enhanced for-loop, enums  
- 2014 onward: Java 8+ — Streams, Lambda (important for this project)

## Java ME vs SE vs EE (short table)
- ME: Micro devices; SE: Standard Edition (this project); EE: Enterprise (web services)

## JDK vs JRE vs JVM (short)
- JDK: compiler + tools; JRE: runtime; JVM: engine that runs bytecode.

## Mapping: syllabus topic → file/class
- Singleton: `edu.ccrm.config.AppConfig`  
- Builder: `edu.ccrm.domain.Course` (inner `Builder` class)  
- Enums: `edu.ccrm.domain.Semester`, `edu.ccrm.domain.Grade`  
- Custom Exceptions: `edu.ccrm.exceptions.DuplicateEnrollmentException`, `...MaxCreditLimitExceededException`  
- NIO.2 file ops: `edu.ccrm.io.ImportExportService`, `edu.ccrm.io.BackupService`  
- CLI / Menu: `edu.ccrm.cli.Main`, `edu.ccrm.cli.Menu`  
- Streams / Filters: used in `edu.ccrm.service.*` (search/filter implementations)

## Notes on assertions
Enable assertions:
```bash
java -ea -cp out edu.ccrm.cli.Main
```

## Screenshots
- `screenshots/java-version.png` (java -version)
- `screenshots/eclipse-setup.png` (Eclipse run)
- `screenshots/program-run.png` (sample menu)
- `screenshots/backups.png` (timestamped backups folder)

## Academic integrity
This submission is my own work. Acknowledgements: [any libs or references].
