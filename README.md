# Reposcanner
Reposcanner is a python script to search through the commit history of Git repositories looking for interesting strings such as API keys, inspires by [truffleHog](https://raw.githubusercontent.com/dxa4481/truffleHog).

## Installation
The python Git module is required (python-git on Debian).

## Usage

```
./reposcanner -r <repository>
```

Options:

```
optional arguments:
  -h, --help                     show this help message and exit
  -r REPO, --repo REPO           Repo to scan
  -c COUNT, --count COUNT        Number of commits to scan (default 500)
  -e ENTROPY, --entropy ENTROPY  Minimum entropy to report (default 4.3)
  -l LENGTH, --length LENGTH     Maxmimum line length (default 500)
  -a, --all-branches             Scan all branches
  -b BRANCH, --branch BRANCH     Scan a specific branch
  -v, --verbose                  Verbose output
```

Example:

```
./reposcanner.py -r https://github.com/Dionach/reposcanner -v -a -c 30
```
