# Orientações e procedimentos para o funcionamento

## Multitenancy

Em `resource/application.yml`, configurar o datasource root, que gerencia as conexões dos tenants.
Nele será criado uma tabela chamada `DataSourceConfig`, a qual será responsável por armazenar as credencias de acesso
dos clientes. *obs : pode ser substituido por um json, por exemplo.

## Tenants
** Lembrar de manter o hbm2ddl como create, para criação das entidades

select * from public.datasourceconfig ;
select * from city c ;

INSERT INTO public.datasourceconfig
(id,driverclassname, initialize, "name", "password", url, username)
VALUES( 0,'org.postgresql.Driver', false, 'local', 'admin', 'jdbc:postgresql://localhost:5432/codingworld?ApplicationName=MultiTenant', 'postgres');
