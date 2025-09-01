# BootCamp ♨️Santander & DIO: BackEnd Python 🐍 2025 (*Desafio 01*)
## Desafio 01 - Desenvolvendo sua Primeira API com FastAPI, Python e Docker  
  
## 🎯Objetivo:
O desafio consiste em adaptar e personalizar esse modelo para criar um agente que informe e auxilie usuários com dados sobre destinos, pacotes promocionais, dicas de 

Agora é a sua hora de brilhar e construir um perfil de destaque na DIO! Explore todos os conceitos explorados até aqui e replique (ou melhore, porque não?) este projeto prático. Para isso, crie seu próprio repositório e aumente ainda mais seu portfólio de projetos no GitHub, o qual pode fazer toda diferença em suas entrevistas técnicas.
 
Neste repositório, insira todos os links e arquivos necessários para seu projeto, seja um arquivo de banco de dados ou um link para o template no Figma.
 
Dica: Se o expert forneceu um repositório Github, você pode dar um "fork" no repositório dele para organizar suas alterações e evoluções mantendo uma referência direta ao código-fonte original.  
  ![img_DesafioAceito.png](./imgs/img_DesafioAceito.png)  

## 🤓Repositório Git:
O Git é um conceito essencial no mercado de trabalho atualmente, por isso sempre reforçamos sua importância em nossa metodologia educacional. Por isso, todo código-fonte desenvolvido durante este conteúdo foi versionado no seguinte endereço para que você possa consultá-lo a qualquer momento:
 
[https://github.com/digitalinnovationone/workout_api](https://github.com/digitalinnovationone/workout_api)
.  

---

## 🛠️Passo a Passo:

- adicionar query parameters nos endpoints
      - atleta
            - nome
            - cpf
- customizar response de retorno de endpoints
      - get all
            - atleta
                  - nome
                  - centro_treinamento
                  - categoria
- Manipular exceção de integridade dos dados em cada módulo/tabela
      - sqlalchemy.exc.IntegrityError e devolver a seguinte mensagem: “Já existe um atleta cadastrado com o cpf: x”
      - status_code: 303
- Adicionar paginação utilizando a lib: fastapi-pagination
      - limit e offset.

---

## 🤓Desafio Feito😎! Minha resolução🎉🎉🎉:

> Veja a solução no código do meu git:  
> 📋[desafio_BootcampBackEndPython_001.py](https://github.com/Roberto-Pfaltzgraff/estudos_DIO-labs/blob/main/DIO/Santander/2025_06_BackEndPython/desafio_BootcampBackEndPython_001.py)  .

---
