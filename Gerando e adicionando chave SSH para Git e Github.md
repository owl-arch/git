

Abra seu terminal e digite o seguinte o comando para gerar uma nova chave SSH que usa o algoritmo Ed25519:

´´´bash
ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/dev-carvalho_ed25519 -C "marcos.antonio.carvalho@gmail.com"
´´´

- -o : Salve a private-key usando o novo formato OpenSSH em vez do formato PEM. Na verdade, essa opção está implícita quando você especifica o tipo de tecla como .ed25519
- -a: São os números das rodadas KDF (Key Derivation Function). Números mais altos resultam em verificação mais lenta da senha, aumentando a resistência à quebra de senha de força bruta caso a private-key seja roubada.
- -t: Especifica o tipo de chave que será criar, no nosso caso o Ed25519.
- -f: Especifique o nome do arquivo do arquivo gerado.
- -C: Uma opção para especificar um comentário. É puramente informativo e pode ser qualquer coisa.
