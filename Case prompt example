#!/bin/ksh
XMLDIR=/home/build/pdiaz/xmldir/

echo "Enter Date Release: "
read _var1
echo "Enter CCID Name: "
read _var2
echo "Enter Clear Case Name: "
read _var3

echo "Release Date: $_var1 CCID Name: $_var2 ClearCase Name: $_var3"

echo " "

sed "s/DATEREL/$_var1/g;s/CCIDNME/$_var2/g;s/CCProjectTEST/$_var3/g;" $XMLDIR/CreateCCID.xml

while true; do
    echo "Do you want to create XML file for this CCID?"
    read yn
    case $yn in
        [Yy]* )
          echo "Preparing CCID"
          sed "s/DATEREL/$_var1/g;s/CCIDNME/$_var2/g;s/CCProjectTEST/$_var3/g;" $XMLDIR/CreateCCID.xml > $XMLDIR/$_var2.xml
          echo "Created CCID XML"
          echo "$XMLDIR/$_var2.xml"
          break;;
        [Nn]* ) exit;;
        * ) echo "Please answer yes or no.";;
    esac
done
