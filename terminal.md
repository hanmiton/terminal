primer commit para la clase termianr

invocar programas que no sabemos qeu tenemos
	metodos para ubscar dentor del archivo
banderas
	
Terminal
	La terminal nos abre un mundo de posibilidades increíbles. Desde tener una navegación avanzada entre todos nuestros nodos y archivos, hasta contar con programas previamente instalados e increíbles que solo pueden ser ejecutados desde este entorno y ni siquiera sabemos que existen.

Comandos ( y algunas bandreas)
	ls: lista lso contenidos de un direcotrio
		ls -l: lista los archivos con datos de cada nodo, ordenados alfabeticamente
		ls-lS: lista lso contenidos ordenador por tamño
		ls -lh: lista los contenido mostrando los datos legibles facilmente(tamaño)
		ls -r: lsita los archivos ordenados de forma inversa(srive con las bandersaS y t)
	rm [file] : elimina un archivo
	rm -rf [DIRECTORY]: elimina un direcotiro recursivamente sin preguntar
	mv [file] [directory] : mueve file a directory
	mv [file] [name] reonombra file a name
	cd [directory] : lleva el prompt a directory
	touch [file]: si File existe ,modifica la hora de ultiam modificacon al momento de la ejecucion del comando ,si

lista comando repositorio beco
Lista de comandos usados en #PlatziTerm

Work in progress

Conceptos

PROMPT: Donde se encuentra el cursor, un lugar en el árbol de nodos que es la representación del disco duro en el sistema operativo
Comandos (y algunas banderas)

ls: lista los contenidos de un directorio
ls -l: lista los archivos con datos de cada nodo, ordenados alfabéticamente
ls -lS: lista los contenidos ordenados por tamaño
ls -lh: lista los contenidos mostrando los datos legibles fácilmente (tamaño)
ls -r: lista los archivos ordenados de forma inversa (sirve con las banderas S y t)
ls -a: lista los contenidos de un directorio incluyendo los archivos ocultos
tree lista recursivamente la estructura de árbol de un directorio incluyendo tanto archivos como directorios (NOTA: No viene pre-instalado así que hay que instalarlo primero con su administrador de paquetes preferido: para RHEL/CentOS/Fedora yum install tree para Debian/Mint/Ubuntu apt-get install tree, para OS X brew install tree)
tree -L 1: muestra recursivamente la estructura de árbol de un directorio pero sólo hasta el primer subnivel de directorios
tree -a: muestra recursivamente la estructura de árbol de un directorio incluyendo tanto archivos como directorio ocultos
tree -d: muestra recursivamente la estructura de árbol de un directorio tomando en cuenta sólo los directorios
tree -dL 1: muestra recursivamente la estructura de árbol de un directorio tomando en cuenta sólo los directorios y hasta el primer subnivel
rm [FILE]: elimina un archivo
rm -rf [DIRECTORY]: elimina un directorio recursivamente sin preguntar
mv [FILE] [DIRECTORY]: mueve FILE a DIRECTORY
mv [FILE] [NAME]: renombra FILE a NAME
cd [DIRECTORY]: lleva el PROMPT a DIRECTORY
touch [FILE]: si FILE existe, modifica la hora de última modificación al momento de la ejecución del comando, si FILE no existe, lo crea
ln -s [DIRECTORY] [NAME]: crea un link simbólico llamado NAME hacia DIRECTORY, NAME se comporatará como DIRECTORY
tail [FILE]: muestra las últimas 10 lineas de un archivo de texto
tail -f [FILE]: tail forever, en principio muestra las últimas 10 líneas de FILE, pero mantiene abierto el archivo e imprime los cambios que se vayan escribiendo (secuencialmente) en éste, muy útil para logs.
more [FILE]: muestra el contenido de un archivo de texto de forma páginada
cat [FILE]: imprime todo el contenido de un archivo en pantalla
clear:limpia la terminal
pwd: imprime o muestra la ruta actual donde nos encontramos ubicados
man [COMANDO]: muestra la documentacion de todos los comandos
mkdir [DIRECTORY]: crea un directorio en la ubicación actual
mkdir -p [RUTA]: crea un árbol de directorios completo que no existe
cp [archivo/directorio origen] [archivo/directorio destino]: copia un archivo o directorio desde un origen a un destino
cp -r [directorio origen] [directorio destino]: copia un directorio y todos sus directorios hijos de forma recursiva
open [-a APP] [ FILE | DIRECTORY ]: abre el (archivo o directorio) con la aplicación por defecto en el sistema operativo, si se manda la bandera -a usará la APP para abrirlo
Operadores para STDIN, STDOUT/STDERR

      entrada      ->    ejecución     ->        salida
                                 +-------> STDOUT (1)
                                 |
                  +--------+     |
  STDIN (0) ----> | script | ----+
                  +--------+     |
                      T          |
                      |          +-------> STDERR (2)
                      |
          STDIN (0)---+
operador | (pipe):

command_1 | command_2 Manda el STDOUT de command_1 al STDIN de command_2

operador >

command_1 > FILE Manda el STDOUT de command_1 al inicio de FILE. Si FILE no existe lo crea, si existe lo sobreescribe.

operador >>

command_1 >> FILE Manda el STDOUT de command_1 al inicio de FILE. Si FILE no existe lo crea, si existe lo concatena al fina (tras un newline).

operador <

command_1 < FILE Manda al STDIN de command_1 el contenido de FILE.

redirección de salidas

command > FILE - manda el STDOUT a FILE
command 1> FILE 2>FILE_ERROR - manda el STDOUT a FILE y el STDERR a FILE_ERROR
command > FILE 2>&1 - manda, tanto el STDOUT como el STDERR a FILE
command >> FILE 2>&1 - manda a concatenar las salidas de STDOUT y STDERR a FILE
Combinación de teclas como comandos

[ctrl]-C - este comando termina el proceso que se esté ejecutando en la terminal, haya o no acabado de ejecutarse.
[ctrl]-D - el sistema lo interpreta como EOF (End Of File) y cierra el stream de entrada (STDIN) para un archivo en donde se esté escribiendo desde la terminal.
Cómo salir de VI/VIM

Ejecutar la siguiente combinación de teclas para

salir guardando los cambios: [ESC] : w q ![ENTER]
salir sin guardar cambios: [ESC] : q ! [ENTER]

clear
	para limpiar la pantalla
pwd
	donde estoy
cd ~ 
	para volver al home
cd /
	raiz
cd 
	para ir al home
ls
	archivos y direcotrios que hay dentro
ls -l
	dame listado pero en forma de lista
	Primer letra
		q tipo de nodo es
			- archivo
			l link
			d directroio
cd
	change direcotry (mueve el apuntador de donde estoy a otro direcotrio)
ls -lt
	va ordenar todo con respecto a la fechas mascercanaa la mas lejana
tecla arriba
	accedemos a hisotiral de ejecucion de ocmandos
ls-ltr
	va ordenar tood ocn repsecto a la fechas mas lejanaa cercana
numeros
	son el tamaño del archivo
ls -lh
	h: human readlible
	va mostar n consolo algo legibre pra el humano
ls -lhS
	direcotrio no tiene tamñao
	mayor a menor los archivos segun el peso de cada uno
ls -lhSr
	lo mismo q el anterior pero en reversa
du -h -d 1
	du:desc usage
	-h:
	-d: imprime cuanto pesa todo
	1
cd .
	nos sirve para llevarnos al directorio donde nos encontramos
mkdir fotos
	creacion de direcotiro fotos
mv [archivo] [directorio]
	mv hol.md fotos/
		moviendo archivo hol.md a fotos
../
	regresa un direcotrio
./
	directorio actual
mv ~/donwlaodas/*.jpg
	* : que es archivo se llame como sea y que termien en jpg
cp ../foto.jpg .
	copiar archivos
mv foto.jpg imagen.jpg
	renombrar archivos
touch 
	abre archivo y lo cierra (par amodificar fecha d emodificacion)
touch [archvo]
ln -s [flickr_photos.csv] [fotos.csc]
	creacin de un link fotos.csv para vlickr_photos..csv
	espacio en el diso duro que apunta a otro lugar
rm 
	remove (usar ocn exprema precaucion)
rm -r
	borra todo
rm [archivo]
	borrar un archivo
	no hay bandeja de basura
rm csvs/*
	borra todo lo que haya dentro de csvs
rm -rf csvs/
	borrando dinrectorio csvs
rm fotos.csv
	borranod link
bc
	calculadora
	quit
		pra salir
open -a textedit [archivo]
	-a q app se desea usar
	open para abrir un archivo
bc [calculos]
	para realizar los calculos de un archivo solo muestra los resultados
bc -q
	entra directamente a la operacino sin mostarr la licencia
md5
	entrega la huella digital d eun archivo
	es mas rapido q sha
md5 [archivo]
	huella digital de dicho archivo
more / less
	muestra lo que estan en el archivo en consola
	si el arichivo es muy grande lo va paginar
	espacio para ir a la siguient epagina
	b em regresa
	enter avanza de uno en uno
tail  -20 [documetno]
	nos va dar las ultimas 20 linas
tail -f [documento]
	deja esuchcando este archivo e impre las ultimas lineas
	se usa para atener el archivo de log abierto
cat 
	es concatenacion
cat [documento]
	imprimer todo el documento
wc [documento]
	para ver el nuermo de lineas palabras
wc [documento.csv]
	nos sirve par aver las ultimas plabras
wc -l [documento]
	muestra el numero de lineas
wc -c [documento]
	numeor de caracteres de un archivo

	wc siginifa word count
man
	manual
	man bc 
		ayyda para el comando bc
	man wc
		aydua sobre wordcount y nos da las banderas
	man man
		manual de man
echo $PATH
	echo: simplemente imprime
	enumra los directorios donde el sistema puede leer los ejecutables
which cat
	ver donde se encuentra
Como ejecutra un comando
	comando
	comando -f 1 --banderas=1 
		sin espacion signific q e es bandera prendida
		--para mandar un valor a una bandera
	comando prametro.txt
	comando parametro_1.txt parametro_2.txt
	comando -b -h 1 parametro
top
	me da un estaus de como se encuentra mi sistemas
	y qeu sistemas se encuentra corriendo
	snapshot de que esta ocurriendo en mi sistema
procesos
	pid: procesos id siver para identificar un determiando proceso
	apalstando o
		para ordenar por lo que lo deseamos
php ../scripts/1-process.php
	terminar la ejecucion de un proceso 
		ctrl+c

php ../scripts/1-process.php &
	& me regresa el control de la terminal
kill -9 12547
	matando el proceso con id 12547
ps -wA
	process status
	enlista los procesos que se sesta ejecutnado en este momento
?
	EL PROCESS STATUS DEL UNICO proceso que se ejecuto
	exit status
		1 es qeu algo salio mal
		0 todo esta bien
Standar Input 
Standar Output
Standar Error
	programa
		recibe datos
		interprtarlos procesarlos
		y sacar una respuesta
Standar Output
	STDOUT
	Es lo que imprime un programa
Standar Error
	STDERROR
sTANDAR OUTPUT Y ESTANDAR ERORRO
	salen en la misma pantalla
> salida del standar la imprime a un archivo si no existe el archivo lo crea
php ../scripts/2-stdou.php >results
	solo imprime loq ue no es error como resualtado
>>
	......ver para q sirve
one liner
	touch operacones.bc
|
	sirve para con catenar comadnos
	Linea especial de algo esta fal
	landao

cat operacines.bc | bc -q
	operacins es el input para bc -q
concatenando 3 comandos
cat operaciones.bc | bc-q | wc -l > res_bc

more ../keynotes/schemas/io.txt
	para pder ver el eschuma de stardarinput y stander output
Entradras 
	pupeden ser de diferentes fuentes
Salidas
	STDOUT (1)
		donde todo sale por defecto
	STDERR (2)
		lo qeu da error dentro del sistema sale por aqui

<
	lee un archivo y lo manda como stardar input

bc-q < operacines .bc
	diferencia entre | y <
		qeu tiene q esperar la ejecucion de otro programa
bc -1 < operaciones.bc > resultado
	input operaciones.bc
	comnado bc -1
	la manda a resultado output

2>&1
	concatenar stremas de salida y de error
2> errores
	manda de errores a errores

tail -f resultado
	lo esta viendo comandos en vivo 
	-f forever

grep 
	de lo que llega busca un cadena de caracters
	grep beco
grep ,beco$
	$endofline donde termina la linea
grep -r . -e beco$
	-r recursivamente
	-e expresion
	$	end of line
grep -r . -e beco$ -n -v
	-n linea en la que se esta encontrando
	-v icanbecontacted 
		es para q no escoja este itpo de palabras
^: start of line

find ~/src -name '*.csv' -type -f -exec md5 {} \;

find .  -name 'flickr_*' -type f -exec mv {} {}.scv \;

	find: buscar
	-name: nobmre
	-type: f que se archivo
	-exce ejecute comando
	mv: mover
	{} archivo
	\ terminar ejecuacin de comando
split -l 3000 ../flickr_pohotos.csv ./fl_3000_
	split pra dividir el archivo en distintos

curl
	emula un request
	genera un reques a un url
httpbin.org
	te manda los datos del reqeutsp
curl -o google_preuba.html http://ww.gogoel.com.mx
	snapshot de status
	como se encuentra bajando las cosas
	-o output donde se queire guardad
curl -O https://raw.githubusercontetn.com/beco/cli/master/files/close_call.gif 
	-O es para preservar el nombre original del docuemtno o archivo

	/dev/null
		no muestara lo qeu se demora la peticnon
get
curl http://httpbin.org/get?variable=2&uno=1&dos=2
	realizando un perticno get con curl
	&sirve para añadir mas parametros auna peticion get
curl "http://httpbin.org/get?variable=2&uno=1"
	"": como llas para que no exitas problemas con & ya q es reservado pra la ocnsola
curl --data "varibale1=1&variable2=2" http://httpgin.rog/post
	haciendo post ocn curl
	-A "agente_beco": para cambiar el user-agent
		sirver para hcer paginas responsive

User-Agent : que se esta utilizacno pra hacer la peticon

curl --data "message_nada y tu " https................

curl -d @request_data.txt https://guarder-dusck-oouo.herkouapa.com/mesasge
	-d: para especificar un mensaje con las variables
	@ especificando el archivo
vi
	editro de texto de consola

crontab
	agendar comandos que se ejecuten cuando queramos
	cada hroa
	min
	etc...
ctrontab -l
	tienen 5 columnas
	* todas las opciones
	1ra minutos
	2da horas
	3ra dia del mes (1-31)
	4ta mes [1-12]
	5to dia de la seman[´0domingo- 6 sabado]
	script.sh que se piensa ejecutar
todos los valores
crontab -e
	-e para poder editar

	* todos los valores
	1-10 de 1 a 10
	*/5 cada 5
	1,3,5,9 que se ejecute algo puntualmente

*/2	12-15	2,5,15,16,19,21	*	1-5 date > $HOME/hora.txt
	*/cada dos minutos
	entre 12 y 15 horas
	dias 2.......21
	todos los meses del año
	que sean entre lunes y vienres
	comaondo date
chmod para pmodificar los permisos

Estudiar

El comando cat>file
	imprimir en pantalla
Para mandar el STDOUOT de commandX al STDIN de commandY, usario
	commandX>commandY
Si quiero busar todos los direcotrios que se llamen src, aparti de home, usario
	find ~ /src........
La variable del sistema $? guarda
	Stdout del ultimo comando







Notas para live
	
	isr ganancias netas 
		gastos deducible o perdidas
		gana mas paga mas
	consolidacion fiscal
		contra perdidas de otras empresas con perdidas propias
tacticas del dobel irlandes
inlanda como registro de compañia con eso bajan ganancias fuera de maerica

cada año desaparecen dinero en paraisos fiscales
10km fracesas hersey
sistema de leyes eludiendo los impuesto
hombre de paja
	siempre necesitasba hombres pra establecer ocmpanias en el el extranjero
	cualqueiera peude ser direcror o testaferro
	hersey
	no producen dinero si no atraen dinero
	captar capitaels de paises a paraisos fiscalesp para eleduir los impuestos
	jersey isla parasio fiscal
Bozetos



cat