Como colocar um pedaço de texto em um registro?
-----------------------------------------------
```
 <Esc> ...... vai para o modo normal
 "a10j ...... coloca no registro `a' as próximas 10 linhas `10j'
```
Pode-se fazer:
```
<Esc> ...... para ter certeza que está em modo normal
"ap ........ registro a `paste', ou seja, cole
``
Em modo de inserção faz-se:
```
Ctrl-r a
```
Há situações em que se tem caracteres não "*ascii* " que são complicados
de se colocar em uma busca ou substituição, nestes casos pode-se usar os
seguintes comandos:
```
"ayl ............. copia para o registro `a' o caractere sob o cursor
:%s/<c-r>a/char .. subsitui o conteúdo do registro `a' por char
```
Pode-se ainda usar esta técnica para copiar rapidamente comentários do
`bash`[^1], representados pelo caracteres `#`, em *modo
normal* usando o atalho `0yljP`.
```
0 ............... posiciona o cursor no início a linha
yl .............. copia o caractere sob o cursor
j ............... desce uma linha
P ............... cola o caractere copiado
```

[^1]: Interpretador de comandos do GNU/Linux
