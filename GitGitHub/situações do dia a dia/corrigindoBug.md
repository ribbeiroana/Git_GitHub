### Corrigindo um Bug

### Cenário

Um bug crítico foi encontrado em produção e precisa ser corrigido o mais rápido possível. Você deve isolar a correção em uma branch separada, testá-la e integrá-la à branch principal.

### Passo a Passo com Comandos

1. **Crie e Mude para uma Nova Branch de Correção**
    
    ```bash
    git checkout -b bugfix/critical-bug
    
    ```
    
2. **Implemente a Correção**
    
    Após fazer as alterações necessárias, verifique o status dos arquivos modificados.
    
    ```bash
    git status
    
    ```
    
3. **Adicione os Arquivos Modificados ao Staging Area**
    
    ```bash
    git add .
    
    ```
    
4. **Faça o Commit da Correção**
    
    ```bash
    git commit -m "Corrige o bug crítico"
    
    ```
    
5. **Atualize a Branch de Correção com o Código Mais Recente**
    
    ```bash
    git checkout main
    git pull origin main
    git checkout bugfix/critical-bug
    git merge main
    
    ```
    
6. **Resolva Conflitos (se houver)**
    
    ```bash
    # Resolva conflitos manualmente, depois
    git add .
    git commit -m "Resolve conflitos ao mesclar main em bugfix/critical-bug"
    
    ```
    
7. **Envie suas Mudanças para o Repositório Remoto**
    
    ```bash
    git push origin bugfix/critical-bug
    
    ```
    
8. **Abra um Pull Request no GitHub**
    
    No GitHub, abra um pull request da branch `bugfix/critical-bug` para a branch `main`.
    
9. **Mescle a Branch (após aprovação)**
    
    Após a aprovação do pull request, mescle a branch `bugfix/critical-bug` na `main`.
    
10. **Sincronize seu Repositório Local**
    
    ```bash
    git checkout main
    git pull origin main
    
    ```
    
