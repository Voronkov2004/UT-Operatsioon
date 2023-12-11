# Praktikum 12

Täna töötasime linuxis faili skriptimisega

3 ülesanne:

```
echo "Sisesta oma nimi:"
     read nimi
echo "Sisesta oma eriala:"
     read eriala
echo "Sisesta oma matriklinumber:"
     read matriklinumber
echo "Sisestatud andmed:"
echo "Nimi: $nimi"
echo "Eriala: $eriala"
echo "Matriklinumber: $matriklinumber"
```

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/OP_1.png?raw=true">


4 ülesanne:

```
#!/bin/bash

if [ "$#" -ne 2 ]; then
     echo "Kasutus: $0 <old_extension> <new_extension>"
     exit 1
fi
old_extension=$1
new_extension=$2

for file in *"$old_extension";
do
     if [ ${file##*.} = "$old_extension" ]; then
         new_name="${file%$old_extension}$new_extension"
         mv "$file" "$new_name"
         echo "$file on nimetatud $new_name."
     fi
done
```

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/OP_1.png?raw=true">

5 ülesanne

Selle ülesannega mul tekkinud probleemid

```
#!/bin/bash

if [ $# -eq 0 ]; then
     echo "Kasutus $0 <process_name>"
     exit 1
fi

process_name=$1

for line in $(ps -A);
do
     pid=$(echo "$line" | awk '{print $1}')
     nimi=$(echo "$line" | awk '{print $4}')
     if [[ "$name" == *"$process_name"* ]]; then
         echo "Protsessi nimi: $nimi, PID: $pid"
     fi
done
```

6 ülesanne

```
#!/bin/bash

astendamine() {
     esimene=$1
     teine=$2
     start=1
     while [ $teine -gt 0 ];
     do
         start=$((start * esimene))
         teine=$((teine-1))
     done
     echo $start
}
esimene=9
teine=5
tulemus=$(astendamine $esimene $teine)
echo "9^5 tulemus on $tulemus"
```

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/OP_1.png?raw=true">

7 ülesanne

<img width="491" alt="OS23_lab1a" src="https://github.com/Voronkov2004/UT-Operatsioon/blob/main/OP_1.png?raw=true">

