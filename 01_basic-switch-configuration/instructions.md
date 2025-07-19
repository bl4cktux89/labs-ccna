# Configuração Básica de Switch

Para esse laboratório, vamos utilizar como base o laboratório do nosso amigo, Jeremy, do canal Jeremy's IT Lab, ele usou o packet tracer.
Aproveita e já dá uma moral lá no [vídeo](https://www.youtube.com/watch?v=SDocmq1c05s&list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ&index=9) dele, maluco fez um curso completo, e gratuito, para o CCNA 200-301!

Eu uso o PNETLab, mas as imagens são compatíveis com o EVE-NG.

## Instruções

1. Altere o hostname do roteador e do switch para (R1 e SW1, respectivamente)
    - Utilize o comando '''hostname''' no modo de configuração global
2. Configure uma senha para o modo EXEC privilegiado sem criptografia (CCNA) em ambos os dispositivos
3. Retorne para o modo EXEC usuário e teste a senha aplicada
4. Veja a senha com o comando '''show running-configuration'''
5. Garanta que a senha atual, e todas as senhas futuras, sejam criptografadas
6. Veja novamente a senha com o comando '''show running-configuration'''
7. Configure uma senha criptografada e mais segura para acessar o modo EXEC privilegiado em ambos os dispositivos (Cisco)
8. Retorne novamente ao modo EXEC usuário e teste novamente a senha para acessar o modo EXEC privilegiado. Qual senha foi aceita?
9. Veja novamente as senhas com o comando '''show running-configuration'''
    - Qual o tipo de criptografia utilizada para a senha '''enable password'''?
    - Qual o tipo de criptografia utilizada para a senha '''enable secret'''?
10. Salve a configuração atual para que ela seja armazenada na configuração de startup
