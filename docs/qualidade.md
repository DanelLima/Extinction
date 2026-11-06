# Qualidade

[Voltar ao início](../README.md)

Resultados da execução de 22/10/2026 no MVP 1.0, em ambiente local com Docker Compose e o serviço de IA em CPU.

## Resumo

| Bateria | Resultado |
|---|---|
| Testes do backend, incluindo integração com MySQL via Testcontainers | 133 de 133 aprovados |
| Regressão do MVP 0.1 | 41 de 41 aprovadas |
| Regressão do MVP 0.2, com estresse do modo offline | 57 de 57 aprovadas |
| Testes de API do MVP 1.0 | 87 de 87 aprovadas |
| Análise do app (`tsc`, `expo export` e `expo-doctor`) | Sem erros, 21 de 21 verificações do `expo-doctor` |
| TLS no domínio público | TLS 1.3 com certificado válido |

## Desempenho

**Identificação de espécie:** 30 identificações com fotos diferentes tiveram média de 874 ms e p95 de 972 ms, para uma meta de até 5 s.

**Carga:** o JMeter simulou usuários autenticados percorrendo feed, mapa, enciclopédia e catálogo, com pausas de 1 a 3 s entre as telas.

| Execução | Requisições | Sucesso | Média | Mediana | p95 | Vazão |
|---|---:|---:|---:|---:|---:|---:|
| 1 usuário, 90 s | 41 | 100% | 17,1 ms | 15 ms | 28 ms | 0,5 req/s |
| 100 usuários, 180 s | 7.836 | 100% | 11,7 ms | 8 ms | 28 ms | 49,8 req/s |

O JMeter rodou na mesma máquina do backend e a execução-base tem poucas amostras. O teste mostra que 100 usuários não degradaram o tempo de resposta nesse ambiente, mas a média menor com carga não deve ser lida como ganho real.

## Segurança

A varredura autenticada do OWASP ZAP foi feita a partir do OpenAPI, em uma cópia descartável do backend.

| Risco | Alertas |
|---|---|
| Alto | 0 |
| Médio | 0 |
| Baixo | 2 |
| Informativo | 3 |

## Defeitos encontrados pelos testes

- **Corpo multipart malformado:** a primeira varredura do ZAP mostrou respostas 500 em quatro endpoints. Agora a API responde 400, e a varredura final confirmou a correção.
- **Token de conta excluída:** com o feed público, um token de conta excluída deixou de receber 401. A regressão pegou a falha, e agora um token inválido recebe 401 em qualquer rota de dados.
- **Medição de identificação:** respostas 503 do serviço ainda em carregamento entravam na média. O script passou a esperar o serviço e a medir só respostas bem-sucedidas.
- **Catálogo de conservação:** com 5 espécies, quase tudo aparecia como "Não avaliado". O catálogo foi ampliado para 56 espécies brasileiras.

## Integração contínua

O GitHub Actions executa os testes do backend com JDK 17 em pushes na `main` e pull requests que alteram o backend.

## O que ainda falta validar

| Item | Situação |
|---|---|
| Login com Google e Apple | Código pronto, credenciais externas pendentes |
| Push no aparelho | Verificação no APK pendente |
| Usabilidade com 10 pessoas | Não executado |
| Paridade entre Android e iOS | Não executado, exige build para iPhone |
| Consumo de bateria | Medição em aparelho real pendente |
