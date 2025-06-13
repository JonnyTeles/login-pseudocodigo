
# Sistema Simples de Login  
**Autor:** Jonny Gabriel Teles

---

## Descrição do Sistema

Sistema básico de autenticação, onde:
- O usuário deve digitar um nome de usuário e uma senha.
- O sistema precisa verificar se as informações digitadas estão corretas (comparando com dados previamente armazenados).
- Se as credenciais forem corretas, o sistema permite o acesso.
- Se as credenciais estiverem erradas, o sistema nega o acesso e exibe uma mensagem de erro.

Esse tipo de sistema é comum em sites, aplicativos e dispositivos para controlar o acesso de pessoas autorizadas.

---

## Pseudocódigo

```
Início

    Definir USUARIO_CORRETO como "admin"
    Definir SENHA_CORRETA como "1234"
    
    Escreva "Digite o nome de usuário:"
    Leia usuarioDigitado
    
    Escreva "Digite a senha:"
    Leia senhaDigitada

    Se usuarioDigitado = USUARIO_CORRETO E senhaDigitada = SENHA_CORRETA então
        Escreva "Login realizado com sucesso!"
    Senão
        Escreva "Usuário ou senha incorretos."

Fim
```

---

## Explicação do Pseudocódigo Passo a Passo

### Início
O algoritmo começa a execução.

### Definir o usuário e senha corretos
O sistema já possui armazenados:
- `USUARIO_CORRETO = "admin"`
- `SENHA_CORRETA = "1234"`

Esses serão os dados de referência para a comparação.

### Solicitar entrada do usuário
O sistema pede que a pessoa digite:
- O nome de usuário (`usuarioDigitado`)
- A senha (`senhaDigitada`)

### Verificação
O sistema compara:
- Se `usuarioDigitado` é igual a `USUARIO_CORRETO`
- Se `senhaDigitada` é igual a `SENHA_CORRETA`

### Condição:
- Se a comparação for **verdadeira** (as duas informações estiverem corretas):  
  O sistema exibe: **"Login realizado com sucesso."**

- Se a comparação for **falsa** (alguma informação estiver errada):  
  O sistema exibe: **"Usuário ou senha incorretos."**

### Fim
O algoritmo é encerrado.

---
# FLUXOGRAMA

![Fluxograma do Sistema](Fluxograma%20-%20Sistema%20de%20Login.png)
---

# BÔNUS

Como já tenho certo conhecimento e experiência com as linguagens **Java** e **JavaScript (Node.js)**, aproveitei para transformar o pseudocódigo em exemplos reais de código. Isso mostra como o raciocínio lógico pode ser aplicado diretamente em uma linguagem de programação.

---

## Exemplo em Node.js (JavaScript)

```javascript

const prompt = require('prompt-sync')();

const USUARIO_CORRETO = 'admin';
const SENHA_CORRETA = '1234';

const usuarioDigitado = prompt('Digite o nome de usuário: ');
const senhaDigitada = prompt('Digite a senha: ');

if (usuarioDigitado === USUARIO_CORRETO && senhaDigitada === SENHA_CORRETA) {
    console.log('Login realizado com sucesso!');
} else {
    console.log('Usuário ou senha incorretos.');
}
```

---

## Exemplo em Java

```java

import java.util.Scanner;

public class SistemaLogin {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        final String USUARIO_CORRETO = "admin";
        final String SENHA_CORRETA = "1234";
        
        System.out.print("Digite o nome de usuário: ");
        String usuarioDigitado = scanner.nextLine();
        
        System.out.print("Digite a senha: ");
        String senhaDigitada = scanner.nextLine();
        
        if (usuarioDigitado.equals(USUARIO_CORRETO) && senhaDigitada.equals(SENHA_CORRETA)) {
            System.out.println("Login realizado com sucesso!");
        } else {
            System.out.println("Usuário ou senha incorretos.");
        }

        scanner.close();
    }
}
```

---
