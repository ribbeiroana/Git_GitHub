### Revertendo uma Mudança Problemática

### Cenário

Um commit recente introduziu um problema no sistema. Você precisa reverter essa mudança para manter a estabilidade do código.

### Passo a Passo com Comandos

1. **Identifique o Commit Problemático**
    
    Use `git log` para encontrar o hash do commit que precisa ser revertido.
    
    ```bash
    git log
    
    ```
    
2. **Reverta o Commit**
    
    Use o comando `git revert` seguido do hash do commit.
    
    ```bash
    git revert <commit-hash>
    
    ```
    
3. **Resolva Conflitos (se houver)**
    
    Se houver conflitos durante a reversão, resolva-os manualmente. Depois de resolver os conflitos, faça um commit.
    
    ```bash
    git add .
    git commit -m "Resolve conflitos ao reverter commit <commit-hash>"
    
    ```
    
4. **Envie a Reversão para o Repositório Remoto**
    
    ```bash
    git push origin main
    
    ```
    
5. **Comunique a Equipe**
    
    Informe sua equipe sobre a reversão e o motivo, para que todos estejam cientes da mudança.
    