#### Install Tools:
* Postman 
* Newman

#### Postman > Import: (Files)
* api_sandbox.postman_collection.json
* api_sandbox_prod.postman_environment.json
* globals.postman_globals.json

Obs.: Crie uma pasta com nome Postman no diretório "C" e salve os arquivos em "C:\Postman". 


##### Comando Newman para executar folder com cenarios validos 

newman run C:\Postman\api_sandbox.postman_collection.json -e C:\Postman\api_sandbox_prod.postman_environment.json -g C:\Postman\globals.postman_globals.json  --folder cenarios_validos --reporters cli,html --reporter-html-export C:\Postman\newman\reporter_cenarios_valid.html


##### Comando Newman para executar folder com cenarios invalidos

newman run C:\Postman\api_sandbox.postman_collection.json -e C:\Postman\api_sandbox_prod.postman_environment.json -g C:\Postman\globals.postman_globals.json  --folder cenarios_invalidos --reporters cli,json --reporter-json-export C:\Postman\newman\reporter_cenarios_invalid.json


##### Comando Newman para executar folder insertionbin usando conjunto de dados

newman run C:\Postman\api_sandbox.postman_collection.json -e C:\Postman\api_sandbox_prod.postman_environment.json -g 
C:\Postman\globals.postman_globals.json -d C:\Postman\bins_valid.json -n 4 --folder insertionbin --reporters cli,html --reporter-html-export C:\Postman\newman\reporter_insertionbin.html


##### Links Uteis

*Newman

Instalação: https://learning.getpostman.com/docs/postman/collection_runs/command_line_integration_with_newman/
Reporter: https://www.npmjs.com/package/newman-reporter-html ou https://www.npmjs.com/package/newman-reporter-text

*Jenkins

Download: https://jenkins.io/download/
Instalação: https://www.youtube.com/watch?v=za6O5yRxtGY
Integração: https://learning.getpostman.com/docs/postman/collection_runs/integration_with_jenkins/
