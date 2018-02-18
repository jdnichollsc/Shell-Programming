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
echo "|||                                                                                   |||"
echo "|||                                    SYSTEM MENU                                    |||"
echo "|||                                                                                   |||"
echo "|||      1. GENERAL COMMANDS                                                          |||"
echo "|||                                                                                   |||"
echo "|||      2. USERS                                                                     |||"
echo "|||                                                                                   |||"
echo "|||      3. FILE SYSTEM                                                               |||"
echo "|||                                                                                   |||"
echo "|||      9. FINISH                                                                    |||"
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
echo "|||      Please select desired option index                                00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read option
case $option in
1) sh commands; exit;;
2) sh users; exit;;
3) sh files; exit;;
9) clear; exit;;
*) echo "Typing error"; sleep 1;;
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
echo "|||                                  GENERAL COMMANDS                                 |||"
echo "|||                                                                                   |||"
echo "|||      1. DISPLAY SYSTEM TIME                                                       |||"
echo "|||                                                                                   |||"
echo "|||      2. PATH OF THE CURRENT DIRECTORY                                             |||"
echo "|||                                                                                   |||"
echo "|||      3. CHANGE PASSWORD                                                           |||"
echo "|||                                                                                   |||"
echo "|||      9. RETURN                                                                    |||"
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
echo "|||      Please select desired option index                                00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read option
case $option in
1) echo "The current time of the system is "; date;
   echo "Press ENTER to continue"; read nothing;;
2) echo "The current path is "; pwd;
   echo "Press ENTER to continue"; read nothing;;
3) passwd;
   echo "Press ENTER to continue"; read nothing;;
9) sh menu; break;;
*) echo "Typing error"; sleep 1;;
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
echo "|||                                       USERS                                       |||"
echo "|||                                                                                   |||"
echo "|||      1. SHOW CONNECTED USERS                                                      |||"
echo "|||                                                                                   |||"
echo "|||      2. SEND MESSSAGE TO AN USER                                                  |||"
echo "|||                                                                                   |||"
echo "|||      9. RETURN                                                                    |||"
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
echo "|||      Please select desired option index                                00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read option
case $option in
1) echo "The users connected in the system are "; who -q;
   echo "Press ENTER to continue"; read nulo;;
2) echo "Type the recipient's name";
   read user;
   quantity=`who | grep -w $user | wc -l`;
   if test $quantity -gt 0
   then
        echo "Please, write your message and press ENTER to send"
        read message
        echo $message | mesg $user
        echo "Your message has been sent correctly"
   else
        echo "Error, the recipient $user is not connected"
   fi;
   sleep 2;;
9) sh menu; break;;
*) echo "Typing error"; sleep 1;;
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
echo "|||                                       FILES                                       |||"
echo "|||                                                                                   |||"
echo "|||      1. CREATE DIRECTORY                                                          |||"
echo "|||                                                                                   |||"
echo "|||      2. COPY FILES                                                                |||"
echo "|||                                                                                   |||"
echo "|||      3. MODIFY PERMITS TO A FILE                                                  |||"
echo "|||                                                                                   |||"
echo "|||      4. DISPLAY THE CONTENT OF A FILE                                             |||"
echo "|||                                                                                   |||"
echo "|||      5. DELETE A FILE                                                             |||"
echo "|||                                                                                   |||"
echo "|||      6. CHANGE THE FILE'S NAME                                                    |||"
echo "|||                                                                                   |||"
echo "|||      9. RETURN                                                                    |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                                   |||"
echo "|||                                                                        0000___000 |||"
echo "|||      Please select desired option index                                00000__000 |||"
echo "|||                                                                        000_000000 |||"
echo "|||                                                                        000__00000 |||"
echo "|||                                                                        000___0000 |||"
echo "|||___________________________________________________________________________________|||"
echo "||_____________________________________________________________________________________||"
echo "|_______________________________________________________________________________________|"
read option
case $option in
1) echo "Enter the name of the directory to be created and Press ENTER";
   read directory;
   if test -d $directory
   then
      echo "Error, the directory $directory already exist"
   else
      mkdir $directory
      echo "The directory $directory has been created correctly"
   fi; echo "Press ENTER to continue"; read lol;;
2) echo "Enter the file name you want to copy and Press ENTER";
   read origin;
   if test -f $origin;
   then
       echo "Enter the name of the new copy and Press ENTER"
       read destiny
       if test -f $destiny
       then
           while :
           do
             echo "The file $destiny already exist, Do you want to replace it? (yes/no)"
             read selection
             case "$selection" in
             "yes") cp $origin $destiny; echo "The copy has been created correctly"; break;;
             "no") break;;
             *) echo "Typing error"; sleep 1;;
             esac
           done
       else
           cp $origin $destiny
           echo "The copy has been created correctly"
       fi
   else
       echo "Error, the file $origin doesn't exist"
   fi;
   echo "Press ENTER to continue";
   read nothing;;
3) sh permissions; exit;;
4) echo "Enter the file name to display its content";
   read fileName;
   if test -f $fileName
   then
       if test -s $fileName
       then
           echo "The contents of the file $fileName is the following:"
           cat $fileName
           echo "Press ENTER to continue"
           read nothing
       else
           echo "Error, the file $fileName is empty"
           sleep 2
       fi
   else
       echo "Error, the file $fileName doesn't exist"
       sleep 1
   fi;;
5) echo "Enter the name of the file to delete";
   read fileName;
   if test -f $fileName;
   then
       rm -rf $fileName
       echo "The file $fileName has been deleted correctly"
       echo "Press ENTER to continue"
       read nothing
   else
       echo "Error, the file $fileName doesn't exist"
       sleep 1
   fi;;
6) echo "Enter the name of the file to change";
   read fileName;
   if test -f $fileName;
   then
       echo "Enter the new name of the file"
       read newName
       if test -f $newName
       then
           while :
           do
           echo "The file $newName already exist, Do you want to overwrite it?? (yes/no)"
           read optionSelected
           case "$optionSelected" in
           "yes") mv $fileName $newName; echo "The file has been overwrited correctly"; break;;
           "no") break;;
           *) echo "Typing error"; sleep 1;;
           esac
           done
       else
           mv $fileName $newName; echo "The file $fileName has been modified correctly"
       fi
       echo "Press ENTER to continue"
       read nothing
   else
       echo "Error, the file $fileName doesn't exist"
       sleep 1
   fi;;
9) sh menu; exit;;
*) echo "Error de Digitación"; sleep 1;;
esac
done
```

## permissions
```
echo "Enter the name of the file to modify its permissions"
read fileName
if test -f $fileName
then
cont=0
quantity=0
while [ $cont -lt 3 ]
do
if test $cont -eq 0
then
    control="Owner"
elif test $cont -eq 1
then
    control="Group"
else
    control="Others"
fi
clear
echo "_________________________________________"
echo "|                                       |"
echo "||    Manage "$control" permissions    ||"
echo "||                                     ||"
echo "||  1. Only executable                 ||"
echo "||  2. Only writing                    ||"
echo "||  3. Writing and executable          ||"
echo "||  4. Only reading                    ||"
echo "||  5. Reading and executable          ||"
echo "||  6. Reading and writing             ||"
echo "||  7. Reading, writing and executable ||"
echo "||  8. Nothing                         ||"
echo "|_______________________________________|"
read option
case $option in
1)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 100 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 10 ))
  else
      quantity=$(( $quantity + 1 ))
  fi;;
2)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 200 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 20 ))
  else
      quantity=$(( $quantity + 2 ))
  fi;;
3)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 300 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 30 ))
  else
      quantity=$(( $quantity + 3 ))
  fi;;
4)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 400 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 40 ))
  else
      quantity=$(( $quantity + 4 ))
  fi;;
5)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 500 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 50 ))
  else
      quantity=$(( $quantity + 5 ))
  fi;;
6)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 600 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 60 ))
  else
      quantity=$(( $quantity + 6 ))
  fi;;
7)cont=$(( $cont + 1 ));
  if test $cont -eq 1
  then
      quantity=$(( $quantity + 700 ))
  elif test $cont -eq 2
  then
      quantity=$(( $quantity + 70 ))
  else
      quantity=$(( $quantity + 7 ))
  fi;;
8)cont=$(( $cont + 1 ));;
*)echo "Typing error"; sleep 1;;
esac
done
chmod $quantity $fileName
echo "The file $fileName has been modified its permissions correctly"
echo "Press ENTER to continue"
read nothing
else
   echo "Error, The file $fileName doesn't exist"
sleep 1
fi
sh files
```

# Happy coding
Made with <3

<img width="150px" src="http://phaser.azurewebsites.net/assets/nicholls.png" align="right">
