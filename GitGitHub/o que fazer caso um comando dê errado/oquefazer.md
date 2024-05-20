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
    
