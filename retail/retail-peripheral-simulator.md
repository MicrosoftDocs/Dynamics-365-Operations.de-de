---
title: Einzelhandelsperipheriesimulator
description: In diesem Thema wird das Peripheriesimulatortool, das mit Microsoft Dynamics 365 for Operations - Retail bereitgestellt wird.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Einzelhandelsperipheriesimulator

[!include[banner](includes/banner.md)]


In diesem Thema wird das Peripheriesimulatortool, das mit Microsoft Dynamics 365 for Operations - Retail bereitgestellt wird.

<a name="overview"></a>Überblick
--------

Das Microsoft Dynamics 365 for Operations - Retail Peripheriesimulatortool ist ein Tool, mit dessen Hilfe Peripheriegeräte Sie einrichten, testen und beheben, die in der Einzelhandelsumgebung verwendet werden. Sie können das Peripheriesimulatortool verwenden, um die Tests der Einzelhandelsperiperiegeräten zu optimieren, und Probleme zu suchen, die von Setup versagende falsche oder Gerätetreiber verursacht werden. Der ist ein Peripheriesimulator dieses Desktopprogramm, das virtuelle Versionen der Features von Geräten ein, die Dynamics 365 for Operations - Retail unterstützt. Ein Abschnitt für jedes virtuelle Gerät wird die Interaktion zwischen dem und dem POS an. Sie können jedoch auch verwenden, um die Eingabe zu erhalten, die für verschiedene POS-Szenarien gültig ist. Der unterstützt Peripheriesimulator Interaktion zwischen dem POS und den folgenden virtuellen Geräten:

-   **Drucker** – Der Peripheriesimulator kann Belege angezeigt, die für einen POS-Drucker konfiguriert werden.
-   **Zeilendisplay** – Sie können ein virtuelles Zeilendisplay konfigurieren, um auf einem physischen Zeilendisplay anzuzeigen.
-   **Magnetstreifenleser (MSR)** – Sie können Magnetstreifenereignisse simulierte dem POS aus dem Peripheriesimulator senden.
-   **Kassenlade** – Eine physische Geldlade simulieren.
-   **Kassenlade 2** – Indem Sie eine zweite Geldlade im Peripheriesimulator einrichten, können Sie Szenarien simulieren, die ein einzelnes POS-Register bedingt, das zwei aktive Schichten hat.
-   **Scanner** – Der virtuelle Strichcodescanner, den der Peripheriesimulator unterstützt, kann Strichcodescanereignissen ausstellen.
-   **Waage** – Eine Waage wird die Interaktion von gewogenen Artikel dem POS simulieren.
-   **Geheimzahl (PIN) Pad**– Sie können PIN-Pad simulieren. **Hinweis:**Sie müssen Support für eine physische PIN-Feld durch den Zahlungskonnektor implementieren.
-   **Unterschriftserfassung** – Der Peripheriesimulator enthält ein Gerät für elektronische Unterschriften das Sie einrichten können, um Signaturen, die für etwas Zahlungsmittel erforderlich sind, zu Debitorenkontozahlungen wie erforderlich.

Sie können den Peripheriesimulator auch verwenden, um Tastatursektorereignisse zu simulieren, die aus einem Strichcodescanner und einen MSR stammen. Der Simulator des virtuellen Peripheriegeräts unterstützt speziell Object Linking and Embedding für Geräte für Retail POS-Geräte (OPOS).

## <a name="key-scenarios"></a>Wichtige Szenarien
### <a name="troubleshooting"></a>Problembehandlung

Sie können den Peripheriesimulator verwenden, um Geräteinstallation behandeln. Wenn Sie nicht den Peripheriesimulator oder ein zweites Gerät derselben Klasse wurde, kann es sein schwierig, zu ermitteln, woher Abgänge stammen. Wenn Sie jedoch den Peripheriesimulator haben, können Sie virtuelle Geräte einrichten und die gleichen Codepfade und Geschäftslogik ausführen, die für physische Geräte verwendet werden. Aus der Sicht des ist der Peripheriesimulator Hauptunterschied zwischen virtuellen Geräten und Systemtestgeräten das Serviceobjekt oder Gerätetreiber. Für physische Geräte wird das Serviceobjekt für ein Gerät von dem Gerätenhersteller bereitgestellt. Im Kontrast für den Peripheriesimulator die Serviceobjekte, werden als Teil des Peripheriesimulator bereitgestellt. Wenn der Peripheriesimulator ordnungsgemäß funktioniert, wenn ein Gerät nicht ordnungsgemäß funktioniert, nachdem der Gerätename im Hardwareprofil dem Namen eines reellen Geräts geändert wird, können Sie Übernehmen, dass ein Problem für das Serviceobjekt vorhanden, das der Hersteller bereitgestellt hat.

### <a name="training"></a>Schulung

Sie können den Peripheriesimulator verwenden, um eine realistische Ebene Kassierertraining hinzuzufügen, wenn eine physische Hardwareeinstellung nicht verfügbar ist. Wenn der Peripheriesimulator in den Trainingsszenarien einbezogen wird, kann der Kassierer dem Point-of-Sale effektiv interagieren, indem er wie Produktstrichcodescans eingegeben und Geschenkkarteschläge bereitstellt und indem er berücksichtigen soll, auf welche Zugänge für eine bestimmte Buchung gedruckt.

### <a name="testing"></a>Testen

Sie können den Peripheriesimulator verwenden, um Produktstrichcodes, Bonlayouts zu testen usw. ohne zu müssen, physischen Hardware in einer Umgebung virtuellen bereitzustellen. Da physische Hardware nicht erforderlich ist und Sie einen POS-Kunden auf einer physischen Hardwarestation oder einem Computer nicht eingehalten werden müssen, können Änderungen schneller Sie testen, bei denen im Back Office erst vorgenommen werden.

## <a name="set-up-the-peripheral-simulator"></a>Peripheriesimulator einrichten
### <a name="set-up-a-hardware-profile"></a>Einrichten von Hardwareprofilen

1.  Um den Peripheriesimulator einzurichten, klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofile**.
2.  Klicken Sie auf **Neu**, um ein neues Profil zu erstellen.
3.  Geben Sie im Feld **Profilnumer** und **Beschreibung** einen Wert ein.
4.  Verwenden Sie die folgenden Tabelle zur Einrichtung. Hier ist eine Erläuterung der Spalten der Tabelle:
    -   **Gerät** – Diese Spalte gibt die Namen des Inforegisters, dem Sie erweitert werden, um das Gerät zu installieren.
    -   **Einheitentyp** – diese Spalte gibt den Wert, den Sie im Feld auswählen, wird der Name des Geräts versehen wird.
    -   **Gerätename** – diese Spalte gibt den genauen Wert, den Sie für den Gerätenamen eingeben. **Wichtig:** Die Gerätenamen, die hier angegeben sind, erforderlich, da die Hardwarestation diese bestimmten Namen der Adresse die Geräte verwendet. Wurde diese bestimmten Namen verwenden, lautet das Gerät nicht verwendbar.

    | Gerät            | Gerätetyp | Gerätename              |
    |-------------------|-------------|--------------------------|
    | Drucker           | OPOS        | MockOPOSPrinter          |
    | Zeilenanzeige      | OPOS        | MockOPOSLineDisplay      |
    | MSR               | OPOS        | MockOPOSMSR              |
    | Aussteller            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Scanner           | OPOS        | MockOPOSScanner          |
    | Skalieren             | OPOS        | MockOPOSScale            |
    | PIN-Feld           | OPOS        | MockOPOSPinPad           |
    | Signaturerfassung | OPOS        | MockOPOSSignatureCapture |

**Hinweis:**Keine bestimmten Einstellungen im Hardwareprofil ist erforderlich, Tastatursektorereignisse vom Strichcodescanner und vom MSR zu simulieren.

### <a name="assign-the-hardware-profile-to-a-register"></a>Zuweisen eines Hardwareprofils zu einem Register

1.  Nachdem das Hardwareprofil erstellt wurde, fahren **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **Register**.
2.  In der **POS-Register** Liste klicken Sie auf den Link für das **Registernummer** Feld für das Register, das den Peripheriesimulator verwenden.
3.  Klicken Sie auf **Bearbeiten**.
4.  Im **Profile **Abschnitt im Feld **Hardwareprofil** Feld, wählen Sie das Hardwareprofil aus, das Sie für virtuelle Peripheriegeräte erstellt haben.
5.  Klicken Sie auf **Speichern**.

### <a name="synchronize-changes-to-the-channel-database"></a>Änderungen an die Kanaldatenbank synchronisieren

1.  Wechseln Sie zu **Einzelhandel und Handel** &gt; **IT (Einzelhandel)** &gt; **Vertriebsplan**.
2.  Wählen Sie den Vertriebsplan **1090** aus.
3.  Klicken Sie auf **Jetzt ausführen**, um die Änderungen am POS zu synchronisieren.

Nachdem die Daten synchronisiert sind, sind das Hardwareprofil neue und die Änderungen im Register in der Kanaldatenbank verfügbar.

## <a name="install-the-peripheral-simulator"></a>Peripheriesimulator installieren
1.  Wechseln Sie zu **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofile**.
2.  Klicken Sie Auf **Download** und klicken dann **PeripheralSimulator**. **Hinweis:** Sie müssen Popupblocker beenden, bevor Sie den Peripheriesimulator herunterladen können.
3.  Nachdem der Abschluss Download, öffnen Sie den Ordner für **Downloads** und doppelklicken Sie **VirtualPeripherals.msi** um das Installationsprogramm zu starten.
4.  Installieren Sie den Peripheriesimulator, indem Verwendung der Standardeinstellungen.

Zusätzlich zum Peripheriesimulator müssen die Objekte der gemeinsamen Regelung von Monroe Consulting Services einrichten. Andernfalls arbeitet der Peripheriesimulator nicht korrekt. Um den Objekten der gemeinsamen Regelung herunterzuladen, wechseln Sie zu <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Peripheriesimulator nutzen
Um den Peripheriesimulator zu nutzen, Klicken Sie auf **Start** auf dem Computer, geben Sie **Peripheriesimulator** ein, und wählen Sie dann aus, wenn er in den Suchergebnissen angezeigt wird. Nachdem Sie den Peripheriesimulator gestartet wurde, klicken Sie auf, um einen Gerätenamen die unterstützten Geräte anzuzeigen. Diese Geräte werden als Registerkarten links des Fensters aufgeführt. Wenn Sie ein bestimmtes Gerät anzuzeigen, klicken Sie auf die Registerkarte für dieses Gerät.

### <a name="line-display-capabilities"></a>Parameter für Zeilendisplays

Das Zeilendisplay ist er erste Gerät, das im Peripheriesimulator aufgeführt ist. Wenn das virtuelle Zeilendisplay konfiguriert ist, wird der Artikel an, die im Formular im Lieferumfang POS-Buchung werden. Neben den Positionen wird die Anzeige die Summe an, die fällig ist, wenn am POS ein Zahlungsmittel ausgewählt wurde. Außerdem wird das Saldo an, der fällig ist, wenn ein Zahlungsmittel eingegeben wird, doch ein Saldo für die Buchung noch fällig ist. Wenn vom POS nicht verwendet wird, kann eine Nachricht angezeigt werden, um anzugeben, dass bis geschlossen wird. Sie müssen die Nachricht im **Zeilendisplay** Inforegister im Hardwareprofil konfigurieren.

### <a name="cash-drawer-capabilities"></a>Geldlade-Funktionen

Die Geldlade ist das zweite Gerät, das im Peripheriesimulator aufgeführt ist. Wenn das Hardwareprofil konfiguriert wird, um virtuelle Geldladen zu verwenden, wird der Betrag vom POS die Kassenlade für die aktuelle Schicht als Reaktion auf Kassenladearbeitsgänge wie kann und damit der Kassierer Änderung vornehmen oder Bargeld während der cash-and-carry Standardbuchungen einzahlen kann. Die Geldladen virtuellen haben Bezeichnungen **Hauptkassenlade** und **Sekundäre Kassenlade**. Diese Beschriftungen enthalten Kassenlade und Kassenlade 2 im Hardwareprofil Geldlade. Wenn eine Kasse geschlossen ist, wird einem Bild einer abgeschlossenen Geldlade angezeigt, und die Schaltfläche auf der geschlossenen Geldlade wird als **Offene Kassenlade** gezeigt. Wenn Sie auf diese Schaltfläche klicken, wird das Bild durch ein Bild einer offenen Geldlade ersetzt, um anzugeben, dass jetzt die Geldlade geöffnet ist. Die Schaltfläche für die offene (n Geldlade wird als bezeichnet **Kassenlade schließen**. Einige Arbeitsgänge am POS die Kassenlade können veranlassen sie zu öffnen. Die meisten Arbeitsgänge können nicht fortfahren, wenn die Geldlade geöffnet ist. Eine Ausnahme einige Prozeduren am Tagesende. Wenn der POS-Benutzer eine Fehlermeldung erhalten, die angibt, dass ein Arbeitsgang nicht ausgeführt werden kann, wenn die Geldlade geöffnet ist, muss der Benutzer der virtuelle oder physischer Geldlade schließen, um fortzufahren. Wenn eine Geldlade als **Freigegeben** im Hardwareprofil markiert wird, überprüft das System dafür, dass die Kassenlade vor einem Arbeitsgang abgeschlossen wird. Der Arbeitsgang beginnt wie gewohnt fort, wenn die Geldlade geöffnet ist. Dieses Verhalten unterstützt Szenarien, in denen Geldladen unter Vertriebsmitarbeitern freigegeben werden, und mithilfe eine Geldlade zuordnen, während andere beziehen, nicht verwandte Aufgaben auf seinem eigenem oder POS-Gerät ausführt. Ändert, das der Geldlade werden nicht offensichtlich vorgenommen werden, wenn die aktuelle Schicht abgeschlossen ist und eine neue Schicht geöffnet wird.

### <a name="msr-capabilities"></a>MSR-Funktionen

Der Peripheriesimulator zulässig robusten Support für virtuelle MSR-Arbeitsgänge, indem Sie entweder in OPOS- Tastatur oder im Weichenmodus arbeitet. Der OPOS-Modus setzt voraus, dass das im MSR Hardwareprofil konfiguriert ist, wählen als OPOS-Gerät zu arbeiten. Der Tastaturweichenmodus sendet derzeit Tastatursektordatenereignisse zu Microsoft Windows. Außer Unterschiede in den Einstellungen, unterscheiden sich OPOS- und Tastatursektormodi wie folgt:

-   Der POS-Kunde aktiviert Geräte um anzugeben Szenarien für bestimmte, als auch Szenarien ermittelt, die Magnetstreifendaten Treue oder Geschenkkarteeintrag zulässig ist.
-   Im Tastaturweichenmodus sendet der Peripheriesimulator Tastatursektordaten dem Feld, das aktiv ist, wenn die Daten gesendet werden. Dieses Verhalten ähnelt zum Verhalten, das auftritt, wenn die Daten eingegeben werden, indem eine Tastatur verwendet. Um einen MSR (Magnetstreifenleser) als Tastatursektor verwenden zu können, muss der Benutzer zu Retail Modern POS (MPOS) wechseln um sicherzustellen ob Daten in das richtige Feld eingehen. Daher können Sie eine Verzögerung konfigurieren, dass der Benutzer über Zeit verfügt, zu überprüfen, ob die richtigen Daten dem Feld gesendet werden.

#### <a name="testing-gift-and-payment-card-swipes"></a>Geschenk- und Zahlungskarten testen

Das virtuelle MSR, das der Peripheriesimulator auch bereitstellt, können Sie bestimmte MSR-Daten zu den Testszenarien für Geschenk- und Zahlungskarte nach Lesegerät konfigurieren. Um eine Karte erstellen, auf die Schaltfläche klicken das Pluszeichens (**+**), den Kreditkartentyp und auswählen. Geben Sie anschließend die Kartennummer anzeigen oder Nachverfolgen von Daten, die dem POS, zusammen mit dem Ablaufmonat und Jahr für die Karte gesendet werden sollen, die Sie definieren. Der Wert, den Sie im Feld auswählen **Kreditkartentyp**, Feld ist derzeit eine Beschriftung, die einer Karte zugeordnet werden kann. Diese Bezeichnung wird es einfacher, Karten zu identifizieren, wenn dies im Peripheriesimulator Karte durch ein Lesegerät gezogen werden. Karten können auswählen, die im Peripheriesimulator konfiguriert wurden, indem die Schaltfläche mit dem Pfeil nach links (**&lt;**)und mit dem Pfeil nach rechts (**&gt;**) zu dem Bild der Karte ein. Sie können bearbeitet und Karten, indem Sie **Bearbeiten** und **Löschen** Schaltflächen neben der Schaltfläche verwenden des Pluszeichens (**+**)

### <a name="pin-pad"></a>PIN-Feld

Sie können den PIN-Pad-Simulator konfigurieren, um eine OPOS-PIN-Auflage zu simulieren. Wenn eine Buchung (EFT)- für elektronische Überweisungen am Point-of-Sale ausgeführt und PIN-Eintrag erforderlich ist, die Hardwarestationsanrufe das PIN-Gerät, um zu PIN-Eintrag erforderlich. Um zu umgehen, benötigt das PIN-Feld im Peripheriesimulator Unterstützung des EFT-Konnektors.

### <a name="printer"></a>Drucker

Der Drucker des virtuellen Peripheriegeräts werden derzeit Zugänge an, wenn diese vom POS gedruckt werden. Wenn ein Druckvorgang mehrere Zugänge erzeugt, können Sie die Belege zurücksetzen.

#### <a name="configure-receipt-printing"></a>Bondrucker konfigurieren

1.  Wechseln Sie zu **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofile**.
2.  Wählen Sie das Hardwareprofil aus, das Sie für virtuelle Peripheriegeräte erstellt haben.
3.  Klicken Sie im Formular **Drucker** auf **Bearbeiten**.
4.  Im Feld **Bonprofilkennung** ein Bonprofil aus.
5.  Klicken Sie auf **Speichern**.

### <a name="scale"></a>Skalieren

Wenn ein Wagenprodukt der POS-Buchung hinzugefügt wird und eine Waage konfiguriert wird, ruft das POS das Gewicht von der Waage ab. Für der virtuelle und physische Waage, sollte das Produkt oder Gewicht angegeben werden, bevor das Produkt der Buchung hinzugefügt wird. Bevor Sie das Waagenprodukt der Buchung hinzufügen, wechseln zur Sie im Peripheriesimulator, und verwenden Sie das Pluszeichen (**+**) und Schaltflächen des Minuszeichens (**–**), zum Gewicht anzupassen, das den Maßstab fertig melden soll. Sie können den Sollgewicht direkt im Feld **Aktueller Wert** Feld auch eine eingeben. Sie können die Gewichtseinheiten auf die Waage regulieren, indem Sie das Pluszeichen (**+**), **Bearbeiten** und **Löschen** Schaltflächen. Auf diese Weise können Einheiten auf Grundlage die Produkte geliefert werden, die oder Auswählen des Gebietsschemas gewogen werden, in dem den Maßstab verwendet wird.

#### <a name="configure-a-scale-product"></a>Waagenprodukt konfigurieren

1.  Navigieren Sie zu **Einzelhandel und Handel****** &gt; **Produkte und Kategorien** &gt; **Freigegebene Produkte nach Kategorie.**
2.  Öffnen Sie den Produktdatensatz.
3.  Wählen Sie das Produkt zum Wiegen aus.
4.  Wählen Sie im Inforegister **Einzelhandel** wählen Sie die Option aus **Waagenprodukt** **Nein** auf **Ja**

#### <a name="synchronize-changes-to-the-channel-database"></a>Änderungen an die Kanaldatenbank synchronisieren

1.  Wechseln Sie zu **Einzelhandel und Handel** &gt; **IT (Einzelhandel)** &gt; **Vertriebsplan**.
2.  Wählen Sie den Vertriebsplan **1040** aus.
3.  Klicken Sie auf **Jetzt ausführen**, um die Änderungen am POS zu synchronisieren.

Wenn ein Wagenprodukt der POS-Buchung hinzugefügt wird und eine Waage konfiguriert wird, ruft das POS das Gewicht von der Waage ab.

### <a name="signature-capture"></a>Signaturerfassung

Das virtuelle Gerät für elektronische Unterschriften fordert den Benutzer auf, eine Unterschrift auf der Signatur virtuellen bereitzustellen aufzeichnen Auflage, wenn das Zahlungsmittel, das verwendet wird, eine Signatur erfordert. Der Benutzer kann die Signatur akzeptieren, um diese am Point-of-Sale angezeigt. Der Kassierer kann dann akzeptieren die Signatur. Die Unterschrift wird dann zusammen mit dem Zahlungsmittel wird gespeichert und an das zuständige Back-Office-Team sowie weitere Buchungsdaten synchronisiert.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Richten Sie ein Zahlungsmittel, um eine Unterschrift festzulegen

1.  Navigieren Sie zu **Einzelhandel und Handel** &gt; **Kanäle** &gt; **Einzelhandelsgeschäfte** &gt; **Alle Einzelhandelsgeschäfte.**
2.  Wählen Sie den Shop aus.
3.  Klicken Sie auf **Bearbeiten**.
4.  Klicken Sie auf **Einstellungen** und dann auf **Einstellungen** im Abschnitt **Zahlungsmethoden**.
5.  Klicken Sie auf **Bearbeiten**.
6.  Wählen Sie eine Zahlungsmethode aus, die eine Unterschrift erfordert.
7.  Im Abschnitt **Allgemein ** unter **Unterschrifterfassung** legen Sie die **Gerät für elektronische Unterschriften verwenden** Option auf **Ja** fest.
8.  Wählen Sie im **Mindestbetrag für Signaturerfassung** Feld geben Sie den Mindestbetrag ein, der Signatur auslösen soll aufzeichnen.

#### <a name="synchronize-changes-to-the-channel-database"></a>Änderungen an die Kanaldatenbank synchronisieren

1.  Wechseln Sie zu **Einzelhandel und Handel** &gt; **IT (Einzelhandel)** &gt; **Vertriebsplan**.
2.  Wählen Sie den Vertriebsplan **1070** aus.
3.  Klicken Sie auf **Jetzt ausführen**, um die Änderungen am POS zu synchronisieren.

Nachdem die Daten synchronisiert sind, wenn ein Zahlungsmittel, die erforderlich, um eine Unterschrift verwendet wird und der Betrag den Unterzeichnungsschwellenwert gilt, die POS-Verlangungen eine Unterschrift auf dem virtuellen. Gerät für elektronische Unterschriften

## <a name="additional-configuration"></a>Zusätzliche Konfiguration
Sie können die Zusatzkonfigurationsdatei zur Adresse des Simulators passender bearbeiten die Szenarien, den Sie testen. Sie können die Konfigurationsdatei hier finden: C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Die freizugebenden wird die Einheit, der für das Testen auf die Waage, den Kartentypen, der für das Testen verfügbar sind und den Strichcodetypen verfügbar sind. Beispielsweise indem Sie die Textwerte in Konfigurationsdatei ändern, können Sie einen neuen Kartentyp eine Maßeinheit oder hinzufügen, die zur Bearbeitungszeit ausgewählt werden können. Die neue Werte angezeigt werden, nachdem der Zeit-App Neustart.

## <a name="troubleshooting"></a>Problembehandlung
Aktivitäten für den Peripheriesimulator werden innerhalb des Peripheriesimulators protokolliert. Sie können die Protokoll hier finden C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. der Peripheriesimulator Speicher auch Probleme im Windows-Ereignisprotokoll, an dem Sie über **Anwendung und an Diensten** &gt; **Microsoft** &gt; **DynamicsAX** zugreifen können. Wenn Änderungen, die Sie dem Hardwareprofil oder in andere Bereiche vorgenommenen, nicht offensichtlich sind, wenn Sie MPOS oder den Peripheriesimulator verwenden, sollten Sie die Verteilungssteuerprogrammeinzelvorgänge, die Sie verwenden, um die Daten anzuzeigen Kanaldatenbank zu synchronisieren. Wenn die Änderungen synchronisiert wurden, aber noch nicht am POS offensichtlich sind, starten Sie den POS-Kunden neu. Änderungen an Geldladen konfigurierten sind nicht gültig, sofern keine neue Schicht erstellt wurde. Wenn Sie Änderungen an den Geldladen vornehmen, prüfen Sie, ob Sie immer die vorhandene Schicht schließen, um die neue Geldladeneinstellung zu testen. Manchmal wenn der Fahrer des Herstellers nach Objekten der gemeinsamen Regelung von den Monroe-Beratungsdiensten eingerichtet wird, kann die Fahrer die Objekte der gemeinsamen Regelung veranlassen einwandfrei, die Arbeit einzustellen. In diesem Fall sollten Sie die abweichenden Objekte der gemeinsamen Regelung erneut installieren.

<a name="see-also"></a>Siehe auch
--------

[Einzelhandelsperipheriegeräte – Überblick](retail-peripherals-overview.md)




