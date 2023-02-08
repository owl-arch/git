## Normatização (Especificação) da Conventional Commits
<https://www.conventionalcommits.org/pt-br/v1.0.0/>
> As palavras-chaves “DEVE” (“MUST”), “NÃO DEVE” (“MUST NOT”), “OBRIGATÓRIO” (“REQUIRED”), “DEVERÁ” (“SHALL”), “NÃO DEVERÁ” (“SHALL NOT”), “PODEM” (“SHOULD”), “NÃO PODEM” (“SHOULD NOT”), “RECOMENDADO” (“RECOMMENDED”), “PODE” (“MAY”) e “OPCIONAL” (“OPTIONAL”), nesse documento, devem ser interpretados como descrito na **RFC 2119**.

1. A mensagem de commit DEVE ser prefixado com um tipo, que consiste em um substantivo, feat, fix, etc., seguido por um escopo OPCIONAL, símbolo OPCIONAL !, e OBRIGATÓRIO terminar com dois-pontos e um espaço.

1. O tipo feat DEVE ser usado quando um commit adiciona um novo recurso ao seu aplicativo ou biblioteca.

1. O tipo fix DEVE ser usado quando um commit representa a correção de um problema em seu aplicativo ou biblioteca.

1. Um escopo PODE ser fornecido após um tipo. Um escopo DEVE consistir em um substantivo que descreve uma seção da base de código entre parênteses, por exemplo, fix(parser): .

1. Uma descrição DEVE existir depois do espaço após o prefixo tipo/escopo. A descrição é um breve resumo das alterações de código, por exemplo, fix: problema na interpretação do array quando uma string tem vários espaços.

1. Um corpo de mensagem de commit mais longo PODE ser fornecido após a descrição curta, fornecendo informações contextuais adicionais sobre as alterações no código. O corpo DEVE começar depois de uma linha em branco após a descrição.

1. Um corpo de mensagem de commit é livre e PODE consistir em infinitos parágrafos separados por uma nova linha.

1. PODE(M) ser fornecidos um ou mais rodapés, uma linha em branco após o corpo. Cada rodapé DEVE consistir em um token de palavra, seguido por um separador :<espaço> ou <espaço>#, seguido por um valor de uma string (isso é inspirado pelo git trailer convention).

1. Um token de rodapé DEVE usar - no lugar de espaços em branco, por exemplo, Acked-by (isso ajuda a diferenciar a seção de rodapé de um corpo de vários parágrafos). Uma exceção é feita para BREAKING CHANGE, que PODE também ser usado como um token.

1. O valor de um rodapé PODE conter espaços e novas linhas, e a análise (parsing) DEVE terminar quando o próximo token/separador de rodapé válido for encontrado.

1. BREAKING CHANGES DEVEM ser indicadas após o tipo/escopo de uma mensagem de commit, ou como uma entrada no rodapé.

1. Se incluída como um rodapé, uma alteração de quebra DEVE consistir no texto em maiúsculas QUEBRAR ALTERAÇÃO, seguido por dois pontos, espaço e descrição, por exemplo, BREAKING CHANGE: as variáveis de ambiente agora têm precedência sobre os arquivos de configuração.

1. Se incluído no prefixo de tipo/escopo, as BREAKING CHANGES DEVEM ser indicadas por um ! imediatamente antes de :. Se o símbolo ! for usado, BREAKING CHANGE: PODE ser omitido da seção de rodapé, e a descrição da mensagem de commit DEVE ser usada para descrever a BREAKING CHANGE.

1. Tipos diferentes de feat e fix PODEM ser usados em suas mensagens de commit, por exemplo, docs: documentos de referência atualizados

1. As unidades de informação que compõem o Conventional Commits NÃO DEVEM ser tratadas com distinção entre maiúsculas e minúsculas pelos implementadores, com exceção de BREAKING CHANGE que DEVE ser maiúscula.

1. BREAKING-CHANGE DEVE ser sinônimo de BREAKING CHANGE, quando usado como um token em um rodapé.

### Porque utilizar Conventional Commits
- Criação automatizada de CHANGELOGs.
- Determinar automaticamente alterações no versionamento semântico (com base nos tipos de commits).
- Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas.
- Disparar processos de build e deploy.
- Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits melhor estruturado.
