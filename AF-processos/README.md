## Exercício 1

Você deve escrever um programa em C em que o processo pai crie 2 processos filhos (fork()).

Para cada processo filho criado, o processo pai deve imprimir "Processo pai criou XXX", onde XXX é o PID do processo criado.

Cada processo filho deve apenas imprimir "Processo filho XXX criado", onde XXX é o PID do processo corrente (use a função getpid() para isso).

O processo pai (e apenas ele) deve imprimir "Processo pai finalizado!", somente após os filhos terminarem (use a função wait() para aguardar que os filhos terminem de executar).


## Exercício 2

Você deve escrever um programa C em que:

O processo principal crie 2 processos filhos.

Cada um dos processos filhos deve, por sua vez, criar mais três processos.

Cada processo filho (tanto do processo principal quanto dos criados no passo anterior) deve imprimir "Processo XXX, filho de YYY", onde XXX é o PID do processo em questão e YYY o PID do processo que o criou (use as funções getpid() e getppid() para isso).

Os processos netos (filhos dos filhos do processo principal) devem, após imprimir esta mensagem, aguardar 5 segundos antes de terminar (use a função sleep() para isso) 

Os processos que criaram filhos devem aguardar que seus filhos terminem de executar (utilize a função wait()).

Todos os processos filhos devem imprimir, ao finalizar, "Processo XXX finalizado", onde XXX é o PID do processo em questão.

O processo principal deve imprimir "Processo principal XXX finalizado", onde XXX é o PID do processo principal.
