# DESAFIO 1 SEMANA BIG DATA

você foi selecionado para participar de um projeto, sabemos que encontra-se bastante empolgado para iniciar sua jornada como DEV BIG DATA, então elaboramos um desafio para que você possa treinar suas habilidades.

### IMPORTANTE

este desafio não é obrigatório e tem apenas como finalidade passar um cenario de um projeto para que vocês tenham uma noção como é o dia dia de um Engenheiro de Dados, não existe maneira certa ou errada de fazer invente a sua.

* Pesquise
* Converse com seus Amigos
* Compartilhe seus resultados em suas redes
* Se divirta 

## ESCOPO

você recebera em um pacote desafio.tar que ira conter uma pasta dados com arquivos para serem ingeridos no HDFS, note que dentro da pasta existe uma ordem para que os arquivos sejam injeridos, 1 ingestao, 2 ingestao, 3 ingestao, dentro de cada pasta possui um arquivo com dados de cadastro de clientes na sequencia de criação dos arquivos e uma pasta vazia de scripts onde vocês deverão criar dois arquivos em shell para executar os processos de criação do ambiente e a execução dos processos.

Layout da Pasta
    
- desafio
    - dados
        - 1_ingestao/dados_cliente.txt
        - 2_ingestao/dados_cliente.txt
        - 3_ingestao/dados_cliente.txt
    - scripts
        - rollout.sh
        - job.sh
       
## Requisitos

no linux você recebera o pacote desafio.zip, que deverá ser descompactado em /home/'SEU NOME'/implantacao (lembre-se de criar o diretorio)

no pacote:

desafio terá a pasta dados e dentro as pastas com os arquivos para serem ingeridas e a pasta script onde você criara os scripts de rollout.sh e job.sh

no HDFS você terá que criar a segunte estrutura de diretórios

- /dados/indiana_jones/in
- /dados/indiana_jones/process
- /dados/indiana_jones/delete

1 - você terá que criar um script shell parta efetuar a criação (rollout) da estrutura que pode ser chamado de rollout.sh, neste script deverá ter todo o processo de criação das pastas e permissionamento

2 - Criar outro script em shell para efetuar o trabalho de migração dos arquivos que poderá ser chamado de job.sh

## Regras de Negocio:

- RN01 - na pasta /dados/indiana_jones/in só deverá conter o arquivo mais atual
- RN02 - na pasta /dados/indiana_jones/process deverá conter os arquivos já processados que tenham menos de 1 dias, arquivos com mais de  1 dias deve ser migrado para a pasta /dados/indiana_jones/delete compactado em tar com a data de compactação ex. dados_clientes_05052022.tar

### OBS 

usem e abusem do echo para evidenciar o seu processo em tela
