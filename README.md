# Stockholm

## Description

This program will encrypt files in the directory '/home/user/infection'. 
Only affects files with extensions that were affected by Wannacry.
It save the key to decrypt the files in a file called 'decrypt.key'.

## Prerrequisits

It use Python with the modules: sys, os, argparse, Fernet and pathlib.

## Use

```
usage: stockholm.py [-h] [-v] [-r KEY_FILE PATH] [-s]

It is a program that encrypts anf decrypts the files on the computer

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         version of the program
  -r KEY_FILE PATH, --reverse KEY_FILE PATH
                        decrypt the files with key file in the path indicated
  -s, --silent          silent mode
```
### Examples

Encrypt all files in `/home/user/infection`

```shell
$ python3 stockholm.py
```

Decrypt files from `/home/user/infection` to folder

```shell
$ python3 stockholm.py -r decrypt.key folder
```

- To silent mode, simple add `-s`

```shell
$ python3 stockholm.py -s
```
