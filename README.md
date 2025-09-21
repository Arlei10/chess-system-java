usecaseDiagram
    actor Cliente
    actor Worker
    actor Backup
    actor Orquestrador

    Cliente --> (Login)
    Cliente --> (Submeter Tarefa)
    Cliente --> (Consultar Status)

    Worker --> (Registrar-se no Orquestrador)
    Worker --> (Enviar Heartbeat)

    Orquestrador --> (Despachar Tarefa ao Worker)

    Backup --> (Sincronizar Estado via Multicast)
    Backup --> (Assumir em Falha do Primário)
