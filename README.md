# Softwares
- **QuickHash-GUI**: Analisa e compara hashes de arquivos, diretórios
- **AccessData FTK Imager**: Permite fazer cópias de imagens de dispositivos para modificar somente elas, mas manter o dispositivo original intacto
- **OSFMount**: Monta imagens de disco no sistema
- **WinDirStat**: Busca arquivos no disco rígido, por: tipo, tamanho etc
- **Total Commander**: Buscas "automatizadas" de diretórios e pastas
- **OSForenssics**: Multiferramentas para análise forense
- **Copiadora 666**: Copiar arquivos para outro diretório
- **WinAudit**: Informações sobre hardware e periféricos do sistema
- **NirLauncher**: Pack forense com diversas ferramentas úteis
- **RegShot**: Captura o estado atual do regedit e permite comparar dois estados e capturar diferenças
- **Autopsy**: Recuperação de arquivos deletados
- **Cryptool1**: Decodificação de cifras de César e Vigenere usando bruteforce
- **HTTrack**: Permite baixar websites e armazená-los localmente
- **DIE-engine**: Descompilação completa de programas
- **hashID | hash-identifier**: Identifica os diferentes tipos de hashes usados na encriptação de dados
- **OpenPuff**: Esteganografia em arquivos
- **QuickStego**: Esteganografia em arquivos
- **SilentEye**: Esteganografia em arquivos

---

# Criptoanálise
Dada uma mensagem, analisamos padrões para identificar qual o tipo de criptografia foi usada para criptografar a mensagem
- Há criptografias que nãos são possíveis quebrar, como SHA-256, pois não seria viável usar ataques de bruteforce, mesmo com o Hardware atual
## Tabela ASCII
### Bases numéricas
- Binário para ASCII: Mensagem codificada em binário pode ser facilmente traduzida para caracteres ASCII
Dica: 00101001010010 -> Há somente 0s e 1s
- Octal para ASCII: Mensagem codificada em octal pode ser facilmente traduzida para caracteres ASCII
Dica:  150 157 154 134 -> Agrupadas por 3 caracteres, cada grupo iniciado geralmente por 1
- Hexadecimal para ASCII: Mensagem codificada em hexadecimal pode ser facilmente traduzida para caracteres ASCII
Dica: 68 65 5C 4F 3A -> Agrupadas por 2 caracteres, existência de ABCDEF
Dica de site: https://www.unit-conversion.info

## Cifra de César e Vigenere
- Cifra de César: rotaciona o texto N vezes para direita ou esquerda
Dicas de sites: https://planetcalc.com/8572/, https://www.dcode.fr/caesar-cipher
- Cifra de Vigenere: codifica o texto dada uma key
Dicas de sites: https://www.cs.du.edu/~snarayan/crypt/vigenere.html

## Criptografias inquebráveis
Como falei, há criptografias que não são quebráveis e só seria possível por bruteforce, mas é possível tentar decifrar uma mensagem criptografada por tentativa e erro ao acertar qual critografia foi usada na mensagem
Dica de site: crypo.pw/encryptors ou http://qbarbe.free.fr/crypto/ (alternativa do crypo) ou https://cryptii.com

- Bruteforce
O bruteforce é útil quando queremos quebrar senhas, mensagens criptografadas usando Hashes como SHA-256, MD5 etc, pois exige tempo e muitas das vezes não é viável
Dica de site: https://crackstation.net

---

# Esteganografia
Ato de esconder mensagens e informações em arquivos convencionais.
- Por exemplo, quero esconder password=admin123 nos bits de uma imagem

## 1ª forma: texto em imagem simples
Essa seria a forma mais simples, menos segura de esconder dados em uma arquivos
- Dada uma imagem e um .txt com a mensagem desejada, sigamos
- Abra o cmd e digite: cd nomeDoDiretorioDosArquivos
- Digite: copy /b nomeDaImagem.extensaoImagem + arquivo.txt resultadoFinal.extensaoImagem
Após isso, a mensagem do .txt estará escondida na imagem.
Entretanto, qualquer um que abrir essa imagem em um editor hexadecimal e verificar as strings presentes verá facilmente a mensagem.
Por tal motivo, não é a forma mais adequada para esconder informações em arquivos.

## 2ª forma: metadados
Como a 1ª forma, esteganografia por metadados é extremamente básica
Consiste em esconder informações nos detalhes de um arquivo, como no nome do álbum, artista, descrição etc.


## 3ª forma: programas específicos
A melhor forma para utilizar a esteganografia é utilizando programas auxiliares, existem milhares, como por exemplo:
- OpenPuff
- QuickStego
- SilentEye
Dica: buscar usando programa auxiliar de busca em diretórios por palavras chaves ou nomes de programas que indiquem que o sujeito usava alguma técnica de esteganografia

## Sinais de uso de esteganografia:
- Tamanhos incomuns para um tipo de arquivo: Por exemplo, uma imagem com tamanho grande demais pode indicar que há algo escondido ali
- Ruídos de áudio: É possível descobrir uma mensagem ao jogar um áudio com esteganografia em um espectrograma
- Pixelização incomum de imagem: Imagens que apresentam contorno, pixelização ou distorções incomuns pode indicar que houve uma adulteração dos bits da imagem, podendo conter alguma informação ali
- Imagens em BMP: Alguns programas que realizam esteganografia salvam os arquivos finais usando a extensão .bmp
- Marcas d'água em arquivos: Ao analisar o hexadecimal e strings de um arquivo ou programa, pode indicar uma marca d'água referente ao programa que foi feita a esteganografia, ou seja, entregue de mão beijada o restante do processo

---

# Busca reversa
Útil para procurar informações a respeito de um tema sem sabe nada à respeito, isso pode ser feito de diversas formas.

## Busca por imagem
Suponhamos que temos uma imagem e queremos extrair possíveis informações sobre ela, podemos realizar os seguintes procedimentos:
- Abrir um mecanismo de busca como o próprio Google
- Selecionar o método de busca por imagem
- Anexar a imagem em questão
Logo, será retornado resultados referentes à imagem que buscamos e suas informações tais como nome, tema, contexto da imagem etc
É possível se aprofundar ainda mais na busca ao abrir links sobre a imagem, fóruns, páginas etc

## Busca ao pé da letra
Consiste em buscas que retornam apenas resultados que possuem exatamente os termos da busca.
Para ativar essa opção, faça:
- Faça uma pesquisa em um mecanismo de busca
- Vá em ferramentas
- Mude de "Todos os resultados" para "Ao pé da letra"

## Busca por um site específico
Podemos filtrar nossa busca baseado em termos que estão em um site específico.
Para isso, siga esse exemplo de busca:
site:nome-do-site.domínio:Termos para procurar

## Busca avançada do Google
O próprio google nos permite buscar de forma mais avançada, com filtros, palavras-chave, idiomas etc, utilizando:
- https://www.google.com/advanced_search

## Busca por intervalos de tempo
Outra forma interessante é ir buscando termos em determinados intervalos de tempo.
Isso é útil para sabermos exatamente qual foi a primeira aparição de uma busca em um mecanismo.

## Código fonte em publicações
Após buscar uma imagem e encontrar um site, pode ser útil buscar no código fonte da página da imagem encontrada e procurar por "date" que é justamente o termo referente à data da imagem

## Ferramenta de busca
### TinEye
Dada uma imagem, o site permite fazer uma busca e escavar toda a web, verificar e rastrear imagens online.
Além disso, é possível comparar imagem atual com a imagem real.
- Link: https://tineye.com
