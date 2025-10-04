# Respostas do Lab Abaixo

Acesse o switch SW1 e aplique as seguintes configurações:

```cisco
enable
configure terminal
alias exec shint show interfaces
alias exec shver show version
alias exec shrun show running-config
line console 0
 history size 50
 logging synchronous
line vty 0 4
 history size 50
 logging synchronous
exit
logging buffered 8192
service timestamps log datetime
end
write memory
```

### Explicação da Solução

1. **alias exec**: Cria atalhos para comandos comuns
2. **history size 50**: Configura o histórico de comandos para 50 linhas
3. **logging synchronous**: Evita interrupção de comandos por mensagens de log
4. **logging buffered 8192**: Configura buffer de log com 8192 bytes
5. **service timestamps log datetime**: Adiciona timestamp nas mensagens de log
6. **write memory**: Salva a configuração na NVRAM

### Verificação

Use os seguintes comandos para verificar a configuração:

```cisco
show alias
show history
show logging
```

