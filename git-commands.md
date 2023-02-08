
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

