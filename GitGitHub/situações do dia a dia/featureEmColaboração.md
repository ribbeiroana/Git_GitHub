### Implementando uma Nova Feature em Colaboração

### Cenário

Você e um colega estão trabalhando juntos em uma nova feature chamada "Feature Y". Vocês precisam colaborar de forma eficiente e evitar conflitos.

### Passo a Passo com Comandos

1. **Crie e Mude para uma Nova Branch**
    
    ```bash
    git checkout -b feature/feature-y
    
    ```
    
2. **Implemente Parte da Feature e Faça Commit**
    
    ```bash
    # Faça mudanças no código
    git add .
    git commit -m "Implementa parte inicial da Feature Y"
    
    ```
    
3. **Envie as Mudanças para o Repositório Remoto**
    
    ```bash
    git push origin feature/feature-y
    
    ```
    
4. **Colega Puxa e Continua o Trabalho**
    
    Seu colega puxa as mudanças da branch `feature/feature-y`.
    
    ```bash
    git pull origin feature/feature-y
    
    ```
    
    Depois, ele faz suas próprias mudanças, commits e envia novamente para o repositório remoto.
    
    ```bash
    git add .
    git commit -m "Continua implementação da Feature Y"
    git push origin feature/feature-y
    
    ```
    
5. **Integre a Feature na Branch Principal**
    
    Após finalizar a feature, você ou seu colega pode abrir um pull request no GitHub para integrar a branch `feature/feature-y` na `main`.
    
    ```bash
    # Na interface do GitHub, abra um pull request e mescle após a revisão.
    
    ```
    
6. **Sincronize seu Repositório Local**
    
    ```bash
    git checkout main
    git pull origin main
    
    ```
    