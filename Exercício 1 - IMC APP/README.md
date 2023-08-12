# Relatório de Avaliação do Aplicativo de Cálculo de IMC

## 👩🏻👨🏻 Integrantes:
- **Nome:** Camylla Lima Dias **RA:** 22.217.005-2
- **Nome:** Lucca Bonsi Guarreschi **RA:** 22.120.016-5

## 1. Informações Gerais

- **Nome do Aplicativo:** IMC
- **Versão:** 1.0.0
- **Data da Avaliação:** 11/08/2023
- **Avaliadores:** Camylla e Lucca

## 2. Objetivo da Avaliação

O objetivo desta avaliação é verificar a funcionalidade e precisão do aplicativo IMC. O sistema deve exibir o valor do IMC calculado corretamente e deve retornar as seguintes mensagens de acordo com a condição identificada a partir das informações fornecidas: 
- abaixo do peso: " Você está abaixo do peso recomendado. " 
- no peso normal: "Você está muito bem! Continue assim!" 
- acima do peso: " Você está acima do peso recomendado. Cuidado!"
- obeso: Você está Obeso. Procure o acompanhamento de um nutricionista e realizar mais atividades físicas! 

A intenção da Clínica é incorporar essa aplicação no seu portal.

## 3. Metodologia

Foram inseridos diferentes valores de peso e altura no aplicativo para gerar diferentes categorias de IMC. As mensagens retornadas pelo aplicativo foram então comparadas com as mensagens esperadas.

## 4. Resultados

### 4.1 Testes Realizados

- Teste 1: Homem, Altura 1,81m, Peso 65kg com IMC 19,84
  - **Esperado:** "Você está muito bem! Continue assim! IMC 19,84" 
  - **Retornado:** "CUIDADO!!!Voce estar abaixo do peso! IMC 19,84"
  
- Teste 2: Mulher, Altura 1,55m, Peso 53kg com IMC 22,06
  - **Esperado:** "Você está muito bem! Continue assim! IMC 22,06" 
  - **Retornado:** "PARABENS!!Voce estar com o peso ideal! IMC 22,06"
  
- Teste 3: Mulher, Altura 1,55m, Peso 62kg com IMC 25,81
  - **Esperado:** "Você está acima do peso recomendado. Cuidado! IMC 25,81" 
  - **Retornado:** "CUIDADO!!Voce estar obesa! IMC 25,81"
  
- Teste 4: Homem, Altura 1,55, Peso 62kg com IMC 25,81 
  - **Esperado:** "Você está acima do peso recomendado. Cuidado! IMC 25,81" 
  - **Retornado:** PARABENS!!Voce estar com o peso ideal! IMC 25,81"

### 4.2 Problemas Identificados

Em resumo, o aplicativo retorna a mensagem de "Você está muito bem! Continue assim!" para IMCs acima de 25 quando o sexo escolhido é o masculino. Já para o sexo feminino, para o mesmo IMC, o aplicativo retorna a mensagem "CUIDADO!!Voce estar obesa!", por exemplo. Os mesmos erros se repetem para outros ranges de IMC (veja a Figura 1 no tópico 6).
  - **Severidade:** Alta
  - **Recomendação:** Corrigir a lógica para retornar a mensagem correta para os IMCs e retirar os ranges de IMC específicos para homens e mulheres.

## 5. Conclusão

O aplicativo IMC apresenta erros críticos nas mensagens retornadas com base no cálculo do IMC. É essencial que esses problemas sejam corrigidos antes de incorporar essa aplicação no portal da Clínica.

## 6. Anexos
Capturas de tela dos testes realizados e mensagens retornadas.

- Figura 1 - Arrays ``imc_homens[]`` e ``imc_mulheres[]`` <br>
![f3.jpg](https://github.com/camylladias/CC8550/blob/main/Exerc%C3%ADcio%201%20-%20IMC%20APP/img/f3.jpg?raw=true)

- Figura 2 - Homem <br>
![f1.jpg](https://github.com/camylladias/CC8550/blob/main/Exerc%C3%ADcio%201%20-%20IMC%20APP/img/f1.jpg?raw=true)

- Figura 3 -  Mulher <br>
![f2.jpg](https://github.com/camylladias/CC8550/blob/main/Exerc%C3%ADcio%201%20-%20IMC%20APP/img/f2.jpg?raw=true)

- Figura 3 - Homem 2 <br>
![f4.jpg](https://github.com/camylladias/CC8550/blob/main/Exerc%C3%ADcio%201%20-%20IMC%20APP/img/f4.jpg?raw=true)
