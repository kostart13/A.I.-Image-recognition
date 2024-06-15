# Αναγώριση και καταμέτρηση οχημάτων
Συμμετοχή στον 6o Πανελλήνιος Διαγωνισμός Ανοιχτών Τεχνολογιών στην Εκπαίδευση

1. Έρευνα:
Κάμερες χρησιμοποιούνται εδώ και αρκετά χρόνια στους δρόμους κυρίως για την καταγραφή παραβιάσεων των ορίων ταχύτητας.
Δεν είναι όμως τόσο εξελιγμένες όσο θα έπρεπε. Δεν αναγνωρίζουν τον τύπο του οχήματος, δεν δίνουν στοιχεία που θα μπορούσαν να βοηθήσουν στη ρύθμιση της κυκλοφορίας, δεν αναγνωρίζουν οχήματα που εμπλέκονται σε ατυχήματα κτλ.

2. Σχεδιασμός:
Χρησιμοποιώντας αλγορίθμους τεχνητής νοημοσύνης θα δημιουργήσουμε ένα σύστημα που θα μπορεί να αναγνωρίζει σε εικόνες ή σε βίντεο, διαφορετικού τύπου οχήματα και να τα καταμετρά.
Θα χρησιμοποιήσουμε την ενσωματωμένη κάμερα του esp32-cam. Στον αρχικό μας σχεδιασμό ήταν η αναγνώριση να λειτουργεί και σε πραγματικό χρόνο, κάτι που λόγω ταχύτητας επεξεργασίας τελικά δεν υλοποιήθηκε.

Βασικός μας στόχος να φτάσουμε μετά από μια σειρά βημάτων, στην χρήση της για την καταμέτρηση οχημάτων.
Η λειτουργία της καταμέτρησης οχημάτων μπορεί να βοηθήσει στην ρύθμιση της κυκλοφορίας, στον ορισμό ορίων ταχύτητας καθώς και στην διέλευση στα διόδια.

![example](https://github.com/kostart13/image-recognition/assets/99647289/db216ebd-e210-455c-b535-7a5a453c5ab8)

Χρησιμοποιήσαμε:
1 esp32-cam
1 FTDI serial adapter
3d printed camera case

Το κόστος των υλικών είναι ιδιαίτερα χαμηλό ενώ και το κάλυμα της κάμερας είναι προαιρετικό.

3. Υλοποίηση:
Ακολουθήσαμε μια σειρά βημάτων για να φτάσουμε στο επιθυμητό αποτέλεσμα:
α) Προγραμματίσαμε την κάμερα ώστε να λειτουργεί σαν server και να μεταφέρει την εινόνα στον υπολογιστή
β) Χρησιμοποιήσαμε το μοντέλο YOLOv3 για αναγνώριση αντικειμένων.
γ) Φτιάξαμε και το δικό μας μοντέλο μέσω του Teachable Machine της Google.
δ) Τέλος, προγραμματίσαμε την κάμερα ώστε να αναγνωρίζει και να μετρά οχήματα.

Χρησιμοποιήσαμε το arduino ide για τον προγραμματισμό και το σετάρισμα της κάμερας
και την python 3.8 για την επεξεργασία της εικόνας - βίντεο και την αναγνώριση - καταμέτρηση των οχημάτων.

Όλα τα βήματα περιγράφονται στο βίντεο που ακολουθεί ενώ και ο κώδικας είναι διαθέσιμος.

https://www.youtube.com/watch?v=quh_iXH4vM4
