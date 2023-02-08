
<div style="display: inline_block"><br>
  <img align="right" alt="git-command" style="border-radius: 50%; width: auto; height:60px;" 
     src="https://nitayneeman.gallerycdn.vsassets.io/extensions/nitayneeman/git-semantic-commit/2.0.0/1581021638044/Microsoft.VisualStudio.Services.Icons.Default">
</div>


# Convenção de mensagem para commit

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

