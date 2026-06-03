# Atividades Simulador SOSim

## Atividade 1: Criação de Processos

### a) Práticas de simulação

- Execute o simulador SOsim e identifique as quatro janelas que são abertas na inicialização.
<img width="868" height="890" alt="image" src="https://github.com/user-attachments/assets/798cff3a-0831-40ca-8959-bf31a934a0f3" />

- Crie um processo: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="520" height="309" alt="image" src="https://github.com/user-attachments/assets/9e4eb132-3d12-4450-940b-d67260ab3033" />

### b) Análise Prática

- Na janela Gerência de Processos, observe algumas informações sobre o contexto de software do processo como PID, prioridade, estado do processo e tempo de processador.
<img width="404" height="51" alt="image" src="https://github.com/user-attachments/assets/1580cba4-ab4e-4036-961b-89749470a717" />

- Na janela Gerência de Processador, observe o processo transicionando entre estados.
<img width="519" height="424" alt="image" src="https://github.com/user-attachments/assets/fdf4737d-f104-40f1-8a72-94f0fbd13d24" />

- Na janela Gerência de Processador, movimente a barra de Clock de UCP e observe as variações ocorridas.
<img width="168" height="63" alt="image" src="https://github.com/user-attachments/assets/d32d03b5-e663-4c55-bd35-1ab8d9250d72" />

**Observação:** *Na gerência de processos foi possível acompanhar os principais dados do processo criado, como PID, prioridade, estado e tempo de processador. Na gerência de processador, o processo alternou entre estados conforme o simulador executava, e a mudança no clock apenas alterou a velocidade com que essas transições eram percebidas.*

### c) Questão teórica para responder com a ajuda do simulador

- Com base na observação do comportamento do processo criado, identifique se o processo é I/O-bound ou CPU-bound? Justifique a resposta.

**Resposta:** *O processo criado é CPU-bound, porque passa a maior parte do tempo usando o processador e quase não fica bloqueado esperando operações de entrada e saída.*

## Atividade 2: Tipos de Processos

### a) Práticas de simulação

- Reinicialize o simulador.
- Crie um processo do tipo CPU-bound: janela Gerência de Processos / Criar - janela Criação de Processos / Criar (tipo de processo deve ser CPU-bound).
<img width="304" height="308" alt="image" src="https://github.com/user-attachments/assets/a3078e41-f59a-4181-aabd-9e6d283bdc4d" />

- Crie outro processo do tipo I/O-bound: janela Gerência de Processos / Cria - janela Criação de Processos / Criar (tipo de processo deve ser I/O-bound).
<img width="307" height="309" alt="image" src="https://github.com/user-attachments/assets/ac7f28a3-88f2-4b98-b0f6-d793f888e71b" />

### b) Análise Prática

- Na janela Gerência de Processos, observe as mudanças de estado dos dois processos.
<img width="523" height="130" alt="image" src="https://github.com/user-attachments/assets/c6f0bb2d-30a8-4ae1-8c38-4b10c8f070f6" />

- Na janela Gerência de Processador, observe o comportamento dos processos e as mudanças de contexto em função do tipo I/O-bound e CPU-bound.
<img width="516" height="421" alt="image" src="https://github.com/user-attachments/assets/55aba3cf-3571-41db-8db5-b13ab2e71817" />

- Na janela Gerência de Processos, compare a taxa de crescimento do tempo de processador dos dois processos.
<img width="404" height="68" alt="image" src="https://github.com/user-attachments/assets/162bcefa-8253-4cf5-b833-c20768092c9a" />

**Observação:** *Os dois processos tiveram comportamentos diferentes durante a execução. O CPU-bound permaneceu mais tempo usando o processador, enquanto o I/O-bound alternou mais vezes entre execução e espera, pois depende das operações de entrada e saída.*

### c) Questão teórica para responder com a ajuda do simulador

- Analise os efeitos gerados no caso de redução do tempo gasto na operação de E/S pelo processo I/O-bound.

**Resposta:** *Reduzindo o tempo gasto em E/S, o processo I/O-bound volta mais rápido para o estado de pronto. Com isso, ele passa a disputar o processador com mais frequência e pode aumentar seu tempo total de uso da CPU.*

## Atividade 3: PCB

### a) Práticas de simulação

- Reinicialize o simulador.
- Crie dois novos processos: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="521" height="187" alt="image" src="https://github.com/user-attachments/assets/98549728-7f9e-463e-92b2-14e8afe9f5f4" />

### b) Análise Prática

- Na janela Gerência de Processos / PCB, observe as informações sobre o contexto de software e hardware dos processos criados.
<img width="405" height="65" alt="image" src="https://github.com/user-attachments/assets/d9463233-ca28-4ad6-b56a-daf4da6c8a08" />

**Observação:** *O PCB mostrou as informações usadas pelo sistema para controlar cada processo. Algumas informações permaneceram fixas, como identificação e dados básicos, enquanto outras mudaram durante a execução, como estado, tempo de processador e informações ligadas ao contexto de hardware.*

### c) Questão teórica para responder com a ajuda do simulador

- Identifique quais informações do PCB são estáticas ou dinâmicas e quais fazem parte do contexto de software e do contexto de hardware.

**Resposta:** *As informações estáticas são aquelas que não mudam durante a execução, como PID e tipo do processo. As dinâmicas mudam com o tempo, como estado, prioridade dinâmica, tempo de processador e registradores. O contexto de software inclui PID, prioridade, estado e informações de controle do processo. O contexto de hardware inclui registradores, contador de programa e demais dados necessários para o processo continuar executando de onde parou.*
  
## Atividade 4: Estatísticas

### a) Práticas de simulação

- Reinicialize o simulador.
- Ative a janela de Estatísticas em Console SOsim / Janelas / Estatísticas.
<img width="585" height="300" alt="image" src="https://github.com/user-attachments/assets/1b5af7a1-906d-4b83-a3f7-c3e44f6f1fc3" />

- Crie dois novos processos: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="517" height="132" alt="image" src="https://github.com/user-attachments/assets/010ec53a-0547-4573-a1eb-fe0724ca3107" />

### b) Análise Prática

- Na janela Estatísticas, observe as informações: número de processos, estados dos processos e processos escalonados.
<img width="546" height="117" alt="image" src="https://github.com/user-attachments/assets/f08b0586-96d6-407f-8886-0976f5537913" />

**Observação:** *A janela de estatísticas permitiu acompanhar a quantidade de processos em cada estado e os processos escalonados. Conforme os processos mudaram de estado, os valores exibidos também mudaram, mostrando o funcionamento do escalonamento em tempo real.*

### c) Questão teórica para responder com a ajuda do simulador

- Observe que em alguns momentos existem processos no estado de pronto porém nenhum em estado de execução. Explique o porquê dessa situação.

**Resposta:** *Isso acontece porque o processador pode estar temporariamente sem executar nenhum processo durante uma troca de contexto, interrupção ou atualização interna do sistema. Mesmo havendo processos prontos, existe um pequeno intervalo até que algum seja escalonado.*

## Atividade 5: Log de Execução dos Processos

### a) Práticas de simulação

- Reinicalize o simulador.
- Ative a janela de Log em Console SOsim / Janelas / Log.
<img width="506" height="237" alt="image" src="https://github.com/user-attachments/assets/993e7717-b9bd-4ffe-b977-df01a6c1120e" />

- Crie dois novos processos do tipo CPU-bound: janela Gerência de Processos / Cria - janela Criação de Processos / Criar (tipo de processo deve ser CPU-bound).
<img width="518" height="174" alt="image" src="https://github.com/user-attachments/assets/210f8fa2-545d-41b4-aff2-7f39d129e5f6" />

### b) Análise Prática

- Na janela Log, observe as informações sobre as mudanças de estado dos processos observando o tempo que cada processo permanece nos estados de Execução e Pronto.
<img width="298" height="242" alt="image" src="https://github.com/user-attachments/assets/204b5a82-ed05-494c-8b61-161724f5e773" />

- Reinicalize o simulador parametrizando com um valor de fatia de tempo diferente observe as diferenças na janela Log.
<img width="181" height="68" alt="image" src="https://github.com/user-attachments/assets/d477dbaf-1964-454c-af19-b306695e8c9a" />
<img width="347" height="232" alt="image" src="https://github.com/user-attachments/assets/0aa6affa-fa97-40eb-8403-08ca846d8a38" />

**Observação:** *O log registrou as mudanças de estado dos processos e deixou claro quanto tempo cada um permaneceu em execução ou pronto. Ao alterar a fatia de tempo, a frequência das trocas de contexto mudou, já que os processos passaram a alternar mais ou menos vezes no uso da CPU.*

### c) Questão teórica para responder usando o simulador

- Analise comparativamente a concorrência de dois processos CPU-bound executando em dois sistemas operacionais que se diferenciam apenas pelo valor da fatia de tempo.

**Resposta:** *Com uma fatia de tempo menor, os processos alternam mais vezes entre pronto e execução, aumentando a quantidade de trocas de contexto. Com uma fatia maior, cada processo fica mais tempo seguido usando a CPU, diminuindo as trocas. O balanceamento continua parecido, mas a resposta do sistema muda.*

## Atividade 6: Suspensão e Eliminação de Processos

### a) Práticas de simulação

- Reinicalize o simulador.
- Crie dois novos processos: janela Gerência de Processos / Cria - janela Criação de Processos / Criar.
<img width="518" height="130" alt="image" src="https://github.com/user-attachments/assets/00021691-ddf1-46ad-a616-be8daad360eb" />

### b) Análise Prática

- Na janela Gerência de Processos, observe as informações sobre o contexto de software dos processos criados.
<img width="394" height="73" alt="image" src="https://github.com/user-attachments/assets/f175791f-c410-4289-bd46-f8de7f103648" />

- Na janela Gerência de Processador, observe a concorrência no uso do processador pelos dois processos.
<img width="517" height="423" alt="image" src="https://github.com/user-attachments/assets/ba87088b-0c89-49c9-a2b1-7c0dce6570f2" />

- Compare percentualmente os tempos de uso do processador entre os dois processos.
- Suspenda temporariamente um dos processos na janela Gerência de Processos / Suspender.
<img width="505" height="83" alt="image" src="https://github.com/user-attachments/assets/178b77ea-5261-4cd9-a9e4-f5c057facaf5" />

- Observe os estados dos processos, a concorrência no uso do processador e novamente compare percentualmente os tempos de uso do processador entre os dois processos.
- Libere o processo do estado de espera (suspenso) na janela Gerência de Processos / Prosseguir.
<img width="505" height="131" alt="image" src="https://github.com/user-attachments/assets/e2c7472c-b323-440c-83c8-e8581e7ae346" />

- Elimine um dos processos na janela Gerência de Processos / Finalizar.
<img width="501" height="166" alt="image" src="https://github.com/user-attachments/assets/da2358c4-2514-4714-b130-8a487ef2778c" />

**Observação:** *Com dois processos ativos, o uso do processador foi dividido entre eles. Ao suspender um processo, ele saiu da disputa pela CPU e o outro passou a concentrar mais tempo de processador; depois, ao prosseguir, o processo voltou a concorrer normalmente. Ao finalizar um processo, ele deixou de aparecer na gerência e seus recursos foram liberados.*

### c) Questão teórica para responder com a ajuda do simulador

- Ao se eliminar um processo em estado de suspenso, o processo não é eliminado imediatamente. Reproduza essa situação no simulador e explique o porquê da situação.

**Resposta:** *O processo suspenso não é eliminado imediatamente porque ele não está ativo na CPU naquele momento. O sistema precisa primeiro tratar a mudança de estado e liberar corretamente os recursos associados ao processo antes de finalizar sua execução.*

## Atividade 7: Escalonamento Circular

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="602" height="413" alt="image" src="https://github.com/user-attachments/assets/4b483f1d-d0aa-4d60-8e63-42fe8523a8c1" />

### b) Análise Prática

- Crie dois processos com a mesma prioridade (um CPU-bound e outro I/O-bound): janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="516" height="156" alt="image" src="https://github.com/user-attachments/assets/925cd7ff-a933-4289-a4ba-e74cf911cdad" />

- Na janela Gerência de Processos, observe o tempo de processador de cada processo durante dois minutos e as mudanças de estado. Após esse período anote o tempo de processador de cada processo. Analise o balanceamento no uso do processador pelos dois processos.
- Na janela Gerência de Processos finalize os dois processos.
<img width="518" height="207" alt="image" src="https://github.com/user-attachments/assets/0edae493-0252-4f0f-9151-bb1fa42587fe" />

- Na janela Gerência de Processador, aumente a fatia de tempo movimentando a barra de Fatia de Tempo.
<img width="161" height="62" alt="image" src="https://github.com/user-attachments/assets/d8da8dee-2461-4fe9-847c-147f5eae40d8" />

- Na janela Gerência de Processos, observe mais uma vez o tempo de processador de cada processo durante dois minutos e as mudanças de estado. Após esse período anote o tempo de processador de cada processo. Compare os tempos anotados nas duas e analise o resultado do balanceamento no uso do processador pelos dois processos. Identifique as causas da variação.

**Observação:** *No escalonamento circular, os processos de mesma prioridade alternaram o uso da CPU. O CPU-bound aproveitou melhor a fatia de tempo por estar quase sempre pronto para executar, enquanto o I/O-bound saiu mais vezes para espera. Ao aumentar a fatia de tempo, o CPU-bound passou a ficar mais tempo seguido na CPU, alterando o balanceamento observado.*

- ### c) Questão teórica para responder com a ajuda do simulador

Considere a concorrência, nesse tipo de escalonamento, com dois processo CPU-bound que não realizam operações de E/S. Qual o efeito da variação da fatia de tempo sobre o balanceamento no uso do processador?

**Resposta:** *Para dois processos CPU-bound, a variação da fatia de tempo quase não muda o balanceamento final do uso do processador. Como ambos sempre precisam de CPU e não fazem E/S, a tendência é dividir o processador de forma equilibrada. A diferença principal fica na quantidade de trocas de contexto.*

## Atividade 8: Escalonamento Circular com Prioridades Estáticas I

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular com Prioridades Estáticas: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="602" height="414" alt="image" src="https://github.com/user-attachments/assets/20efc6d1-d61f-4640-8622-72582a1beb8f" />

### b) Análise Prática

- Crie um processo CPU-bound com prioridade 3 e um outro I/O-bound com prioridade 4: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="513" height="126" alt="image" src="https://github.com/user-attachments/assets/e5b6ee4e-91f4-4d53-9216-32fb87dd58bb" />

- Na janela Gerência de Processos, observe o tempo de processador de cada processo durante dois minutos e as mudanças de estado. Após esse período anote o tempo de processador de cada processo.
<img width="400" height="75" alt="image" src="https://github.com/user-attachments/assets/25acc015-0961-4083-94ee-fd6674e71cfd" />

- Verifique a preempção por prioridade que ocorre toda vez que o processo I/O-bound de maior prioridade passa para o estado de Pronto.
- Analise o balanceamento no uso do processador pelos dois processos comparativamente a Atividade 1.

**Observação:** *Como o processo I/O-bound foi criado com prioridade maior, ele recebeu preferência sempre que voltou para o estado de pronto. Isso causou preempção sobre o CPU-bound, mas o CPU-bound ainda conseguiu executar nos intervalos em que o I/O-bound estava em espera por E/S.*

### c) Questões teóricas para responder com a ajuda do simulador

- Quais devem ser os critérios para determinar as prioridades dos processos?

**Resposta:** *As prioridades devem considerar a importância do processo, o tempo de resposta esperado, o tipo de processo e o impacto dele no sistema. Processos interativos ou de E/S geralmente precisam de prioridade maior para responderem mais rápido.*

- Caso, nesse escalonamento, todos os processos sejam criados com a mesma prioridade, qual o benefício dessa política sobre o Escalonamento Circular?

**Resposta:** *Se todos os processos tiverem a mesma prioridade, essa política fica praticamente igual ao escalonamento circular. O benefício da prioridade só aparece quando os processos têm prioridades diferentes.*

## Atividade 9: Escalonamento Circular com Prioridades Estática II

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular com Prioridades Estáticas: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="588" height="375" alt="image" src="https://github.com/user-attachments/assets/63ae626d-6f8b-4fee-8f7e-d4e235d30678" />

### b) Análise Prática

- Crie um processo CPU-bound com prioridade 4 e um outro I/O-bound com prioridade 3: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="520" height="125" alt="image" src="https://github.com/user-attachments/assets/36094788-8a11-4781-87b8-e47a12bf10c0" />

- Na janela Gerência de Processos, observe o escalonamento dos dois processos. Analise o problema do starvation.

**Observação:** *Com o CPU-bound em prioridade maior, ele foi escolhido com mais frequência pelo escalonador, pois quase sempre estava pronto para executar. O processo I/O-bound, por ter prioridade menor, ficou em desvantagem e pôde permanecer aguardando por mais tempo, caracterizando o risco de starvation.*

### c) Questões teóricas para responder com a ajuda do simulador

- Por que o problema do starvation pode ocorrer?

**Resposta:** *O starvation pode ocorrer quando um processo de baixa prioridade fica esperando indefinidamente porque processos de maior prioridade continuam sendo escolhidos antes dele.*

- Cite duas ações que o administrador do sistema pode realizar quando é identificada a situação de starvation em um processo?

**Resposta:** *Duas ações possíveis são aumentar a prioridade do processo prejudicado ou ajustar a política de escalonamento para usar envelhecimento de prioridade, dando mais chance a quem espera por muito tempo.*

## Atividade 10: Escalonamento Circular com Prioridades Dinâmica

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular com Prioridades Dinâmicas: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="603" height="338" alt="image" src="https://github.com/user-attachments/assets/12f3c605-ae04-4a86-8821-e8d1b5b2ff4f" />

- Habilite as janelas de log e estatísticas: janela Console SOsim / Janelas.
<img width="1106" height="299" alt="image" src="https://github.com/user-attachments/assets/2034d4e4-ddc0-49d6-bdba-b4f9cb6394d6" />

- Na janela Gerência do Processador desloque a barra Frequência clock para a metade da escala.
<img width="170" height="64" alt="image" src="https://github.com/user-attachments/assets/dbccabff-e986-47fc-97d3-cdf4239b1d53" />

### b) Análise Prática

- Crie um processo CPU-bound com prioridade base 3 e mais três processos I/O-bound com prioridade base 4, porém com perfis diferentes (tipo 1, 2 e 3): janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="518" height="170" alt="image" src="https://github.com/user-attachments/assets/1dafd69a-c06a-44a0-b6d4-e4f81f7554b6" />

- Observe as prioridades base e dinâmica dos quatro processos na janela Gerência de Processos.
- Identifique os motivos das prioridades dinâmicas dos processos variarem ao longo do tempo.
- Observe na janela de log o valor do incremento recebido na prioridade de cada processo, Identifique o porquê das diferenças nos valores do incremento.
<img width="367" height="163" alt="image" src="https://github.com/user-attachments/assets/1de175f2-5a5d-45b8-821f-8e9aa95f1826" />
<img width="358" height="162" alt="image" src="https://github.com/user-attachments/assets/765e89f5-e7d7-4543-bad2-7f9c62d463b1" />
<img width="320" height="131" alt="image" src="https://github.com/user-attachments/assets/5a94eecf-fa7e-4b22-bf2d-773c5948b99a" />

- Observe na janela de estatísticas o percentual de utilização da UCP.
<img width="181" height="30" alt="image" src="https://github.com/user-attachments/assets/05e00577-b443-4d3c-8fe3-9666485ff863" />

- Suspenda o processo CPU-bound: janela Gerência de Processos / Suspender.
<img width="505" height="126" alt="image" src="https://github.com/user-attachments/assets/ba191ee6-3063-4083-b0f8-453b729d818d" />

- Observe na janela de estatísticas as mudanças no percentual de utilização da UCP e identifique o porquê.
<img width="590" height="301" alt="image" src="https://github.com/user-attachments/assets/9c3d0c30-7fe9-45a3-b062-f911780f8765" />

- Libere o processo CPU-bound do estado de suspenso: janela Gerência de Processos / Prosseguir.
<img width="510" height="172" alt="image" src="https://github.com/user-attachments/assets/db2a9ca4-282d-4f01-b660-bd49f939e007" />


**Observação:** *s prioridades dinâmicas mudaram conforme o comportamento dos processos durante a execução. Os processos I/O-bound receberam incrementos diferentes ao voltarem de espera para pronto, de acordo com o tempo e o perfil de bloqueio em E/S. Ao suspender o CPU-bound, a utilização da UCP mudou porque restaram processos que passam mais tempo esperando E/S.*

### c) Questão teórica para responder com a ajuda do simulador

- Qual o critério utilizado pelo sistema operacional para determinar diferentes valores de incremento à prioridade base de um processo quando há uma mudança do estado de espera para pronto?

**Resposta:** *O critério usado é o comportamento do processo. Processos que ficam mais tempo esperando E/S recebem incremento maior ao voltar para pronto, pois tendem a precisar de resposta rápida. Processos CPU-bound recebem menos incremento porque usam mais processador continuamente.*

## Atividade 11: Política de Busca - Paginação Antecipada

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="592" height="414" alt="image" src="https://github.com/user-attachments/assets/635439f5-25b0-4c83-a38f-5c91d46872f1" />

- Configure a política de busca de páginas antecipada: janela Console SOsim / Opções / Parâmetros do Sistema na guia Memória.
<img width="590" height="229" alt="image" src="https://github.com/user-attachments/assets/7c3ec933-a449-4ecb-b237-c31b0bb1d1ac" />

- Re-inicie o simulador SOsim para que a nova parametrização passe a ser válida.

### b) Análise Prática

- Crie um processo CPU-bound: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="526" height="140" alt="image" src="https://github.com/user-attachments/assets/7a23ebb6-cf8a-4ecb-a0ed-ac5a4185d20d" />

- Ative a janela Contexto do Processo para visualizar a tabela de páginas do processo criado: Gerência de Processos / PCB na guia Tab. de Pag.
<img width="249" height="320" alt="image" src="https://github.com/user-attachments/assets/6006f242-2045-45e6-8149-79840ea45de8" />

- Verifique os valores do Bit de Validade (Bit V) nas Entradas das Tabelas de Páginas (ETP).
<img width="242" height="245" alt="image" src="https://github.com/user-attachments/assets/062d5970-ddec-4979-8191-81fb79f95c91" />

**Observação:** *Com a paginação antecipada, a tabela de páginas mostrou páginas já carregadas antes de cada acesso individual do processo. Isso indica que o sistema tentou trazer páginas para a memória principal previamente, reduzindo a chance de falta de página durante a execução.*

### c) Questão teórica para responder com a ajuda do simulador

- Quais as vantagens e/ou desvantagens de se trabalhar com paginação por demanda ou antecipada?

**Resposta:** *A paginação antecipada pode reduzir faltas de página, pois carrega páginas antes de elas serem usadas. A desvantagem é que pode carregar páginas desnecessárias, gastando memória e tempo de E/S. Na paginação por demanda, só são carregadas as páginas realmente usadas. A vantagem é economizar memória; a desvantagem é que podem ocorrer mais faltas de página durante a execução.*

## Atividade 12: Política de Busca - Paginação sob Demanda

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="600" height="323" alt="image" src="https://github.com/user-attachments/assets/22e093a9-b876-4adb-a138-bea868e980d5" />

- Configure a política de busca de páginas sob demanda: janela Console SOsim / Opções / Parâmetros do Sistema na guia Memória.
<img width="596" height="273" alt="image" src="https://github.com/user-attachments/assets/e880ad77-ab64-417b-a88f-8a48c8857831" />

- Re-inicie o simulador SOsim para que a nova parametrização passe a ser válida.

### b) Análise Prática

- Crie um processo CPU-bound: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="520" height="136" alt="image" src="https://github.com/user-attachments/assets/de1399ff-6c17-4cde-a0e5-3c7bcf1bc53f" />

- Ative a janela Contexto do Processo para visualizar a tabela de páginas do processo criado: Gerência de Processos / PCB na guia Tab. de Pag.
<img width="238" height="317" alt="image" src="https://github.com/user-attachments/assets/d00b57dd-b260-49f9-b361-c3fadb05d4d6" />

- Verifique os valores do Bit de Validade (Bit V) nas Entradas das Tabelas de Páginas (ETP) e o local em que se encontram as páginas.
<img width="246" height="298" alt="image" src="https://github.com/user-attachments/assets/05d14476-4aa2-4b12-a843-d2d428beb037" />

**Observação:** *Na paginação sob demanda, a tabela de páginas mostrou que nem todas as páginas estavam válidas no início. As páginas passaram a ser carregadas apenas quando o processo precisou acessá-las, ficando claro o uso do bit de validade para indicar o que estava ou não na memória.*

### c) Questão teórica para responder com ajuda do simulador

- Considerando as atividades práticas 11 e 12, quais as diferenças encontradas nas ETPs do processo criado? Justifique o motivo.

**Resposta:** *Na paginação antecipada, várias páginas já aparecem válidas na tabela porque foram carregadas antes do uso. Na paginação sob demanda, inicialmente menos páginas ficam válidas, pois elas só são trazidas para a memória quando o processo realmente acessa cada uma.*

## Atividade 13: Espaço de Endereçamento Virtual

### a) Práticas de simulação

- Execute o simulador SOsim e configure-o para trabalhar com Escalonamento Circular: janela Console SOsim / Opções / Parâmetros do Sistema na guia Processador.
<img width="580" height="342" alt="image" src="https://github.com/user-attachments/assets/1380a50f-6fbe-4d0e-ad57-9c96eddbb456" />

- Configure a política de busca de páginas sob demanda: janela Console SOsim / Opções / Parâmetros do Sistema na guia Memória.
<img width="604" height="279" alt="image" src="https://github.com/user-attachments/assets/9840fa51-fb1a-4b5a-b61a-37da9637ee77" />

- Re-inicie o simulador SOsim para que a nova parametrização passe a ser válida.

### b) Análise Prática

- Crie dois processos CPU-bound: janela Gerência de Processos / Criar - janela Criação de Processos / Criar.
<img width="515" height="164" alt="image" src="https://github.com/user-attachments/assets/7d9623d8-ccad-4d5d-a383-81fbdf1406aa" />

- Ative a janela Contexto do Processo para visualizar a tabela de páginas do processo criado: Gerência de Processos / PCB na guia Tab. de Pag.
<img width="346" height="319" alt="image" src="https://github.com/user-attachments/assets/fac4548f-0c0d-45ce-a348-3c0b98a95eb7" />

- Na janela Gerência de Memória observe a alocação dos frames na memória principal.
<img width="318" height="417" alt="image" src="https://github.com/user-attachments/assets/3abb26e8-b4c3-4b36-a775-03331f9cbb83" />

- Na janela Contexto do Processo observe as alterações nas tabelas de páginas dos dois processos navegando com as setas inferiores.
<img width="329" height="236" alt="image" src="https://github.com/user-attachments/assets/1cf18ad9-fcd2-48ba-b5d0-655a049d9738" />
<img width="323" height="240" alt="image" src="https://github.com/user-attachments/assets/4e4a0ad5-d27d-4723-a817-622a3522be1f" />

**Observação:** *Os dois processos criados passaram a ter tabelas de páginas próprias, mesmo usando a mesma memória física do sistema. Na gerência de memória foi possível observar os frames ocupados, enquanto no contexto de cada processo apareceram os mapeamentos entre páginas virtuais e frames físicos. Isso mostra que cada processo enxerga seu próprio espaço virtual.*

### c) Questões teóricas para responder com a ajuda do simulador

- Qual o espaço de endereçamento máximo de um computador?

**Resposta:** *O espaço de endereçamento máximo depende da arquitetura do computador e da quantidade de bits usada para endereçar memória. Por exemplo, em uma arquitetura de 32 bits, o limite teórico é 4 GB.*

- Qual o tamanho de uma página virtual? Quem define isso?

**Resposta:** *O tamanho da página virtual é definido pelo sistema operacional junto com a arquitetura de hardware. Ele depende da forma como a memória virtual foi implementada no sistema.*
