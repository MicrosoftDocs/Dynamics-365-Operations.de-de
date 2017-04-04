---
title: Retail peripheral simulator
description: "In diesem Thema wird das Zusatzsimulatortool, das mit Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge bereitgestellt wird."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
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

# <a name="retail-peripheral-simulator"></a>Retail peripheral simulator

In diesem Thema wird das Zusatzsimulatortool, das mit Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge bereitgestellt wird.

<a name="overview"></a>Überblick
--------

Das Microsoft Dynamics 365 für Arbeitsgänge - Kleinzusatzsimulator ist ein Tool, mit dessen Hilfe Peripheriegeräte Sie einrichten, testen und beheben, die in der Kleinumgebung verwendet werden. Sie können den Zusatzsimulator verwenden, um die Tests der Kleinperipheriegeräten zu optimieren, und Probleme zu suchen, die von Setup versagende falsche oder Gerätetreiber verursacht werden. Der ist ein Zusatzsimulator dieses Tischplattenprogramm virtuelle Versionen der Features von Geräten ein, die Dynamics 365 für Einzelhandel - Arbeitsgänge unterstützt. Ein Abschnitt für jedes virtuelle Gerät wird die Interaktion zwischen dem und der Kleinverkaufsstelle Gerät (POS) an. Sie können jedoch auch verwenden, um die Eingabe zu erhalten, die für verschiedene POS-Szenarien gültig ist. Der unterstützt Zusatzsimulator Interaktion zwischen dem POS und den folgenden virtuellen Geräten:

-   ** Drucker ** – Der Zusatzsimulator kann Zugänge angezeigt, die für einen POS-Drucker konfiguriert werden.
-   ** Zeilendisplay ** – können Sie ein virtuelles Zeilendisplay Aktivität konfigurieren, um auf einem physischen Zeilendisplay anzuzeigen.
-   ** Magnetstreifenleser (MSR) ** – Sie können Magnetstreifenereignisse simulierte dem POS aus dem Zusatzsimulator senden.
-   ** Kassenlade ** – Eine physische Geldlade simulieren.
-   ** Kassenlade 2 ** – indem Sie eine zweite Geldlade im Zusatzsimulator einrichten, können Sie Szenarien simulieren, die ein einzelnes POS-Register bedingt, das zwei aktive Schichten hat.
-   ** Scanner ** – Der virtuelle Strichcodescanner, den der Zusatzsimulator unterstützt, kann Strichcodescanereignissen ausstellen.
-   ** Waage ** virtuelle – Eine Waage wird die Interaktion von gewogenen Artikel dem POS simulieren.
-   ** Geheimzahl (PIN)- Auflage ** – Sie können PIN-Auflagenarbeitsgänge simulieren. ** Hinweis: ** Sie müssen Support für eine physische PIN-Feld durch den Zahlungskonnektor implementieren.
-   ** Signatur zeichnen ** – den Zusatzsimulator enthält ein Gerät für elektronische Unterschriften virtuelles auf, das Sie einrichten können, um Signaturen, die für etwas Zahlungsmittel erforderlich sind, zu Debitorenkontozahlungen wie erforderlich.

Sie können den Zusatzsimulator auch verwenden, um Tastatursektorereignisse zu simulieren, die aus einem Strichcodescanner und einen MSR stammen. Der Simulator des virtuellen Peripheriegeräts unterstützt speziell Object Linking and Embedding für Geräte um Retail POSs ().

## <a name="key-scenarios"></a>Entscheidende Szenarien
### <a name="troubleshooting"></a>Problembehandlung

Sie können den Zusatzsimulator verwenden, um Geräteinstallation behandeln. Wenn Sie nicht den Zusatzsimulator oder ein zweites Gerät derselben Klasse wurde, kann es sein schwierig, zu ermitteln, woher Abgänge stammen. Wenn Sie jedoch den Zusatzsimulator haben, können Sie virtuelle Geräte einrichten und die gleichen Codepfade und Geschäftslogik ausführen, die für physische Geräte verwendet werden. Aus der Sicht des ist der Zusatzsimulators Hauptunterschied zwischen virtuellen Geräten und Systemtestgeräten das Serviceobjekt oder Gerätetreiber. Für physische Geräte wird das Serviceobjekt aus dem Gerätenhersteller bereitgestellt. Durch Kontrast für den Zusatzsimulator die Serviceobjekte, werden als Teil des Zusatzsimulators bereitgestellt. Wenn der Zusatzsimulator ordnungsgemäß funktioniert, wenn ein Gerät nicht ordnungsgemäß funktioniert, nachdem der Gerätename im Hardwareprofil dem Namen eines reellen Geräts geändert wird, können Sie " Übernehmen, dass ein Problem für das Serviceobjekt vorhanden, das der Hersteller bereitgestellt hat.

### <a name="training"></a>Schulung

Sie können den Zusatzsimulator verwenden, um eine realistische Ebene Kassierertraining hinzuzufügen, wenn eine physische Hardwareeinstellung nicht verfügbar ist. Wenn der Zusatzsimulator in den Trainingsszenarien einbezogen wird, kann der Kassierer dem Point-of-Sale effektiv interagieren, indem er wie Produktstrichcodescans eingegeben und Geschenkkarteschläge bereitstellt und indem er berücksichtigen soll, auf welche Zugänge für eine bestimmte Buchung gedruckt.

### <a name="testing"></a>Testen

Sie können den Zusatzsimulator verwenden, um Produktstrichcodes, Bonlayouts zu testen usw. ohne zu müssen, physischen Hardware in einer Umgebung virtuellen bereitzustellen. Da physische Hardware nicht erforderlich ist und Sie einen POS-Kunden auf einer physischen Hardwarestation oder einem Computer nicht eingehalten werden müssen, können Änderungen schneller Sie testen, bei denen im Back Office erst vorgenommen werden.

## <a name="set-up-the-peripheral-simulator"></a>Richten Sie den Zusatzsimulator
### <a name="set-up-a-hardware-profile"></a>Richten Sie ein Hardwareprofil

1.  Um den Zusatzsimulator eingerichtet, fahren ** Sie Einzelhandel und Handel ** ** &gt; richtet der Kanal ** ** &gt; POS eingerichtet ** ** &gt; POS-Profile ** ** &gt; Hardwareprofile **.
2.  Wenn ein neues Profil zu erstellen, klicken Sie erneut ** **.
3.  Geben Sie Werte in ** Profilnummer ** und ** Beschreibung ** die Felder ein.
4.  In der folgenden Tabelle, um den virtuellen Geräte einrichten, die getestet werden müssen. Ist eine kurze Erläuterung der Spalten in der folgenden Tabelle:
    -   ** Gerät ** – diese Spalte gibt die Namen des Inforegisters, dem Sie erweitert werden, um das Gerät zu installieren.
    -   ** Einheitentyp ** – diese Spalte gibt den Wert, den Sie im Feld auswählen, wird der Name des Geräts versehen wird.
    -   ** Gerätename ** – diese Spalte gibt den genauen Wert, den Sie für den Gerätenamen eingeben. ** Wichtig: ** Die Gerätenamen, die hier angegeben sind, erforderlich, da die Hardwarestation diese bestimmten Namen der Adresse die Geräte verwendet. Wurde diese bestimmten Namen verwenden, lautet das Gerät nicht verwendbar.

    | Gerät            | Gerätetyp | Gerätename              |
    |-------------------|-------------|--------------------------|
    | Drucker           | Um        | MockOPOSPrinter          |
    | Zeilenanzeige      | Um        | MockOPOSLineDisplay      |
    | MSR               | Um        | MockOPOSMSR              |
    | Aussteller            | Um        | MockOPOSDrawer1          |
    | Drawer2           | Um        | MockOPOSDrawers          |
    | Scanner           | Um        | MockOPOSScanner          |
    | Skalieren             | Um        | MockOPOSScale            |
    | PIN-Feld           | Um        | MockOPOSPinPad           |
    | Signaturerfassung | Um        | MockOPOSSignatureCapture |

** Hinweis: ** Keine bestimmten Einstellungen im Hardwareprofil ist erforderlich, Tastatursektorereignisse vom Strichcodescanner und vom MSR zu simulieren.

### <a name="assign-the-hardware-profile-to-a-register"></a>Verteilt das Register zu einem Hardwareprofil

1.  Nachdem das Hardwareprofil erstellt wurde, fahren ** Einzelhandel und Handel ** &gt; ** richtet der Kanal ** &gt; ** POS eingerichtet ** &gt; ** Register **.
2.  ** POS-Register ** In der Liste klicken Sie auf den Link für das Datenverarbeitungsregister ** ** Feld für das Register, das den Zusatzsimulator verwenden.
3.  Klicken Sie auf **Bearbeiten**.
4.  ** ** Profile im Abschnitt im Feld Hardwareprofil ** ** Feld, wählen Sie das Hardwareprofil aus, das Sie für virtuelle Peripheriegeräte erstellt haben.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synchronisieren Sie Änderungen an der Kanaldatenbank

1.  Wechseln ** Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
2.  Wählen Sie den Verteilungszeitplan ** ** 1090 aus.
3.  ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.

Nachdem die Daten synchronisiert sind, sind das Hardwareprofil neue und die Änderungen im Register in der Kanaldatenbank verfügbar.

## <a name="install-the-peripheral-simulator"></a>Richten Sie den Zusatzsimulator
1.  Wechseln ** Einzelhandel und Handel ** &gt; ** richtet der Kanal ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwareprofile **.
2.  ** Auf Download ** und klicken dann PeripheralSimulator ** **. ** Hinweis: ** Sie müssen Popupblocker beenden, bevor Sie den Zusatzsimulator herunterladen können.
3.  Nachdem der Abschluss Download, öffnen Sie den Ordner für Downloads ** **, und doppelklicken Sie VirtualPeripherals.msi ** ** um das Installationsprogramm zu starten.
4.  Richten Sie den Zusatzsimulator, indem Verwendung der Standardeinstellungen.

Zusätzlich zum Zusatzsimulator müssen die Objekte der gemeinsamen Regelung von den Monroe-Beratungsdiensten einrichten. Andernfalls arbeitet der Zusatzsimulator nicht korrekt. Um den Objekten der gemeinsamen Regelung herunterzuladen, fahren Sie http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Verwenden des Zusatzsimulators
Um den Zusatzsimulator, auf den Beginn ** ** auf dem Computer, Typ beginnen ** Kleinzusatzsimulator ** der Zeit-App, und wählen Sie dann aus, wenn er in den Suchergebnissen angezeigt wird. Nachdem Sie den Zusatzsimulator gestartet wurde, klicken Sie auf, um einen Gerätenamen die unterstützten Geräte anzuzeigen. Diese Geräte werden als Registerkarten links des Fensters aufgeführt. Wenn Sie ein bestimmtes Gerät anzuzeigen, klicken Sie auf die Registerkarte für dieses Gerät.

### <a name="line-display-capabilities"></a>Zeilendisplayfunktionen

Das Zeilendisplay ist er erste Gerät, das im Zusatzsimulator aufgeführt ist. Wenn das virtuelle Zeilendisplay konfiguriert ist, wird der Artikel an, die im Formular im Lieferumfang POS-Buchung werden. Neben den Positionen wird die Anzeige die Summe an, die fällig ist, wenn am POS ein Zahlungsmittel ausgewählt wurde. Außerdem wird das Saldo an, der fällig ist, wenn ein Zahlungsmittel eingegeben wird, doch ein Saldo für die Buchung noch fällig ist. Wenn vom POS nicht verwendet wird, kann eine Nachricht angezeigt werden, um anzugeben, dass bis geschlossen wird. Sie müssen die Nachricht im Zeilendisplay ** ** Inforegister im Hardwareprofil konfigurieren.

### <a name="cash-drawer-capabilities"></a>Geldladenfunktionen

Die zweite Geldlade ist das Gerät, das im Zusatzsimulator aufgeführt ist. Wenn das Hardwareprofil konfiguriert wird, um virtuelle Geldladen zu verwenden, wird der Betrag vom POS die Kassenlade für die aktuelle Schicht als Reaktion auf Kassenladearbeitsgänge wie kann und damit der Kassierer Änderung vornehmen oder " Bargeld- während der cash-and-carry StandardBuchungen einzahlen kann. Die Geldladen virtuellen haben Bezeichnungen ** Hauptkassenlade ** ** und sekundäre Kassenlade **. Diese Beschriftungen enthalten Kassenlade und 2 im Hardwareprofil Geldlade, z dar. Wenn eine Kasse geschlossen ist, wird einem Bild einer abgeschlossenen Geldlade angezeigt, und die Schaltfläche auf der geschlossenen Geldlade wird als bezeichnet ** offene Kassenlade **. Wenn Sie auf diese Schaltfläche klicken, wird das Bild durch ein Bild einer offenen Geldlade ersetzt, um anzugeben, dass jetzt die Geldlade geöffnet ist. Die Schaltfläche für die offene (n Geldlade wird als bezeichnet ** neben Kassenlade **. Einige Arbeitsgänge am POS die Kassenlade können veranlassen sie zu öffnen. Die meisten Arbeitsgänge können nicht fortfahren, wenn die Geldlade geöffnet ist. Eine Ausnahme einige Prozeduren am Tagesende. Wenn der POS-Benutzer eine Fehlermeldung erhalten, die angibt, dass ein Arbeitsgang nicht ausgeführt werden kann, wenn die Geldlade geöffnet ist, muss der Benutzer der virtuelle oder physischer Geldlade schließen, um fortzufahren. Wenn eine Geldlade wie ** freigegeben ** im Hardwareprofil markiert wird, überprüft das System dafür, dass die Kassenlade vor einem Arbeitsgang abgeschlossen wird. Der Arbeitsgang beginnt wie gewohnt fort, wenn die Geldlade geöffnet ist. Dieses Verhalten unterstützt Szenarien, in denen Geldladen unter Vertriebsmitarbeitern freigegeben werden, und mithilfe eine Geldlade zuordnen, während andere beziehen, nicht verwandte Aufgaben auf seinem eigenem oder POS-Gerät ausführt. Ändert, das der Geldlade werden nicht offensichtlich vorgenommen werden, wenn die aktuelle Schicht abgeschlossen ist und eine neue Schicht geöffnet wird.

### <a name="msr-capabilities"></a>MSR-Funktionen

Der Zusatzsimulator zulässig robusten Support für virtuelle MSR-Arbeitsgänge, indem Sie entweder in OPOS- Tastatur oder im sektormodus arbeitet. OPOS-Modus setzt voraus, dass das im MSR Hardwareprofil konfiguriert ist, wählen als OPOS-Gerät zu arbeiten. Tastatursektormodus sendet derzeit Tastatursektordatenereignisse zu Microsoft Windows. Außer Unterschiede in den Einstellungen, unterscheiden sich OPOS- und Tastatursektormodi wie folgt:

-   Der POS-Kunde aktiviert Geräte um anzugeben Szenarien für bestimmte, als auch Szenarien ermittelt, die Magnetstreifendaten Treue oder Geschenkkarteeintrag zulässig ist.
-   Im sektormodus Tastatur sendet der Zusatzsimulator Tastatursektordaten dem Feld, das aktiv ist, wenn die Daten gesendet werden. Dieses Verhalten ähnelt zum Verhalten, das auftritt, wenn die Daten eingegeben werden, indem eine Tastatur verwendet. Um einen MSR (Magnetstreifenleser) als Tastatursektor verwenden zu können, muss der Benutzer zu modernem KleinPOS () wechseln MPOS um sicherzustellen ob Daten in das richige Feld eingehen. Daher können Sie eine Verzögerung konfigurieren, dass der Benutzer Uhrzeit verfügt, zu überprüfen, ob die richtigen Daten dem Feld gesendet werden.

#### <a name="testing-gift-and-payment-card-swipes"></a>Testsgeschenk- und -Zahlungsziehen der karte nach lesegerät

Das virtuelle MSR, das der Zusatzsimulator auch bereitstellt, können Sie bestimmte MSR-Daten zu den Testszenarien für Geschenk- und Zahlungsziehen der karte nach lesegerät konfigurieren. Um eine Karte erstellen, auf die Schaltfläche klicken (des Pluszeichens **+**), den Kreditkartentyp und auswählen. Geben Sie anschließend die Kartennummer anzeigen oder Nachverfolgen von Daten, die dem POS, zusammen mit dem Ablaufmonat und Jahr für die Karte gesendet werden sollen, die Sie definieren. Der Wert, den Sie im Feld auswählen ** Kreditkartentyp **, Feld ist derzeit eine Beschriftung, die einer Karte zugeordnet werden kann. Diese Bezeichnung wird es einfacher, Karten zu identifizieren, wenn dies im Zusatzsimulator Karte durch ein Lesegerät gezogen werden. Karten können auswählen, die im Zusatzsimulator konfiguriert wurden, indem die Schaltfläche mit dem Pfeil nach links (****)&lt;und mit dem Pfeil nach rechts (****)&gt;zu dem Bild der Karte ein. Sie können bearbeitet und Karten, indem Sie ** Bearbeiten ** ** und Löschung ** Schaltflächen neben der Schaltfläche verwenden des Pluszeichens **+(+).

### <a name="pin-pad"></a>PIN-Feld

Sie können den PIN-Auflagensimulator konfigurieren, um eine OPOS-PIN-Auflage zu simulieren. Wenn eine Buchung (EFT)- für elektronische Überweisungen am Point-of-Sale ausgeführt und PIN-Eintrag erforderlich ist, die Hardwarestationsanrufe das PIN-Gerät, um zu PIN-Eintrag erforderlich. Um zu umgehen, benötigt das PIN-Feld im Zusatzsimulator Unterstützung des EFT- konnektors.

### <a name="printer"></a>Drucker

Der Drucker des virtuellen Peripheriegeräts werden derzeit Zugänge an, wenn diese vom POS gedruckt werden. Wenn ein Druckvorgang mehrere Zugänge erzeugt, können Sie die Belege zurücksetzen.

#### <a name="configure-receipt-printing"></a>Konfigurieren Sie Bondruck

1.  Wechseln ** Einzelhandel und Handel ** &gt; ** richtet der Kanal ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwareprofile **.
2.  Wählen Sie das Hardwareprofil aus, das Sie für virtuelle Peripheriegeräte erstellt haben.
3.  Wählen Sie im Inforegister auf Drucker ** ** ** Bearbeiten **.
4.  ** Im Feld Bonprofilkennung ** Feld ein Bonprofil aus.
5.  Click **Save**.

### <a name="scale"></a>Skalieren

Wenn ein Skalaprodukt der POS-Buchung hinzugefügt wird und eine Waage konfiguriert wird, ruft das POS das Gewicht von der Waage ab. Für der virtuelle und körperlichen Waage, sollte das Produkt oder Gewicht angegeben werden, bevor das Produkt der Buchung hinzugefügt wird. Bevor Sie das Skalaprodukt der Buchung hinzufügen, wechseln zur Sie im Zusatzsimulator, und verwenden Sie das Pluszeichen (**+**+und Schaltflächen des Minuszeichens ** ** (-), zum Gewicht anzupassen, das den Maßstab fertig melden soll. Sie können den Sollgewicht direkt im Feld Aktueller ** Wert ** Feld auch eine eingeben. Sie können die Gewichtseinheiten auf die Waage regulieren, indem Sie das Pluszeichen ** ** verwenden (+), ** Bearbeiten ** ** und Löschung ** Schaltflächen. Auf diese Weise können Einheiten auf Grundlage die Produkte geliefert werden, die oder Auswählen des Gebietsschemas gewogen werden, in dem den Maßstab verwendet wird.

#### <a name="configure-a-scale-product"></a>Konfigurieren eines Skalaprodukt

1.  Wechseln ** Einzelhandel und ** ** Handel ** &gt; ** Produkte und Kategorien ** &gt; ** freigegebene Produkte nach Kategorie **.
2.  Öffnen Sie den Produktdatensatz.
3.  Wählen Sie das Produkt aus, der Waage.
4.  Wählen Sie im Inforegister ** Einzelhandel ** wählen Sie die Option aus Skalaprodukt ** ** ** no ** auf fest ** Ja **.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronisieren Sie Änderungen an der Kanaldatenbank

1.  Wechseln ** Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
2.  Wählen Sie den Verteilungszeitplan ** ** 1040 aus.
3.  ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.

Nachdem die Daten synchronisiert sind, wenn ein Skalaprodukt der POS-Buchung hinzugefügt wird, überprüft das POS den Maßstab für das Gewicht.

### <a name="signature-capture"></a>Signaturerfassung

Das Gerät für elektronische Unterschriften virtuelle fordert den Benutzer auf, eine Unterschrift auf der Signatur virtuellen bereitzustellen aufzeichnen Auflage, wenn das Zahlungsmittel, das verwendet wird, eine Signatur erfordert. Der Benutzer kann die Signatur akzeptieren, um diese am Point-of-Sale angezeigt. Der Kassierer kann dann akzeptieren die Signatur. Die Unterschrift wird dann zusammen mit dem Zahlungsmittel wird gespeichert und an das zuständige Back-Office-Team sowie weitere Buchungsdaten synchronisiert.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Richten Sie ein Zahlungsmittel, um eine Unterschrift festzulegen

1.  Wechseln ** Einzelhandel und Handel ** &gt; ** Kanäle ** &gt; ** Einzelhandelsgeschäfte ** &gt; ** alle Einzelhandelsgeschäfte **.
2.  Wählen Sie das aus auf Shop Lagermanagement.
3.  Klicken Sie auf **Bearbeiten**.
4.  ** ** Auf Einstellungen und dann, ** ** Einstellungen im Abschnitt, auf ** Zahlungsmethoden **.
5.  Klicken Sie auf **Bearbeiten**.
6.  Wählen Sie die Zahlungsmethode aus, die eine Signatur erfordern.
7.  ** ** Allgemein im Abschnitt unter ** Signatur zeichnen ** auf, legen Sie die verwenden ** Gerät für elektronische Unterschriften Sie ** Option fest ** Ja **.
8.  Wählen Sie im ** Signatur zeichnen Mindestbetrag auf ** Feld geben Sie den Mindestbetrag ein, der Signatur auslösen soll aufzeichnen.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronisieren Sie Änderungen an der Kanaldatenbank

1.  Wechseln ** Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
2.  Wählen Sie den Verteilungszeitplan ** ** 1070 aus.
3.  ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.

Nachdem die Daten synchronisiert sind, wenn ein Zahlungsmittel, die erforderlich, um eine Unterschrift verwendet wird und der Betrag den Unterzeichnungsschwellenwert gilt, die POS-Verlangungen eine Unterschrift auf dem virtuellen. Gerät für elektronische Unterschriften

## <a name="additional-configuration"></a>Zusätzliche Konfiguration
Sie können die Zusatzkonfigurationsdatei zur Adresse des simulators passender bearbeiten die Szenarien, den Sie testen. Sie können die Suche bei Konfigurationsdatei C: Programme \\(x86)\\Microsoft Dynamics 365\\70 VirtualPeripherals\\\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Die freizugebenden wird die Einheit, der für das Testen auf die Waage, den Kartentypen, der für das Testen verfügbar sind und den Strichcodetypen verfügbar sind. Beispielsweise indem Sie die Textwerte in Konfigurationsdatei ändern, können Sie einen neuen Kartentyp eine Maßeinheit oder hinzufügen, die zur Bearbeitungszeit ausgewählt werden können. Die neue Werte angezeigt werden, nachdem der Zeit-App Neustart.

## <a name="troubleshooting"></a>Problembehandlung
Aktivitäten für den Zusatzsimulator werden innerhalb des Zusatzsimulators protokolliert. Sie können das Protokoll C zu suchen: Programme \\(x86)\\Microsoft Dynamics 365\\70 VirtualPeripherals\\\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Die Zusatzdes simulators Berichtsabgänge auch an das Windows-Ereignisprotokoll, an dem Sie ** Anwendung und an Diensten zugreifen können protokolliert ** ** Microsoft &gt; DynamicsAX &gt; ** ** **. Wenn Änderungen, die Sie dem Hardwareprofil oder in andere Bereiche vorgenommenen, nicht offensichtlich sind, wenn Sie MPOS oder den Zusatzsimulator verwenden, sollten Sie die Verteilungssteuerprogrammeinzelvorgänge, die Sie verwenden, um die Daten anzuzeigen Kanaldatenbank zu synchronisieren. Wenn die Änderungen synchronisiert wurden, aber noch nicht am POS offensichtlich sind, starten Sie den POS-Kunden neu. Änderungen an Geldladen konfigurierten sind nicht gültig, sofern keine neue Schicht erstellt wurde. Wenn Sie Änderungen an den Geldladen vornehmen, prüfen Sie, ob Sie immer die vorhandene Schicht schließen, um die neue Geldladeneinstellung zu testen. Manchmal wenn der Fahrer des Herstellers nach Objekten der gemeinsamen Regelung von den Monroe-Beratungsdiensten eingerichtet wird, kann die Fahrer die Objekte der gemeinsamen Regelung veranlassen einwandfrei, die Arbeit einzustellen. In diesem Fall sollten Sie die abweichenden Objekte der gemeinsamen Regelung erneut installieren.

<a name="see-also"></a>Siehe auch
--------

Kleinperipheriegerätenüberblick [] (retail-peripherals-overview.md )


