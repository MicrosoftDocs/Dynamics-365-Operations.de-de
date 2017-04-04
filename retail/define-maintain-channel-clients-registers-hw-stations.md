---
title: Definieren und Verwalten von Kanalkunden, Register und Hardwarestationen verwalten
description: "Dieses Wiki erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definieren und Verwalten von Kanalkunden, Register und Hardwarestationen verwalten

Dieses Wiki erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden.

**Hinweis:** Spezifische Installationshinweise finden Sie unter [Retail-Hardwarestation-Konfiguration und -Installation](retail-hardware-station-configuration-installation.md) und [Retail Modern POS Self-Service-Download/-Installation und Geräteaktivierung von Modern POS und Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Schlüsselkomponenten
Eine Reihe von Komponenten werden zum Definieren der Beziehung zwischen einem Shop, den Verkaufsstellen (POS/Point-of-Sale)-Registern oder -Kanälen innerhalb des Shops und der Einzelhandelsperipheriegeräte, die diese Register oder Kanäle verwenden, um Transaktionen zu verarbeiten, genutzt. Dieser Abschnitt beschreibt jede Komponente und erklärt, wie sie in einer Bereitstellung für Einzelhandelsgeschäfte verwendet werden soll.

### <a name="pos-registers"></a>POS-Register

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** Register **. Das POS-Register ist eine Entität, die verwendet wird, um die Merkmale einer bestimmten AOS-Instanz des POS zu definieren. Diese umfassen das Hardwareprofil Merkmale bzw. die Einstellung für Kleinperipheriegeräte, die am Register verwendet werden, den Shop, der die Kasse zugeordnet ist, und die Sichterfahrung für den Benutzer, der bei diesem Register anmeldet.

### <a name="devices"></a>Geräte

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** Geräte **. Ein Gerät ist eine Entität, die eine physische Instanz eines Gerätes darstellt, das dem POS-Register zugeordnet ist. Wenn ein Gerät eingerichtet wird, wird es einem POS-Register zugeordnet. Die Geräteentität verfolgt Informationen darüber, ob ein POS-Register aktiviert ist, welcher Client verwendet wird und das Anwendungspaket, das für ein bestimmtes Gerät bereitgestellt wurde. Es werden zwei Typen von Geräten unterschieden: **Retail Modern POS** (MPOS) oder **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS ist eine POS-Clientanwendung, die in Windows 8.1 oder einem höheren PC-Betriebssystem installiert ist. Wenn die **Retail Modern POS**-Anwendung einem Gerät zugeordnet ist, kann das Downloadpaket für ein bestimmtes Gerät spezifiziert werden. Das Downloadpaket kann angepasst werden, um unterschiedliche Versionen des Installationspakets einzubeziehen. Die Möglichkeit, verschiedene Pakete bereitzustellen, bietet Flexibilität in Fällen, in denen unterschiedliche POS-Register unterschiedliche Integrationen benötigen. MPOS wird mit einer integrierten Hardwarestation bereitgestellt.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS ist ein browserbasiertes POS. Da jedoch in Browser ausgeführt wird, müssen Cloud POS nicht Windows 8,1 oder ein aktuelleres PC-basiertes Betriebssystem. Wenn die **Retail Cloud POS**-Anwendung einem bestimmten Gerät im Back-Office zugeordnet ist, kann dieses Gerät über den Browser verwendet werden, ohne dass ein Paket heruntergeladen oder installiert werden muss. Cloud POS erfordert eine Hardwarestation, um mehr Hardware als einen Barcodescanner per Tastaturweiche zu verwenden.

### <a name="hardware-profile"></a>Hardwareprofil

Navigationspfad: ** Auf Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwareprofile **. Ein Hardwareprofil identifiziert die Hardware, die mit einem POS-Register oder einer Hardwarestation verbunden ist. Das Hardwareprofil wird auch verwendet, um Zahlungsverarbeitungsparameter anzugeben, die während der Kommunikation mit dem Software Development Kit (SDK) für Zahlungen verwendet werden sollen. (Die Zahlungs-SDK wird als Teil der Hardwarestation bereitgestellt.)

### <a name="hardware-station"></a>Hardwarestation

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanäle ** &gt; ** Einzelhandelsgeschäfte ** &gt; ** alle Einzelhandelsgeschäfte **. Wählen Sie einen Shop aus, und klicken Sie anschließend auf die Registerkarte **Hardwarestationen**. Eine Hardwarestation ist eine Instanz der Geschäftslogik, die POS-Peripheriegeräte steuert. Eine Hardwarestation wird automatisch mit MPOS zusammen installiert. Eine Hardwarestation kann als eigenständige Komponente installiert werden, auf die dann mit MPO oder Cloud POS über einen Webdienst zugegriffen werden kann. Die Hardwarestation muss auf der Kanalebene definiert werden.

### <a name="hardware-station-profile"></a>Hardwarestation-Profil

Navigationspfad: ** Auf Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwarestationsprofile **. Während die Hardwarestation selbst auf der Kanalebene unter Einbeziehung Instanzen-spezifischer Informationen, wie z. B. der URL für die Hardwarestation, festgelegt wird, beinhaltet das Hardwarestationsprofil Informationen, die statisch sind oder für mehrere Hardware-Stationen freigegeben sind. Statische Informationen umfassen den Port, der verwendet werden soll, das Hardwarestation-Paket und das Hardwareprofil. Die statischen Informationen enthalten auch eine Beschreibung der Art der bereitgestellten Hardwarestation, wie z.B. **Auschecken **oder **Retouren**, je nach Hardware, die für jede spezifische Hardwarestation erforderlich ist.

## <a name="scenarios"></a>Szenarien
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS mit verbundenen Peripheriegeräten

traditionelle, [] (feste Verkaufsstelle ![. /media/traditional-300x279.png)]". /media/traditional.png) Für die MPOS an POS-Peripheriegeräte traditionellen, in einem festen POS-Szenario werden, navigieren zuerst dem Register selbst und Zuweisen eines Hardwareprofils zu zu. Sie können die und Retail POS-Registers ** Handel ** ** &gt; am richten Kanal suchen ** &gt; ** POS eingerichtet ** &gt; ** Register **. Nachdem Sie das Hardwareprofil zugewiesen haben, synchronisieren Sie die Änderungen mit der Kanaldatenbank unter Verwendung des Vertriebsplans "Register". Sie können die Verteilungszeitpläne ** Einzelhandel und Handel ** ** &gt; am Einzelhandel IT suchen ** &gt; ** Verteilungszeitplan **. Nun richten Sie eine "lokale" Hardwarestation auf dem Kanal ein. ** Sie Einzelhandel und Handel ** &gt; ** Kanäle ** &gt; ** Einzelhandelsgeschäfte ** &gt; ** alle Einzelhandelsgeschäfte ** und wählen Sie den Shop aus. Klicken Sie dann im Inforegister **Hardwarestationen** auf **Hinzufügen**, um eine Hardwarestation hinzuzufügen. Geben Sie eine Beschreibung ein, **Localhost** als Hostname und synchronisieren Sie dann die Änderungen mit dem Kanal, indem Sie den Vertriebsplan "Kanalkonfiguration"verwenden. Sie können die Verteilungszeitpläne ** Einzelhandel und Handel ** ** &gt; am Einzelhandel IT suchen ** &gt; ** Verteilungszeitplan **. Abschließend verwenden Sie den Vorgang **Hardwarestation auswählen** in MPOS und wählen die Hardwarestation **Localhost**. Legen Sie die Hardwarestation auf **Aktiv** fest. Das Hardwareprofil, das in diesem Szenario verwendet wird, sollte aus dem POS-Register selbst stammen. Für dieses Szenario ist kein Hardwarestationsprofil notwendig. **Hinweis:** Für einige Hardwareprofiländerungen, wie z. B. Änderungen an Geldladen, ist es erforderlich, dass eine neue Schicht geöffnet wird, nachdem die Änderungen mit dem Kanal synchronisiert wurden. **Hinweis:** Cloud POS muss die eigenständige Hardwarestation verwenden, um mit Einzelhandels-Peripheriegeräten zu kommunizieren.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS oder Cloud POS mit eigenständiger Hardwarestation

\[id= Beschriftung "\_"align= Anhang 340041 " alignleft" width= " 300 "\]freigegebene Peripheriegeräte [] (![. /media/shared-300x254.png)]". /media/shared.png" Der Peripheriegeräten\[/caption\] in diesem Szenario können, ist eine eigenständige Hardwarestation unter MPOS und Kunden der Cloud POS freigegeben. Dieses Szenario erfordert die Erstellung eines Hardwarestationsprofils zum Spezifizieren des Download-Pakets, des Ports und des Hardwareprofils, das die Hardwarestation verwendet. Sie können das Hardwarestationsprofil ** Einzelhandel und Handel ** ** am richten &gt; Kanal suchen ** ** POS &gt; eingerichtet ** ** POS-Profile &gt; ** ** Hardwarestationsprofile &gt; **. Nachdem Sie das Hardwarestationsprofil erstellt wurde, greifen Sie auf das Einzelhandelskanal ** bestimmte (Einzelhandel und Handel ** ** Kanäle &gt; ** ** Einzelhandelsgeschäfte &gt; ** ** alle &gt; Einzelhandelsgeschäfte **), und fügen Sie eine neue Hardwarestation hinzu. Weisen Sie diese neue Hardwarestation dem Hardwarestationsprofil zu, das zuvor erstellt wurde. Als Nächstes erstellen Sie eine Beschreibung, die dem Kassierer hilft, die Hardwarestation zu identifizieren. Wählen Sie im Hostname ** ** Feld die Hostmaschine URL im folgenden Format ein: ** https://MachineName:Port/HardwareStation**&lt;&gt;. **&lt;"Ersetzen Sie MachineName: ** Port&gt;mit dem tatsächlichen Maschinennamen der Hardwarestation und der Anschluss, der im Hardwarestationsprofil angegeben ist). Eine eigenständige sollten Sie die Hardwarestation (EFT)- Terminal Kennung für elektronische Überweisungen auch angeben Dieser Wert gibt den EFT-Terminal an, der mit der Hardwarestation verbunden ist, wenn der Zahlung-Connector mit dem Zahlungsanbieter kommuniziert. Anschließend wechseln Sie vom tatsächlichen Hardwarestationsgerät zum Kanal und wählen die Hardwarestation aus. Klicken Sie dann auf **Herunterladen** und installieren Sie die Hardwarestation. Als nächstes führen Sie aus MPOS oder Cloud POS den Vorgang **Hardwarestation auswählen** aus, um die zuvor installierte Hardwarestation auszuwählen. Wählen Sie **Koppeln**, um eine sichere Beziehung zwischen dem POS und der Hardware einzurichten. Dieser Schritt muss einmal für jede Kombination von einem POS und einer Hardwarestation abgeschlossen werden. Nachdem die Hardwarestation gekoppelt wurde, wird derselbe Vorgang verwendet, um die Hardwarestation zu aktivieren. Für dieses Szenario sollte das Hardwareprofil dem Hardwarestationsprofil anstatt selbst das Register zugewiesen werden. Wenn aus einem bestimmten Grund einer Hardwarestation kein direkt zugewiesenes Hardwareprofil enthält, wird das Hardwareprofil, das dem Register zugewiesen, verwendet wird

## <a name="client-maintenance"></a>Client-Wartung
### <a name="registers"></a>Register

POS-Register werden hauptsächlich über die Register selbst und die den Registern zugewiesenen Profile verwaltet. Attribute, die für ein einzelnes Register spezifisch sind, werden auf der Register-Ebene verwaltet. Zu diesen Attributen gehören der Shop, der das Register verwendet, die Registernummer, die Beschreibung und die Terminalkennung für Überweisung (elektronisch), die für das Register spezifisch ist.

### <a name="pos-profiles"></a>POS-Profile

Sie können die und POS-Profile ** Einzelhandel Handel ** ** &gt; am richten Kanal suchen ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile **. Es empfiehlt sich, viele Aspekte eines Registers über Profile zu verwalten, da die Profile für mehrere Register freigegeben werden können. Profile können entweder einem einzelnen Register oder einem Einzelhandelsgeschäft, sollte ein Profil auf shopweiter Basis gültig sein, zugeordnet werden. Die folgenden Abschnitte beschreiben die POS-Profile und ihre Verwendung.

#### <a name="offline-profile"></a>Offlineprofil

Das Offline-Profil wird auf der Shopebene festgelegt. Es wird verwendet, um die Einstellungen zum Hochladen für Vorgänge festzulegen, die auf einem POS-Register ausgeführt werden, wenn dieses Register nicht mit einer Kanaldatenbank verbunden ist.

#### <a name="functionality-profile"></a>Funktionsprofil

Das Funktionsprofil wird auf der Shopebene festgelegt. Die Beschriftung besitzt verwendet, um Shop-weiten Einstellungen zu Aufgaben anzugeben, die am Point-of-Sale durchgeführt werden können. Folgende Funktionen werden im Funktionsprofil verwaltet. Diese Funktionen werden im Inforegister angeordnet.

-   **Allgemein**-Inforegister:
    -   Internationale Organisation für Normung (ISO).
    -   Einen Debitor im Offlinemodus erstellen.
    -   E-Mail-Bonprofil.
    -   Zentrale Mitarbeiteranmeldeauthentifizierung.
-   **Funktionen**-Inforegister:
    -   Verwaltung der Anmeldung und erweiterten Anmeldung.
    -   Finanz- und Währungsbezogene Aspekte des POS, wie das Festlegen von Preisen und ob Dezimalstellen für kleinere Währungseinheiten erforderlich sind.
    -   Aktivieren der Zeiterfassung über POS.
    -   Wie Produkte und Zahlung im POS und auf Belegen angezeigt werden.
    -   Tagesendeverwaltung.
    -   Transaktionsaufbewahrungsparameter für die Kanaldatenbank.
    -   Wie Kunden im POS gesucht und erstellt werden können.
    -   Wie Rabatte berechnet werden.
-   **Betrag**-Inforegister:
    -   Zulässige maximale und minimale Preise.
    -   Anwendung und Berechnung von Rabatten.
-   **Infocodes**-Inforegister:
    -   Alle Aspekte von, z Infocodes am POS verwaltet werden. Details finden Sie unter Infocodes information-codes-retail.md []().
-   **Bonnummerierung**-Inforegister:
    -   Spezifizieren Sie Bonnummerierungsmasken, die Segmente der Shopnummer, Terminalnummer, Konstanten enthalten können, und ob Verkäufe, Retouren, Aufträge und Anmerkungen in separaten Reihenfolgen oder alle in derselben Reihenfolge gedruckt werden.

#### <a name="receipt-profiles"></a>Bonprofile

Bonprofile werden über das Hardwareprofil den Druckern direkt zugewiesen. Sie werden verwendet, um Bontypen festzulegen, die auf einem bestimmten Drucker gedruckt werden. Die Profile enthalten Einstellungen für die Bonformate und Einstellungen, die festlegen, ob ein Bon immer gedruckt wird, oder ob ein Kassierer entscheidet, ob der Bon gedruckt werden muss. Verschiedene Drucker können auch unterschiedliche Bonprofile verwenden. Drucker 1 ist beispielsweise ein standardmäßiger Thermobondrucker und hat daher kleinere Bonformate. Drucker 2 ist ein Vollformat-Bondrucker, der verwendet wird, um ausschließlich Bons für Debitorenaufträge zu drucken, die mehr Platz benötigen.

#### <a name="hardware-profiles"></a>Hardwareprofile

Hardwareprofile werden als Komponente der Clientinstallation weiter oben in diesem Artikel erläutert. Hardwareprofile sind direkt dem POS-Register oder einem Hardwarestationsprofil zugewiesen. Sie werden verwendet, um die Art der Geräte, die von einem bestimmen POS-Register oder einer Hardwarestation verwendet werden, festzulegen. Hardwareprofile dienen außerdem dazu, EFT-Einstellung festzulegen, die zum Kommunizieren mit dem Zahlungs-SDK verwendet werden.

#### <a name="visual-profiles"></a>Visuelle Profile

Visuelle Profile werden auf der Registerebene zugewiesen. Sie werden verwendet, um das Thema eines bestimmten Registers zu spezifieren. Die Profile umfassen Einstellungen für den verwendeten Anwendungstyp (MPOS oder Cloud POS), die Akzentfarbe und -design, das Schriftartenschema, den Anmeldehintergrund und den POS-Hintergrund.

### <a name="custom-fields"></a>Benutzerdefinierte Felder

Darüber hinaus können Sie benutzerdefinierte Felder erstellen, um Felder hinzuzufügen, die nicht verfügbar gestellter Standard dem POS sind. Weitere Informationen dazu, wie eine benutzerdefinierte Felder, finden Sie im Feldblogbeitrag die Arbeit mit kundenspezifischem []( https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Sprachentext

Sie können Standardzeichenfolgen im POS mit Sprachtexteinträgen überschreiben. Zum Überschreiben einer Zeichenfolge im POS fügen Sie eine neue Sprachtextzeile hinzu. Geben Sie dann eine Kennung, die Standardzeichenfolge, die überschrieben werden soll und den Text, der im POS statt der Standardzeichenfolge angezeigt werden soll, ein.

### <a name="hardware-station-profiles"></a>Hardwarestation-Profile

Hardwarestationsprofile werden weiter oben in diesem Artikel erläutert. Sie werden zum Zuweisen von nicht-instanzspezifischen Informationen zu Hardwarestationen verwendet.

### <a name="channel-reports-configuration"></a>Konfiguration für Kanalberichte

Berichte, die über den Einzelhandelskanal verfügbar sind, richten Sie auf der Seite **Konfiguration für Retail Channel-Berichte** ein. Sie können neue Berichte über die XML-Definition des Berichts erstellen und den Bericht einer bestimmten Berechtigungsgruppe im POS zuweisen.

### <a name="devices"></a>Geräte

Geräte werden weiter oben in diesem Artikel erläutert. Sie werden verwendet, um die Aktivierung eines bestimmten POS-Registers zu spezifieren. Geräte werden auch verwendet, um die Anwendung, die in einem bestimmten Register verwendet wird und das Installationspaket, das zur Installation des MPOS-Clients verwendet werden soll, anzugeben. Dies sind die Geräteaktivierungsstatus:

-   **Ausstehend** – Das Gerät kann jetzt aktiviert werden.
-   **Aktiviert** – Das Gerät wurde aktiviert.
-   **Deaktiviert** – Das Gerät wurde entweder im Back-Office oder über den POS deaktiviert.
-   **Gesperrt** – das Gerät wurde deaktiviert.

Zusätzliche Informationen zur Aktivierungen beinhalten die Arbeitskraft,die den Aktivierungsstatus für das Gerät geändert hat, einen Zeitstempel der Aktivierung und ob die Gerätekonfiguration überprüft wurde.

### <a name="client-data-synchronization"></a>Client-Datensynchronisierung

Alle Änderungen an einem POS-Client, ausgenommen der Änderungen am Geräteaktivierungsstatus, müssen mit der Kanaldatenbank synchronisiert werden, um wirksam zu werden. Um Änderungen an der Kanaldatenbank zu synchronisieren, navigieren Sie Einzelhandel und ** Handel ** ** &gt; Einzelhandel IT ** ** &gt; Verteilungszeitplan ** und führen Sie die erforderlichen Verteilungszeitplan aus. Für Änderungen am Client sollten Sie die Vertriebszeitpläne "Register" und "Kanalkonfiguration" ausführen.


