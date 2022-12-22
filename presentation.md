---
marp: true
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Chivo+Mono&display=swap');
  *{
    font-family: 'Chivo Mono', monospace;
  }
  section{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>

---
<section>

# Github Actions
## CI & CD

</section>

---

<section>

# O que é?
🤔
- Automatização de Fluxos diretamente do repositório
- Integração com sdks de produção como no Firebase, AWS, composer etc
- Integração com CIs & CDs
- Personalização de Jobs (scripts)

</section>
---

---

<section>

# Como funciona?

- Github funciona com eventos, ao subirmos, criar novas branches etc, é disparado um evento, esse evento, podemos dar certos triggers, por exemplo: ao criar um novo pull request ou um novo commit, podemos rodar um *Script que roda os testes unitários no código, ou até mesmo subir diretamente para a Google Play ou Serviço de Hospedagem* 
  <br/>
 
- Os scripts usam síntaxe YAML para construir as instruções de serviços

</section>

---
<section>
W
# Exemplo
Todo repositório do github apresenta uma aba de "actions", onde ficarão todos os fluxos de automação

![description](images/image1.png)

Os jobs aparecerão dessa forma, com os seus respectivos Status
![description](images/image2.png)


Os jobs são criados com .YAML. No exemplo abaixo, o script que faz com que ao fazer um novo push, o job roda um comando NPM para pegar as dependências do projeto, rodar um build e assim que terminar, faz a publicação para o __Firebase Hosting__
![description](images/image3.png)


</section>


---
<section>

# Um exemplo em Flutter

Para flutter, há alguns [Scripts no próprio marketplace do GitHub](https://github.com/r0adkll/upload-google-play) para rodar essas integrações. No caso, precisamos também ter uma Acces Key no Google Cloud Platform, para setar o CI e termos a permissão de mandar o **Appbundle diretamente para a loja**. Com a Access Key, podemos colocá-la no **SECRETS** do repo no GitHub. 

![image4](images/image4.png)
Exemplo de Script que faz o deploy para o Google Play **na variável ```serviceAccountJsonPlainText``` é onde fica o SecretKey que pegamos do Google Cloud**
![image](images/image5.png)

</section>
---

---
<section>

# Alternativas ao GitHub Actions (pagas)
[Code magic](https://codemagic.io/start/)
[BitRise](https://bitrise.io/?utm_source=google&utm_medium=cpc&utm_campaign=conversion-focus&utm_source=google&utm_medium=cpc&utm_campaign=US-S-Platform&utm_term=Android_Androidbuild&gclid=CjwKCAiAnZCdBhBmEiwA8nDQxS2pb8bj5YInX9DF3wEVMl7eD-cENW-lqg421YgCMCYD9prztlas1RoC_mkQAvD_BwE&gclsrc=aw.ds)

Também vale lembrar que o GitHub Actions não é totalmente free, temos um limite mensal de uso, no caso 2000 minutos:
![image](images/image6.png)

</section>


---
<section>
# THE END 👌
---