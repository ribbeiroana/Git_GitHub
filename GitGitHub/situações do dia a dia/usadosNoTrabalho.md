### Comandos Usados no Trabalho

- **Branching e Merging**:
    - **Criar uma nova branch**:
        
        ```bash
        git checkout -b nova-branch
        
        ```
        
    - **Mudar de branch**:
        
        ```bash
        git checkout main
        
        ```
        
    - **Mesclar uma branch**:
        
        ```bash
        git merge nova-branch
        
        ```
        

### Trabalhando com Mais de um Contribuinte

1. **Fork**: Cria uma cópia do repositório em sua conta no GitHub.
2. **Clone o Fork**: Clona seu fork localmente.
    
    ```bash
    git clone <url-do-seu-fork>
    
    ```
    
3. **Configurar o Repositório Original como Upstream**:
    
    ```bash
    git remote add upstream <url-do-repositorio-original>
    
    ```
    
4. **Sincronizar seu Fork com o Original**:
    
    ```bash
    git fetch upstream
    git merge upstream/main
    
    ```
    
