# Shell Programming
Shell Programming and Scripting

# Unix Examples:
## menu
```
while :
do
clear
echo "_________________________________________________________________________________________"
echo "|_______________________________________________________________________________________|"
echo "||_____________________________________________________________________________________||"
echo "|||                                                                                                                                                    |||"
echo "|||                                  MENU DEL SISTEMA                                 |||"
echo "|||                                                                                   |||"
echo "|||      1. COMANDOS GENERALES                                                        |||"
echo "|||                                                                                   |||"
echo "|||      2. VARIOS USUARIOS                                                           |||"
echo "|||                                                                                   |||"
echo "|||      3. SISTEMA DE ARCHIVOS                                                       |||"
echo "|||                                                                                   |||"
echo "|||      9. TERMINAR                                                                  |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                        0000___000 |||"
echo "|||      Señor Usuario, Por favor Seleccione Índice de Opción deseada      00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read opcion
case $opcion in
1) sh commands; exit;;
2) sh users; exit;;
3) sh files; exit;;
9) clear; exit;;
*) echo "Error de Digitación"; sleep 1;;
esac
done
```


## commands
```
while :
do
clear
echo "_________________________________________________________________________________________"
echo "|_______________________________________________________________________________________|"
echo "||_____________________________________________________________________________________||"
echo "|||                                                                                   |||"
echo "|||                               MENU COMANDOS GENERALES                             |||"
echo "|||                                                                                   |||"
echo "|||      1. VISUALIZAR HORA DEL SISTEMA                                               |||"
echo "|||                                                                                   |||"
echo "|||      2. PATH O RUTA ACTUAL                                                        |||"
echo "|||                                                                                   |||"
echo "|||      3. CAMBIO DE PASSWORD                                                        |||"
echo "|||                                                                                   |||"
echo "|||      9. REGRESAR                                                                  |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                        0000___000 |||"
echo "|||      Señor Usuario, Por favor Seleccione Índice de Opción deseada      00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read opcion
case $opcion in
1) echo "La Hora Actual del sistema es "; date;
   echo "Presione Enter para Continuar"; read nulo;;
2) echo "La Ruta Actual es "; pwd;
   echo "Presione Enter para Continuar"; read nule;;
3) passwd;
   echo "Presione Enter para Continuar"; read nuli;;
9) sh menu; break;;
*) echo "Error de Digitación"; sleep 1;;
esac
done
```

## users
```
while :
do
clear
echo "_________________________________________________________________________________________"
echo "|_______________________________________________________________________________________|"
echo "||_____________________________________________________________________________________||"
echo "|||                                                                                   |||"
echo "|||                                    MENU USUARIOS                                  |||"
echo "|||                                                                                   |||"
echo "|||      1. MOSTRAR USUARIOS CONECTADOS                                               |||"
echo "|||                                                                                   |||"
echo "|||      2. ENVIAR MENSAJE A UN USUARIO                                               |||"
echo "|||                                                                                   |||"
echo "|||      9. REGRESAR                                                                  |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                        0000___000 |||"
echo "|||      Señor Usuario, Por favor Seleccione Índice de Opción deseada      00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read opcion
case $opcion in
1) echo "Los Usuarios Actualmente Conectados en el sistema son"; who -q;
   echo "Presione Enter para Continuar"; read nulo;;
2) echo "Digite el Nombre del Destinatario";
   read usuario;
   cantidad=`who | grep -w $usuario | wc -l`;
   if test $cantidad -gt 0
   then
        echo "Por favor, escriba su mensaje y presione Enter para enviar"
        read mensaje
        echo $mensaje | mesg $usuario
        echo "Su mensaje se ha enviado correctamente"
   else
        echo "Error, el destinatario $usuario no está conectado"
   fi;
   sleep 2;;
9) sh menu; break;;
*) echo "Error de Digitación"; sleep 1;;
esac
done
```

## files
```
while :
do
clear
echo "_________________________________________________________________________________________"
echo "|_______________________________________________________________________________________|"
echo "||_____________________________________________________________________________________||"
echo "|||                                                                                   |||"
echo "|||                                  MENU DE ARCHIVOS                                 |||"
echo "|||                                                                                   |||"
echo "|||      1. CREAR DIRECTORIO                                                          |||"
echo "|||                                                                                   |||"
echo "|||      2. COPIAR ARCHIVOS                                                           |||"
echo "|||                                                                                   |||"
echo "|||      3. MODIFICAR PERMISOS A UN ARCHIVO                                           |||"
echo "|||                                                                                   |||"
echo "|||      4. VISUALIZAR EL CONTENIDO DE UN ARCHIVO                                     |||"
echo "|||                                                                                   |||"
echo "|||      5. BORRAR UN ARCHIVO                                                         |||"
echo "|||                                                                                   |||"
echo "|||      6. CAMBIAR EL NOMBRE DE UN ARCHIVO                                           |||"
echo "|||                                                                                   |||"
echo "|||      9. REGRESAR                                                                  |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                        0000___000 |||"
echo "|||      Señor Usuario, Por favor Seleccione Índice de Opción deseada      00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read opcion
case $opcion in
1) echo "Ingrese Nombre del Directorio a crear y Presione Enter";
   read directorio;
   if test -d $directorio
   then
      echo "Error, el Directorio $directorio ya Existe"
   else
      mkdir $directorio
      echo "El Directorio $directorio se ha creado correctamente"
   fi; echo "Presione Enter para Continuar"; read lol;;
2) echo "Ingrese Nombre del Archivo que desea copiar y Presione Enter";
   read origen;
   if test -f $origen;
   then
       echo "Ingrese el Nombre de la nueva copia y Presione Enter"
       read destino
       if test -f $destino
       then
           while :
           do
             echo "El archivo $destino ya existe, desea reemplazarlo? (si/no)"
             read seleccion
             case "$seleccion" in
             "si") cp $origen $destino; echo "La Copia se ha realizado correctamente"; break;;
             "no") break;;
             *) echo "Error de Digitación"; sleep 1;;
             esac
           done
       else
           cp $origen $destino
           echo "La Copia se ha realizado correctamente"
       fi
   else
       echo "Error, el Archivo $origen no Existe"
   fi;
   echo "Presione Enter para Continuar";
   read nada;;
3) sh permissions; exit;;
4) echo "Ingrese el Nombre del Archivo a Visualizar su Contenido";
   read visualizar;
   if test -f $visualizar
   then
       if test -s $visualizar
       then
           echo "El Contenido del Archivo $visualizar es el Siguiente:"
           cat $visualizar
           echo "Presione Enter para Continuar"
           read visual
       else
           echo "Error, el Archivo $visualizar está vacio"
           sleep 2
       fi
   else
       echo "Error, El Archivo $visualizar No Existe"
       sleep 1
   fi;;
5) echo "Ingrese el Nombre del Archivo a Borrar";
   read borrar;
   if test -f $borrar;
   then
       rm -rf $borrar
       echo "El Archivo $borrar se ha eliminado correctamente"
       echo "Presione Enter para Continuar"
       read borrar
   else
       echo "Error, El Archivo $borrar No existe"
       sleep 1
   fi;;
6) echo "Ingrese el Nombre del Archivo a Cambiar";
   read rename;
   if test -f $rename;
   then
       echo "Ingrese el nuevo Nombre del Archivo"
       read name
       if test -f $name
       then
           while :
           do
           echo "El Archivo $name ya Existe, desea sobreescribirlo? (si/no)"
           read decision
           case "$decision" in
           "si") mv $rename $name; echo "El Archivo se ha Sobreescribido Correctamente"; break;;
           "no") break;;
           *) echo "Error de Digitación"; sleep 1;;
           esac
           done
       else
           mv $rename $name; echo "El Archivo $name se ha Modificado Correctamente"
       fi
       echo "Presione Enter para Continuar"
       read nada
   else
       echo "Error, El Archivo $rename No Existe"
       sleep 1
   fi;;
9) sh menu; exit;;
*) echo "Error de Digitación"; sleep 1;;
esac
done
```

## permissions
```
echo "Ingresar el Nombre del Archivo a Modificar sus Permisos"
read archivo
if test -f $archivo
then
cont=0
cantidad=0
while [ $cont -lt 3 ]
do
if test $cont -eq 0
then
    control="Dueño"
elif test $cont -eq 1
then
    control="Grupo"
else
    control="Otros"
fi
clear
echo "_________________________________________"
echo "|                                       |"
echo "||   Administrar Permisos de "$control"     ||"
echo "||                                     ||"
echo "||  1. Solo Ejecutable                 ||"
echo "||  2. Solo Escritura                  ||"
echo "||  3. Escritura y Ejecutable          ||"
echo "||  4. Solo Lectura                    ||"
echo "||  5. Lectura y Ejecutable            ||"
echo "||  6. Lectura y Escritura             ||"
echo "||  7. Lectura, Escritura y Ejecutable ||"
echo "||  8. Ninguno                         ||"
echo "|_______________________________________|"
read opcion
case $opcion in
1)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 100 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 10 ))
  else
      cantidad=$(( $cantidad + 1 ))
  fi;;
2)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 200 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 20 ))
  else
      cantidad=$(( $cantidad + 2 ))
  fi;;
3)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 300 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 30 ))
  else
      cantidad=$(( $cantidad + 3 ))
  fi;;
4)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 400 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 40 ))
  else
      cantidad=$(( $cantidad + 4 ))
  fi;;
5)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 500 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 50 ))
  else
      cantidad=$(( $cantidad + 5 ))
  fi;;
6)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 600 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 60 ))
  else
      cantidad=$(( $cantidad + 6 ))
  fi;;
7)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      cantidad=$(( $cantidad + 700 ))
  elif test $cont -eq 2
  then
      cantidad=$(( $cantidad + 70 ))
  else
      cantidad=$(( $cantidad + 7 ))
  fi;;
8)cont=$(( $cont + 1 ));;
*)echo "Error de Digitación"; sleep 1;;
esac
done
chmod $cantidad $archivo
echo "Al Archivo $archivo se le han Modificado los Permisos Correctamente"
echo "Presione Enter para Continuar"
read nada
else
   echo "Error, El Archivo $archivo no Existe"
sleep 1
fi
sh files
```
