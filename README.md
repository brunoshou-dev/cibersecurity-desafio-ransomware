# Ransomware com Python (Educacional)
Este projeto foi desenvolvido como parte do Desafio de Projeto do Bootcamp de Cibersegurança da DIO. O objetivo é criar um "Ransomware" simples utilizando a linguagem Python para demonstrar na prática os conceitos de criptografia.

## Aviso
**Este código foi desenvolvido estritamente para fins educacionais.** O objetivo é entender a lógica por trás de malwares baseados em criptografia para melhor defender sistemas. A utilização deste código para fins maliciosos é ilegal e antiética.

## Ferramentas Utilizadas
* **Python:** Linguagem de programação escolhida pela simplicidade e poder.
* **Biblioteca `pyaes`:** Utilizada para implementar a criptografia AES (Advanced Encryption Standard).

## Estrutura do Projeto
O projeto é composto por dois scripts principais:

1.  `encrypter.py`: Responsável por criptografar o arquivo alvo.
2.  `decrypter.py`: Responsável por descriptografar e recuperar o arquivo original.

## Funcionamento Técnico
### Criptografia (`encrypter.py`)
1.  O script localiza o arquivo alvo (neste exemplo, `teste.txt`).
2.  Lê o conteúdo do arquivo e o armazena na memória.
3.  Exclui o arquivo original.
4.  Utiliza a chave de criptografia (hardcoded para fins de teste) e o algoritmo AES (modo CTR) para encriptar os dados.
5.  Cria um novo arquivo com a extensão modificada contendo os dados criptografados.

### Descriptografia (`decrypter.py`)
1.  O script localiza o arquivo criptografado.
2.  Lê o conteúdo criptografado.
3.  Utiliza a **mesma chave** usada na criptografia para reverter o processo (chave simétrica).
4.  Exclui o arquivo criptografado e restaura o arquivo original (`teste.txt`).

## Como Executar
1.  Certifique-se de ter o Python instalado.
2.  Instale a biblioteca necessária:
    bash
    pip install pyaes
3.  Crie um arquivo de texto chamado `teste.txt` na mesma pasta dos scripts e escreva algo nele.
4.  Execute o encriptador:
    bash
    python encrypter.py
    *Observe que o arquivo `teste.txt` sumiu e apareceu um arquivo criptografado.*
5.  Execute o decriptador para restaurar:
    bash
    python decrypter.py

---
## Autor
Desafio realizado por Bruno Shou
