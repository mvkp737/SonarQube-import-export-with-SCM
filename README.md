# SonarQube-import-export-with-SCM
Import / export SonarQube's quality profiles and gates with SCM

## Introduction
SonarQube is an open source platform for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities on 20+ programming languages.
SonarQube uses “Quality Profiles” and “Quality Gates” to analyze your project. Quality Profiles allows you to define the requirements from the project by defining sets of rules, and with Quality Gate you can define set of Boolean conditions based on measure thresholds against which projects are measured.

SonarQube currently provides the ability to back up and restore Quality Profiles but not of Quality Gates. In addition, this option does not support integration with SCM tools (like git).

**The purpose of this project is to enable:**
- *export* of Quality Profiles/Gates from SonarQube to Git.
- *import* of Quality Profiles/Gates from Git to SonarQube.

**Project structure:
- the folder `groovy-scripts` contains groovy scripts that use the existing SonarQube API to import/export profiles/gates.
- the folders `jenkins_jobs` and `jenkinsfiles` contains the configuration of Jenkins, through which we integrated the export and import operations with GIT.
