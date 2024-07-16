# Simulatore-ATM
Gli attuali ATM, seppur provvisti di un valido sistema di sicurezza (dato dal PIN segreto), spesso sono nel mirino di criminali che hanno l’obiettivo di clonare la carta inserita e risalire al PIN segreto per poi effettuare operazioni non previste dal reale utente. Proprio su questo punto chiave si è basato il lavoro svolto in questo progetto. Librerie QR-Code:

Zxing: ZXing ("zebra crossing") è una libreria di elaborazione di codice a barre 1D/2D multi formato ed open-source implementata in java, con porting ad altri linguaggi. Librerie Webcam:
WebcamCapture: Questa libreria consente di sfruttare webcam integrate o esterne direttamente tramite java. È stata progettata per astrarre le caratteristiche comunemente utilizzate dalle fotocamere.
Webcam.getWebcams(): Acquisisce la lista delle webcam disponibili. Questo metodo attenderà un intervallo di tempo predefinito necessario ad individuare i device disponibili. Di default è settato ad un minuto.
Webcam.isOpen(): restituisce VERO se la webcam è attiva, FALSO altrimenti.
Webcam.getImage(): Cattura immagini dalla Webcam e le restituisce. Restituirà un oggetto di tipo immagine o NULL nel caso la webcam sia disattivata o sia stata disabilitata dalla JVM.
LuminanceSource: Lo scopo di questa classe è di astrarre le diverse implementazioni di un’immagine bitmap da diverse piattaforme in un formato con valori standard in scala di grigi.
BinaryBitmap: Questa è la classe principale utilizzata da Zxing per rappresentare un dato binario.
HybridBinarizer: Si occupa della binarizzazione dell’immagine acquisita. È progettata per le immagini di codici a barre ad alta frequenza con dati neri su sfondo bianco.
MultiFormatReader: Di default cerca di decodificare tutti i formati di codici a barre supportati dalla libreria. Opzionalmente, si può richiedere un differente comportamento, ad esempio solo la decodifica di QRCode.
MultiFormatReader.decode(BinaryBitmap image): decodifica l’immagine passata come argomento nella maniera di default (senza specificare nessun particolare tipo di decodifica)
Random: Un’istanza di questa classe è usata per generare un flusso di numeri pseudocasuali. Questa classe usa un seme di 48 bit, che è modificata usando una formula lineare.
Random.nextInt(int n): Genera un numero pseudocasuale compreso tra 0 (incluso) ed n (escluso).
Come si può facilmente capire l’OTP generato risulta essere un codice di quattro cifre, comprese fra 1000 e 9999, generato senza l’utilizzo di un particolare algoritmo, ma in maniera del tutto pseudocasuale.
