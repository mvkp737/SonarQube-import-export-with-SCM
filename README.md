# SonarQube-import-export-with-SCM
Import / export SonarQube's quality profiles and gates with SCM

## Introduction
SonarQube is an open source platform for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities on 20+ programming languages.  
SonarQube uses “Quality Profiles” and “Quality Gates” to analyze your project.  
Quality Profiles allows you to define the requirements from the project by defining sets of rules, and with Quality Gate you can define set of Boolean conditions based on measure thresholds against which projects are measured.

SonarQube currently provides the ability to back up and restore Quality Profiles but not of Quality Gates. In addition, this option does not support integration with SCM tools (like git).

**The purpose of this project is to enable:**
- *export* of Quality Profiles/Gates from SonarQube to Git.
- *import* of Quality Profiles/Gates from Git to SonarQube.

**Project structure:**
- The folder `groovy-scripts` contains groovy scripts that use the existing SonarQube API to import/export profiles/gates.
- The folders `jenkins_jobs` and `jenkinsfiles` contains the configuration of Jenkins, through which we integrated the export and import operations with GIT.

## The groovy scripts

### Export Profile
#### Description
Export Quality Profile from SonarQube to `workspace`.
This operation has two options:
1. Export all Quality Profiles that associated with specific project.  
   - This group of profiles includes:  
     - The profiles from the last scan of the projecy (appears on the left side of the project page, under the title "Quality Profiles").  
     - The profiles currently associated to the project (appears in project page -> Administration -> Quality Profiles, and includes only the profiles that correspond to the programming languages used by the project).  
   -  To use this option, the parameter "projectKey" must be passed, but not the parameters "language" and "profileName".  
2. Export specip Quality Profile, given the ptofile name and its correspond programming language.
   - To use this option, the parameters "language" and "profileName" must be passed, but not the parameter "projectKey".  
#### Arguments - option 1
- `p1`
#### Usage
- In case you want to export quality profile that used by specific project (:


#### Arguments - option 2


