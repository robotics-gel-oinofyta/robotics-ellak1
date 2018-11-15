# robotics-ellak1
1ος Πανελλήνιος Διαγωνισμός Ρομποτικής Ανοιχτών Τεχνολογιών


# Έλεγχος ρομπότ με την κίνηση του χεριού

# Ιδέα

Κατασκευή ενός ρομπότ (όχημα) του οποίου η κίνηση θα ελέγχεται ασύρματα (μέσω wifi) με την κίνηση του χεριού χρησιμοποιώντας το επιταχυνσιόμετρο ADXL335 και ένα ζεύγος WemosD1.

Ο χρήστης θα φοράει ένα γάντι πάνω στο οποίο θα έχει προσαρμοστεί ένα Wemos D1 Mini και ένα επιταχυνσιόμετρο ADXL335 ([https](https://www.arduino.cc/en/Tutorial/ADXL3xx)[://](https://www.arduino.cc/en/Tutorial/ADXL3xx)[www](https://www.arduino.cc/en/Tutorial/ADXL3xx)[.](https://www.arduino.cc/en/Tutorial/ADXL3xx)[arduino](https://www.arduino.cc/en/Tutorial/ADXL3xx)[.](https://www.arduino.cc/en/Tutorial/ADXL3xx)[cc](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[en](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[Tutorial](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[ADXL](https://www.arduino.cc/en/Tutorial/ADXL3xx)[3](https://www.arduino.cc/en/Tutorial/ADXL3xx)[xx](https://www.arduino.cc/en/Tutorial/ADXL3xx) ) το οποίο θα αντιλαμβάνεται τις κινήσεις του χεριού του χρήστη. Το Wemos D1 Mini ( [https://wiki.wemos.cc/products:d1:d1\_mini](https://wiki.wemos.cc/products:d1:d1_mini)   ) έχει διαστάσεις 34x25mm, είναι συμβατό με Arduino και διαθέτει:

- WiFi (ESP-8285)
- 11 ψηφιακές εισόδους / εξόδους,
- 1 αναλογική είσοδο (3.2Vmax)
- σύνδεση MicroUSB
- 1MBFlash

Οι διαφορετικές χειρονομίες που θα χρησιμοποιηθούν για τον έλεγχο της κίνησης του ρομπότ (όχημα) είναι:

- Χέρι παράλληλα με το έδαφος: _στάσιμο_
- Το χέρι έχει κλίση προς τα εμπρός: _εμπρός_
- Το χέρι έχει κλίση προς τα πίσω: _πίσω_
- Το χέρι κλίνει δεξιά: _δεξιά_
- Το χέρι έχει κλίση προς τα αριστερά: _αριστερά_

Το επιταχυνσιόμετρο ADXL335 ([https](https://www.arduino.cc/en/Tutorial/ADXL3xx)[://](https://www.arduino.cc/en/Tutorial/ADXL3xx)[www](https://www.arduino.cc/en/Tutorial/ADXL3xx)[.](https://www.arduino.cc/en/Tutorial/ADXL3xx)[arduino](https://www.arduino.cc/en/Tutorial/ADXL3xx)[.](https://www.arduino.cc/en/Tutorial/ADXL3xx)[cc](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[en](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[Tutorial](https://www.arduino.cc/en/Tutorial/ADXL3xx)[/](https://www.arduino.cc/en/Tutorial/ADXL3xx)[ADXL](https://www.arduino.cc/en/Tutorial/ADXL3xx)[3](https://www.arduino.cc/en/Tutorial/ADXL3xx)[xx](https://www.arduino.cc/en/Tutorial/ADXL3xx) ) εξάγει την επιτάχυνση σε κάθε άξονα X,Y,Z ως αναλογική τάση μεταξύ 0 και 5 volt.

Με τη χρήση WiFi οι εντολές από το γάντι θα μεταφέρονται σε ένα WeMosD1 το οποίο και θα ελέγχει τις κινήσεις της πλατφόρμας (όχημα) robot.

Το Wemos D1 ( [https://wiki.wemos.cc/products:d1:d1](https://wiki.wemos.cc/products:d1:d1) ) είναι συμβατό με το Arduino Uno και διαθέτει:

- .WiFi (ESP8266EX)
- .11 ψηφιακές εισόδους / εξόδους,
- .1 αναλογική είσοδο (3.2Vmax)
- .σύνδεση MicroUSB
- .1MBFlash
- .Power jack, 9-24V

Η οδήγηση των κινητήρων γίνεται με την χρήση του _L293D Motor Driver Shield_ ( βλέπε [https://playground.arduino.cc/Main/AdafruitMotorShield](https://playground.arduino.cc/Main/AdafruitMotorShield)  και  [http://wiki.sunfounder.cc/index.php?title=L293D\_Motor\_Driver\_Shield](http://wiki.sunfounder.cc/index.php?title=L293D_Motor_Driver_Shield)για την πλήρη περιγραφή και το κύκλωμα του συγκεκριμένου shield ). Toshield περιέχει δύο οδηγούς κινητήρα L293D και έναν shiftregister 74HC595. Το _Motor Shield_ είναι ικανό να οδηγήσει 2 κινητήρες.


## Απαιτούμενα υλικά και ενδεικτικό κόστος

| Περιγραφή | Ενδεικτικό κόστος(σε € με ΦΠΑ) |
| --- | --- |
| WeMosD1 Mini | 6,98 |
| WeMosD1 | 7,90 |
| Επιταχυνσιόμετρο ADXL335 | 3,99 |
| Arduino shield οδηγού κινητήρα L293D | 4,89 |
| Breadboard | 1,05 |
| Καλώδιακλπ | 2,00 |
| Πλατφόρμα (όχημα) robot | 14,99 |
| Μπαταρίες AA | 1,50 |
| **ΣΥΝΟΛΟ** | **43,30** |

