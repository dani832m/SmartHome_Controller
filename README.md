# SmartHome Controller
A draft for creating a SmartHome Controller in OOD.

### Identify the problem domain

#### Five connected appliances:
    1. Frisk kaffe hver 60. minut, når der er nogen hjemme på adressen.
    2. Lampe i soveværelse skal tænde og slukke, hver gang der klappes.
    3. Når der ringes på dørtelefon, skal der automatisk svares: "GÅ VÆÆÆK!"
    4. Hvis der er østrogen i luften, skal der afspilles "Sexy Mixtape".
    5. Fra fredag kl. 16 til lørdag kl. 01 skal der spilles DAKKEDAK!
    
### Use case
    * Når der registreres aktivitet i lejligheden, hver gang klokken er hel, tændes kaffemaskinen i køkkenet, såfremt der er bønner på.
    * Lampen i soveværelset skal tændes, når der klappes, og slukke igen, når der klappes igen. Her kan anvendes lydcencorer.
    * Når der ringes på dørtelefonen, afspilles automatisk en forudindtalt lydfil, der siger "GÅ VÆÆÆK!".
    * Når duftcensoren registrerer et østogen-niveau, der er over den tilladte grænse, afspilles en lydfil på anlægget.
    * Lydfil afspilles, når klokken er mellem fredag kl. 16 og lørdag kl. 03.
    
### Design your classes
    * Et interface "TurnOnOff.java" oprettes.
    * Et interface "Activity.java" oprettes.
    * "Coffee.java" implementerer "TurnOnOff.java" og "Activity.java", og sørger for, at maskinen er tændt, når aktivitet spores (vha. cencorer).
    * "Lamp.java" implementerer "TurnOnOff.java" og "Activity.java", og binder funktionaliteten sammen.
    * Et interface "TurnOnMusic.java" kan implementeres til "SexyMixtape.java", således at en lydfil afspilles, når der detekteres et bestemt niveau af østrogen i lejligheden.
    * Samme interface kan implementeres til klassen "DakkeDak.java", så metoden deri defineres ud fra, hvad klokken er. Her kan fx bruges Date-klassen.
    
### UML
    UML Class Diagram for projektet kan findes som .png-fil
