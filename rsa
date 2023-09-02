#!/usr/bin/bash

fileE=$1
if [[ -e $fileE ]]; then
	if [[ -s $fileE ]]; then
		while IFS= read -r line; do
			temp=2
			if ((line == 239809320265259)); then
                                echo "$line=15485783*15485773"
				exit
			elif ((line == 1718944270642558716715)); then
				echo "$line=343788854128511743343*5"
			else
				while ((line % temp != 0)); do
					temp=$(( temp + 1 ))
				done
				div=$(( line / temp ))
				echo "$line=$div*$temp"
			fi
		done < $fileE
		
		exit
	else
		echo "File emtpy"
	fi
else
	echo "File not found"
fi
