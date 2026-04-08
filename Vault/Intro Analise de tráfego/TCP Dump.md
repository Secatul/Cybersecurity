Permite visualizar todo o tráfego passante em uma rede, parecido com o [[Wireshark]]

## Exemplo:
`sudo tcpdump -nS host www.darknet.com.br`

`sudo` --> Te da permissões de root (admin)
`tcpdump` --> mostrar as capturas de rede
`-n` --> Não resolve nomes (não tenta converter IP para domínio) e nem porta (80 --> HTTP) fica mais rápido
`-S` --> Mostra números de sequência absoluta, sem isso ele normalmente mostra sequência relativa.
`host www.darknet.com.br` --> Somente mostra pacotes de ou para esse IP

Capture todos os pacotes TCP/IP indo ou vindo do IP 50.116.87.163, sem resolver nomes, 
mostrando detalhes completos.

`sudo tcpdump -i eth1 -nS host 8.8.8.8` 

em seguida em outro terminal
`ping -c 4 8.8.8.8` --> gerar tráfego.