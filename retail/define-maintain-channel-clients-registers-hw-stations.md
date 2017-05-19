---
title: Definieren und Verwalten von Kanal-Clients, Kassen und Hardwarestationen
description: "Dieses Thema erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: db8b059309ecf4da9728394fc3acb091d60baf4d
ms.contentlocale: de-de
ms.lasthandoff: 04/26/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definieren und Verwalten von Kanal-Clients, Kassen und Hardwarestationen

[!include[banner](includes/banner.md)]


Dieses Thema erläutert, wie Sie Peripheriegeräte mit Ihrer Retail POS verbinden.

**Hinweis:** Spezifische Installationshinweise finden Sie unter [Retail-Hardwarestation-Konfiguration und -Installation](retail-hardware-station-configuration-installation.md) und [Retail Modern POS Self-Service-Download/-Installation und Geräteaktivierung von Modern POS und Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Schlüsselkomponenten
Eine Reihe von Komponenten werden zum Definieren der Beziehung zwischen einem Shop, den Verkaufsstellen (POS/Point-of-Sale)-Registern oder -Kanälen innerhalb des Shops und der Einzelhandelsperipheriegeräte, die diese Register oder Kanäle verwenden, um Transaktionen zu verarbeiten, genutzt. Dieser Abschnitt beschreibt jede Komponente und erklärt, wie sie in einer Bereitstellung für Einzelhandelsgeschäfte verwendet werden soll.

### <a name="pos-registers"></a>POS-Register

Navigieren: Klicken Sie auf **Einzelhandel und Handel**&gt; **Kanaleinstellungen**&gt;**POS-Einstellungen**&gt;**Register**. Das POS-Register ist eine Entität, die verwendet wird, um die Merkmale einer bestimmten Instanz des POS zu definieren. Diese umfassen das Hardwareprofil bzw. die Einstellung für Einzelhandelsperipheriegeräte, die für die Register verwendet werden, den Shop, dem die Register zugeordnet ist, und die Sichterfahrung für den Benutzer, der sich an der Register anmeldet.

### <a name="devices"></a>Geräte

Navigieren: Klicken Sie auf **Einzelhandel und Handel**&gt; **Kanaleinstellungen**&gt; **POS-Einstellungen** &gt; **Geräte**. Ein Gerät ist eine Entität, die eine physische Instanz eines Gerätes darstellt, das dem POS-Register zugeordnet ist. Wenn ein Gerät eingerichtet wird, wird es einem POS-Register zugeordnet. Die Geräteentität verfolgt Informationen darüber, ob ein POS-Register aktiviert ist, welcher Client verwendet wird und das Anwendungspaket, das für ein bestimmtes Gerät bereitgestellt wurde. Es werden zwei Typen von Geräten unterschieden: **Retail Modern POS** (MPOS) oder **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS ist eine POS-Clientanwendung, die in Windows 8.1 oder einem höheren PC-Betriebssystem installiert ist. Wenn die **Retail Modern POS**-Anwendung einem Gerät zugeordnet ist, kann das Downloadpaket für ein bestimmtes Gerät spezifiziert werden. Das Downloadpaket kann angepasst werden, um unterschiedliche Versionen des Installationspakets einzubeziehen. Die Möglichkeit, verschiedene Pakete bereitzustellen, bietet Flexibilität in Fällen, in denen unterschiedliche POS-Register unterschiedliche Integrationen benötigen. MPOS wird mit einer integrierten Hardwarestation bereitgestellt.

#### <a name="cloud-pos"></a>Cloud POS

Cloud POS ist ein browserbasiertes POS. Da er im Browser ausgeführt wird, benötigt Cloud POS kein Windows 8.1 oder eine höheres PC-Betriebssystem. Wenn die **Retail Cloud POS**-Anwendung einem bestimmten Gerät im Back-Office zugeordnet ist, kann dieses Gerät über den Browser verwendet werden, ohne dass ein Paket heruntergeladen oder installiert werden muss. Cloud POS erfordert eine Hardwarestation, um mehr Hardware als einen Barcodescanner per Tastaturweiche zu verwenden.

### <a name="hardware-profile"></a>Hardwareprofil

Navigation: Klicken Sie auf **Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile** &gt; **Hardwareprofile**. Ein Hardwareprofil identifiziert die Hardware, die mit einem POS-Register oder einer Hardwarestation verbunden ist. Das Hardwareprofil wird auch verwendet, um Zahlungsverarbeitungsparameter anzugeben, die während der Kommunikation mit dem Software Development Kit (SDK) für Zahlungen verwendet werden sollen. (Die Zahlungs-SDK wird als Teil der Hardwarestation bereitgestellt.)

### <a name="hardware-station"></a>Hardwarestation

Navigieren: Klicken Sie auf **Einzelhandel und Handel**&gt; **Kanäle** &gt; **Einzelhandelsgeschäfte** &gt; **Alle Einzelhandelsgeschäfte**. Wählen Sie einen Shop aus, und klicken Sie anschließend auf die Registerkarte **Hardwarestationen**. Eine Hardwarestation ist eine Instanz der Geschäftslogik, die POS-Peripheriegeräte steuert. Eine Hardwarestation wird automatisch mit MPOS zusammen installiert. Eine Hardwarestation kann als eigenständige Komponente installiert werden, auf die dann mit MPO oder Cloud POS über einen Webdienst zugegriffen werden kann. Die Hardwarestation muss auf der Kanalebene definiert werden.

### <a name="hardware-station-profile"></a>Hardwarestation-Profil

Navigation: Klicken Sie auf H**Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile** &gt; **Hardwarestationprofile**. Während die Hardwarestation selbst auf der Kanalebene unter Einbeziehung Instanzen-spezifischer Informationen, wie z. B. der URL für die Hardwarestation, festgelegt wird, beinhaltet das Hardwarestationsprofil Informationen, die statisch sind oder für mehrere Hardware-Stationen freigegeben sind. Statische Informationen umfassen den Port, der verwendet werden soll, das Hardwarestation-Paket und das Hardwareprofil. Die statischen Informationen enthalten auch eine Beschreibung der Art der bereitgestellten Hardwarestation, wie z.B. **Auschecken**oder **Retouren**, je nach Hardware, die für jede spezifische Hardwarestation erforderlich ist.

## <a name="scenarios"></a>Szenarien
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS mit verbundenen Peripheriegeräten

[![Herkömmlich, feste Verkaufsstelle](./media/traditional-300x279.png)](./media/traditional.png) 

Um MPOS mit POS-Peripheriegeräte in einem herkömmlichen, festen POS-Szenario zu verbinden, navigieren Sie zuerst zum Register selbst und weisen Sie dann ein Hardwareprofil zu. Sie finden die POS-Register unter **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **Register**. Nachdem Sie das Hardwareprofil zugewiesen haben, synchronisieren Sie die Änderungen mit der Kanaldatenbank unter Verwendung des Vertriebsplans "Register". Sie finden die Vertriebspläne unter **Einzelhandel und Handel** &gt; **IT für den Einzelhandel** &gt; **Vertriebsplan**. Nun richten Sie eine "lokale" Hardwarestation auf dem Kanal ein. Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanäle** &gt; **Einzelhandelsgeschäfte** &gt; **Alle Einzelhandelsgeschäfte** und wählen einen Shop aus. Klicken Sie dann im Inforegister **Hardwarestationen** auf **Hinzufügen**, um eine Hardwarestation hinzuzufügen. Geben Sie eine Beschreibung ein, **Localhost** als Hostname und synchronisieren Sie dann die Änderungen mit dem Kanal, indem Sie den Vertriebsplan "Kanalkonfiguration"verwenden. Sie finden die Vertriebspläne unter **Einzelhandel und Handel** &gt; **IT für den Einzelhandel** &gt; **Vertriebsplan**. Abschließend verwenden Sie den Vorgang **Hardwarestation auswählen** in MPOS und wählen die Hardwarestation **Localhost**. Legen Sie die Hardwarestation auf **Aktiv** fest. Das Hardwareprofil, das in diesem Szenario verwendet wird, sollte aus dem POS-Register selbst stammen. Für dieses Szenario ist kein Hardwarestationsprofil notwendig. **Hinweis:** Für einige Hardwareprofiländerungen, wie z. B. Änderungen an Geldladen, ist es erforderlich, dass eine neue Schicht geöffnet wird, nachdem die Änderungen mit dem Kanal synchronisiert wurden. **Hinweis:** Cloud POS muss die eigenständige Hardwarestation verwenden, um mit Einzelhandels-Peripheriegeräten zu kommunizieren.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS oder Cloud POS mit eigenständiger Hardwarestation
[![Freigegebene Peripheriegeräte](./media/shared-300x254.png)](./media/shared.png)

In diesem Szenario ist eine eigenständige Hardwarestation für MPO- und Cloud POS-Kunden freigegeben. Dieses Szenario erfordert die Erstellung eines Hardwarestationsprofils zum Spezifizieren des Download-Pakets, des Ports und des Hardwareprofils, das die Hardwarestation verwendet. Sie können die Hardwarestationsprofile unter **Einzelhandel und Handel**&gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile** &gt; **Hardwarestationsprofile** finden. Nachdem Sie das Hardwarestationsprofil erstellt haben, navigieren Sie zum entsprechenden Einzelhandelskanal (**Einzelhandel und Handel** &gt; **Kanäle** &gt; **Einzelhandelsgeschäfte** &gt; **Alle Einzelhandelsgeschäfte**), und fügen Sie eine neue Hardwarestation hinzu. Weisen Sie diese neue Hardwarestation dem Hardwarestationsprofil zu, das zuvor erstellt wurde. Als Nächstes erstellen Sie eine Beschreibung, die dem Kassierer hilft, die Hardwarestation zu identifizieren. Geben Sie im Feld **Hostname** die URL des Host-Computers im folgenden Format ein: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Ersetzen Sie **&lt;MachineName:Port&gt;** mit dem tatsächlichen Maschinennamen der Hardwarestation und der Anschluss, der im Hardwarestationsprofil angegeben ist). Eine eigenständige sollten Sie die Hardwarestation (EFT)- Terminal Kennung für elektronische Überweisungen auch angeben Dieser Wert gibt den EFT-Terminal an, der mit der Hardwarestation verbunden ist, wenn der Zahlung-Connector mit dem Zahlungsanbieter kommuniziert. Anschließend wechseln Sie vom tatsächlichen Hardwarestationsgerät zum Kanal und wählen die Hardwarestation aus. Klicken Sie dann auf **Herunterladen** und installieren Sie die Hardwarestation. Als nächstes führen Sie aus MPOS oder Cloud POS den Vorgang **Hardwarestation auswählen** aus, um die zuvor installierte Hardwarestation auszuwählen. Wählen Sie **Koppeln**, um eine sichere Beziehung zwischen dem POS und der Hardware einzurichten. Dieser Schritt muss einmal für jede Kombination von einem POS und einer Hardwarestation abgeschlossen werden. Nachdem die Hardwarestation gekoppelt wurde, wird derselbe Vorgang verwendet, um die Hardwarestation zu aktivieren. Für dieses Szenario sollte das Hardwareprofil dem Hardwarestationsprofil zugewiesen werden und nicht dem  Register selbst. Wenn aus einem bestimmten Grund eine Hardwarestation kein direkt zugewiesenes Hardwareprofil enthält, wird das Hardwareprofil, das dem Register zugewiesen, verwendet

## <a name="client-maintenance"></a>Client-Wartung
### <a name="registers"></a>Register

POS-Register werden hauptsächlich über die Register selbst und die den Registern zugewiesenen Profile verwaltet. Attribute, die für ein einzelnes Register spezifisch sind, werden auf der Register-Ebene verwaltet. Zu diesen Attributen gehören der Shop, der das Register verwendet, die Registernummer, die Beschreibung und die Terminalkennung für Überweisung (elektronisch), die für das Register spezifisch ist.

### <a name="pos-profiles"></a>POS-Profile

Sie finden die POS-Profile unter **Einzelhandel und Handel**&gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile**. Es empfiehlt sich, viele Aspekte eines Registers über Profile zu verwalten, da die Profile für mehrere Register freigegeben werden können. Profile können entweder einem einzelnen Register oder einem Einzelhandelsgeschäft, sollte ein Profil auf shopweiter Basis gültig sein, zugeordnet werden. Die folgenden Abschnitte beschreiben die POS-Profile und ihre Verwendung.

#### <a name="offline-profile"></a>Offlineprofil

Das Offline-Profil wird auf der Shopebene festgelegt. Es wird verwendet, um die Einstellungen zum Hochladen für Vorgänge festzulegen, die auf einem POS-Register ausgeführt werden, wenn dieses Register nicht mit einer Kanaldatenbank verbunden ist.

#### <a name="functionality-profile"></a>Funktionsprofil

Das Funktionsprofil wird auf der Shopebene festgelegt. Wird verwendet, um Shop übergreifende Einstellungen zu Aufgaben anzugeben, die am Point-of-Sale durchgeführt werden können. Folgende Funktionen werden im Funktionsprofil verwaltet. Diese Funktionen werden im Inforegister angeordnet.

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
    -   Alle Aspekte wie Infocodes werden am POS verwaltet. Details finden Sie unter [Infocodes ](info-codes-retail.md)
-   **Bonnummerierung**-Inforegister:
    -   Spezifizieren Sie Bonnummerierungsmasken, die Segmente der Shopnummer, Terminalnummer, Konstanten enthalten können, und ob Verkäufe, Retouren, Aufträge und Anmerkungen in separaten Reihenfolgen oder alle in derselben Reihenfolge gedruckt werden.

#### <a name="receipt-profiles"></a>Bonprofile

Bonprofile werden über das Hardwareprofil den Druckern direkt zugewiesen. Sie werden verwendet, um Bontypen festzulegen, die auf einem bestimmten Drucker gedruckt werden. Die Profile enthalten Einstellungen für die Bonformate und Einstellungen, die festlegen, ob ein Bon immer gedruckt wird, oder ob ein Kassierer entscheidet, ob der Bon gedruckt werden muss. Verschiedene Drucker können auch unterschiedliche Bonprofile verwenden. Drucker 1 ist beispielsweise ein standardmäßiger Thermobondrucker und hat daher kleinere Bonformate. Drucker 2 ist ein Vollformat-Bondrucker, der verwendet wird, um ausschließlich Bons für Debitorenaufträge zu drucken, die mehr Platz benötigen.

#### <a name="hardware-profiles"></a>Hardwareprofile

Hardwareprofile werden als Komponente der Clientinstallation weiter oben in diesem Artikel erläutert. Hardwareprofile sind direkt dem POS-Register oder einem Hardwarestationsprofil zugewiesen. Sie werden verwendet, um die Art der Geräte, die von einem bestimmen POS-Register oder einer Hardwarestation verwendet werden, festzulegen. Hardwareprofile dienen außerdem dazu, EFT-Einstellung festzulegen, die zum Kommunizieren mit dem Zahlungs-SDK verwendet werden.

#### <a name="visual-profiles"></a>Visuelle Profile

Visuelle Profile werden auf der Registerebene zugewiesen. Sie werden verwendet, um das Thema eines bestimmten Registers zu spezifieren. Die Profile umfassen Einstellungen für den verwendeten Anwendungstyp (MPOS oder Cloud POS), die Akzentfarbe und -design, das Schriftartenschema, den Anmeldehintergrund und den POS-Hintergrund.

### <a name="custom-fields"></a>Benutzerdefinierte Felder

Darüber hinaus können Sie benutzerdefinierte Felder erstellen, um Felder hinzuzufügen, die nicht standardmäßig am POS zur Verfügung stehen. Weitere Informationen dazu, wie eine benutzerdefinierte Felder verwendet werden finden Sie unter [Arbeiten mit benutzerdefinierten Blog-Einträgen](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

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

Alle Änderungen an einem POS-Client, ausgenommen der Änderungen am Geräteaktivierungsstatus, müssen mit der Kanaldatenbank synchronisiert werden, um wirksam zu werden. Um Änderungen an der Kanaldatenbank zu synchronisieren, navigieren Sie zu **Einzelhandel und Handel** &gt; **IT für den Einzelhandel** &gt; **Vertriebsplan**, und führen Sie den erforderlichen Vertriebsplan aus. Für Änderungen am Client sollten Sie die Vertriebszeitpläne "Register" und "Kanalkonfiguration" ausführen.




