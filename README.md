# Orientações e procedimentos para o funcionamento

## Multitenancy

Em `resource/application.yml`, configurar o datasource root, que gerencia as conexões dos tenants.
Nele será criado uma tabela chamada `DataSourceConfig`, a qual será responsável por armazenar as credencias de acesso
dos clientes. *obs : pode ser substituido por um json, por exemplo.

