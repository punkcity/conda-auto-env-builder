# Automated Conda Project Environment Builder

A useful utility to help accelerate new projects by automating the building of a Conda virtual environment from a project repository zipfile

### Start Date: February 7, 2024

## Project Participants:

    Mentor: Rich Lysakowski
    Pankaj Verma, Olena Tokova, Hilary Shea, Nadia Stoyanova, Rocio Calle, Monzia Moodie, Biraja Dash, Cesar Anderson, Anil Naik, others

## Project Workflow to create a tool with Copilot in VScode

    Using 6D Agile Software Development Workflow
        - define
        - design
        - develop
        - debug
        - document
        - deliver

## Brainstorm Project Idea

Project Description: CondaQuickBuilder is an automated tool designed to accelerate the setup of new projects by generating a Python script that builds a new Conda environment from a project repository package. This tool aims to reduce the manual effort involved in setting up environments, thus increasing productivity and efficiency.

    ## Features:

    Input: Accepts a project repository package (zip file) as input.

    ## Environment Extraction: Extracts the project repository and identifies the necessary dependencies from files like requirements.txt or environment.yml.

    ## Script Generation: Generates a Python script that uses Conda commands to create a new environment and install the necessary dependencies.

    ## Environment Creation: Option to automatically run the generated script to create the environment.

    ## Logging: Provides detailed logs of the process for debugging and transparency.

    ## Error Handling: Gracefully handles errors and provides useful error messages.

    ## Implementation Steps:
    	## Setup: Set up a Python project with a good structure and necessary configurations.

    	## Develop Input Module: Develop a module to accept and validate the input zip file.

    	## Develop Extraction Module: Develop a module to extract the zip file and identify necessary dependencies.

    	## Develop Script Generation Module: Develop a module to generate a Python script with Conda commands for creating a new environment and installing dependencies.

    	## Develop Environment Creation Module: Develop a module to run the generated script and create the Conda environment.

    	## Develop Logging Module: Develop a module to log the process details.

    	## Develop Error Handling Module: Develop a module to handle errors and exceptions.

    	## Testing: Write unit tests for each module and perform integration testing.

    	## Documentation: Document the usage of the tool and each of its modules.

    	## Technologies:

    		## Python: The main language for developing the tool.

    		## Conda: The package and environment management system.

    		## pytest: The testing framework for Python (use this for the development version only)

    	## Future Enhancements:

    		## GUI: Develop a graphical user interface for easier usage.

    		## Support for Other Package Managers: Extend the tool to support other package managers like npm, ruby-on-rails, R, etc.

    		## Custom Configuration: Allow end-users (both developers and regular users) to provide custom configurations for environment setup.

## Define Phase [Purpose and Requirements]

    ### Project Purpose: The purpose of the CondaQuickBuilder project is to automate the process of setting up a new Conda environment for a Python project. This is achieved by generating a Python script that can create a new Conda environment and install the necessary dependencies based on the contents of a project repository package. The goal is to reduce the time and effort required to manually set up environments, thus increasing productivity and efficiency for developers.

    ### Project Requirements:

    	### Input Handling: Accept a project repository package (zip file) as input.

    	### Environment Extraction: Extract the project repository and identify necessary dependencies.

    	### Script Generation: Generate a Python script with Conda commands for creating a new environment and installing dependencies.

    	### Environment Creation: Provide an option to automatically run the generated script to create the environment.

    	### Logging: Provide detailed logs of the process.

    	### Error Handling: Handle errors gracefully and provide useful error messages.

    	### Testing: Include thorough testing, with unit tests for each module and integration tests for the whole system.

    	### Documentation: Provide comprehensive documentation, including usage instructions and explanations of each module.

\*\*\* Make these descriptions very concise without losing any technical explanation

#### Project Purpose: Create End-to-end Automated Tool to generate Python script that builds a new conda environment from a project repository package.

##### Setup Project Development Tools

    1) Open VSCode

    2) Create New Workspace with the Name for New Project

    3) Develop and flesh out "Project Description"

###### Define and Describe Project Purpose & Requirements

    1) create a catchy project title: CondaQuickBuilder

    2) articulate 1-paragraph description that:
        a) defines the "business problem"

    	###### Business Problem: In the fast-paced world of software development, setting up new project environments can be a time-consuming and error-prone process. Developers often need to manually create a new Conda environment and install necessary dependencies based on the contents of a project repository package. This manual process can lead to inconsistencies across different environments and slow down the overall development process, reducing productivity and efficiency. Doing this quickly requires expertise and experience as well as methodology that is informed by experience. The issue of broken environments leading to the waste of time.

    	*** Make this problem description more concise.

    	b) describes technical solution to solve business problem

    	###### Technical Solution: CondaQuickBuilder addresses this problem by automating the process of setting up a new Conda environment. It accepts a project repository package as input, extracts the necessary dependencies, and generates a Python script that uses Conda commands to create a new environment and install these dependencies. This tool can also automatically run the generated script to create the environment. With detailed logging and error handling, CondaQuickBuilder ensures transparency and reliability in the environment setup process.

    	Make requirements actionable for the purposes of code generation representing the objects and functions of your code: identify the nouns/objects and the verbs/functions, adjective/metrics/measures.
    	"This solution not only saves time and reduces errors, but also ensures consistency across different environments, thereby accelerating the software development process."
    	*** Make this problem description more concise.

    3) articulate project scrope, requirements, and constraints

    	###### Project Scope: The scope of the CondaQuickBuilder project includes the design, development, and testing of a tool that automates the process of setting up a new Conda environment from a project repository package. The tool will be able to extract necessary dependencies from the package, generate a Python script with Conda commands to create a new environment and install the dependencies, and optionally run the generated script. The project also includes the development of detailed logging and error handling mechanisms.

    	###### Project Requirements:

    		###### Input Handling: Accept a project repository package (zip file) as input.

    		###### Environment Extraction: Extract the project repository and identify necessary dependencies.

    		###### Script Generation: Generate a Python script with Conda commands for creating a new environment and installing dependencies.

    		###### Environment Creation: Provide an option to automatically run the generated script to create the environment.

    		###### Logging: Provide detailed logs of the process.

    		###### Error Handling: Handle errors gracefully and provide useful error messages.

    		###### Testing: Include thorough testing, with unit tests for each module and integration tests for the whole system.

    		###### Documentation: Provide comprehensive documentation, including usage instructions and explanations of each module.

    	###### Project Constraints:

    		###### Technical Constraints: The tool is designed to work with Conda and Python. It may not work with other package managers or programming languages without modifications.

    		###### Time Constraints: Depending on the project timeline, some features (like a graphical user interface or support for other package managers) may need to be deferred to future versions.

    		###### Resource Constraints: The development of the tool depends on the availability of resources, including development tools and personnel. Any changes in these resources could impact the project timeline and deliverables.

## Design Phase

######## High-Level Design
High-level description of the workflow - What? how to download the best tool for your project, does not describe the exact code (except business reqs - must have env).

######### Detailed Design: exactly how to use the environment, or the code: step by step, algorhythm, pseudocode.

########## Project Workflow - Define Detailed Steps:

    2) Search for pre-existing packages that fit the bill
         Don't reinvent the wheel - find something already available that meets the requirements
    3) Select existing that meets the initial requirements
    4) Download the best fitting package

    4b) user-specifies project folder name - function: get_new_project_name()
    5) unzip the best fitting package into new project folder [with a user-specified name]
            function: unzip_starter_project_repo()
    6) scan the project folder to find the (unique) set of required Python package dependencies
            function: scan_project_modules()
            py_dependencies_set
    7) scan our local pre-existing virtual environments to see which fits the dependency tree the best.
            function: scan_existing_env()
            current_env_dependencies_set
    8) decide whether to use or clone a pre-existing virtual environment or create a new one?
        Does an existing environment have required "current enough" packages to stand up the project?
            function: measure_env_fit() ?
    9) use "conda search" to see if each package dependency is available in conda-channel priority:
            search function: 1) search_conda_forge(), 2) search_anaconda(), 3) search_pip()
            a) conda-forge     (set of packages IN conda-forge)
            b) anaconda        (set of packages NOT IN conda-forge, but anaconda)
            c) pip             (set of packages NOT IN (conda-forge OR anaconda)

    10) iterate over step 9 until all (new) packages and required versions are found
            a) build list of repos (conda-forge, anaconda, CONDA-OTHER, or pip) containing required versions
                function: build_repos_lists()

    12) create Python functions (or separate script commands?) needed to execute the environment build steps.

        a) conda create "core" environment using as many conda-forge packages as possible
            Example: conda create -n new_env -c conda-forge python, conda, etc.

        b) conda activate new_env

        c) conda install -c conda-forge ... all the other packages
            [conda install -c anaconda (???)]
            [conda install -c conda-OTHER

        d) pip install ... all remaining packages that are NOT available in conda format

    13) Build final script to execute The 12 Steps
    14) Test final script
    15) Deliver

##### Project Object Model:

    new_project_dependency_set

    existing_env_package_set  - (for v1, assume we inquire about only one preexisting env)

    conda_forge_pkg_list
    anaconda_pkg_list
    pip_only_pkg_list

##### Functions API Model

    Extract functions identified above in Project Workflow - Define Detailed Steps:

## Develop Phase (TBD)

### **FEED PROJECT OVERVIEW, DETAILED DESIGN (WORKFLOW AND OBJECT MODEL)**

### \*\*use the following (possibly redundant) text with the section above: "Project Workflow - Define Detailed Steps">>

    Create a Python program to sequentially search for a Python conda packages list provided by the user.

    Use "conda search" for conda-only versions of packages in the "conda-forge" channel,

    Use "conda search" infor "anaconda" channel.

    Build a list of the latest versions of packages is available in each repository (conda-forge, anaconda, pip),

    Finally search pip for the remaining Python packages that do not have a current conda package, and build a Python function to install the remaining packages.

    Prioritize the installation commands:
        "conda install -c conda-forge" packages first
        "conda install -c anaconda" packages next
        "pip install <pip-only package names>"

    Critical "robustness" requirements:
        Add fault-tolerance and error-checking,
        Log process to a time-stamped file

    Provide output report files as a markdown or HTML text file(s) for final lists of packages pulled and installed from conda-forge, anaconda, and pip.

    Display final reports:
        In web browser (Markdown/HTML format).
        In Notepad++ (Markdown format, for editing)

## Debug (test) Phase

    Get core functionality tested
    Enhance with important features missed earlier

## Document Phase

## Deliver Phase

# FOLLOW-ON PROJECT USING LANGCHAIN

Purpose: Build Automated Tool for Building Tools
A Lower-code forms-driven way to automate the process of building tools and utilities using LLMs

MetaTool Creation Meta-Workflow:

This could be part of a suite of automated intelligent software "project accelerators".
2024.02.08-Automated_Project_Conda_Env_Builder.md
Zoomed out of item.

### Define and Describe Project Purpose & Requirements

    1) create a catchy project title
    2) articulate 1-paragraph description that:
        a) defines the "business problem"
        b) describes technical solution to solve business problem
    3) articulate project scrope, requirements, and constraints
