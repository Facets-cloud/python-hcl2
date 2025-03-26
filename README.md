[![Codacy Badge](https://app.codacy.com/project/badge/Grade/2e2015f9297346cbaa788c46ab957827)](https://app.codacy.com/gh/amplify-education/python-hcl2/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)
[![Build Status](https://travis-ci.org/amplify-education/python-hcl2.svg?branch=master)](https://travis-ci.org/amplify-education/python-hcl2)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/amplify-education/python-hcl2/master/LICENSE)
[![PyPI](https://img.shields.io/pypi/v/python-hcl2.svg)](https://pypi.org/project/python-hcl2/)
[![Python Versions](https://img.shields.io/pypi/pyversions/python-hcl2.svg)](https://pypi.python.org/pypi/python-hcl2)
[![Downloads](https://img.shields.io/badge/dynamic/json.svg?label=downloads&url=https%3A%2F%2Fpypistats.org%2Fapi%2Fpackages%2Fpython-hcl2%2Frecent&query=data.last_month&colorB=brightgreen&suffix=%2FMonth)](https://pypistats.org/packages/python-hcl2)

# Python HCL2

A parser for [HCL2](https://github.com/hashicorp/hcl/blob/hcl2/hclsyntax/spec.md) written in Python using
[Lark](https://github.com/lark-parser/lark). This parser only supports HCL2 and isn't backwards compatible
with HCL v1. It can be used to parse any HCL2 config file such as Terraform.

## About Amplify

Amplify builds innovative and compelling digital educational products that empower teachers and students across the
country. We have a long history as the leading innovator in K-12 education - and have been described as the best tech
company in education and the best education company in tech. While others try to shrink the learning experience into
the technology, we use technology to expand what is possible in real classrooms with real students and teachers.

Learn more at <https://www.amplify.com>

## Getting Started

### Prerequisites

python-hcl2 requires Python 3.7 or higher to run.

### Installing

This package can be installed using `pip`

```sh
pip3 install python-hcl2
```

### Usage

```python
import hcl
with open('foo.tf', 'r') as file:
    dict = hcl.load(file)
```

### Parse Tree to HCL2 reconstruction

With version 6.x the possibility of HCL2 reconstruction from the Lark Parse Tree and Python dictionaries directly was introduced.

Documentation and an example of manipulating Lark Parse Tree and reconstructing it back into valid HCL2 can be found in [tree-to-hcl2-reconstruction.md](https://github.com/amplify-education/python-hcl2/blob/main/tree-to-hcl2-reconstruction.md) file.

More details about reconstruction implementation can be found in PRs #169 and #177.

## Building From Source

For development, `tox>=4.0.9` is recommended.

### Running Tests

python-hcl2 uses `tox`. You will need to install tox with `pip install tox`.
Running `tox` will automatically execute linters as well as the unit tests.

You can also run them individually with the `-e` argument.

For example, `tox -e py37-unit` will run the unit tests for python 3.7

To see all the available options, run `tox -l`.

## Releasing

To create a new releaes go to Releases page, press 'Draft a new release', create a tag
with a version you want to be released, fill the release notes and press 'Publish release'.
Github actions will take care of publishing it to PyPi.

## Responsible Disclosure

If you have any security issue to report, contact project maintainers privately.
You can reach us at <mailto:github@amplify.com>

## Contributing

We welcome pull requests! For your pull request to be accepted smoothly, we suggest that you:

- For any sizable change, first open a GitHub issue to discuss your idea.
- Create a pull request.  Explain why you want to make the change and what it’s for.

We’ll try to answer any PR’s promptly.
