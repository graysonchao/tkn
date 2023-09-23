# `tk`

`tk` is a command-line utility for working with tokenizers.

Example usage:

```
$ ls
training_data_1.json
training_data_2.json

$ tk training_data_1.json
[tokenized version of the data]

$ tk training_data_1.json -s '\n' | wc -l
2094 # document contains 2094 tokens

$ tk training_data_1.json -o json
[the tokenized data represented in json]
```
