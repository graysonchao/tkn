# `tk`

`tk` is a command-line utility to quickly tokenize with `tiktoken`.

## Installation

`pip install tk`

Example usage:

```
$ ls
document_1.txt
document_2.txt

$ tk document_1.txt
[tokenized version of the data]

$ tk document_1.txt -s '\n' | wc -l
2094 # document contains 2094 tokens

$ tk document_1.txt -o json
[the tokenized data represented in txt]

$ tk document_1.txt -d
[decoded version of the data]

$ tk document_1.txt -e utf-8
[the data encoded in utf-8]

$ tk document_1.txt -m model_name
[the data tokenized using the specified model]
```
