echo "hi devops team. pleas eenter the programme to install. \n"
 read input

if grep -q "$input" list.txt; then
      echo " $input package installed" 
else 
      echo "$input package not installed. \n"
	echo "Installing the package for you."
	sudo apt install -y $input
fi 
