# `tkn`

`tkn` is a command-line utility to quickly tokenize with `tiktoken`.

## Installation

`pip install tkn`

## Usage:

```
$ tkn -h                                                                                                                                                                                                       2 ↵
usage: tkn [-h] [-s] [-d | -c] (-e ENCODING | -m MODEL) [filename]

Encode or decode a file using tiktoken.

positional arguments:
  filename              The file to encode or decode.

options:
  -h, --help            show this help message and exit
  -s, --split           Tokenize each line separately
  -d, --decode          Whether to decode the input instead of encoding
  -c, --count           Return the token count instead of the tokens
  -e ENCODING, --encoding ENCODING
                        The encoding to use. Passed to tiktoken.get_encoder
  -m MODEL, --model MODEL
                        The model to use. Passed to tiktoken.encoder_for_model
```

### Examples

```
$ ls
document_1.txt
document_2.txt

$ tkn -e base_cl100 document_1.txt
[tokenized version of the data]

$ tkn -m gpt-4 document_1.txt -s '\n' | wc -l
2094 # document contains 2094 tokens

$ tkn -m gpt-4 document_1.txt | tkn -m gpt-4 -d
[the contents of document_1.txt]
```
