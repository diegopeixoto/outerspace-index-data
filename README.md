# Outerspace Forum Index Data Repository

This repository allows users to submit JSON files containing topics from the Outerspace forum. Users can contribute by submitting a Pull Request (PR) or by reporting an issue, after which a collaborator can upload the file on their behalf.

## Table of Contents

- [Introduction](#introduction)
- [Repository Structure](#repository-structure)
- [JSON Processing Workflow](#json-processing-workflow)
- [Example JSON File](#example-json-file)
- [How to Contribute](#how-to-contribute)
- [Dependencies](#dependencies)
- [License](#license)

## Introduction

The Outerspace Forum Index Data Repository automates the process of adding forum topics to the [outerspace-index-handler](https://github.com/diegopeixoto/outerspace-index-handler) repository. This facilitates user contributions by providing a standardized way to submit forum topic data.

## Repository Structure

- `.github/workflows/process-json.yml`: Contains the GitHub Actions workflow that processes the submitted JSON files.
- `fa0ea260-f58c-452e-85ec-f59761b64229.json`: Example of a JSON file containing a forum topic.

## JSON Processing Workflow

The workflow defined in `.github/workflows/process-json.yml` is triggered upon a push to the main branch. Below is a summary of the steps involved in the workflow:

1. **Check out the repository**: The repository is checked out to the workflow environment.
2. **Get the JSON file name from the commit**: Extracts the JSON file name from the commit details.
3. **Set up Node.js**: Configures Node.js, specifically version 18, for the environment.
4. **Clone the outerspace-index-handler repository**: The outerspace-index-handler repository is cloned, and the JSON file is copied to it.
5. **Perform a dry run**: Simulates the JSON file processing to ensure everything is set up correctly.
6. **Run the actual task**: Executes the actual task of processing the JSON file.
7. **Clean up**: Removes the cloned outerspace-index-handler repository from the workflow environment.

## Example JSON File

The repository includes an example JSON file (`fa0ea260-f58c-452e-85ec-f59761b64229.json`) that contains a sample forum topic. This serves as a reference for users who wish to contribute similar data.

## How to Contribute

There are two ways to contribute to this project:

1. **Submit a Pull Request**: Fork this repository, add your JSON file, and submit a PR.
2. **Open an Issue**: Report an issue with the details of the JSON file, and a collaborator will assist in uploading the file.

Please ensure that your JSON file follows the structure and format as outlined in the example provided in this repository.

## Dependencies

This project relies on Node.js version 18, which is configured automatically as part of the GitHub Actions workflow.
