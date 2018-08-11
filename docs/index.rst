![KAS Key Access SSH](netbox_logo.png "NetBox logo")

Author="Marcos Ferreira da Rocha"
EMail="marcos.fr.rocha@gmail.com"
Descr="Este script envia automatiza a geração e inserção de chave  pública em um servidor ssh."
version=1.0

source ~/.local/share/acesso/variables
name=kas
data=$(date +%d-%m-%Y-%H-%M-%S)


 ## Ajuda
	
	Todas as opções;
	
	-a --add 		Adiciona um nova conexão
	-c --conf		Lista os arquivos de configuração e diretórios do script
	-e --edit		edita o arquivo de  conexões
	-h --help		Exibe o menu de ajuda
	-i --import		importar registro de conexões
	-I --import-all		Importa  as chaves e as  conexões registradas
	-l --list		Lista as conexões registradas
	-n --new-key		Cria um novo par de chaves
	-r --reset		Limpar   registro de conexões
	-s --save-key		Salva o par de chaves utilizadas  pelo script  na home do usuário corrente
	   --set-editor		Configure o editor padrão
	   --uninstall		Remover o script	   
	-x --export		Exportar registro de conexões
	-X --export-all		Salva as chaves e as  conexões registradas
	   --install		Instala ou atualiza o Key Access ssh (kas)

	


## Ajuda-registro
	
	Para registrar uma nova  conexão siga o exemplo;

	$name -a servidor user@192.168.1.1

## Ajuda-export
	Para exportar todos os registros de conexões siga o exemplo;
	
	$name -e nome-do-arquivo
	$name --export nome-do-arquivo


## Ajuda-import


	Para importar todos os registros de conexões siga o exemplo;

	$name -i nome-do-arquivo
	$name --import nome-do-arquivo


## Ajuda-import-all


	Para importar todos os registros de conexões e chave ssh siga o exemplo;
	
	$name -I nome-do-arquivo
	$name --import-all nome-do-arquivo

## Ajuda-export-all
   

	Para exportar todos os registros de conexões e chave ssh siga o exemplo;

	$name -X nome-do-arquivo
	$name --export-all nome-do-arquivo


## Config
	Abaixo é apresentado o conjuto de  diretórios e arquivos que compõem a aplicação

	access_functions	Armazena as conexões registradas
	~/.local/share/acesso/	Armazena os arquivos de configuração da aplicação
	~/.bashrc		Exportar o arquivo access_functions para o shell corrent
	~/.zshrc		Exportar o arquivo access_functions para o shell corrente
	~/.ssh/			Diretório utilizado para  acessar o par de chaves
	/usr/bin/		Diretório com  script executável