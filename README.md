# Terminal Commands Activity

Complete each step using terminal commands only! Feel free to look up any commands you are not familiar with online when you encounter them in the steps below. 

1. In the terminal, navigate to your Documents folder and create a directory called "cool\_directory".

mkdir

2. From the current directory (Documents) create a file in that new directory called "cool\_file.txt". Do this without changing the directory (i.e. without using cd)

ni  "cool\_file.txt"

3. Rename "cool\_directory" to "extra\_cool\_directory".

rename-item  .\cool\_directory\ "extra\_cool\_directory"

4. Find which directory you're currently in using the appropriate command. In your notes, write down the full path in the output. 

pwd

5. _Without using a keyboard shortcut_, clear the terminal of all printed output.

clear

6. From the current directory (should be Documents still), copy the directory "extra\_cool\_directory" including its contents to your Home directory.

cp -r .\extra\_cool\_directory\ "extra\_cool\_directory\_copy"

7. Delete the original directory and its contents from the Documents directory (do this one carefully!)

Remove-Item -Recurse -Force .\extra\_cool\_directory\\

`Remove-Item`: es el comando para eliminar un archivo o directorio.

`-Recurse`: asegura que todo el contenido del directorio (subdirectorios y archivos) se elimine también.

`-Force`: permite eliminar archivos de solo lectura, si es necesario.

`.\extra_cool_directory\`: es el directorio que se eliminará (en este caso, el directorio actual).

\
\
\
\
\


8. Navigate to the copy of the extra\_cool\_directory that you put in your home directory _using tab-completion_ to complete the directory name after only typing "ext".

cd .\extra\_cool\_directory\_copy\\

9. Append the text "This is some text" to the cool\_file.txt file.

Add-Content -Path .\cool\_file.txt -Value "This is some text"

10. Print the contents of the file to stdout. Write down what you see.

PS C:\Users\denni\Documents\extra\_cool\_directory\_copy> cat .\cool\_file.txt

This is some text

PS C:\Users\denni\Documents\extra\_cool\_directory\_copy>

\


11. Using the repeat command (repeat \<num of times> \<command>), repeat the phrase "More lines of text" 10 times and append the output to cool\_file.txt.

 1..10 | ForEach-Object { "More lines of text" } | Add-Content -Path .\cool\_file.txt

`1..10`: Crea una secuencia de números del 1 al 10.

`ForEach-Object { "More lines of text" }`: Para cada número en la secuencia, repite la frase "More lines of text".

`Add-Content -Path .\cool_file.txt`: Agrega cada línea de texto al archivo `cool_file.txt`.

12. Use the up arrow to re-run the command that adds "This is some text" to the cool\_file.txt.

Add-Content -Path .\cool\_file.txt -Value "This is some text"

\


13. Print the contents of that file and pass the output to the function that searches for the phrase "text". Write down what the output looks like?

PS C:\Users\denni\Documents\extra\_cool\_directory\_copy> cat .\cool\_file.txt

This is some text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

More lines of text

This is some text

PS C:\Users\denni\Documents\extra\_cool\_directory\_copy>

\
\


**Bonus** 

- Create 20 additional files in the extra\_cool\_directory using “brace expansion” (feel free to google this). The file names should resemble “file1.txt”, “file2.txt”, and so on.

- Create a file called .secret\_stuff (note the dot is part of the filename).

- Use the appropriate flag(s) to list the contents of this directory in a vertically oriented list. If you don’t see the .secret\_stuff file in the list, figure out what flag will display it when listing the directory contents.

