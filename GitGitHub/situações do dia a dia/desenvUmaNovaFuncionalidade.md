### Cenário

Você e sua equipe estão trabalhando em um projeto de software. Seu líder de equipe pede para você desenvolver uma nova funcionalidade chamada "Feature X". Você precisa criar uma nova branch para essa funcionalidade, implementar as mudanças, e depois integrar essa funcionalidade ao repositório principal sem interromper o trabalho dos outros membros da equipe.

### Passo a Passo com Comandos

1. **Clone o Repositório Principal**
    
    Primeiro, você precisa clonar o repositório principal para o seu ambiente local.
    
    ```bash
    git clone <https://github.com/usuario/repo.git>
    
    ```
    
2. **Crie e Mude para uma Nova Branch**
    
    Em seguida, você cria uma nova branch chamada `feature-x` e muda para essa branch. Isso isola suas mudanças das outras funcionalidades e do código principal.
    
    ```bash
    git checkout -b feature-x
    
    ```
    
3. **Implemente a Funcionalidade**
    
    Agora, você pode começar a codificar a nova funcionalidade. Depois de fazer as mudanças necessárias, verifique o status do seu repositório para ver quais arquivos foram modificados.
    
    ```bash
    git status
    
    ```
    
4. **Adicione os Arquivos Modificados ao Staging Area**
    
    Adicione os arquivos modificados ao índice (staging area) para prepará-los para o commit.
    
    ```bash
    git add .
    
    ```
    
5. **Faça o Commit das Mudanças**
    
    Grave as mudanças no repositório local com uma mensagem descritiva.
    
    ```bash
    git commit -m "Implementa a Feature X"
    
    ```
    
6. **Atualize sua Branch com o Código Mais Recente**
    
    Antes de integrar suas mudanças ao repositório principal, certifique-se de que sua branch está atualizada com as últimas mudanças do repositório remoto. Primeiro, mude para a branch principal (`main`).
    
    ```bash
    git checkout main
    
    ```
    
    Em seguida, puxe as últimas mudanças do repositório remoto.
    
    ```bash
    git pull origin main
    
    ```
    
    Volte para sua branch `feature-x`.
    
    ```bash
    git checkout feature-x
    
    ```
    
    E então mescle as mudanças da branch `main` na sua branch `feature-x`.
    
    ```bash
    git merge main
    
    ```
    
7. **Resolva Conflitos (se houver)**
    
    Se houver conflitos durante a mesclagem, resolva-os manualmente. Depois de resolver os conflitos, adicione os arquivos modificados e faça um commit para registrar a resolução dos conflitos.
    
    ```bash
    git add .
    git commit -m "Resolve conflitos ao mesclar main em feature-x"
    
    ```
    
8. **Envie suas Mudanças para o Repositório Remoto**
    
    Envie as mudanças da sua branch `feature-x` para o repositório remoto para que outros membros da equipe possam revisá-las.
    
    ```bash
    git push origin feature-x
    
    ```
    
9. **Abra um Pull Request no GitHub**
    
    No GitHub, abra um pull request da branch `feature-x` para a branch `main`. Solicite uma revisão de código para garantir que suas mudanças sejam verificadas por outros membros da equipe.
    
10. **Integre a Branch (após aprovação)**
    
    Após a aprovação do pull request, mescle a branch `feature-x` na `main`. Isso pode ser feito diretamente no GitHub, onde você pode usar o botão de merge.
    
11. **Sincronize seu Repositório Local**
    
    Depois que o pull request for mesclado, sincronize seu repositório local com o repositório remoto para manter seu ambiente de desenvolvimento atualizado.
    
    ```bash
    git checkout main
    git pull origin main
    
    ```
    

### O que Fazer Caso Algo Dê Errado

1. **Desfazer um Commit Local (sem perder as mudanças)**:
    
    ```bash
    git reset --soft HEAD~1
    
    ```
    
2. **Desfazer um `git add`**:
    
    ```bash
    git reset <arquivo>
    
    ```
    
3. **Cancelar uma Mesclagem que Deu Errado**:
    
    ```bash
    git merge --abort
    
    ```
    
4. **Reverter um Commit Específico**:
    
    ```bash
    git revert <commit-hash>
    
    ```
    

