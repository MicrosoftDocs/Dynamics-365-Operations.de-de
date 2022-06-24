---
title: Peripheriegeräte mit der Verkaufsstelle (POS) verbinden
description: Dieser Artikel erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897107"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Peripheriegeräte mit der Verkaufsstelle (POS) verbinden

[!include [banner](includes/banner.md)]

Dieser Artikel erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden.

> [!NOTE]
> Spezifische Installationsanweisungen finden Sie unter [Konfigurieren und richten Sie Retail hardware station](retail-hardware-station-configuration-installation.md) und unter [Konfigurieren, Installieren und Aktivieren von Modern POS (MPOS)](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Schlüsselkomponenten

Eine Reihe von Komponenten werden zum Definieren der Beziehung zwischen einem Shop, den Verkaufsstellen (POS/Point-of-Sale)-Registern oder -Kanälen innerhalb des Shops und der Peripheriegeräte, die diese Register oder Kanäle verwenden, um Transaktionen zu verarbeiten, genutzt. Dieser Abschnitt beschreibt jede Komponente und erklärt, wie sie in einer Bereitstellung für Geschäfte verwendet werden soll.

### <a name="pos-registers"></a>POS-Register

Navigieren: Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Register**.

Das POS-Register ist eine Entität, die verwendet wird, um die Merkmale einer bestimmten Instanz des POS zu definieren. Zu diesen Merkmalen gehören das Hardwareprofil oder die Einrichtung der Peripheriegeräte, die an der Kasse verwendet werden, die Filiale, der die Kasse zugeordnet ist, und die visuelle Erfahrung für den Benutzer, der sich an der Kasse anmeldet.

### <a name="devices"></a>Geräte

Navigieren: Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Geräte**.

Ein Gerät ist eine Entität, die eine physische Instanz eines Gerätes darstellt, das dem POS-Register zugeordnet ist. Wenn ein Gerät eingerichtet wird, wird es einem POS-Register zugeordnet. Die Geräteentität verfolgt Informationen darüber, ob ein POS-Register aktiviert ist, welcher Client verwendet wird und das Anwendungspaket, das für ein bestimmtes Gerät bereitgestellt wurde. Es werden zwei Typen von Geräten unterschieden: **Retail Modern POS** (MPOS) oder **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS ist eine POS-Clientanwendung, die in Windows 8.1 oder einem höheren PC-Betriebssystem installiert ist. Wenn die **Retail Modern POS**-Anwendung einem Gerät zugeordnet ist, kann das Downloadpaket für ein bestimmtes Gerät spezifiziert werden. Das Downloadpaket kann angepasst werden, um unterschiedliche Versionen des Installationspakets einzubeziehen. Die Möglichkeit, verschiedene Pakete bereitzustellen, bietet Flexibilität in Fällen, in denen unterschiedliche POS-Register unterschiedliche Integrationen benötigen. MPOS wird mit einer integrierten Hardwarestation bereitgestellt.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS ist ein browserbasiertes POS. Da er im Browser ausgeführt wird, benötigt Cloud POS kein Windows 8.1 oder eine höheres PC-Betriebssystem. Wenn die **Retail Cloud POS**-Anwendung einem bestimmten Gerät in der Zentralverwaltung zugeordnet ist, kann dieses Gerät über den Browser verwendet werden, ohne dass ein Paket heruntergeladen oder installiert werden muss. Cloud POS erfordert eine Hardwarestation, um mehr Hardware als einen Barcodescanner per Tastaturweiche zu verwenden.

### <a name="hardware-profile"></a>Hardwareprofil

Zur Navigation: Gehen Sie zu **Einzelhandel und Commerce \> Kanal Einrichtung \> POS Einrichtung \> POS Profile \> Hardware Profile**.

Ein Hardwareprofil identifiziert die Hardware, die über eine integrierte oder gemeinsam genutzte Hardwarestation mit einer POS-Kasse verbunden ist. Das Hardwareprofil wird auch verwendet, um Zahlungsverarbeitungsparameter anzugeben, die während der Kommunikation mit dem Software Development Kit (SDK) für Zahlungen verwendet werden sollen. Das Zahlungs-SDK wird als Teil der Hardware-Station bereitgestellt.

### <a name="hardware-station"></a>Hardwarestation

Navigation: Gehen Sie zu **Einzelhandel und Commerce \> Kanäle \> Stores \> Alle Stores**, wählen Sie einen Store und dann das Inforegister **Hardware-Stationen** aus.

Eine Hardwarestation ist eine Instanz der Geschäftslogik, die POS-Peripheriegeräte steuert. Eine Hardwarestation wird automatisch mit MPOS zusammen installiert. Eine Hardwarestation kann als eigenständige Komponente installiert werden, auf die dann mit MPO oder Cloud POS über einen Webdienst zugegriffen werden kann. Die Hardwarestation muss auf der Kanalebene definiert werden.

## <a name="scenarios"></a>Szenarien

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS mit verbundenen Peripheriegeräten

[![Herkömmlich, feste Verkaufsstelle.](./media/traditional-300x279.png)](./media/traditional.png)

Um MPOS mit POS-Peripheriegeräte in einem herkömmlichen, festen POS-Szenario zu verbinden, navigieren Sie zuerst zum Register selbst und weisen Sie dann ein Hardwareprofil zu. Sie finden die POS-Register unter **Retail nd Commerce** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Register**. 

Nachdem Sie das Hardwareprofil zugewiesen haben, synchronisieren Sie die Änderungen mit der Kanaldatenbank unter Verwendung des Vertriebsplans **Register**. Sie finden die Vertriebspläne unter **Einzelhandel und Handel** &gt; **Retail and Commerce IT** &gt; **Vertriebsplan**. 

Als nächstes legen Sie eine dedizierte Hardwarestation im Channel fest. Gehen Sie zu **Einzelhandel und Commerce \> Kanäle \> Stores \> Alle Stores**, und wählen Sie einen Store aus. 

Wählen Sie dann auf der Inforegisterkarte **Hardware-Stationen** die Option **Hinzufügen**, um eine Hardware-Station hinzuzufügen. Wählen Sie **Dediziert** als Hardware-Stationstyp und geben Sie eine Beschreibung ein. Das Feld **Hardwareprofil** kann leer gelassen werden, da das Hardwareprofil, das in diesem Szenario verwendet wird, von der Registrierkasse selbst stammt. Synchronisieren Sie dann die Änderungen mit dem Channel, indem Sie den **Channel-Konfiguration** Verteilungsplan verwenden. Die Verteilungspläne finden Sie unter **Retail und Commerce \> Retail und Commerce IT \> Verteilungsplan**. 

Verwenden Sie schließlich in MPOS den Vorgang **Hardwarestation auswählen**, um die Hardwarestation auszuwählen, die dem Wert entspricht, den Sie zuvor für die Beschreibung eingegeben haben, und legen Sie die Hardwarestation auf **Aktiv** fest. 

> [!NOTE]
> - Für einige Hardwareprofiländerungen, wie z. B. Änderungen an Geldladen, ist es erforderlich, dass eine neue Schicht geöffnet wird, nachdem die Änderungen mit dem Kanal synchronisiert wurden.
> - Cloud POS muss die eigenständige Hardwarestation verwenden, um mit Peripheriegeräten zu kommunizieren.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS oder Cloud POS mit eigenständiger Hardwarestation

[![Freigegebene Peripheriegeräte.](./media/shared-300x254.png)](./media/shared.png)

In diesem Szenario wird eine eigenständige Hardwarestation von MPOS und Cloud POS Clients gemeinsam genutzt. Dieses Szenario erfordert, dass Sie eine gemeinsame Hardwarestation erstellen und das Download-Paket, den Port und das Hardwareprofil angeben, das die Hardwarestation verwendet. Sie definieren eine neue Hardwarestation, indem Sie **das Inforegister Hardwarestationen** im jeweiligen Channel (**Einzelhandel und Commerce \> Channels \> Stores \> Alle Stores**) auswählen und eine neue Hardwarestation vom Typ **Gemeinsam** hinzufügen. 

Als Nächstes erstellen Sie eine Beschreibung, die dem Kassierer hilft, die Hardwarestation zu identifizieren. Geben Sie im Feld **Hostname** die URL des Host-Computers im folgenden Format ein: `https://<MachineName:Port>/HardwareStation`. (Ersetzen Sie **&lt;computername:port&gt;** durch den tatsächlichen Computernamen der Hardwarestation.) Bei einer eigenständigen Hardwarestation sollten Sie auch die Terminal-ID für den elektronischen Zahlungsverkehr (EFT) angeben. Dieser Wert gibt den EFT-Terminal an, der mit der Hardwarestation verbunden ist, wenn der Zahlung-Connector mit dem Zahlungsanbieter kommuniziert. 

Gehen Sie als Nächstes von dem Rechner, auf dem die Hardwarestation installiert werden soll, zum Kanal in der Zentrale und wählen Sie die Hardwarestation aus. Wählen Sie dann **Herunterladen**, um das Installationsprogramm der Hardware-Station herunterzuladen und die Hardware-Station zu installieren. Weitere Informationen über die Installation der Hardware-Station finden Sie unter [Hardware-Station für den Einzelhandel konfigurieren und installieren](retail-hardware-station-configuration-installation.md). 

Als nächstes führen Sie aus MPOS oder Cloud POS den Vorgang **Hardwarestation auswählen** aus, um die zuvor installierte Hardwarestation auszuwählen. Wählen Sie **Koppeln**, um eine sichere Beziehung zwischen dem POS und der Hardware einzurichten. Dieser Schritt muss einmal für jede Kombination von einem POS und einer Hardwarestation abgeschlossen werden. 

Nachdem die Hardwarestation gekoppelt wurde, wird derselbe Vorgang verwendet, um die Hardwarestation zu aktivieren. Bei diesem Szenario sollte das Hardwareprofil der gemeinsam genutzten Hardwarestation zugewiesen werden und nicht dem Register selbst. Wenn einer Hardwarestation aus irgendeinem Grund kein Hardwareprofil direkt zugewiesen ist, wird das Hardwareprofil verwendet, das der Kasse zugewiesen ist.

## <a name="client-maintenance"></a>Client-Wartung

### <a name="registers"></a>Register

POS-Register werden hauptsächlich über die Register selbst und die den Registern zugewiesenen Profile verwaltet. Attribute, die für ein einzelnes Register spezifisch sind, werden auf der Register-Ebene verwaltet. Zu diesen Attributen gehören der Shop, der das Register verwendet, die Registernummer, die Beschreibung und die Terminalkennung für Überweisung (elektronisch), die für das Register spezifisch ist.

### <a name="pos-profiles"></a>POS-Profile

Sie finden die POS-Profile unter **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile**. Es empfiehlt sich, viele Aspekte eines Registers über Profile zu verwalten, da die Profile für mehrere Register freigegeben werden können. Profile können entweder einem einzelnen Register oder einem Geschäft, sollte ein Profil auf shopweiter Basis gültig sein, zugeordnet werden. Die folgenden Abschnitte beschreiben die POS-Profile und ihre Verwendung.

#### <a name="offline-profile"></a>Offlineprofil

Das Offline-Profil wird auf der Shopebene festgelegt. Es wird verwendet, um die Einstellungen zum Hochladen für Vorgänge festzulegen, die auf einem POS-Register ausgeführt werden, wenn dieses Register nicht mit einer Kanaldatenbank verbunden ist.

#### <a name="functionality-profile"></a>Funktionsprofil

Das Funktionsprofil wird auf der Shopebene festgelegt. Wird verwendet, um Shop übergreifende Einstellungen zu Aufgaben anzugeben, die am Point-of-Sale durchgeführt werden können. Folgende Funktionen werden im Funktionsprofil verwaltet. Diese Funktionen werden im Inforegister angeordnet.

- **Allgemein**-Inforegister:

    - Internationale Organisation für Normung (ISO).
    - Einen Debitor im Offlinemodus erstellen.
    - E-Mail-Bonprofil.
    - Zentrale Mitarbeiteranmeldeauthentifizierung.

- **Funktionen**-Inforegister:

    - Verwaltung der Anmeldung und erweiterten Anmeldung.
    - Finanz- und Währungsbezogene Aspekte des POS, wie das Festlegen von Preisen und ob Dezimalstellen für kleinere Währungseinheiten erforderlich sind.
    - Aktivieren der Zeiterfassung über POS.
    - Wie Produkte und Zahlung im POS und auf Belegen angezeigt werden.
    - Tagesendeverwaltung.
    - Transaktionsaufbewahrungsparameter für die Kanaldatenbank.
    - Wie Kunden im POS gesucht und erstellt werden können.
    - Wie Rabatte berechnet werden.

- **Betrag**-Inforegister:

    - Zulässige maximale und minimale Preise.
    - Anwendung und Berechnung von Rabatten.

- **Infocodes**-Inforegister:

    - Alle Aspekte wie Infocodes werden am POS verwaltet. Weitere Informationen finden Sie unter [Infocodes und Infocodegruppen](info-codes-retail.md).

- **Bonnummerierung**-Inforegister:

    - Geben Sie Masken für die Belegnummerierung an, z.B. Segmente für die Filialnummer, die Terminalnummer, Konstanten und ob Verkäufe, Retouren, Verkaufsaufträge und Angebote in separaten Sequenzen gedruckt werden oder ob sie alle der gleichen Sequenz folgen.

#### <a name="receipt-profiles"></a>Bonprofile

Empfangsprofile werden Druckern innerhalb des Hardwareprofils zugewiesen. Sie werden verwendet, um Bontypen festzulegen, die auf einem bestimmten Drucker gedruckt werden. Die Profile enthalten Einstellungen für die Bonformate und Einstellungen, die festlegen, ob ein Bon immer gedruckt wird, oder ob ein Kassierer entscheidet, ob der Bon gedruckt werden muss. Verschiedene Drucker können auch unterschiedliche Bonprofile verwenden. Drucker 1 ist beispielsweise ein standardmäßiger Thermobondrucker und hat daher kleinere Bonformate. Drucker 2 ist ein Vollformat-Bondrucker, der verwendet wird, um ausschließlich Bons für Debitorenaufträge zu drucken, die mehr Platz benötigen. Weitere Informationen finden Sie unter [Konfigurieren Sie ein Belegprofil](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Hardwareprofile

Hardwareprofile werden als Komponente der Clientinstallation weiter oben in diesem Artikel erläutert. Hardwareprofile werden direkt der Kasse oder einer gemeinsamen Hardwarestation zugewiesen und dienen dazu, die Gerätetypen festzulegen, die eine bestimmte Kasse oder Hardwarestation verwendet. Hardwareprofile dienen außerdem dazu, EFT-Einstellung festzulegen, die zum Kommunizieren mit dem Zahlungs-SDK verwendet werden.

#### <a name="visual-profiles"></a>Visuelle Profile

Visuelle Profile werden verwendet, um das Design für ein bestimmtes Register festzulegen und werden auf Registerebene zugewiesen. Die Profile enthalten Einstellungen für den Typ der verwendeten Anwendung (MPOS oder Cloud POS), die Akzentfarbe und das Design, das Schriftschema, den Hintergrund der Anmeldeseite und den POS-Hintergrund. Weitere Informationen finden Sie unter [Erstellen Sie visuelle Profile für Point of Sale (POS)](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Benutzerdefinierte Felder

Darüber hinaus können Sie benutzerdefinierte Felder erstellen, um Felder hinzuzufügen, die nicht standardmäßig am POS zur Verfügung stehen. Weitere Informationen dazu, wie eine benutzerdefinierte Felder verwendet werden finden Sie unter [Arbeiten mit benutzerdefinierten Blog-Einträgen](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Sprachentext

Sie können Standardzeichenfolgen im POS mit Sprachtexteinträgen überschreiben. Zum Überschreiben einer Zeichenfolge im POS fügen Sie eine neue Sprachtextzeile hinzu. Geben Sie dann eine Kennung, die Standardzeichenfolge, die überschrieben werden soll und den Text, der im POS statt der Standardzeichenfolge angezeigt werden soll, ein.

### <a name="channel-reports-configuration"></a>Konfiguration für Kanalberichte

Berichte, die über den Einzelhandelskanal verfügbar sind, richten Sie auf der Seite **Konfiguration für Kanalberichte** ein. Sie können neue Berichte über die XML-Definition des Berichts erstellen und den Bericht einer bestimmten Berechtigungsgruppe im POS zuweisen.

### <a name="devices"></a>Geräte

Geräte werden weiter oben in diesem Artikel erläutert. Sie werden verwendet, um die Aktivierung eines bestimmten POS-Registers zu spezifieren. Geräte werden auch verwendet, um die Anwendung, die in einem bestimmten Register verwendet wird und das Installationspaket, das zur Installation des MPOS-Clients verwendet werden soll, anzugeben. Dies sind die Geräteaktivierungsstatus:

- **Ausstehend** – Das Gerät kann jetzt aktiviert werden.
- **Aktiviert** – Das Gerät wurde aktiviert.
- **Deaktiviert** – Das Gerät wurde entweder in der Zentralverwaltung oder über den POS deaktiviert.
- **Gesperrt** – das Gerät wurde deaktiviert.

Zusätzliche Informationen zur Aktivierungen beinhalten die Arbeitskraft,die den Aktivierungsstatus für das Gerät geändert hat, einen Zeitstempel der Aktivierung und ob die Gerätekonfiguration überprüft wurde.

### <a name="client-data-synchronization"></a>Client-Datensynchronisierung

Alle Änderungen an einem POS-Client, ausgenommen der Änderungen am Geräteaktivierungsstatus, müssen mit der Kanaldatenbank synchronisiert werden, um wirksam zu werden. Um Änderungen an der Kanaldatenbank zu synchronisieren, navigieren Sie zu **Retail and Commerce** &gt; **IT für Retail and Commerce** &gt; **Vertriebsplan**, und führen Sie den erforderlichen Vertriebsplan aus. Für Änderungen am Client sollten Sie die Vertriebszeitpläne **Register** und **Kanalkonfiguration** ausführen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Retail Hardware Station konfigurieren und installieren](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
