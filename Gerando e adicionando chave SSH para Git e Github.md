

Abra seu terminal e digite o seguinte o comando para gerar uma nova chave SSH que usa o algoritmo Ed25519:

```bash
ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/id_ed25519 -C "marcos.antonio.carvalho@gmail.com"
```

Não coloque senha!

```bash
Generating public/private ed25519 key pair.
Created directory '/root/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /root/.ssh/id_ed25519
Your public key has been saved in /root/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX marcos.antonio.carvalho@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
| .    .o.+E.     |
|. .   =oo  o     |
|.o   +.=...      |
| .o   +.o.       |
|.  +.o..S        |
|. o.Xo+ o        |
| o.* @.o .       |
|.o .* =..        |
|.o+  o++         |
+----[SHA256]-----+
```

- -o : Salve a private-key usando o novo formato OpenSSH em vez do formato PEM. Na verdade, essa opção está implícita quando você especifica o tipo de tecla como .ed25519
- -a: São os números das rodadas KDF (Key Derivation Function). Números mais altos resultam em verificação mais lenta da senha, aumentando a resistência à quebra de senha de força bruta caso a private-key seja roubada.
- -t: Especifica o tipo de chave que será criar, no nosso caso o Ed25519.
- -f: Especifique o nome do arquivo do arquivo gerado.
- -C: Uma opção para especificar um comentário. É puramente informativo e pode ser qualquer coisa.


### Adicionando sua chave ao agente SSH
- Chave Privada: ~/.ssh/dev-carvalho_ed25519
- Chave Pública: ~/.ssh/dev-carvalho_ed25519.pub
- Lembre-se sempre que sua chave pública é a que você copia para o host alvo para autenticação.

#### Antes de adicionar sua nova chave privada ao agente SSH, certifique-se de que o agente SSH esteja rodando
```bash
eval "$(ssh-agent -s)"
```
```bash
Agent pid 5948
```

#### Adicionar sua nova Chave Privada ~/.ssh/dev-carvalho_ed25519 ao agente SSH
```bash
ssh-add  ~/.ssh/id_ed25519
```
```bash
Enter passphrase for /root/.ssh/dev-carvalho_ed25519:
Identity added: /root/.ssh/dev-carvalho_ed25519 (marcos.antonio.carvalho@gmail.com)
```

### Adicione a Chave Pública no Github
XXXXXXXXXXXXXX
XXXXXXXXXXXXXX
XXXXXXXXXXXXXX

#### Teste utilizando o endereçamento para git para ssh
```bash
git clone git@github.com:dev-carvalho/teste.git
```

<br>

#### Referência:
- https://rogerioadris.medium.com/atualize-sua-chave-ssh-para-ed25519-8cf5a7d4b18
