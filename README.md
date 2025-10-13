# Computação Forense

---

## Softwares

- **QuickHash-GUI**: Analisa e compara hashes de arquivos e diretórios.
- **AccessData FTK Imager**: Permite criar cópias de imagens de dispositivos, preservando o dispositivo original.
- **OSFMount**: Monta imagens de disco no sistema.
- **WinDirStat**: Busca arquivos no disco rígido por tipo, tamanho, etc.
- **Total Commander**: Realiza buscas automatizadas de diretórios e pastas.
- **OSForensics**: Multiferramenta para análise forense.
- **Copiadora 666**: Copia arquivos para outro diretório.
- **WinAudit**: Coleta informações sobre hardware e periféricos do sistema.
- **NirLauncher**: Pacote forense com diversas ferramentas úteis.
- **RegShot**: Captura o estado atual do registro e permite comparar dois estados, identificando diferenças.
- **Autopsy**: Recuperação de arquivos deletados.
- **Cryptool1**: Decodificação de cifras de César e Vigenere usando bruteforce.
- **HTTrack**: Baixa websites e os armazena localmente.
- **DIE-engine**: Descompilação completa de programas.
- **hashID / hash-identifier**: Identifica tipos de hashes usados na criptografia de dados.
- **OpenPuff**: Esteganografia em arquivos.
- **QuickStego**: Esteganografia em arquivos.
- **SilentEye**: Esteganografia em arquivos.
- **ExifTool**: Leitura e extração de metadados de arquivos.

---

# Criptoanálise

Dada uma mensagem, analisamos padrões para identificar qual tipo de criptografia foi utilizada.  
**Observação:** algumas criptografias, como SHA-256, não são viáveis de quebrar com bruteforce mesmo com hardware moderno.

### Tabela ASCII

#### Bases numéricas

- **Binário para ASCII**: Mensagem codificada em binário pode ser traduzida para caracteres ASCII.  
  *Dica:* `00101001 010010` → contém apenas 0s e 1s.
  
- **Octal para ASCII**: Mensagem codificada em octal pode ser convertida para caracteres ASCII.  
  *Dica:* `150 157 154 134` → agrupadas por 3 caracteres, iniciando geralmente por 1.

- **Hexadecimal para ASCII**: Mensagem codificada em hexadecimal pode ser convertida para ASCII.  
  *Dicas:* `68 65 5C 4F 3A` → agrupadas por 2 caracteres, presença de A-F.  
  *Site útil:* [Unit Conversion](https://www.unit-conversion.info)

---

### Cifras de César e Vigenere

- **Cifra de César**: Rotaciona o texto N vezes para a direita ou esquerda.  
  *Sites de referência:* [PlanetCalc](https://planetcalc.com/8572/), [dCode](https://www.dcode.fr/caesar-cipher)

- **Cifra de Vigenere**: Codifica o texto usando uma chave (key).  
  *Site de referência:* [CS DU - Vigenere](https://www.cs.du.edu/~snarayan/crypt/vigenere.html)

---

### Criptografias inquebráveis

- Algumas criptografias só podem ser quebradas via bruteforce, o que muitas vezes não é viável.  
- É possível tentar decifrar mensagens por tentativa e erro, descobrindo a criptografia usada.  
  *Sites úteis:*  
  - [Crypo](https://crypo.pw/encryptors)  
  - [QBarbe](http://qbarbe.free.fr/crypto/)  
  - [Cryptii](https://cryptii.com)

---

### Bruteforce

- Útil para quebrar senhas ou mensagens criptografadas com hashes como SHA-256 e MD5.  
- Exige tempo significativo e pode não ser viável na prática.  
  *Site útil:* [CrackStation](https://crackstation.net)

---

# Esteganografia

**Definição:** Técnica de esconder mensagens e informações em arquivos convencionais.  
Exemplo: esconder `password=admin123` nos bits de uma imagem.

## 1. Texto em imagem simples

- Forma mais simples e menos segura de esteganografia.
- Passos:
  1. Abra o CMD e vá até o diretório dos arquivos:  
     ```cmd
     cd nomeDoDiretorioDosArquivos
     ```
  2. Combine imagem e arquivo de texto:  
     ```cmd
     copy /b nomeDaImagem.extensaoImagem + arquivo.txt resultadoFinal.extensaoImagem
     ```
- Limitações: qualquer pessoa pode abrir o arquivo em um editor hexadecimal e ler a mensagem.

## 2. Metadados

- Esconder informações nos detalhes do arquivo, como nome do álbum, artista, descrição, etc.
- Método básico e pouco seguro.

## 3. Programas específicos

- Utilizar softwares dedicados aumenta segurança e complexidade.  
- Exemplos:
  - OpenPuff
  - QuickStego
  - SilentEye

- **Dica:** use buscas por palavras-chave ou nomes de programas em diretórios para detectar sinais de esteganografia.

## Sinais de uso de esteganografia

- Tamanhos incomuns de arquivos (ex.: imagens grandes podem indicar dados ocultos).  
- Ruídos em áudios (pode revelar mensagens em espectrogramas).  
- Pixelização incomum em imagens.  
- Imagens em `.bmp` (alguns programas salvam nesse formato).  
- Marcas d’água ou padrões no hexadecimal indicando manipulação.

---

# Busca reversa

**Definição:** Técnica para coletar informações sobre um tema sem conhecimento prévio.  

## Busca por imagem

- Passos:
  1. Abra um mecanismo de busca (ex.: Google).  
  2. Selecione “busca por imagem” e anexe a imagem.  
  3. Analise os resultados: nome, contexto, links, fóruns, etc.

## Busca ao pé da letra

- Retorna resultados que contêm exatamente os termos pesquisados.  
- Para ativar no Google: Ferramentas → “Ao pé da letra”.

## Busca por site específico

- Filtra resultados de um site específico:  
  ```text
  site:nome-do-site.domínio Termos para procurar
  ```
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
