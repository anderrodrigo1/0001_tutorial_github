# Tutorial de Git e GitHub
> ### Principais comandos e exemplos para consultas rapidas no dia a dia
>---

A ideia desse material e ter um banco de conhecimento sobre o `Git e GitHub`.
Colaborando assim com amigos e parceiros que sempre me perguntam como utilizar essa tecnologia para historificar, organizar e manter uma copia segura de seus projetos pessoais ou empresariais, e ainda garantir o versionamento.
Apessar de comunmente essa tecnologia ser usada para projetos de desenvolvimento de software e análise/estudos de dados, nada empede que a mesma seja usada em projetos diversos.

<br/>

<div align="center">
    <img src="git_e_github.png" >
    <b><h2>Git e GitHub<h2><b>
</div>

> ### Primeiro ponto importante é a diferença entre elas
>---
<p>
 Git: Tecnologia que está no backend, é a inteligencia com toda a estrutura de pastas e comandos 

<p>

 GitHub: Tecnologia que está no frontend (web), é uma rede social que cria uma camanda de apresentação amigavel e conecta pessoas e projetos

 - ### Como instalar Git:

    *   Na sua máquina, Notebook ou desktop indiferente do sistema operacional, Linux, Mac ou Windowns, acesse https://git-scm.com/downloads baixe a versão para seu sistema operacional e faça a instalação

 *  ### Como criar uma conta no GitHub:

    *   No seu navegador de preferencia acesse https://github.com/ e crie uma conta utilizando seu e-mail, na sequencia entre em seu e-mail e confirme seu cadastro

 *  ### Instale um editor de texto

    * Recomendo também a intsalação de um editor de texto poderoso, que tenha uma boa integração com o Git, no meu caso uso o VS Code, que pode ser baixado em https://code.visualstudio.com/ para Linux, Mac ou Windowns


 *  ### Vamos a diversão:

    - Crie uma pasta com o nome do seu projeto e dentro dela faremos nossa brincadeira
    - Na linha de comando do seu sistema operacional(se você usa Windows abra o executar e digite `cmd` e de enter, se você usa Linux... kkk)
    - Navegue até a pasta criada anteriomente

### Comandos Git:

*   Adicionar projeto ao Git:
<span style="color:lightblue" >Inicia projeto no Git, criando a pasta `.git` e inicializa o monitoramento de verões do projeto
</span>

```sh
        git init
```

*   Cria usuário: 
<span style="color:lightblue" >Local (PC puclico)
</span>

```sh
        git config user.name "Anderson"
```
```sh
        git config user.email "anderrodrigo@gmail.com"
```

*   Cria usuário: 
<span style="color:lightblue" >Global (PC pessoal)
</span>

```sh
        git config --global user.name "Anderson"
```
```sh
        git config --global user.email "anderrodrigo@gmail.com"
```

*   Verificar status do projeto:
<span style="color:lightblue" > Comando recorrente, usado para saber se existem pendencias </span>

```sh
        git status
```

*   Adicionar arquivo no monitoramento do Git:
<span style="color:lightblue" > Para adicionar todos utilizar um "." no lugar do nome_do_arquivo </span>

```sh
        git add nome_do_arquivo
```

*   Cria ponto de controle do projeto (Versão): 
<span style="color:lightblue" > O "-m" serve para passar paramentro de mensagem </span>

```sh
        git commit -m "Meu primeiro comite" 
```

<span style="color:lightblue" >     </span>
*   Verificar os log das alterações: 
```sh
        git log
```

<span style="color:lightblue" >     </span>
*   Mostra os ultimos N(=10) logs: 
```sh
        git log -10
```

<span style="color:lightblue" >     </span>
*   Agrupa evento em uma unica linha: 
```sh
        git log --oneline
```

<span style="color:lightblue" >     </span>
*   Procura eventos anterios a data especificada: 
```sh
        git log --before="2021-04-02"
```

<span style="color:lightblue" >     </span>
*   Procura eventos após a data especificada: 
```sh
        git log --after="2021-04-02"
```

<span style="color:lightblue" >     </span>
*   Procura eventos que ocorreram até 10 dias atrás
```sh
        git log --since="10 day ago"
```

<span style="color:lightblue" >     </span>
*   Procura por autor
```sh
        git log --author="ander" 
```

*   Navegando nas versões: 
<span style="color:lightblue" >Vai para a versão solicitada, que pode ser localizada com o comando `git log --oneline` </span>

```sh
        git checkout numero_hash_desejado
```

*   Volta para a ultima versão: 
<span style="color:lightblue" >     </span>

```sh
        git checkout master
```

*   Renomear arquivos: 
<span style="color:lightblue" >   A grande valtagem de fazer ee processos usando o Git é que ele vai garantir a integridade das versões, sem percisar usar o comando `git add nome_do_arquivo` para readicionar o arquivo no projeto </span>

```sh
        git mv programa.py prog.py
```

*   Removendo arquivos: 
<span style="color:lightblue" >     </span>

```sh
        git rm prog.py
```

*   Compara versão atual com a que está em desenvolvimento: 
<span style="color:lightblue" >     </span>

```sh
        git diff --staged
```

*   Compara versão atual com hash escolhido: 
<span style="color:lightblue" >     </span>

```sh
        git diff hash_do_commit
```

*   Compara versões inicial ".." final escolhida: 
<span style="color:lightblue" >   Cuida para não inverter a ordem dos hash  </span>

```sh
       git diff hash_inicial..Hash_final
```


*   Alterar mensagem do ultimo commit: 
<span style="color:lightblue" >  "No exemplo você poderia ter colocado um 0 a mais: atualização de versão do calculo de desconto para 60%"   </span>

```sh
    git commit --amend -m "atualização de versão do calculo de desconto para 6%"    
```

*   Altera o status do arquivo: 
<span style="color:lightblue" >  Quando você desiste de fazer o commit do arquivo, mas já adiciou para commit   </span>

```sh
      git restore --staged prog.py  
```

*   Restaurando para o seu repositório local a ultima versão comitada: 
<span style="color:lightblue" >  Nesse exemplo você deu aquela bangunçada no arquivo que estava trabalhando e a melhor alternative e pegar uma nova copia da produção para voltar a trabalhar   </span>

```sh
        git checkout prog.py
```

*   Restaurando para o seu repositório local a ultima versão comitada de todos os arquivos: 
<span style="color:lightblue" >  Volta versão dos arquivos do ultimo ponto de controle para o seu repositório local(ultimo commit)   </span>

```sh
        git reset HEAR --hard
```

*   Restaurando para o seu repositório local a penultima versão comitada de todos os arquivos: 
<span style="color:lightblue" >  Volta versão dos arquivos do ultimo ponto de controle para o seu repositório local(penultimo commit)   </span>

```sh
       git reset HEAR^ --hard
```

<BR />

> ### Estruturas de ramos(Branch)
> ----

<BR />

*   Saber em que branch você esta trabalhando: 
<span style="color:lightblue" >     </span>

```sh
        git branch
```

*   Cria um novo ramo de trabalho: 
<span style="color:lightblue" >     </span>

```sh
        git branch func_teste
```

*   Alterar Branch: 
<span style="color:lightblue" >     </span>

```sh
        git branch checkout func_teste
```

*   Apaga o branch, "-D" maiúsculo força apagar: 
<span style="color:lightblue" >     </span>

```sh
        git branch -d func_teste 
```


*   Adiciona no final do branch master a func_teste: 
<span style="color:lightblue" >     </span>

```sh
        git merge func_teste
```

*   Criar novo branch já mudando para ele: 
<span style="color:lightblue" >     </span>

```sh
        git checkout -b func_teste3
```

*   Adiciona no ponto de criação do branch master a func_teste e atualiza mudanças feitas posteriormente: 
<span style="color:lightblue" >     </span>

```sh
        git rebase func_teste2
```

*   Faz uma copia do repositório indicado: 
<span style="color:lightblue" >     </span>

```sh
        git clone ..\001_projeto\ .
```


*   Carrega novas atualizações de branch original, mas não faz merge: 
<span style="color:lightblue" >     </span>

```sh
        git fetch
```


*   Aplica mudanças carragadas do branch original: 
<span style="color:lightblue" >     </span>

```sh
        git rebase
```


*   Carrega e Aplica as mudanças em um passo, fetch+rebase: 
<span style="color:lightblue" >     </span>

```sh
        git pull
```


*   Cria repositório bare: 
<span style="color:lightblue" >  Esse tipo de repositório possibilita o trabalho em conjunto por vários committers   </span>

```sh
        git init --bare 
```


*   Aplica mudanças do repositório clone no master original: 
<span style="color:lightblue" >     </span>

```sh
        git push
```


*   Cria um marcador de versão, usado para fazer entregáveis - Tag não pode sofrer commit: 
<span style="color:lightblue" >     </span>

```sh
        git tag v1.0
```


*   Mostra tag do projeto: 
<span style="color:lightblue" >     </span>

```sh
        git tag
```


*   Publica no repositório remoto: 
<span style="color:lightblue" >     </span>

```sh
        git push origin v1.0
```

<BR />

> ### Utilizando o GitHub
> ----


* Criar uma conta no github.com
* Criar um projeto no github.com

> Definir um repositorio no GitHub

*   Criar arquivo de readne.md: 
<span style="color:lightblue" >  (Windows)   </span>

```sh
        echo "# 0001_tutorial_github" > README.m
```


*   Criar pasta com o mesmo nome do projeto : 
<span style="color:lightblue" >   (Windows)  </span>

```sh
    md 0001_tutorial_github    
```


*   Iniciar projeto no Git: 
<span style="color:lightblue" >     </span>

```sh
        git init 
```


*   Adiciona arquivo no projeto para versionamento: 
<span style="color:lightblue" >     </span>

```sh
        git add README.md
```


*   Criar ponto de contro de versão: 
<span style="color:lightblue" >     </span>

```sh
        git commit -m "Criação do arquivo readme.md"
```

*   Link repositório remoto do GitHub ao projeto local do Git: 
<span style="color:lightblue" >     </span>

```sh
git remote add origin https://github.com/anderrodrigo1/0001_tutorial_github.git 
```

*   Sincroniza os repositórios local e remoto: 
<span style="color:lightblue" >     </span>

```sh
        git push -u origin master
```

*   : 
<span style="color:lightblue" >     </span>

```sh
        git add GitHub - "Principais GitHub - Principais comandos.txt"
```

*   Crio ponto de contro da versão: 
<span style="color:lightblue" >     </span>

```sh
        git commit -m "Adicionando o arquivo GitHub - Principais comandos" 
```

*   Sincroniza os repositórios local e remoto: 
<span style="color:lightblue" >     </span>

```sh
        git push -u origin master
```

*   Grava credencias para esse projeto local - para global --global: 
<span style="color:lightblue" >     </span>

```sh
        git config credential.helper store 
```

*   desfaz o ultimo commit mantendo o histórico: 
<span style="color:lightblue" >     </span>

```sh
        git revert hash_do_commit 
```

*   desfaz o numero de commits N(=3) solicitado sem manter históricos: 
<span style="color:lightblue" >     </span>

```sh
        git reset HEAD~3
```






Por enquanto é isso galera.

by Anderson R M Jesus - anderrodrigo@gmail.com


--------------

> ###

### Nota:

*   Se tiver sugestões de melhorias ou duvidas não exite em entrar em contato, deixando um comentário, issues ou via e-mail anderrodrigo@gmail.com
