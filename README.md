# Guia de Computação Forense

# Sumário

- [1. Ferramentas](#1-ferramentas)
  - [1.2 Softwares](#12-softwares)
    - [QuickHash-GUI](#quickhash-gui)
    - [AccessData FTK Imager](#accessdata-ftk-imager)
    - [OSFMount](#osfmount)
    - [WinDirStat](#windirstat)
    - [Total Commander](#total-commander)
    - [OSForensics](#osforensics)
    - [WinAudit](#winaudit)
    - [NirLauncher](#nirlauncher)
    - [RegShot](#regshot)
    - [Recuva](#recuva)
    - [Disk Drill](#disk-drill)
    - [Autopsy](#autopsy)
    - [Cryptool1](#cryptool1)
    - [DIE-engine](#die-engine)
    - [hashID / hash-identifier](#hashid--hash-identifier)
    - [OpenPuff](#openpuff)
    - [QuickStego](#quickstego)
    - [SilentEye](#silenteye)
    - [MultiObfuscator](#multiobfuscator)
    - [ExifTool](#exiftool)
    - [Crunch](#crunch)
    - [HashCat](#hashcat)
    - [WordListCompiler](#wordlistcompiler)
    - [PDF2TextPilot](#pdf2textpilot)
    - [Cain & Abel](#cain--abel)
    - [PasswareKit](#passwarekit)
    - [Ophcrack](#ophcrack)
    - [Emsisoft Emergency Kit](#emsisoft-emergency-kit)
    - [Copiadora 666](#copiadora666)
  - [1.3 Ferramentas Online](#13-ferramentas-online)
    - [1.3.1 Hashes e Criptoanálise](#131-hashes-e-criptoanálise)
    - [1.3.2 Cifras e Criptografia](#132-cifras-e-criptografia)
    - [1.3.3 Metadados e Análise de Arquivos](#133-metadados-e-análise-de-arquivos)
    - [1.3.4 Esteganografia Online](#134-esteganografia-online)
    - [1.3.5 Busca Reversa e OSINT](#135-busca-reversa-e-osint)
    - [1.3.6 Análise de Arquivos e Binários](#136-análise-de-arquivos-e-binários)
    - [1.3.7 Redes e Tráfego](#137-redes-e-tráfego)
    - [1.3.8 Utilitários Gerais](#138-utilitários-gerais)
- [2. Criptoanálise](#2-criptoanálise)
  - [2.1 Tabela ASCII](#21-tabela-ascii)
    - [Binário → ASCII](#binário-→-ascii)
    - [Octal → ASCII](#octal-→-ascii)
    - [Hexadecimal → ASCII](#hexadecimal-→-ascii)
  - [2.2 Cifras de César e Vigenere](#22-cifras-de-césar-e-vigenere)
  - [2.3 Criptografias inquebráveis](#23-criptografias-inquebráveis)
    - [2.3.1 Bruteforce, Dicionários e Rainbow Tables](#231-bruteforce-dicionários-e-rainbow-tables)
- [3. Esteganografia](#3-esteganografia)
  - [3.1 Texto em imagem simples](#31-texto-em-imagem-simples)
  - [3.2 Alterar o tipo de extensão do arquivo](#32-alterar-o-tipo-de-extensão-do-arquivo)
  - [3.3 Metadados](#32-metadados)
  - [3.4 Spammimic](#spammimic)
  - [3.5 Programas específicos](#33-programas-específicos)
  - [3.6 Sinais de uso de esteganografia](#34-sinais-de-uso-de-esteganografia)
- [4. Busca reversa](#4-busca-reversa)
  - [4.1 Busca por imagem](#41-busca-por-imagem)
  - [4.2 Busca ao pé da letra](#42-busca-ao-pé-da-letra)
  - [4.3 Busca por site específico](#43-busca-por-site-específico)
  - [4.4 Busca avançada do Google](#44-busca-avançada-do-google)
  - [4.5 Busca por intervalos de tempo](#45-busca-por-intervalos-de-tempo)
  - [4.6 Código fonte em publicações](#46-código-fonte-em-publicações)
  - [4.7 Ferramenta de busca — TinEye](#47-ferramenta-de-busca-—-tineye)
- [5. Engenharia Reversa](#5-engenharia-reversa)
- [6. Lab Forense](#5-lab-forense)

---

# 1. Ferramentas
## 1.2 Softwares

- **QuickHash-GUI**: Analisa e compara hashes de arquivos e diretórios.
- **AccessData FTK Imager**: Permite criar cópias de imagens de dispositivos, preservando o dispositivo original.
- **OSFMount**: Monta imagens de disco no sistema.
- **WinDirStat**: Busca arquivos no disco rígido por tipo, tamanho, etc.
- **Total Commander**: Realiza buscas automatizadas de diretórios e pastas.
- **OSForensics**: Multiferramenta para análise forense.
- **WinAudit**: Coleta informações sobre hardware e periféricos do sistema.
- **NirLauncher**: Pacote forense com diversas ferramentas úteis.
- **RegShot**: Captura o estado atual do registro e permite comparar dois estados, identificando diferenças.
- **Recuva**: Recuperação de arquivos deletados de um dispositivo de armazenamento
- **Disk Drill**: Recuperação de arquivos deletados de um dispositivo de armazenamento
- **Autopsy**: Análise forense de arquivos, diretórios e dispositivos de armazenamento.
- **Cryptool1**: Decodificação de cifras de César e Vigenere usando bruteforce.
- **DIE-engine**: Descompilação completa de programas.
- **hashID / hash-identifier**: Identifica tipos de hashes usados na criptografia de dados.
- **OpenPuff**: Esteganografia em arquivos.
- **QuickStego**: Esteganografia em arquivos.
- **SilentEye**: Esteganografia em arquivos.
- **MultiObfuscator**: Corrompe e criptografa arquivos de forma que só serão recuperados ao inserir até 4 senhas no arquivo.
- **ExifTool**: Leitura e extração de metadados de arquivos.
- **Crunch**: Gerador de wordlists
- **HashCat**: Quebra de hashes usando wordlists
- **WordListCompiler**: Transforma um arquivo .txt em wordlist
- **PDF2TextPilot**: Converte PDF em arquivo .txt
- **Cain & Abel**: Cracker de senhas locais
- **PasswareKit**: Cracker de senhas de arquivos específicos
- **Ophcrack**: Cracker de senhas locais baseado em Rainbow tables
- **Emsisoft Emergency Kit**: Scanner portable de arquivos, processos, chaves de registro e histórico de ameaças conhecidas a fim de identificar possíveis softwares maliciosos.
- **Copiadora 666**: Copia arquivos para outro diretório.

## 1.3 Ferramentas Online
### 1.3.1 Hashes e Criptoanálise
- [CrackStation](https://crackstation.net): Quebra de hashes MD5, SHA1, SHA256 etc., usando grandes tabelas de lookup.
- [Hashes.com](https://hashes.com/): Identifica e descriptografa hashes; pesquisa colaborativa e upload para análise.
- [OnlineHashCrack](https://www.onlinehashcrack.com): Serviço de recuperação de senhas via GPU/cluster (WPA, Office, ZIP etc.).
- [MD5Online](https://www.md5online.org): Decodificador e gerador de hashes MD5.
- [dCode Hash Identifier](https://www.dcode.fr/hash-identifier): Identificação automática de tipos de hash.
- [CyberChef](https://gchq.github.io/CyberChef/): Laboratório online para codificação, decodificação, hashing, compressão, criptografia, esteganografia e mais.
- [Base64 Decode](https://www.base64decode.org/): Decodificador e codificador Base64.
- [String Functions](https://www.string-functions.com/): Conversões, transformações e análises de texto codificado.

### 1.3.2 Cifras e Criptografia
- [dCode.fr](https://www.dcode.fr): Portal de criptologia, decodificação, cifras clássicas, conversões entre bases, análise de frequência.
- [Cryptii](https://cryptii.com): Interface modular para decodificação de textos em diversas bases e cifras.
- [Crypo (Alt 1)](https://s3curity.info/.external/crypo/): Códigos de substituição e cifras simples com decodificador automático.
- [Crypo (Alt 2)](http://qbarbe.free.fr/crypto/): Códigos de substituição e cifras simples com decodificador automático.
- [PlanetCalc](https://planetcalc.com): Ferramentas matemáticas e de criptografia (Vigenère, César, etc).
- [Boxentriq Code-Breaking Tools](https://www.boxentriq.com/code-breaking): Decodificadores automáticos e análises de frequência.
- [Cipher Identifier](https://www.guballa.de/substitution-solver): Identifica e resolve cifras de substituição por frequência e padrões.

### 1.3.3 Metadados e Análise de Arquivos
- [ExifTool Online / exif.tools](https://exif.tools/): Leitura de metadados EXIF/IPTC/XMP.
- [Metadata2Go](https://www.metadata2go.com/): Extração de metadados de fotos, vídeos, PDFs e áudios.
- [FotoForensics](https://fotoforensics.com/): Error Level Analysis (ELA) para detectar manipulação de imagens.
- [Forensically](https://29a.ch/photo-forensics/): Conjunto completo de ferramentas forenses para imagens.
- [Jeffrey’s Image Metadata Viewer](https://exif.regex.info/exif.cgi): Leitor detalhado de EXIF.

### 1.3.4 Esteganografia Online
- [StegOnline](https://stegonline.georgeom.net/): Análise bit a bit de imagens e extração de mensagens ocultas (LSB, camadas, offset).
- [Aperi'Solve](https://www.aperisolve.com): Detecção avançada de esteganografia em imagens.
- [Mobilefish Steganography](https://www.mobilefish.com/services/steganography/steganography.php): Ocultar e recuperar texto em imagens BMP/PNG.

### 1.3.5 Busca Reversa e OSINT
- [TinEye](https://tineye.com): Busca reversa por imagem.
- [Yandex Images](https://yandex.com/images/): Busca reversa alternativa para imagens.
- [Bing Visual Search](https://www.bing.com/visualsearch): Busca reversa de imagens com resultados diferentes.
- [Google Advanced Search](https://www.google.com/advanced_search): Busca avançada com filtros por idioma, domínio, data etc.
- [Whois Lookup (ICANN)](https://lookup.icann.org/en): Identifica proprietário e registro de domínios.
- [VirusTotal](https://www.virustotal.com): Análise de arquivos e URLs contra malware.
- [URLVoid](https://www.urlvoid.com/): Verificação de reputação de domínios e blacklist.
- [HackerTarget Tools](https://hackertarget.com/ip-tools/): Conjunto de ferramentas OSINT para IP, domínio e subdomínios.

### 1.3.6 Análise de Arquivos e Binários
- [HexEd.it](https://hexed.it/): Editor hexadecimal online.
- [File Signatures (filesignatures.net)](https://www.filesignatures.net/): Identificação de arquivos via magic numbers.
- [Strings Online](https://emn178.github.io/online-tools/strings.html): Extrai strings ASCII/Unicode de binários.
- [Hybrid Analysis](https://www.hybrid-analysis.com): Sandbox para análise dinâmica de arquivos e scripts.
- [Any.Run](https://app.any.run/): Sandbox interativo para executar amostras maliciosas.
- [Intezer Analyze](https://analyze.intezer.com/): Análise de DNA de código e detecção de malware.

### 1.3.7 Redes e Tráfego
- [PacketTotal](https://packettotal.com): Upload e análise de arquivos `.pcap`.
- [Wireshark Sample Captures](https://wiki.wireshark.org/SampleCaptures): Repositório de capturas de tráfego para estudo.
- [DNSDumpster](https://dnsdumpster.com): Mapeamento de subdomínios e infraestrutura de um domínio.
- [Shodan](https://www.shodan.io): Busca de dispositivos conectados à internet.
- [MXToolbox](https://mxtoolbox.com): Ferramentas de diagnóstico de DNS, IPs e servidores.

### 1.3.8 Utilitários Gerais
- [Unit Conversion](https://www.unit-conversion.info): Conversões de unidades e bases numéricas.
- [Regex101](https://regex101.com): Teste e depuração de expressões regulares.
- [JSONLint](https://jsonlint.com): Validação e formatação de JSONs.
- [CodeBeautify](https://codebeautify.org): Conversão, formatação e decodificação rápida de dados.

---

# 2. Criptoanálise

Dada uma mensagem, analisamos padrões para identificar qual tipo de criptografia foi utilizada.  
**Observação:** algumas criptografias, como SHA-256, não são viáveis de quebrar com bruteforce mesmo com hardware moderno.

### 2.1 Tabela ASCII

#### Bases numéricas

- **Binário para ASCII**: Mensagem codificada em binário pode ser traduzida para caracteres ASCII.  
  *Dica:* `00101001 01001010` → contém apenas 0s e 1s.
  
- **Octal para ASCII**: Mensagem codificada em octal pode ser convertida para caracteres ASCII.  
  *Dica:* `150 157 154 134` → agrupadas por 3 caracteres, iniciando geralmente por 1.

- **Hexadecimal para ASCII**: Mensagem codificada em hexadecimal pode ser convertida para ASCII.  
  *Dicas:* `68 65 5C 4F 3A` → agrupadas por 2 caracteres, presença de A-F.  
  *Site útil:* [Unit Conversion](https://www.unit-conversion.info)

---

### 2.2 Cifras de César e Vigenere

- **Cifra de César**: Rotaciona o texto N vezes para a direita ou esquerda.  
  *Sites de referência:* [PlanetCalc](https://planetcalc.com/8572/), [dCode](https://www.dcode.fr/caesar-cipher)

- **Cifra de Vigenere**: Codifica o texto usando uma chave (key).  
  *Site de referência:* [CS DU - Vigenere](https://www.cs.du.edu/~snarayan/crypt/vigenere.html)

---

### 2.3 Criptografias inquebráveis

- Algumas criptografias só podem ser quebradas via bruteforce, o que muitas vezes não é viável.  
- É possível tentar decifrar mensagens por tentativa e erro, descobrindo a criptografia usada.  
  *Sites úteis:*  
  - [Crypo](https://crypo.pw/encryptors)  
  - [QBarbe](http://qbarbe.free.fr/crypto/)  
  - [Cryptii](https://cryptii.com)


#### 2.3.1 Bruteforce, dicionários e rainbow tables
##### Bruteforce
- Um ataque por força bruta tenta descobrir uma senha testando todas as combinações possíveis de caracteres até encontrar a que gera o mesmo hash ou corresponde ao segredo. É um método puramente de tentativa e erro, sem usar conhecimento prévio sobre padrões de senhas.
- O número de combinações cresce exponencialmente com o comprimento e o alfabeto usado. Senhas maiores e que misturam conjuntos amplos de caracteres (minúsculas, maiúsculas, números, símbolos) aumentam drasticamente a complexidade de busca, tornando inviável testar todas as combinações mesmo com hardware muito rápido.
- Além disso, funções de hashing lentas (p. ex. bcrypt, scrypt, Argon2) reduzem drasticamente a taxa de tentativas por segundo, ampliando ainda mais o tempo necessário para um brute-force bem-sucedido.

##### Dicionários
- Um ataque de dicionário tenta senhas usando listas de palavras e combinações possíveis, as chamadas wordlists, em vez de gerar todas as combinações possíveis. As listas incluem palavras do idioma, palavras mais comuns (ex: senha123, P@ssw0rd), variações leet (3→e, 4→a), frases comuns, nomes próprios e senhas vazadas.
- Em vez de percorrer todo o espaço combinatório, sem "garantias" por assim dizer, usamos um arquivo chamado “dicionário” com entradas ordenadas por probabilidade e testa cada entrada contra o hash ou sistema.
- Normalmente o ataque inclui etapas de transformação (mutações): capitalização, acréscimo de números, substituições e concatenações, para cobrir variações humanas comuns.

##### Rainbow Tables
- Rainbow tables são tabelas pré-computadas que mapeiam hashes para possíveis senhas, através de pontos intermediários em cadeias reduzidas, permitindo recuperar senhas a partir de hashes sem ter que recalcular o hash para cada tentativa individual em tempo real.
- Em vez de armazenar todas as combinações de senha → hash, gera-se cadeias reduzidas (hash → redução → novo hash → ...) e armazena-se somente o início e o fim da cadeia. Ao procurar um hash alvo, o atacante aplica reduções e buscas nas tabelas para localizar qual cadeia pode conter a senha original, e a partir daí reconstrói a cadeia para encontrar a senha correspondente. Isso economiza espaço em troca de tempo e complexidade de reconstrução.

---

# 3. Esteganografia

**Definição:** Técnica de esconder mensagens e informações em arquivos convencionais.  
Exemplo: esconder `password=admin123` nos bits de uma imagem.

## 3.1 Texto em imagem simples
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

## 3.2 Alterar o tipo de extensão do arquivo
- Assim como a anterior, extremamente fácil de descobrir
- Consiste em alterar a extensão de um arquivo
- Ex: Uma imagem originalmente é de extensão .png e você altera para algo como .reg, .bat ou qualquer outra diferente

## 3.3 Metadados

- Esconder informações nos detalhes do arquivo, como nome do álbum, artista, descrição, etc.
- Método básico e pouco seguro.

## 3.4 Spammimic
- Permite esconder uma mensagem em um texto semelhante a um Spam ou chave PGP
- Acesse o site em: [Spammimic](https://www.spammimic.com)

## 3.5 Programas específicos

- Utilizar softwares dedicados aumenta segurança e complexidade.  
- Exemplos:
  - OpenPuff
  - QuickStego
  - SilentEye

- **Dica:** use buscas por palavras-chave ou nomes de programas em diretórios para detectar sinais de esteganografia.

## 3.6 Sinais de uso de esteganografia

- Tamanhos incomuns de arquivos (ex.: imagens grandes podem indicar dados ocultos).  
- Ruídos em áudios (pode revelar mensagens em espectrogramas).  
- Pixelização incomum em imagens.  
- Imagens em `.bmp` (alguns programas salvam nesse formato).  
- Marcas d’água ou padrões no hexadecimal indicando manipulação.

---

# 4. Busca reversa

**Definição:** Técnica para coletar informações sobre um tema sem conhecimento prévio.  

## 4.1 Busca por imagem

- Passos:
  1. Abra um mecanismo de busca (ex.: Google).  
  2. Selecione “busca por imagem” e anexe a imagem.  
  3. Analise os resultados: nome, contexto, links, fóruns, etc.

## 4.2 Busca ao pé da letra

- Retorna resultados que contêm exatamente os termos pesquisados.  
- Para ativar no Google: Ferramentas → “Ao pé da letra”.

## 4.3 Busca por site específico

- Filtra resultados de um site específico:  
  ```text
  site:nome-do-site.domínio Termos para procurar
  ```
## 4.4 Busca avançada do Google
O próprio google nos permite buscar de forma mais avançada, com filtros, palavras-chave, idiomas etc, utilizando:
- https://www.google.com/advanced_search

## 4.5 Busca por intervalos de tempo
Outra forma interessante é ir buscando termos em determinados intervalos de tempo.
Isso é útil para sabermos exatamente qual foi a primeira aparição de uma busca em um mecanismo.

## 4.6 Código fonte em publicações
Após buscar uma imagem e encontrar um site, pode ser útil buscar no código fonte da página da imagem encontrada e procurar por "date" que é justamente o termo referente à data da imagem

## 4.7 Ferramenta de busca
### TinEye
Dada uma imagem, o site permite fazer uma busca e escavar toda a web, verificar e rastrear imagens online.
Além disso, é possível comparar imagem atual com a imagem real.
- Link: https://tineye.com

---

# 5. Engenharia Reversa
- Engenharia reversa é o processo de extrair o máximo de informações possíveis do código-fonte como strings, hexadecimais ou binários de um programa compilado por meio de descompilação, mesmo sem obter total acesso ao código original.
- A ideia aqui não é recriar o código original, mas analisar comportamentos e intenções por trás.
- Essa é uma prática extremamente recomendada pois auxilia na análise de possíveis malwares e funcionalidades ocultas ou maliciosas.
- É necessário uma boa compreensão de linguagens como:
  - Assembly (x86/x64/ARM)
  - C/C++
  - Python
  - Java
- Há diversos programas que permitem realizar tal feito, como:
  - (DIE Engine): https://github.com/horsicq/DIE-engine
  - (x64dbg): https://x64dbg.com
  - (Ghidra): https://github.com/NationalSecurityAgency/ghidra
  - (IDA): https://hex-rays.com/
  - (Radare2): https://rada.re/n/

---

# 6. Lab Forense
Com o laboratório a seguir é possível treinar conceitos iniciais aprendidos nesse guia de Computação Forense, tudo de forma 100% prática.
- Link: https://github.com/ththales/LAB-FORENSE
