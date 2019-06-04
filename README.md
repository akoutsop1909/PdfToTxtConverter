# CMD_PdfToTxtConverter
Pdf to txt converter πρόγραμμα που δημιούργησα ως μικρό project κατά τη διάρκεια της πρακτικής μου.\
Το πρόγραμμα τρέχει από Command line.\
Χρειάζεται τη βιβλιοθήκη (αρχείο jar) που βρίσκεται σε αυτό τον φάκελο.\
Για ευκολία, το πρόγραμμα μπορεί να τρέξει και από το αρχείο bat.\
Το ανοίγουμε με κάποιον editor και βάζουμε τις παραμέτρους στην 3η γραμμή, δίπλα από το PDFToTextConverter.\
Διπλό κλικ στο αρχείο bat για να τρέξει το πρόγραμμα.

Παράμετροι command line arguments\
========================================================================\
1η παράμετρος (υποχρεωτική): φάκελος πηγή (source folder).\
2η παράμετρος (υποχρεωτική): φάκελος προορισμού (destination folder).\
3η παράμετρος (προαιρετική): μικρότερη ημερομηνία τελευταίας τροποποήσης.\
4η παράμετρος (προαιρετική): μεγαλύτερη ημερομηνία τελευταίας τροποποίησης.\

Οδηγίες χρήσης\
=========================================================================\
Το πρόγραμμα για να λειτουργίσει χρειάζεται τουλάχιστον 2 παραμέτρους command line arguments. Τον φάκελο πηγή και τον φάκελο προορισμού, είτε με absolute path είτε με relative path (σε σχέση με την τοποθεσία του αρχείου class.\
Αν δεν υπάρχει ο φάκελος προορισμού, δημιουργείται αυτόματα.\
Μπορούμε να δώσουμε και wildcards, αν θέλουμε.\
Το wildcard το δίνουμε σαν 1η παράμετρο του path.\
To wildcard για το αστεράκι είναι το (.*)\
Πχ: myFolder/myOtherFolder\wild(.*)\
Η 3η παράμετρος είναι προαιρετική.\
Αν την παραλείψουμε θα ισούται με 1-1-1900 για να είμαστε σίγουροι ότι θα βρούμε αρχεία με μεγαλύτερη ημερομηνία τροποποίησης από αυτή.\
Η 4η παράμετρος είναι επίσης προαιρετική, αλλά δεν μπορεί να υπάρξει αν δεν έχουμε δώσει ημερομηνία για την 3η παράμετρο.\
Αν την παραλείψουμε θα ισούται με την τωρινή ημερομηνία για να είμαστε σίγουροι ότι θα βρούμε αρχεία με μικρότερη ημερομηνία τροποποίησης από αυτή.\
Η ημερομηνία που θα βάλουμε πρέπει να είναι της μορφής dd-MM-yyy\

Παραδείγματα\
=========================================================================\
java PDFToTextConverter folder1 folder2
java PDFToTextConverter folder1/subfolder folder2
java PDFToTextConverter folder1/wild(.*) folder2 
java PDFToTextConverter folder1 folder/subfolder2 1-1-2019
java PDFToTextConverter folder1/subfolder folder2 3-4-2018 3-4-2018
java PDFToTextConverter folder1/subfolder/wi(.*) folder2/sub1/sub2 4-5-2018 5-10-2019
