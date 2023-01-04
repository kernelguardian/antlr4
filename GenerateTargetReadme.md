# ANTLR

ANTLR can be used to generate AST which can be “walked” to do stuff (features for language server)

Run this to test ANTLR for converting JSON.g4 (JSON grammar) to ANTLR files (Tokens, Lexer’s and other things) + Java code

PS: This won’t run on the new M1 Mac or any arm architecture.


```bash
git clone https://github.com/antlr/antlr4.git
cd antlr4/docker
docker build -t antlr/antlr4 --platfort linux/amd64　.

wget [https://raw.githubusercontent.com/antlr/grammars-v4/master/json/JSON.g4](https://raw.githubusercontent.com/antlr/grammars-v4/master/json/JSON.g4)

docker run --rm -u $(id -u ${USER}):$(id -g ${USER}) -v `pwd`:/work antlr/antlr4 -Dlanguage=Go JSON.g4
```

## Get your grammars from here
- [Python3](https://github.com/antlr/grammars-v4/tree/master/python/python3-py)
- [JavaScript](https://github.com/antlr/grammars-v4/tree/master/javascript/javascript)
- https://github.com/antlr/grammars-v4

## Other Target languages

- C
- Java
- Python3
- JavaScript
- Complete list → [https://github.com/antlr/antlr4/blob/master/doc/targets.md](https://github.com/antlr/antlr4/blob/master/doc/targets.md)