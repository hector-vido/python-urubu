---
title: Jenkins
layout: page 
pager: true
---


Jenkins é um software utilizado para CI/CD
{.lead}

# Jenkins

[Jenkins](https://jenkins.io/) é uma ferramenta utilizada para *integração contínua* e *entrega contínua*, popularmente conhecido como **CI/CD** - **C**ontinuous **I**ntegration e **C**ontinuous **D**elivery.
Seu papel é integrar à esteira de produção de software outros programas responsáveis por testes unitários, análise de código, testes de stress e qualidade para que então uma nova versão possa ser disponibilizada em produção, ou em algum repositório de artefatos, com uma alta taxa de confiabilidade.
O Jenkins é um dos grandes nomes ao lado do Docker dentro do universo DevOps.

Cada projeto dentro do Jenkins é conhecido como **Job**, sendo dois deles mais comuns, o *freestyle* e a *pipeline*.

### Freestyle

Jobs do tipo freestyle são construídos pelo próprio painel do Jenkins e geralmente emendam vários passos em shell script, ou outros módulos de modo a criar uma esteira única. A vantagem desse tipo de job é a facilidade em criar pequenas automações principalmente em **shell script**, a desvantagem está na difícil manutenção e falta de padronização.

### Pipeline

A pipeline tem sido a forma de trabalho padrão, inclusive em outras ferramentas, são scripts que controlam todos os estados da esteira, podem ser versionados e incluídos de repositórios remotos sob demanda. O Jenkins utiliza uma DSL chamda de **Pipeline**, e os arquivos ou a forma como é escrita recebe o nome de **Jenkinsfile**. Para casos mais complexos é possível utilizar [Groovy](http://groovy-lang.org/) como linguagem de script o que extenderá e muito a capacidade lógica da pipeline.

Um exemplo da sintaxe de um `Jenkinsfile` seria o seguinte:

```js
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
```
