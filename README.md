# Seminario_ASA

# Controle de Recursos em Containers Docker

## Objetivo
Testar limites de CPU e memória em containers Docker.

## Configuração
- CPU: 0.5 (50% de um núcleo)
- Memória: 200MB

## Execução

Subir o ambiente:
docker-compose up -d

Verificar:
docker stats

## Teste de carga

Foi utilizado Apache Bench:
ab -n 1000 -c 50 http://localhost:8080/

## Resultados

- O container respeitou o limite de CPU (~50%)
- A memória não ultrapassou 200MB
- Sob carga, o tempo de resposta aumentou

## Conclusão

Os limites foram aplicados corretamente, comprovando o controle de recursos em containers.