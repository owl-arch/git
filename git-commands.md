
<div style="display: inline_block"><br>
  <img align="left" alt="git-command" style="border-radius: 50%; width: auto; height:100px;" 
     src="https://codeguida.com/media/post_title/256px-Git_icon.svg_dMqw0Bl.png">
</div>

# GIT 

<br><br>

Repositório (Local) | Finalidade
------------------- | ----------------- 
git init *repo-local* | Criar um novo projeto de git. Criar um repositório novo em branco.
git clone https://repo-remoto | Baixar uma cópia identica da última versão do repositório no seu computador.
git status | Mostrar mudanças no diretório ***Working***. (Working Directory Status)
git add *arquivo* ou<br>**git add .** |  Incluir as alterações de um ou vários arquivos em nosso próximo commit no diretório ***Staging***<br> ou adicionar tudo ao mesmo tempo.
git commit -m *"mensagem"* | Salvar nossas alterações no ***Repositório Local***. <br>(talvez após uma tarefa ou resolução de problema específica).
git log | Motrar log dos commits no repo-local

<br>

Branch (Ramificação)         | Finalidade
---------------------------- | ----------------- 
git branch                   | Lista todas as branches 
git branch *new-branch*      | Cria uma nova branch baseada na atual 
git branch -d *branch*       | Deleta uma branch  
git checkout *branch*        | Trocar de uma ramificação para outra
git checkout -b *new-branch* | cria e faz o checkout de um novo branch.


<br>

Publish (Update) | Finalidade
---------------- | ----------------- 
git push *repo-remoto branch* <br> git push -u *origin branch* | Subir/Upload suas alterações no ***Repositório locall*** para servidor remoto <br> ou todos os arquivos.
git pull *repo-remoto*  | Descer/Download as atualizações do repositório remoto e aplica no seu computador <br> (git fetch + git merge).


<div style="display: inline_block"><br>
  <img align="left" alt="git-command" style="border-radius: 50%; width: auto; height:60px;" 
     src="https://nitayneeman.gallerycdn.vsassets.io/extensions/nitayneeman/git-semantic-commit/2.0.0/1581021638044/Microsoft.VisualStudio.Services.Icons.Default">
</div>


<br>

## Convenção de mensagem para commit

#### A mensagem do commit deve ser estruturada da seguinte forma:
> **tipo/substantivo**(escopo opcional): descrição <br><br>
> [corpo opcional] <br><br>
> [rodapé(s) opcional(is)]
<br>

Substantivo | Finalidade do substantivo da Alteração | Exemplo
---------- | ------ | -------
fix      | Uma correção de bug | fix(scope): bug in scope
feat     | Um novo recurso    | feat(parser): add ability to parse arrays <br> feat(api)!: send an email to the customer
build    | Compilação ou dependências externas | build: update dependencies
chore    | Não Afeta codigo fonte fonte ou os testes | chore(deps): update dependencies
ci       | Arquivos e scripts de configuração de CI (Integração Contínua) | 
ops      | Componentes operacionais como infra, implantação, backup, ... |
docs     | Apenas a documentação | docs: update ref docs
style    | Não afetam o significado do código | style: remove empty line
refactor | Não corrige um bug e nem adiciona um recurso | refactor: implement calculation method as recursion
perf     | Melhora o desempenho | 
test     | Adicionando testes ausentes ou corrigindo testes existentes | 
revert   | Reverter algo | 
others   | Outras não previstos | 

<br>

> Um commit que contém no rodapé opcional o texto **BREAKING CHANGE:**, ou contém o **símbolo ! depois do tipo/escopo**, introduz uma modificação que **quebra a compatibilidade da API** (isso se correlaciona com MAJOR do versionamento semântico). <br>
> Uma BREAKING CHANGE pode fazer parte de commits de qualquer tipo


<br>

