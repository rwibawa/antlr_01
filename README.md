# antlr v4
Learn antlr

1. Install antlr on OS X
```bash
  $ cd /usr/local/lib/
  $ sudo curl -O http://www.antlr.org/download/antlr-4.7-complete.jar
  $ vi ~/.bash_profile
        export CLASSPATH=".:/usr/local/lib/antlr-4.7-complete.jar:$CLASSPATH"
        alias antlr4='java -jar /usr/local/lib/antlr-4.7-complete.jar'
        alias grun='java org.antlr.v4.gui.TestRig'
  $ source ~/.bash_profile
  $ ls -lah /usr/local/lib/antlr-4.7-complete.jar
```
2. Create a sample
```bash
  $ mkdir antlr_01
  $ cd antlr_01/
  $ vi Expr.g4

  $ antlr4 Expr.g4
  $ javac Expr*.java
  $ grun Expr prog -gui
        100+2*34
        ^D
```

