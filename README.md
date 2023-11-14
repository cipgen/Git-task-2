Створіть нову директорію під контролем системи контролю версій Git. -->
    **mkdir git_challenge**
    **cd git_challenge**
    **git init**
В директорії створіть файл з назвою challenge.txt -->
Додайте до файлу текст: This is my Git challenge file.
    **echo "This is my Git challenge file." > challenge.txt**
За допомогою команди git хешуйте вміст файлу challenge.txt.
Збережіть результат виконання команди у файлі з назвою hash.txt.-->
    **git hash-object -w challenge.txt > hash.txt**
Використайте системну команду git для відображення вмісту файлу challenge.txt, використовуючи хеш, збережений у файлі hash.txt та додайте вивід команди до hash.txt.-->
    **git cat-file -p $(cat hash.txt) >> hash.txt**
Використовуйте команду update-index, щоб додати файл challenge.txt до індексу Git.-->
    **git update-index --add challenge.txt**
Використовуйте команду git ls-files, щоб переглянути staged вміст індексу Git. Результат додайте до hash.txt. -->
    **git ls-files --stage >> hash.txt**
