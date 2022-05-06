# DESAFIO 1 SEMANA BIG DATA

você foi selecionado para participar de um projeto, sabemos que encontra-se bastante empolgado para iniciar sua jornada como DEV BIG DATA, então elaboramos um desafio para que você possa treinar suas habilidades.

### IMPORTANTE

este desafio não é obrigatório, tem apenas como finalidade passar um cenário de um projeto possível, para que vocês tenham uma noção como é o dia a dia de um Engenheiro de Dados. 
**não existe maneira certa ou errada de fazer invente a sua**.

* Pesquize
* Converse com seus Amigos
* Compartilhe seus resultados em suas redes
* Se divirta
* Aprenda bastante
* Usem o github

## ESCOPO

você receberá em um pacote desafio_bigdata.zip que ira conter uma pasta "dados" com pastas e arquivos para serem ingeridos no HDFS, note que dentro da pasta dados existe uma ordem para que os arquivos sejam ingeridos, 1_ingestao, 2_ingestao, 3_ingestao, dentro de cada pasta possui um arquivo com dados_clientes.txt na sequencia de criação dos arquivos e uma pasta vazia de "scripts" onde vocês deverão criar dois arquivos em shell para executar os processos de criação do ambiente e a execução dos processos.

Layout da Pasta    
- desafio
    - dados
        - 1_ingestao/dados_cliente.txt
        - 2_ingestao/dados_cliente.txt
        - 3_ingestao/dados_cliente.txt
    - scripts
        - rollout.sh
        - job.sh
       
## Etapas e Explicações

1 - Efetuar o Download do pacote usando o CURL ou usar o Github para clonar o projeto

https://github.com/caiuafranca/desafio_bigdata/archive/refs/heads/main.zip

ou git clone https://github.com/caiuafranca/desafio_bigdata.git

2 - No "Namenode" o pacote desafio_bigdata-main.zip, que deverá ser descompactado em /home/'SEU NOME'/implantacao (lembre-se de criar o diretorio)

o pacote:

desafio_bigdata-main terá a pasta "dados" e dentro as pastas com os arquivos para serem ingeridas e a pasta "script" onde você criara os scripts de rollout.sh (existe um template) e job.sh (existe um template)

# TAREFA
no HDFS você terá que criar a segunte estrutura de diretórios

- /dados/indiana_jones/in
- /dados/indiana_jones/process
- /dados/indiana_jones/delete

1 - você terá que criar um script shell parta efetuar a criação (rollout) da estrutura que pode ser chamado de rollout.sh, neste script deverá ter todo o processo de criação das pastas e permissionamento

2 - Criar outro script em shell (job.sh) para efetuar o trabalho de migração dos arquivos do linux para o hdfs.

## Regras de Negócio (Atenção as Regras):

- RN01 - na pasta /dados/indiana_jones/in só deverá conter o arquivo de ingestão mais atual
- RN02 - na pasta /dados/indiana_jones/process deverá conter os arquivos já processados que tenham menos de 1 dias, arquivos com mais de  1 dias deve ser migrado para a pasta de delete 
- RN03 - na pasta /dados/indiana_jones/delete terá os arquivos compactados(tar/zip/tar.gz) com a data de compactação ex. dados_clientes_05052022.tar

### OBS 

usem e abusem do echo para evidenciar o seu processo em tela

echo "Aproveitem a Jornada para adquirir conhecimento"
