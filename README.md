# Orientação a Objetos e UML: Diagramação de Classes do iPhone

### POO - Desafio

Modelagem e diagramação da representação em UML e Código no que se refere ao componente iPhone.

Com base no vídeo de lançamento do iPhone conforme link abaixo, elabore em uma ferramenta de UML de sua preferência a diagramação das classes e interfaces com a proposta de representar os papéis do iPhone de: Reprodutor Musicial,  Aparelho Telefônico e Navegador na Internet. Em seguida crie as classes e interfaces no formato de arquivos .java

[Lançamento iPhone 2007](https://www.youtube.com/watch?v=9ou608QQRq8)

- Minutos relevantes do 00:15 até 00:55

###### Comportamentos esperados:
* Repodutor Musicial: tocar, pausar, selecionarMusica
* Aparelho Telefônico: ligar, atender, iniciarCorrerioVoz
* Navegador na Internet: exibirPagina, adicionarNovaAba, atualizarPagina



## Vamos modelar a implementação utilizando a abordagem de Interface com Implementação em Classe Concreta na linguagem UML.

### Interface com Implementação em Classe Concreta:
#### Vantagens:

- Flexibilidade: As interfaces permitem que uma classe implemente múltiplas interfaces, o que é útil se o iPhone precisar suportar outras funcionalidades no futuro.
- Separação de Responsabilidades: Ao definir interfaces, você separa claramente os contratos que as classes devem seguir, promovendo um design mais coeso e de fácil manutenção.
- Possibilidade de Herança Múltipla: Em linguagens que suportam herança múltipla através de interfaces (como Java), você pode implementar funcionalidades de várias fontes, fornecendo uma maior flexibilidade de design.
#### Desvantagens:

- Boa Quantidade de Código Redundante: Em certos casos, você pode acabar repetindo a mesma implementação básica em várias classes concretas, o que pode resultar em redundância de código.
- Dificuldade em Alterar Implementações Compartilhadas: Se várias classes compartilham uma implementação comum através de uma interface, mudar essa implementação comum pode ser complicado, pois exigirá alterações em várias classes.

### Descrição das Classes e Interfaces:
###### iPhone (Classe Abstrata)
A classe base que contém os métodos e atributos compartilhados por todas as funcionalidades do iPhone.
###### ReprodutorMusical (Interface)
Define os métodos que um reprodutor musical deve implementar, como tocar música, pausar, avançar, retroceder etc.
###### AparelhoTelefonico (Interface)
Define os métodos relacionados às funcionalidades de telefone, como fazer chamadas, receber chamadas, enviar mensagens etc.
###### NavegadorInternet (Interface)
Define os métodos necessários para navegação na internet, como abrir página, fechar página, navegar para frente, navegar para trás etc.
###### iPhoneFuncionalidade (Classe Concreta)
Implementa as interfaces ReprodutorMusical, AparelhoTelefonico e NavegadorInternet, fornecendo as funcionalidades específicas para cada aspecto do iPhone.

![Diagrama](https://github.com/akranz79/dio-santander2024-desafios-Diagramacao_iphone/blob/main/img/DiagramaiPhone.drawio.png)

### Aqui está a implementação em formato de arquivos .java, seguindo a abordagem de Interface com Implementação em Classe Concreta:

######  iPhone.java
```
public abstract class iPhone {
    // Atributos comuns a todas as funcionalidades do iPhone

    // Métodos comuns a todas as funcionalidades do iPhone
}
```
######  ReprodutorMusical.java
```
public interface ReprodutorMusical {
    void tocarMusica();
    void pausarMusica();
    void avancarMusica();
    void retrocederMusica();
    // Outros métodos relacionados à reprodução musical
}
```
######  AparelhoTelefonico.java
```
public interface AparelhoTelefonico {
    void fazerChamada();
    void receberChamada();
    void enviarMensagem();
    // Outros métodos relacionados ao telefone
}
```
######  NavegadorInternet.java
```
public interface NavegadorInternet {
    void abrirPagina();
    void fecharPagina();
    void atualiza();
    void arbrirNovaAba();
    void fecharAba();
    // Outros métodos relacionados à navegação na internet
}
```
######  iPhoneFuncionalidade.java
```
public class iPhoneFuncionalidade extends iPhone implements ReprodutorMusical, AparelhoTelefonico, NavegadorInternet {
    @Override
    public void tocarMusica() {
        // Implementação específica para tocar música no iPhone
    }

    @Override
    public void pausarMusica() {
        // Implementação específica para pausar música no iPhone
    }

    @Override
    public void avancarMusica() {
        // Implementação específica para avançar música no iPhone
    }

    @Override
    public void retrocederMusica() {
        // Implementação específica para retroceder música no iPhone
    }

    @Override
    public void fazerChamada() {
        // Implementação específica para fazer chamada no iPhone
    }

    @Override
    public void receberChamada() {
        // Implementação específica para receber chamada no iPhone
    }

    @Override
    public void enviarMensagem() {
        // Implementação específica para enviar mensagem no iPhone
    }

    @Override
    public void abrirPagina() {
        // Implementação específica para abrir página no iPhone
    }

    @Override
    public void fecharPagina() {
        // Implementação específica para fechar página no iPhone
    }

    @Override
    public void navegarParaFrente() {
        // Implementação específica para navegar para frente no iPhone
    }

    @Override
    public void navegarParaTras() {
        // Implementação específica para navegar para trás no iPhone
    }
}

```
