# Ataques-em-redes-WIFI
### HISTÓRICO ###

'Wi-fi ou Wireless Area Network (WLAN)
Parão - IEEE 802.11
Nome surgiu em agosto de 1999 criado pela Wi-fi Alliance
Utilizada em sua maioria em redes abertas ou com criptograia WEP.
WPA surge apenas em 2003 e é amplamente difundida apenas após 2009.'



Exemplos de sinais wifi - ondas eletros magneticas

Luz
ondas de radio
Som
Raio-Transmissão Max

todas elas atuam em frequencias diferentes...





# MAC ADDRESS

MAC ADDRESS = ENDEREÇO FISICO DE QUALQUER DISPOSITIVO QUE SE CONECTA NA REDE, VEM DE FABRICA DE CADA DISPOSITIVO


~~~~~~~~~~~~~~~~~~~~~~~~~~
				PADRÕES

Protocolo     |      Data        |    Frequência    |    Transmissão Max.	
              |                  |                  | 
IEEE 802.11   |  Junho - 1997    |     2.4 GHz	    |   2 Mbps
a             |  Setembro - 1999 |     3,7/5 Ghz    |   54 Mbps
b	      |  Setembro - 1999 |     2,4 Ghz      |   11 Mbps
g    	      |  Junho - 2003	 |     2,4 Ghz      |   54 MLbps
n             |  Outubro - 2009  |     2,4/5 Ghz    |   135 Mbps       

ac            |  Dezembro - 2013 |     5 GHz        |   780 Mbps
ad            |  Dezembro - 2012 |     60 GHz	    |   6,75 Gbps
ah            |  2016            |     0,9 GHz	    |
aj            |  2016            |     45/60 Ghz    |
ay            |  2017            |     60 GHz       |	100 Gbps
ax            |	 2019            |     2,4/5 GHz    |

~~~~~~~~~~~~~~~~~~~~~~~~~~




# CANAIS

Conexeção wifi opera em canais, faixa de frequencias diferentes
geralmente as redes atuais operam nas frequencias de 2,4 Ghz, mas existe sub-frequencias que estão dividindo os canais, cada canal é uma sub divisão

~~~~~~~~~~~~~~~~~~~~~~~~~~	

Canal 1   = 2.412    longe
Canal 2	  = 2.417
Canal 3   = 2.422
Canal 4   = 2.427
Canal 5   = 2.432
Canal 6   = 2.437    longe
Canal 7   = 2.442
Canal 8   = 2.447
Canal 9   = 2.452
Canal 10  = 2.457
Canal 11  = 2.462    longe


os canais tem uma largura de banda de 22 MHz, e eles se intrelassam, 
um canal esta sempre interferindo no outro, os canais que tem a maior
distancia um do outro é o 1,6 e 11 por isso se for fazer uma configuração 
em roteadores proximos usar esses canais
ainda existira interferencia, porem sera minima

~~~~~~~~~~~~~~~~~~~~~~~~~~










# CRIPTOGRAFIAS E AUTENTICAÇÕES


~~~~~~~~~~~~~~~~~~~~~~~~~~
-------------------------------------------------------------------------------------------  
OPEN
Rede aberta

-------------------------------------------------------------------------------------------  

				WEP (Wired-Equivalent Privacy)
			    "Uma segurança equivalente a cabeada"

	Secret Key and IV  "Seed"                         Secret Key and IV   "Seed"
		  |						    |
	     RC4 Algorithm	                               RC4 Algorithm
		 | |						   | |
	     0110001010  "Keystream"   				0110001010    "Keystream"
		XOR						   XOR
	     1001110101  "Plain Text and CRC"		      __ 0100110010    "Cipher Text"
		 | |					     |      | |
	     0100110010	 "Cipher Text"			     |	1001110101    "Plain Text and CRC"
		 |___________________________________________|
		          Transmitting message packet		                  

	     ENCRYPTION                                           DECRYPTION


Seed, vai gerar uma criptografia dos seus dados não criptografados, essa seed vai gerar a partir de uma chave ou seja sua senha + IV (Initialization vector(Vetor de Inicialização))

~~~~~~~~~~~~~~~~~~~~~~~~~~

-------------------------------------------------------------------------------------------       
			WPA (Wired Protected Acess) e TKIP
	Todos os dados trafegados com seu roteador são criptografadas,
	TKIP criptrofia avançada

º A tecnologia WPA, ficou disponível em 2003
º Possui 2 versões
º Utiliza TKIP/CCMP(AES) como algoritmos de criptografia
º TKIP é considerado vulnerável, porém o ataque é de extrema complexidade e limitado
º Muitos roteadores possuem WPS
º Ataques são baseados em Brute-force

WPA2 e AES
Criptografia mudou de TKIP para AES

WPA - Enterprise
Nada mais que um WAP, utilizado por algumas organizações utilizando varios rteadores

--------------------------------------------------------------------------------------------


				WPS (Wi-Fi Protected Setup)
	Visa Facilitar a configuração do roteador, trás com sigo muitas falhas

º Tem intuito de facilitar a conexão com roteador através de um PIN
º Possui uma falha gravíssima que leba a um ataque Brute-force
º Apenas 11 mil combinações

		PIN 1234  567   0
		    ___	  ___  ___
		     |	   |	|---> Digito verificador
		     |     |---> Segunda Parte( 3 Digitos) - 1000 combinações 
		     |-----> Primeira Parte(4 digitos) - 10000 combinações	



				Ataque PIXIE DUST WPS
º Falha Pixie Dust foi divulgada pela primeira vez por Dominique Bongard em julho de 2014
º As primeiras ferramentas automatizadas surgiram no início de 2015
º Falha ocorre por que alguns fabricantes definem uma fraca entropia na criação de hash de criptografia



ª E-HASH1 = (E-S1 || PSK1 || PKE || PKR)
ª E-HASH2 = (E-S2 || PSK2 || PKE || PKR)
	
========================================================================================================================================================================================

		ACESS POINTS E TIPOS DE REDES


AP(Acess Point) -BSSID - ESSID - BSSID, distribui o macadress do roteador  ESSID - é o nome da rede que você consegue ler(Nome do wifi)

Independent Basic Service Set (IBSS) - Wi-Fi Ad-hoc - Dois dispositivos se conectando ponto a ponto

BSS (Basic Service Set) - é o que estamos acostumado vendo no dia a dia uma rede local wireless


ESS (extended Service Set) - conjuto de varios roteadores, que compoe uma mesma rede

DS ( Distribution Systems) (DS) toda area que você tem para se conectar na rede


ANTENAS


Antenas Omnidirecionais
Propaga o sinal para todos os lados

Antenas Direcionais
Direciona o sinal para uma direção só


TP-LINK TL-WN722N










MAC ADDRESS - OO:11:FF:AF:55:11
ARP - PACOTE QUE JUNTA UM IP COM O MAC ADDRESS













*****************************ATAQUE A REDES WIRELESS***************************************

Capturando handshake e fazendo ataque de força bruta em wpa/wpa2


handshak = aperto de mãos, seria quando nosso computador tenta conectar com o roteador, capturando a senha criptografada e vamos usar um programa para descriptografar




========================================================================================================================================================================================

		    VISUALIZANDO AS INTERFACES
		        WIRELESS DISPONIVEIS


Após conectar o adaptador wireless á máquina virtual Kali, digite ("iwconfig") para ver as interfaces disponiveis em sua máquina virtual.

			SCAN PARA DESCOBRIR
			  PONTOS DE ACESSO

Agora podemos fazer um scan para procurar pontos de acesso nas proximidades.
O comando ("iwlist wlan0 scan") fará o scan à procura de pontos de acesso próximos usando a interface [wlan0].


			    MODO MONITOR

Antes de prosseguir, vamos colocar nosso adaptador em modo monitor.
De forma muiito semelhante ao modo promoscuo do Wireshark, o modo monitor permite ver o tráfego wireless adicional sobre o tráfego destinado ao adaptador wireless.
Usaremos o script Airmon-ng, que faz parte do pacote de avaliação wireless Aircrack-ng, para colocar o adaptador em modo monitor.
Inicialmente, certifique-=se de que nenhum processo em execução vá interferir no modo monitor digitando ("airmon-ng check")

Se o arimon descobrir algum processo em execução que poderão interferir. Conforme o seu adaptador wireless e seus drivers, você poderá ou não se deparar com agum problema se esses programas não forem encerrador.

Para matar de uma só vez todos os processos que possam interferir, digite ("airmon-ng check kill")

Agora digite ("airmon-ng start wlan0) para mudar a interface wireless para o modo monitor. 

Isso permitirá capturar pacotes que não tenham sido destinados a nós. O airmon-ng cria a interface wireless wlan0mon

########################################################################################################################################################################################



Linha de Comando:

Checando dispositivos de rede:
# ifconfig

Ativando a interface de monitoramento:
# airmon-ng start wlan0

Desativando a interface de monitoramento:
# airmon-ng stop wlan0mon

Fazendo monitoramento do ar:
# airodump-ng wlan0mon

Fazendo monitoramento com restrição de canal e BSSID
# airodump-ng wlan0mon -c <canal> --bssid <bssid da rede>




########################################################################################################################################################################################

			REDES OCULTAS

Descobrindo redes ocultas


Primeiro passo é deixar a placa de rede em modo monitor

airmon-ng start wlan0


Agor temos que monitorar as redes:

airodump-ng wlan0mon

após escolher a vitima, vamos restringir o monitoramento ao canal que ela esta usando


airodump-ng wlan0mon -c <<Canal>>

Agora precisamos desconectar as pessoas na rede delas, para descobrirmos o nome da rede wifi delas

aireplay-ng -0 <<NUMERO DE PACOTES A SEREM ENVIADOS>> -a <<BSSID>> wlan0mon
airodump-ng wlan0mon -c <<Canal>> --bssid <BSSID da rede>>


========================================================================================================================================================================================



### Linha de comando:

Mostrando dispositivos de rede:

 `ifconfig`
Ativando interface de monitoramento:

 `airmon-ng start wlan0`
Monitorando o ar:

 airodump-ng wlan0mon
Filtrando monitoramento

 airodump-ng wlan0mon -c <canal> --bssid <bssid da rede>
Ataque de desautenticação

 aireplay-ng -0 10 -a <bssid> wlan0mon



========================================================================================================================================================================================

			CAPTURANDO PACOTES

Com a nossa interface em modo monitor, vamos ver que dados podemos coletar usando o Airodump-ng do pacote Aircrack-ng.
O Airodump-ng é usado para capturar e salvar o pacotes wireless

~~~~~~~~~~~~Iniciando o dump de um pacote com o Airodump-ng~~~~~~~~

