
# DIO | Resumos Git e GitHub

Repositório destinado a resumos sobre Git e GitHub do módulo "Versionamento de Código com Git e GitHub" presente no Bootcamp [DIO Ri Happy Front-end do Zero](https://web.dio.me/track/coding-future-front-end-do-zero).

## 📚 Documentação
- [Documentação Git](https://git-scm.com/docs/git/pt_BR)
- [Documentação GitHub](https://docs.github.com/pt)

## 💻 Resumo das Aulas

### Sistemas de Controle de Versão - Controlam as versões de um arquivo ao longo do tempo.
- Registra o histórico de atualizações de um arquivo;
- Gerencia quais foram as alterações, a data, autor e etc;
- Organização, controle e segurança.

### Tipos de Sistemas de Controle de Versão - Dentre os Sitemas de Controle de Versão (VCS), temos:
- VCS Centralizado (CVCS). Exemplos: CVS, Subversion.
- VCS Distribuído (DVCS). Exemplos: Git, Mercurial.

#### VCS Centralizado (CVCS)
Nesse sistema temos apenas um servidor contendo todos os arquivos responsáveis pelo controle de versão, tendo desenvolvedores conectados ao servidor. Porém, se o servidor ficar fora do ar, não é possível salvar o arquivo, além de que, se não houver um backup será perdido os arquivos.

#### VCS Distribuído (DVCS)
Nesse sitema, cada banco de versão é duplicado localmente, permitindo a edição mesmo com o servidor fora do ar. Ele clona o repositório completo, o que inclui o histório de versões.
- Cada clone é como um backup;
- Possibilita um fluxo de trabalho flexível;
- Possibilidade de trabalhar sem conexão à rede. <br> <br>

### O que é GIT?
É um sistema de Controle de Versão Distribuído.
- Gratuito e Open Source (Código Aberto);
- Ramificações (branching) e fusões (merging) eficientes;
- Leve e rápido.

### Fluxo Básico no Git
```
git clone
```
Clona um repositório Git existente para um novo diretório (pasta) local.
```
git commit
```
Grava alterações no repositório.
```
git pull
```
Puxa as alterações do repositório remoto para o local (busca e mescla).
```
git push 
```
Empurra as alterações do repositório local para o remoto. <br> <br>

## O que é GitHub?
É uma plataforma de hospedagem de código para controle de versão com Git, e colaboração.
- Comunidade ativa;
- Utilizado mundialmente; <br> <br>

## Mais alguns comandos Git:
```
git remote add origin URL
```
Conecta o repositório local com o remoto.<br><br>
```
git clone URL nome-do-diretorio-local
```
Clona o repositório do qual foi copiado. A parte de "nome-do-diretorio-local" é para caso eu queira mudar o nome do clone.<br><br>

```
git clone URL --branch nome-da-branch-desejada --signle-branch
```
Comando para clonar apenas uma branch.<br><br>

```
gi restore arquivo-a-ser-restaurado
```
Restaura ao último estado em que o arquivo havia sido salvo. Quando utilizar o comando, verifique se você não quer perder alguma alteração da qual foi feitae não salva. Pois, esse comando irá descartá-las.<br><br>

```
git commit --amend -m"novo-nome-do-ultimo-commit"
```
Renomeia o seu último commit para o nome de sua escolha.<br><br>

```
git log
```
Mostra seu histórico de commits.<br><br>

```
git reset --soft hash-do-commit
```
Ele pega os arquivos que estavam no commit selecionado e os adicionam na área de preparação.<br><br>

```
git reset --mixed hash-do-commit
```
Pega os arquivos no commit selecionado e os adicionam na área de trabalho.<br><br>

```
git reset --hard hash-do-commit
```
Ele ignora os arquivos que estavam no commit selecionado e os desfaz.<br><br>

```
git reflog
```
Comando para visualizar o histórico de commits de forma mais detalhada.<br><br>

```
git reset nome-do-arquivo
```
Remove o arquivo descrito em código.<br><br>

```
git restore --staged nome-do-arquivo
```
Também remove os arquivos da área de preparação. <br> <br>

## Trabalhando com Branches
De maneira simplista, uma Branch (ramo) é uma ramificação do seu projeto.
- É um ponteiro móvel para um commit no histórico do repositório;
- Quando você cria uma nova Branch a partir de outra existente, a nova se inicia apontando para o mesmo commit da Branch que estava quando foi criada.

```
git checkout -b nome-da-branch
```
Cria uma nova branch e a substitui a branch "main" pela criada.<br><br>

```
git checkout nome-da-branch
```
Muda para a branch selecionada.<br><br>

```
git ranch -v
```
Mostra o último commit de cada branch.<br><br>


```
git merge nome-da-branch
```
Mescla a branch selecionada com a branch main<br><br>

```
git branch -d nome-da-branch
```
Deleta a branch selecionada. <br> <br>

## Conflito de Merge
Acontece quando há alterações concorrentes. Utilizando um cenário hipotético como exemplo: <br>

Você e um colega estão trabalhando no mesmo repositório e vocês acabam alterando a mesma linha de código. <br>

Isso fará com que ao realizar a tentativa de enviar uma atualização para o GitHub, acabe gerando um conflito com o que seu colega havia enviado. Isso acontece, pois, o Git não entende qual alteração deve ser mantida, então, ele retorna o erro para decidir-mos qual alteração optaremos por manter.

Para corrigir, basta executar o comando abaixo. Pois ele retorna o conteúdo que está no repositório remoto para nossa máquina.
```
git pull
```
Após isso, eu seleciono qual alteração eu desejo manter e depois faço o envio para o repositório remoto. <br><br>

```
git fetch origin main
```
Baixa as alterações do repositório remoto origin da branch main, e não mescla com o repositório local. <br><br>

```
git diff main origin/main
```
Esse comando retorna as diferença entre as branchs selecionadas. <br><br>

```
git merge origin/main
```
Traz as alterações do repositório remoto para o local.<br><br>

```
git clone url-do-repositorio --branch nome-da-branch -- single-branch
```
Esse comando clona apenas a branch escolhida. <br><br>

