# Resumo prova 1 de Sistemas Distribuídos




## 1 - Introdução aos Sistemas Distribuídos

Os sistemas distribuídos representam uma coleção de computadores autônomos que trabalham em conjunto para oferecer serviços integrados e o compartilhamento de recursos. Imagine uma equipe onde cada membro tem funções específicas, mas o resultado final é o da cooperação de todos, sem que o usuário precise identificar cada parte. Esses sistemas, através do uso de uma rede e de protocolos padronizados, proporcionam transparência, escalabilidade e tolerância a falhas. O sistema esconde a complexidade interna da distribuição dos dados e da computação, permitindo que o usuário interaja com o serviço de maneira unificada, como se estivesse lidando com um único computador. Esse ambiente permite que a sobrecarga seja distribuída, possibilitando maior eficiência e desempenho, mesmo com a falha de um ou mais nós da rede.

Tópicos – Palavras-Chave:

    Sistema Distribuído: Conjunto de computadores interligados que cooperam de forma transparente.

    Transparência: O usuário não percebe a distribuição interna dos recursos.

    Escalabilidade: Facilidade de incrementar a capacidade adicionando novos nós.

    Tolerância a Falhas: Continuidade dos serviços mesmo diante de falhas parciais.

Cada nó do sistema é conectado por meio de protocolos de rede, como TCP/IP, que garantem a comunicação confiável entre os componentes. Para manter a consistência dos dados, algoritmos de consenso (por exemplo, Paxos ou Raft) são empregados, assegurando que todas as partes do sistema "conversem" sobre o estado atual dos recursos. Ainda, o sistema se beneficia de métodos de replicação que garantem a integridade dos dados mesmo quando ocorrem falhas. Essa abordagem permite que o serviço seja sempre contínuo e adaptável, possibilitando o aumento dinâmico do poder de processamento e armazenamento conforme a demanda cresce. Assim, os sistemas distribuídos não só ampliam a capacidade computacional, mas também aumentam a segurança e a confiabilidade do processamento.

O ambiente distribuído também se diferencia pelo fato de que cada máquina pode ser heterogênea – variando em hardware, sistema operacional e até em localização geográfica – mas todas se comunicam por meio de interfaces e protocolos padronizados. Essa heterogeneidade exige um design cuidadoso, onde todos os nós participam de uma arquitetura de colaboração que, apesar das diferenças internas, garante uma operação coerente. O compartilhamento de recursos ocorre de maneira sincronizada, evitando discrepâncias e garantindo que o sistema opere de forma consistente. Dessa forma, o conhecimento desses mecanismos é essencial para a construção de aplicações em larga escala, como serviços em nuvem e sistemas empresariais globais.

A robustez desses sistemas depende da capacidade de monitorar e gerenciar o ambiente distribuído, integrando ferramentas para a detecção rápida de falhas e a ativação de protocolos de recuperação. Essa adaptação permite que o sistema continue operando mesmo quando uma parte deixa de funcionar temporariamente. A replicação e o balanceamento de carga são estratégias que garantem que a comunicação e o processamento não fiquem comprometidos devido a interrupções inesperadas. Por fim, a integração dos componentes de segurança – autenticação, autorização e criptografia – assegura que o ambiente distribuído funcione de forma confiável e protegida contra ataques.

A concorrência e o paralelismo são conceitos fundamentais na computação que, apesar de relacionados, tratam de aspectos diferentes do processamento de tarefas. A concorrência diz respeito à capacidade de um sistema gerenciar e progredir em múltiplas tarefas em um mesmo intervalo de tempo, mesmo que, fisicamente, elas não sejam executadas simultaneamente. Ela se baseia na interleaving das instruções, onde o processador alterna entre as tarefas, criando a ilusão de execução simultânea. Por sua vez, o paralelismo exige hardware com múltiplos núcleos ou processadores para que diferentes tarefas sejam de fato executadas ao mesmo tempo. Assim, enquanto a concorrência se concentra na lógica de dividir e gerenciar tarefas, o paralelismo depende dos recursos físicos para realizá-las simultaneamente, contribuindo para a melhoria do desempenho quando bem aplicados. Em sistemas modernos, é comum que a concorrência seja utilizada para organizar o fluxo de execução e o paralelismo para acelerar operações pesadas, aproveitando o hardware disponível.

Tópicos – Palavras-Chave:

    Concorrência: Intercalação de tarefas para progredir independentemente; não necessariamente simultânea.

    Paralelismo: Execução simultânea de tarefas utilizando múltiplos processadores ou núcleos.

    Interleaving: Alternância rápida entre tarefas que cria a ilusão de simultaneidade.

    Hardware Multiprocessado: Componentes físicos (núcleos ou processadores) que possibilitam a execução paralela efetiva.

## 2 - Recapitulação dos Sistemas Operacionais

Os sistemas operacionais são o coração da computação, atuando como gerentes que organizam e distribuem os recursos de hardware para as aplicações que estão em execução. Pense neles como o maestro de uma grande orquestra, onde cada músico (processo) tem a sua parte para tocar, e o resultado final depende da perfeita coordenação entre todos. O sistema operacional gerencia os processos através de estruturas como o Process Control Block (PCB), que contém informações essenciais como o estado do processo, o contador de programa e a pilha de execução. Essa administração complexa garante que os processos recebam sua “fatia” de tempo de CPU e que as transições entre eles ocorram de maneira rápida e eficiente. Cada processo é isolado, mas o sistema operacional possibilita a comunicação entre eles através de mecanismos de Inter Process Communication (IPC), tais como pipes, filas de mensagens e memória compartilhada.

Tópicos – Palavras-Chave:

    Processo: Programa em execução, representado por um PCB.

    Troca de Contexto: Salvamento e restauração do estado dos processos para permitir a multitarefa.

    IPC (Comunicação entre Processos): Mecanismo que permite que processos troquem informações e coordenem suas atividades.

    Syscall: Função que permite que processos solicitem serviços do kernel do sistema operacional.

A gestão de memória é outro aspecto crucial, onde o sistema operacional aloca espaço para processos e gerencia a memória virtual. Técnicas como a paginação e a segmentação garantem que cada processo opere dentro de seu espaço, sem interferir nos demais. Essa divisão interna permite que o gerenciamento dos recursos se torne mais eficiente, possibilitando que o sistema execute múltiplos processos de forma simultânea. As chamadas de sistema (syscalls) são a interface que o software utiliza para interagir com o hardware de forma segura. Essa integração entre gerenciamento de processos, alocação de memória e comunicação é fundamental para a estabilidade do ambiente computacional.

A administração do escalonamento é de extrema importância, pois é o mecanismo que determina a ordem de execução dos processos. Algoritmos como round-robin, escalonamento por prioridades e outros mecanismos avançados são empregados para distribuir os recursos de forma justa e eficiente. Essa alternância rápida entre os processos permite que mesmo um único processador execute múltiplas tarefas sem dar a impressão de lentidão. Com essas técnicas, o sistema operacional mantém a responsividade e a eficiência, mesmo sob condições de carga elevada. Dessa forma, o gerenciamento intrincado dos processos e a capacidade de alternar entre eles são essenciais para o funcionamento harmonioso do computador.

A segurança do sistema operacional é outro pilar essencial, que utiliza métodos de proteção para evitar acessos não autorizados e preservar a integridade dos dados. A diferenciação entre o espaço de usuário e o espaço do kernel protege o sistema contra falhas e ataques. Em suma, o sistema operacional orquestra a execução dos processos e a distribuição dos recursos, funcionando como o gerente indispensável para a operação de qualquer aplicação moderna.

Signals, pipes e sockets são mecanismos de comunicação entre processos e entre computadores. Signals são formas de enviar notificações ou interrupções a um processo; eles geralmente são usados para alertar a ocorrência de eventos especiais, como a necessidade de terminar um processo ou a chegada de uma mensagem crítica. Pipes são canais unidirecionais utilizados para a comunicação entre processos que compartilham um mesmo sistema operacional, permitindo que a saída de um processo seja a entrada de outro. Por sua vez, sockets são interfaces de comunicação que permitem a transmissão de dados entre processos em computadores diferentes através de redes, utilizando protocolos como TCP/IP ou UDP. Esses mecanismos são fundamentais para a construção de sistemas distribuídos, onde a troca de informações entre componentes remotos deve ser realizada de forma segura, robusta e eficiente. Eles possibilitam, por exemplo, que aplicações web comuniquem-se com servidores e bancos de dados, ou que aplicações móveis se conectem a serviços na nuvem.

Tópicos – Palavras-Chave:

    Signals: Notificações ou interrupções enviadas a processos para indicar a ocorrência de eventos.

    Pipes: Canais unidirecionais para comunicação entre processos no mesmo sistema.

    Sockets: Interfaces para comunicação bidirecional entre processos, frequentemente usados em redes (TCP/IP, UDP).

    IPC: Inter Process Communication – conjunto de técnicas para que os processos troquem informações.

## 3 - Threads e Escalonamento

As threads são subdivisões dentro de um processo que permitem a execução concorrente de múltiplas tarefas, proporcionando uma abordagem leve para a implementação de multitarefa. Imagine um livro em que cada capítulo (thread) é lido simultaneamente para acelerar a compreensão do conteúdo; essa é a função das threads, que compartilham o mesmo espaço de memória, mas possuem seus próprios contadores de programa e pilha de execução. Essa característica permite que a comunicação interna seja rápida e evita o overhead associado à criação de processos completos. Por essa razão, aplicações que requerem alta performance, como servidores web e sistemas em tempo real, se beneficiam enormemente do uso de threads.

Tópicos – Palavras-Chave:

    Thread: Unidade leve de execução dentro de um processo.

    Kernel-Level Threads: Gerenciadas diretamente pelo sistema operacional, permitindo escalonamento em múltiplos núcleos.

    User-Level Threads: Geridas por bibliotecas na aplicação, com menor overhead mas com limitações quanto a operações bloqueantes.

    Escalonamento: Algoritmo que determina a sequência de execução das threads para maximizar o uso do processador.

Existem dois principais modelos de threads: as kernel-level, que são controladas pelo próprio sistema operacional e se beneficiam de um melhor suporte em sistemas multiprocessados, e as user-level, que são gerenciadas internamente pela biblioteca do aplicativo. Enquanto as kernel-level threads tendem a ter um overhead maior devido às chamadas de sistema necessárias, as user-level threads são mais eficientes na criação e troca de contexto. Contudo, em situações onde uma thread realiza uma chamada bloqueante, as user-level threads podem limitar a performance, já que o kernel não gerencia sua escalonamento de forma independente. Essa distinção influencia a escolha do modelo de thread conforme o perfil e a demanda da aplicação. Em ambientes complexos, muitas vezes utiliza-se uma combinação dos dois tipos para balancear desempenho e funcionalidade.

O escalonamento de threads envolve técnicas preemptivas e não-preemptivas. No modelo preemptivo, o sistema interrompe a execução de uma thread para dar oportunidade a outra, garantindo que nenhuma thread monopolize o processador por muito tempo. Já no modelo não-preemptivo, a própria thread precisa ceder a CPU, geralmente utilizando uma função de yield. Essas abordagens possuem implicações diretas na responsividade e na eficiência do sistema. Ferramentas de monitoramento e algoritmos avançados são empregados para otimizar a distribuição do tempo de CPU entre as threads, evitando situações de starvation. Dessa forma, o escalonamento eficiente permite que todas as partes do programa sejam executadas sem que haja atrasos ou interrupções prejudiciais.

Kernel-level threads e user-level threads diferem principalmente na forma como são gerenciadas e na integração com o sistema operacional. As kernel-level threads são gerenciadas diretamente pelo kernel, o que permite que o escalonador do sistema operacional distribua as threads entre os diferentes núcleos disponíveis. Essa abordagem oferece um suporte nativo para multiprocessamento e facilita a execução paralela; entretanto, ela envolve um overhead maior devido às chamadas de sistema necessárias para a criação e gerenciamento dessas threads. Em contraste, as user-level threads são controladas por bibliotecas do próprio aplicativo e operam inteiramente no espaço do usuário. Isso permite uma criação e troca de contexto muito mais rápida, pois não há a necessidade de envolvimento do kernel; entretanto, sua desvantagem aparece quando uma thread realiza uma operação bloqueante, fazendo com que todo o processo possa ficar bloqueado, uma vez que o kernel não tem visibilidade detalhada sobre elas.

Tópicos – Palavras-Chave:

    Kernel-Level Threads: Gerenciadas pelo sistema operacional; escalonamento nativo; maior overhead.

    User-Level Threads: Gerenciadas por bibliotecas; criação e troca de contexto mais eficientes; vulneráveis a bloqueios em operações de E/S.

    Overhead: Custo extra de processamento devido à interação com o kernel.

    Bloqueio: Situação em que uma thread impede que outras sejam executadas devido à operação bloqueante.

A comunicação entre threads é geralmente feita através de variáveis compartilhadas, tornando imprescindível o uso de técnicas de sincronização para evitar condições de corrida. O compartilhamento de dados, se não for devidamente coordenado, pode levar a inconsistências e erros críticos na aplicação. O design cuidadoso desses mecanismos de sincronização é um dos maiores desafios na programação concorrente, e dominar essas técnicas é essencial para qualquer desenvolvedor. Assim, as threads proporcionam um meio eficaz de explorar o paralelismo e a concorrência em sistemas modernos.

Em síntese, as threads representam uma ferramenta poderosa para a execução simultânea de tarefas, permitindo uma resposta mais ágil e um melhor aproveitamento dos recursos do hardware. A escolha do modelo e o gerenciamento adequado dessas unidades de execução são fundamentais para alcançar o máximo desempenho e evitar problemas comuns como deadlocks e condições de corrida. Com essas estratégias, os sistemas modernos conseguem atender a demandas complexas e em tempo real, oferecendo alta performance e eficiência.

## 4 - Sincronização e Exclusão Mútua

A sincronização é o conjunto de mecanismos empregados para controlar o acesso a recursos compartilhados, garantindo que, em ambientes concorrentes, os dados sejam manipulados de forma ordenada e consistente. Imagine que várias pessoas tentem escrever no mesmo quadro-negro ao mesmo tempo; sem controle, a mensagem se tornaria ilegível. Da mesma forma, a exclusão mútua impede que múltiplas threads acessem simultaneamente uma região crítica, onde as alterações podem conflitar. Essa coordenação é vital para evitar condições de corrida – situações em que o resultado final depende da ordem em que as threads operam. O uso de locks, semáforos e monitores são exemplos desses mecanismos que organizam e sequenciam o acesso a áreas sensíveis do código.

Tópicos – Palavras-Chave:

    Exclusão Mútua (Mutex): Técnica que garante que apenas uma thread acesse uma região crítica por vez.

    Condição de Corrida: Situação em que a ordem de execução das threads afeta o resultado.

    Deadlock: Estado em que duas ou mais threads ficam bloqueadas, esperando indefinidamente por recursos.

    Lock: Objeto que, quando adquirido, impede que outras threads entrem em determinada seção do código.

A teoria por trás desses mecanismos baseia-se em garantir três propriedades essenciais: segurança (nenhuma thread acessa simultaneamente a região crítica), ausência de deadlock (as threads não ficam travadas permanentemente) e ausência de starvation (todas as threads eventualmente têm acesso ao recurso). Diversos algoritmos clássicos, como o de Peterson, demonstram como essas propriedades podem ser alcançadas em contextos de duas ou mais threads. A implementação desses algoritmos, contudo, demanda um controle rigoroso de variáveis compartilhadas e a utilização de operações atômicas, que garantem que determinadas operações sejam executadas sem interrupção. Tais operações frequentemente são implementadas no nível de hardware, mediante instruções como test-and-set.

Condições de corrida ocorrem quando duas ou mais threads acessam e modificam dados compartilhados sem a devida coordenação, levando a resultados inconsistentes. Por exemplo, considere um trecho de código onde duas threads tentam atualizar uma variável de saldo de uma conta simultaneamente. Se ambas lerem o saldo antes que qualquer uma escreva a nova quantia, o resultado final poderá não refletir a soma correta das operações. Tais trechos são considerados paralelizáveis quando podem ser divididos de modo que as tarefas ocorram em paralelo, mas requerem sincronização quando há acesso a dados compartilhados. Em uma implementação prática, áreas do código que efetuam cálculos independentes (como processamento de imagens ou transformações matemáticas) podem ser paralelizáveis, enquanto operações de escrita ou leitura compartilhada necessitam de mecanismos de bloqueio para evitar a condição de corrida. Essa distinção é crucial na implementação de sistemas concorrentes, uma vez que permite o aproveitamento máximo do paralelismo sem comprometer a consistência dos dados.

Tópicos – Palavras-Chave:

    Condição de Corrida: Situação onde a ordem dos acessos concorrentes afeta o resultado final.

    Região Crítica: Bloco de código onde o acesso simultâneo deve ser controlado.

    Trecho Paralelizável: Parte do código que pode ser executada em paralelo sem dependências críticas.

    Sincronização: Mecanismos (como locks, semáforos) para evitar inconsistências durante o acesso concorrente.

A integração de técnicas de sincronização com outras estratégias, como escalonamento e comunicação entre processos, compõe uma parte central no design dos sistemas concorrentes. A utilização de locks, por exemplo, é uma maneira simples e eficiente de proteger áreas críticas, mas seu uso inadequado pode gerar problemas como o deadlock. Por isso, a escolha e a implementação corretas desses mecanismos requerem um entendimento profundo tanto da teoria quanto das características específicas do ambiente de execução. Essa sinergia entre diferentes ferramentas de sincronização fortalece a robustez e a eficiência dos sistemas modernos.

Além dos locks, os semáforos fornecem um controle mais refinado, permitindo múltiplos acessos simultâneos quando adequado. Já os monitores, que encapsulam dados e métodos em uma única estrutura, oferecem uma abordagem elegante e menos propensa a erros, abstraindo a complexidade do gerenciamento de exclusão mútua para o programador. A escolha entre essas estratégias depende das necessidades específicas da aplicação e da carga de trabalho esperada, sendo fundamental a análise cuidadosa de cada caso para evitar problemas comuns.

Em resumo, a sincronização e a exclusão mútua formam a espinha dorsal do desenvolvimento de aplicações concorrentes, protegendo os dados e garantindo a execução ordenada das operações. O domínio dessas técnicas permite que desenvolvedores criem sistemas que operem de forma eficiente mesmo sob condições de alta demanda. A integração dessas abordagens, alinhadas com um escalonamento inteligente, assegura que os recursos sejam utilizados de forma ideal e que os resultados sejam sempre consistentes. Assim, a compreensão detalhada desses conceitos é essencial para a criação de soluções computacionais robustas.

## 5 - Semáforos

Os semáforos são mecanismos de sincronização que funcionam como contadores atômicos, controlando o acesso às regiões críticas pelos processos ou threads. Imagine um semáforo de trânsito ou um estacionamento com vagas limitadas: quando há vagas disponíveis, os carros (ou threads) podem avançar; quando não há, eles devem esperar sua vez. As operações básicas de um semáforo são wait() e signal(), que decrementam e incrementam o contador, respectivamente. Esse controle garante que o acesso ao recurso seja regulado e que nenhuma operação cause conflito ou sobrecarga. Dessa forma, os semáforos são uma ferramenta essencial para a regulação da concorrência em sistemas operacionais e aplicações paralelas.

Tópicos – Palavras-Chave:

    Semáforo: Variável especial que controla o acesso a regiões críticas por meio de operações atômicas.

    Operação wait(): Decrementa o contador; se o contador for zero, bloqueia a thread.

    Operação signal(): Incrementa o contador e desperta threads em espera.

    Busy Waiting: Técnica onde a thread continua checando a condição, consumindo recursos, se mal gerenciado.

Esses mecanismos podem ser implementados de forma binária, onde o semáforo assume os valores 0 e 1 (funcionando como um lock), ou como um contador que controla vários acessos simultâneos. Em ambientes como o problema produtor-consumidor, três semáforos são geralmente utilizados: um mutex para garantir a exclusão mútua, um empty para contar as vagas disponíveis no buffer e um full para contar a quantidade de itens prontos para consumo. Essa estratégia coordena a produção e o consumo dos itens sem que ocorram conflitos ou perda de dados. Cada operação sobre o semáforo é realizada de forma atômica, garantindo que o contador reflita corretamente a situação do recurso.

A importância de instruções atômicas, como test-and-set, não pode ser subestimada, pois elas garantem que as operações de wait() e signal() sejam executadas sem interrupção, evitando que duas threads modifiquem simultaneamente o contador. Essa consistência é o que torna os semáforos tão eficazes em ambientes concorrentes. Além disso, a implementação do gerenciamento das filas de espera permite que as threads bloqueadas sejam reativadas de forma ordenada, geralmente em ordem FIFO, garantindo justiça no acesso ao recurso. Essa prática é amplamente utilizada em sistemas de tempo real e aplicações críticas.

O design e a implementação corretos dos semáforos são essenciais para a construção de sistemas robustos. Erros na manipulação dos semáforos podem levar a deadlocks, onde as threads ficam bloqueadas indefinidamente, ou a condições de corrida, onde o acesso simultâneo prejudica os dados compartilhados. Assim, além da lógica de contagem, a atenção ao gerenciamento das filas de espera e à ordem de desbloqueio é crucial. Esses aspectos fazem dos semáforos uma ferramenta poderosa e flexível para a coordenação de operações concorrentes, garantindo a integridade e o bom funcionamento dos sistemas paralelos.

Em conclusão, os semáforos proporcionam um meio eficaz de regular o acesso simultâneo aos recursos, funcionando como contadores que, de forma atômica, permitem ou bloqueiam a execução de operações concorrentes. Essa robustez e flexibilidade os tornam indispensáveis em ambientes com alto grau de concorrência, onde o gerenciamento adequado dos recursos é crucial para a estabilidade do sistema.

## 6 - Monitores

Os monitores são estruturas de sincronização integradas à linguagem de programação que encapsulam tanto os dados compartilhados quanto os métodos de acesso a esses dados, garantindo exclusão mútua automaticamente. Imagine um guarda que controla o acesso a uma sala restrita, permitindo que somente uma pessoa entre por vez; essa é a função de um monitor. Dentro de um monitor, as threads podem chamar métodos para operar sobre os dados, mas apenas uma thread será executada a qualquer momento. Essa característica simplifica significativamente a programação concorrente, pois o mecanismo de exclusão mútua é gerenciado pelo próprio monitor, reduzindo o risco de erros. Além disso, monitores possuem variáveis de condição que permitem que threads esperem a ocorrência de um evento específico antes de continuar a execução, coordenando melhor o fluxo das operações.

Tópicos – Palavras-Chave:

    Monitor: Estrutura que encapsula dados e métodos, garantindo acesso exclusivo por vez.

    Variáveis de Condição: Variáveis que permitem que threads aguardem por condições específicas, utilizando métodos wait() e signal().

    Exclusão Mútua Automática: Garantia de que apenas uma thread execute um método do monitor a qualquer momento.

    Semântica Hoare vs. Mesa: Diferença na forma de transferência de controle entre threads após um signal().

Os monitores simplificam o gerenciamento da sincronização, pois o programador não precisa explicitamente adquirir ou liberar locks; isso é feito automaticamente quando uma thread entra ou sai do monitor. Essa abstração elimina muitos erros comuns na programação concorrente, como esquecer de liberar um lock. A utilização de monitores é comum em linguagens orientadas a objeto, como Java e C++, onde o bloco synchronized encapsula o acesso aos métodos críticos. Esse mecanismo torna o código mais legível e menos propenso a erros, pois a responsabilidade de gerenciar a exclusão mútua está centralizada e automatizada.

Além disso, os monitores podem implementar diferentes semânticas de signal() e wait(), como as abordagens Hoare e Mesa. Na semântica Hoare, o signal() transfere imediatamente a execução à thread que estava aguardando, enquanto na semântica Mesa, a thread sinalizada é colocada na fila de prontos e a thread que realizou o signal continua a execução, exigindo que a thread acordada revalide a condição esperada. Essa diferença pode impactar a forma como o código é escrito, exigindo o uso de laços (normalmente while) para garantir a correção quando se utiliza a semântica Mesa. Tais nuances são importantes para o desenvolvimento de aplicações concorrentes robustas.

A implementação de monitores também se beneficia de um design modular, onde o encapsulamento dos dados protege contra acessos indevidos e torna o código mais fácil de manter e evoluir. Essa abordagem reduz significativamente a complexidade da programação concorrente, ao mesmo tempo em que oferece mecanismos poderosos para coordenar a execução de múltiplas threads. Por meio desses recursos, os monitores garantem que a integridade dos dados seja preservada, mesmo quando muitas operações concorrentes estão em andamento.

Em síntese, os monitores elevam o nível de abstração na programação concorrente, integrando os mecanismos de sincronização diretamente na estrutura do código. Essa integração não só simplifica a implementação dos algoritmos concorrentes, mas também proporciona uma segurança adicional, ao encapsular os dados e proteger o acesso de forma automática. Dessa forma, os monitores são essenciais para o desenvolvimento de sistemas complexos, onde a simplicidade e a robustez são indispensáveis.

---

## 7 - Respostas às Questões da Lista

Para a primeira questão, que pede as diferenças entre concorrência e paralelismo, entende-se que a concorrência se refere à capacidade do sistema de gerenciar várias tarefas (ou threads/processos) de maneira intercalada, onde a execução dos processos se sobrepõe de forma lógica, embora fisicamente possam ser executadas por um único núcleo. Ou seja, a concorrência é a estratégia de dividir o tempo de CPU entre diversas tarefas, criando a ilusão de simultaneidade. Já o paralelismo consiste na execução real de múltiplas tarefas ao mesmo tempo, o que exige hardware com múltiplos núcleos ou processadores. Assim, enquanto a concorrência trata de como as tarefas se organizam e se alternam dentro do sistema, o paralelismo está diretamente ligado à capacidade física de realizar as operações simultaneamente. Essa interação entre concorrência e paralelismo é fundamental para projetar sistemas que sejam escaláveis e que maximizem o aproveitamento do hardware disponível.

Tópicos – Palavras-Chave:

    Concorrência: Organização intercalada de múltiplas tarefas.

    Paralelismo: Execução simultânea efetiva em múltiplos núcleos.

Na segunda questão, sobre a metodologia de análise e projeto para paralelização, é necessário adotar uma abordagem estruturada que inicie com a identificação de partes do código que podem ser executadas de forma independente (regiões paralelizáveis). Em seguida, deve-se realizar uma análise minuciosa das dependências entre esses trechos de código, identificando as áreas críticas onde o acesso compartilhado deverá ser protegido por mecanismos de sincronização (locks, semáforos, monitores). Após essa fase, o projeto deve definir qual será a estratégia de implementação, escolhendo entre threads, processos ou outras técnicas, e definindo o algoritmo de escalonamento que distribuira o tempo de CPU entre as tarefas. Finalmente, é crucial validar essa abordagem através de testes, a fim de garantir que não ocorram condições de corrida ou deadlocks, preservando a integridade dos dados e a consistência das operações.

Tópicos – Palavras-Chave:

    Análise de Dependências: Identificação de regiões críticas.

    Mecanismos de Sincronização: Locks, semáforos, monitores.

    Escalonamento: Distribuição do tempo de CPU.

A terceira questão solicita uma comparação entre kernel-level threads e user-level threads. As kernel-level threads são gerenciadas diretamente pelo sistema operacional e permitem que o escalonador disponha de suporte nativo para múltiplos núcleos, o que proporciona melhor aproveitamento em ambientes multiprocessados, embora essa abordagem gere um overhead maior devido às chamadas de sistema frequentes. Em contrapartida, as user-level threads, controladas por bibliotecas no espaço do usuário, têm criação, destruição e troca de contexto muito mais eficientes, mas apresentam a desvantagem de não serem visíveis ao kernel; consequentemente, se uma thread realizar uma operação bloqueante, todo o processo poderá ser afetado. Dessa forma, a escolha entre um e outro depende do equilíbrio entre desempenho e controle fino de execução.

Tópicos – Palavras-Chave:

    Kernel-Level Threads: Gerenciadas pelo SO, maior overhead, suporte multiprocessamento.

    User-Level Threads: Gerenciadas pelo aplicativo, troca de contexto rápida, vulneráveis a bloqueios.

Na quarta questão, que exige a elaboração de um código em Java para resolver um problema (como uma operação de retirada bancária) utilizando mecanismos de paralelização e sincronização, o conceito-chave é proteger as regiões críticas que envolvem a leitura e atualização de variáveis compartilhadas. O código exemplo utiliza o modificador synchronized para garantir que apenas uma thread execute o método de retirada de cada vez, evitando condições de corrida e garantindo que o saldo seja atualizado de forma correta. É importante também comentar e identificar os trechos paralelizáveis – partes do código que podem ser executadas em paralelo (como cálculos independentes), e aquelas que, por envolverem acesso a recursos compartilhados, necessitam de sincronização. Essa abordagem demonstra a aplicação prática dos conceitos teóricos na elaboração de um software paralelo seguro e eficiente.

Tópicos – Palavras-Chave:

    Região Crítica: Trecho onde o saldo é lido e atualizado.

    Synchronized: Mecanismo Java para exclusão mútua.

    Paralelização: Execução concorrente de trechos independentes.

A quinta questão aborda a explicação do que é uma condição de corrida e pede a ilustração com pseudocódigo dos problemas que ela pode causar. Uma condição de corrida ocorre quando duas ou mais threads acessam e modificam uma variável compartilhada sem a devida sincronização, podendo resultar em dados inconsistentes, pois o resultado final depende da ordem de execução dos acessos. Por exemplo, se duas threads leem um saldo antes de qualquer uma alterar o valor, o desconto realizado por ambas pode não ser somado corretamente, resultando em um valor final incorreto. O pseudocódigo serve para ilustrar como essa situação pode ocorrer, demonstrando que sem o controle adequado, as operações concorrentes podem produzir resultados imprevisíveis e indesejáveis.

Tópicos – Palavras-Chave:

    Condição de Corrida: Resultado dependente da ordem de acesso concorrente.

    Pseudocódigo: Exemplo ilustrativo dos erros sem sincronização.

    Região Crítica: Onde a inconsistência pode ocorrer.

Na sexta e última questão, que investiga a diferença entre a função signal() aplicada em semáforos e monitores, a resposta enfatiza que, em semáforos, a operação signal() ou sem_post() incrementa o contador e libera uma ou mais threads bloqueadas, enquanto em monitores, a operação equivalente (geralmente notify() ou signal()) atua sobre uma variável de condição. A diferença fundamental reside no comportamento de transferência de controle: na abordagem Hoare, o signal() transfere imediatamente a execução para a thread acordada, garantindo que a condição seja válida no momento da entrada; já na abordagem Mesa, a thread sinalizada é colocada na fila de prontos e, ao retomar, deve revalidar a condição, pois a thread que realizou o signal continua em execução. Essa distinção é essencial para o design correto de algoritmos concorrentes, pois afeta como a condição de espera é tratada e verificada.

Tópicos – Palavras-Chave:

    Semáforos - Signal(): Incrementa o contador e libera threads.

    Monitores - Signal()/Notify(): Acorda threads bloqueadas; semântica Hoare vs. Mesa.

    Revalidação da Condição: Necessária na semântica Mesa para garantir a correção.

---