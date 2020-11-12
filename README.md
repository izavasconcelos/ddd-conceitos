## DDD


**1. Qual é o objetivo principal do DDD?**

O DDD (Domain-driven Design) é uma abordagem para o desenvolvimento de software para necessidades complexas, conectando profundamente a implementação a um modelo em evolução dos principais conceitos de negócios. O DDD apresenta soluções que têm em conta todas as camadas do sistema.

O principal objetivo é manter sob controle a complexidade inerente aos softwares que atendem necessidades complexas, ou seja, facilitando e acelerarando projetos com domínios complexos através de boas práticas a serem seguidas. Por isso, prioriza o problema ao qual se deseja resolver iniciando o desenvolvimento pelo design da aplicação. Também busca a melhoria na comunicação entre a equipe e o cliente. 


**2. Qual é o impacto que DDD pode causar no projeto?**

Como já citado arteriormente, auxilia na abordagem de domínios complexos, facilitando a desacoplação dos times de desenvolvimento por cada domínio, além de contribuir na manutenção do projeto.
Também evita um design de projeto que não está preparado para escalabilidade ou mudanças de requisitos.

Além disso, visa uma melhor comunicação entre a equipe e o cliente por meio da utilização de uma linguagem que não exija o jargão técnico. 
O DDD depende da quebra de barreiras de comunicação entre especialistas de negócio e especialistas técnicos, além do engajamento do time técnico em programar de forma que o código reflita o domínio. Se uma dessas variáveis for negativa, provavelmente o DDD não serve para o cenário implementado. Estas situações são causadas, principalmente, pela implementação de uma metodologia que não é familiar para os envolvidos. 

Aplicar DDD é utilizar padrões com o objetivo de extrair e reconhecer a essência de um sistema, através de nomenclatura, tipagem e regras de negócio explicitamente definidas, dentre outras práticas, é possível chegar perto disso. Alguns exemplos de práticas do DDD:

#### Nomenclatura:

Para ter um software que atenda perfeitamente a um determinado domínio, é necessário que se estabeleça, em primeiro lugar, uma linguagem ubíqua. Isso significa que, se durante uma conversa com um cliente de um sistema de cobrança, for solicido: “emitir a fatura para o cliente antes da data limite”, irá ser implementado no código algo como:
```
    	Uma classe para a entidade Cliente;
    	Uma classe para a entidade Fatura;
    	Algum serviço que tenha um método emitir;
    	Algum atributo com o nome de data limite.
```
Usar nomes em métodos ou classes que dizem exatamente “o que” essas classes ou métodos fazem, mas não “como” elas fazem. 


#### Integração entre sistemas: 
	
**Camada Anti-corrupção** - Quando se tem um sistema legado, com código muito bagunçado e uma interface complexa, e um novo sistema com o código bem feito utilizando boas práticas está sendo desenvolvido, cria-se uma camada de isolamento para fornecer aos clientes funcionalidade em termos de seu próprio modelo de domínio. A camada se comunica com o outro sistema através de sua interface existente, exigindo pouca ou nenhuma modificação no outro sistema. Internamente, a camada é traduzida nas duas direções conforme necessário entre os dois modelos. 


#### Integração contínua: 

**Núcleo Compartilhado** – Quando dois times alteram uma mesma base de código comum, é importante que esse pedaço de código esteja bem definido e que possua muitos testes automatizados, que devem ser rodados por qualquer um dos grupos que desejar fazer alguma alteração. Todas as alterações devem ser comunicadas ao outro time e os testes precisam fazer parte de um processo de Integração Contínua. Quando se usa um núcleo compartilhado, esse pedaço de código tende a ser mais difícil de mudar, já que precisa da aceitação de várias equipes. Por outro lado, evita-se algumas duplicações, já que conceitos comuns são codificados uma única vez e utilizados por vários sistemas;


#### Contextos delimitados:

**Mapa de Contextos** – Uma forma pragmática de documentar claramente os Contextos Delimitados que fazem parte de um sistema complexo. No mapa de contextos ressalta-se os vários componentes do software e como as equipes que cuidam desse sistema interagem. Muitas vezes, existem termos usados para um mesmo conceito em vários contextos (por exemplo, no contexto do sistema de cobrança usa-se o termo “Fatura”, que significa a mesma coisa que o termo “Nota Fiscal” no contexto do sistema de faturamento). Toda vez que o time do sistema de cobrança for conversar com o time de faturamento, ele terá que usar adequadamente o termo “Nota Fiscal” para que o outro time entenda o que está sendo dito; 




#### Referências de estudo:

- Vídeo aula 09: DDD
- https://www.youtube.com/watch?v=Swc2F6MPtnY
- https://pt.stackoverflow.com/questions/19548
- http://www.agileandart.com/2010/07/16/ddd-introducao-a-domain-driven-design/
- https://www.lambda3.com.br/2017/10/desmistificando-o-ddd/
- https://medium.com/@ppbruna/quero-aplicar-ddd-por-onde-come%C3%A7o-73c9390ca678
