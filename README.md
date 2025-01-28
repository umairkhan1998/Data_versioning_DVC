# Data Versioning with DVC and Git

## Overview

This repository demonstrates how to apply Data Version Control (DVC) along with Git for efficient data versioning. By using DVC, we can manage large datasets, track changes, and roll back to previous versions seamlessly.

## Features

- **Data Version Control**: Track and manage large datasets effectively.
- **Seamless Integration with Git**: Maintain dataset versions just like code.
- **Rollback Capabilities**: Restore previous versions of data with ease.
- **Efficient Storage**: Avoid unnecessary duplication of large files.

## Prerequisites

no Make sure you have the following installed:

- [Git](https://git-scm.com/downloads)
- [DVC](https://dvc.org/doc/install)

## Getting Started

### 2. Initialize DVC

If not already initialized, run:

```bash
dvc init
git commit -m "Initialize DVC"
```

### 3. Add Data Files

```bash
dvc add data/
git add data.dvc .gitignore
git commit -m "Add data files with DVC"
```

### 4. Push Data to Remote Storage

To store data remotely:

```bash
dvc remote add -d myremote <remote_storage_url>
dvc push
```

### 5. Pull Data from Remote

If you clone the repo on another machine, retrieve the dataset:

```bash
dvc pull
```

## Updating Data

To update your dataset:

```bash
dvc add data/
git commit -m "Updated dataset"
dvc push
```

## Rolling Back to a Previous Version

Find the previous commit ID where the data was last correct:

```bash
git log
```

Then, restore the dataset:

```bash
git checkout <commit_id>
dvc checkout
```

## Contributors

- **Umair** - [GitHub Profile](https://github.com/your-profile)

## License

This project is licensed under the MIT License.

---

Feel free to contribute or open an issue if you have any suggestions!

