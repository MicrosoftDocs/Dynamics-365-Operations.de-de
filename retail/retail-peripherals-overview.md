---
title: "Kleinperipheriegerätenüberblick"
description: "In diesem Thema werden die Konzepte, die den Kleinperipheriegeräten zugeordnet werden. Es werden die verschiedenen Arten Peripheriegeräte an, dass die Verkaufsstelle (POS) und die Komponenten verbunden werden können, die für das Verwalten der Verbindung mit dem POS zuständig sind."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Kleinperipheriegerätenüberblick

In diesem Thema werden die Konzepte, die den Kleinperipheriegeräten zugeordnet werden. Es werden die verschiedenen Arten Peripheriegeräte an, dass die Verkaufsstelle (POS) und die Komponenten verbunden werden können, die für das Verwalten der Verbindung mit dem POS zuständig sind.

<a name="concepts"></a>Konzepte
--------

### <a name="pos-registers"></a>POS-Register

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** Register **. Das Register Verkaufsstelle (POS)- ist eine Entität, die verwendet wird, um die Merkmale einer bestimmten AOS-Instanz des POS zu definieren. Diese umfassen das Hardwareprofil Merkmale bzw. die Einstellung für Kleinperipheriegeräte, die am Register verwendet werden, den Shop, der die Kasse zugeordnet ist, und die Sichterfahrung für den Benutzer, der sich bei diesem Register signiert.

### <a name="devices"></a>Geräte

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** Geräte **. Ein Gerät ist eine Entität, die eine physische Instanz eines Gerätes darstellt, das dem POS-Register zugeordnet ist. Wenn ein Gerät erstellt wurde, verfügt diese einem POS-Register zugeordnet. Die Geräteentität verfolgt Informationen darüber, ob ein POS-Register aktiviert ist, welcher Client verwendet wird und das Anwendungspaket, das für ein bestimmtes Gerät bereitgestellt wurde. Geräte können zu folgenden Bewerbungstypen zugeordnet werden: Modernes KleinPOS, Kleincloud POS, modernes - KleinPOS Windows Phone, modernes KleinPOS - Android und modernes - KleinPOS IOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Modernes POS ist das POS-Programm für Microsoft Windows. Es kann ein 10-Betriebssystemen (Windows OSs) bereitgestellt werden.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS ist eine browserbasierte Version des modernen POS-Programms, das in einem Webbrowser zugegriffen werden kann.

### <a name="modern-pos-for-ios"></a>Modernes POS für IOS

Modernes POS für IOS ist eine IOS-basierte Version des modernen POS-Programms, das auf IOS-Geräten bereitgestellt werden kann.

### <a name="modern-pos-for-android"></a>Modernes POS für Android

Modernes POS für Android ist eine Android-basierte Version des modernen POS-Programms, das auf androiden Geräten bereitgestellt werden kann.

### <a name="pos-peripherals"></a>POS-Peripheriegeräte

POS-Peripheriegeräte werden Geräte, die für POS-Funktionen explizit unterstützt werden. Diese Peripheriegeräte werden in der Regel in bestimmten Klassen aufgeteilt. Weitere Informationen über diese Klassen, lesen Sie den Abschnitt "Einheitenklasse" dieses Themas.

### <a name="hardware-station"></a>Hardwarestation

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanäle ** &gt; ** Einzelhandelsgeschäfte ** &gt; ** alle Einzelhandelsgeschäfte **. Wählen Sie einen Shop aus, und klicken Sie anschließend auf die Registerkarte **Hardwarestationen**. ** Die Hardwarestation ** Einstellung ist eine KanalEbeneneinstellung, die verwendet wird, um Rücklieferungen zu definieren, in denen die Kleinzusatzlogik bereitgestellt wird. Diese Einstellung auf der Ebene wird verwendet, um die Merkmale Hardwarestation zu bestimmen. Sie ist außerdem in die Listenhardwarestationen verwendet, die für POS-Instanz eine moderne in einen bestimmten Shop verfügbar sind. Die Hardwarestation wird in das POS-Programm moderne für Windows erstellt. Die Hardwarestation kann auch unabhängig bereitgestellt werden als ein eigenständiges Programm Microsoft-Internetinformationsdienste (IIS)-. In diesem Fall kann sie über ein Netzwerk zugreifen.

### <a name="hardware-profile"></a>Hardwareprofil

Navigationspfad: ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwareprofile **. Das Hardwareprofil ist eine Liste von Geräten, die für ein oder eine Hardwarestation POS-Register konfiguriert werden. Das Hardwareprofil kann direkt einem POS-Register oder eine Hardwarestation zugeordnet werden.

## <a name="devices-classes"></a>Einheitenklassen
POS-Peripheriegeräte werden üblicherweise bei Klassen aufgeteilt. Dieser Abschnitt beschreibt und gibt einen Überblick der Geräte, die modernes POS unterstützt.

### <a name="printer"></a>Drucker

Drucker enthalten traditionelle POS-Zugangsdrucker und ganzseitige Drucker. Drucker werden nach Object Linking and Embedding Fahrer für Retail POSs (um) und Microsoft Windows Schnittstellen unterstützt. Die zwei Drucker können gleichzeitig verwendet werden. Diese Funktion unterstützt Szenarien, in denen cash-and-carry Debitorenbons auf Zugangsdruckern gedruckt werden, für Kundenaufträge, die mehr Informationen führen, in einem ganzseitigen Drucker gedruckt werden. Bondrucker können direkt mit einem Computer zu USB verbunden werden, an Ethernet über ein Netzwerk verbunden sind, oder zu Bluetooth verbunden werden.

### <a name="scanner"></a>Scanner

Die zwei Strichcodescanner können gleichzeitig verwendet werden. Diese Funktion unterstützt Szenarien, in denen ein Scanner, der mehr Mobile ist, erforderlich ist, um die sehr schwere oder Artikel zu scannen, ein fester eingebetteter Scanner für die meisten Standard-skalierten Artikel verwendet wird, um von Auscheckenzeiten zu beschleunigen. Scanner können nach, um Universal-Zugang Plattform (UWP) oder Tastatursektorschnittstellen unterstützt werden. USB oder Bluetooth können verwendet werden, um einem Scanner Verbindung mit einem Computer herstellen.

### <a name="msr"></a>MSR

Ein USB-Magnetstreifenleser (MSR) kann so eingerichtet werden, indem OPOS-Fahrer verwendet. Wenn Sie ein eigenständiges MSR (EFT)- für Zahlungsbuchungen für elektronische Überweisungen verwenden möchten, muss einen MSR (Magnetstreifenleser) durch einen Zahlungskonnektor verwaltet werden. Eigenständiges MSR kann für Debitorenloyalitätseintrag, Mitarbeiteranmeldung und Geschenkkarteeintrag, unabhängig des Zahlungskonnektors verwendet werden.

### <a name="cash-drawer"></a>Geldlade

Zwei Geldladen können pro Hardwareprofil unterstützt werden. Diese Funktion ermöglicht zwei aktive Schichten pro Register, die verfügbar ist gleichzeitig. Im Falle einer freigegebenen oder einer Schicht Geldlade, die durch mehrere Geräte des Mobiles POS gleichzeitig verwendet wird, nur eine Geldlade pro Hardwareprofil zulässig ist. Geldladen können direkt mit einem Computer zu USB verbunden werden, an ein Netzwerk verbunden werden, an einen oder Bondrucker über eine Schnittstelle RJ12 verbunden werden. In einigen Fällen kann Geldladen zu Bluetooth auch verbunden werden.

### <a name="line-display"></a>Zeilenanzeige

Gerätenamens für werden verwendet, um Produkte, nützliche Buchungssaldos und andere Informationen während einer Buchung anzeigen den Debitor. Ein Zeilendisplay kann an den Computer herstellen USB, zu, indem OPOS-Fahrer verwendet.

### <a name="signature-capture"></a>Signaturerfassung

Unterschriftenaufnahmegeräte können direkt mit einem Computer herstellen USB, zu, indem OPOS-Fahrer verwendet. Wenn Signatur, aufzeichnen, wird der Debitor wird aufgefordert, um im Gerät zu signieren konfiguriert. Nachdem die Signatur bereitgestellt wird, hat diese dem Kassierer zur Abnahme dargestellt.

### <a name="scale"></a>Skalieren

Skalen können an den Computer herstellen zu USP, indem OPOS-Fahrer verwendet. Wenn ein Produkt, das als "gewogenes Produkt" markiert wird, einer Buchung hinzugefügt wird, weist das POS das Gewicht von der Waage, fügt das Produkt der Buchung hinzu und verwendet, die die Menge der Skala bereitgestellt hat.

### <a name="pin-pad"></a>PIN-Feld

Geheimzahl (PIN)- Auflagen werden um von unterstützt, müssen aber zu einem Zahlungskonnektor verwaltet werden.

### <a name="secondary-display"></a>Sekundäre Anzeige

Wenn eine sekundäre Anzeige wird konfiguriert, wird die Zahl 2. Windows-Anzeige verwendet, um grundlegende Informationen anzuzeigen. Der Kostenträger der sekundären Anzeige ist, (ISV)- Vergrößerung des unabhängigen Softwarehersteller zu unterstützen, da sekundäre Standard, die Anzeige nicht konfiguriert werden kann und begrenzten Inhalten werden.

### <a name="payment-device"></a>Zahlungsgerät

Zahlungsgerätensupport wird durch den Zahlungskonnektor implementiert. Zahlungsgeräte können eine oder mehrere der Funktionen ausführen, die andere Einheitenklassen bereitgestellt werden. So kann ein Zahlungsgerät als MSR-/cardleser, Zeilendisplay, oder Gerät für elektronische Unterschriften PIN-Feld arbeiten. Unterstützung für Zahlungsgeräte wird unabhängig des eigenständigen Gerätensupports implementiert, die für andere Geräte zulässig ist, die im Hardwareprofil enthalten sind.

## <a name="supported-interfaces"></a>Unterstützte Schnittstellen
### <a name="opos"></a>Um

Sie können der größten Bereich von Geräten mit Microsoft Dynamics 365 für Arbeitsgänge verwendet werden kann - Einzelhandel sicherzustellen, ist das branchenüblichen OLE POS für die primäre Kleinperipheriegerätplattform die in Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge unterstützt wird. OLE Der für POS-Standard wurde aus nationalen Kleinverbund (NRF) erzeugt, der Kommunikationsprotokolle branchenüblichen für Kleinperipheriegeräte herstellt. Um eine handelt weithin anerkannte Implementierung des OLE für POS-Standards. Es wurde entwickeltes im Jahre Mitte 1990 > wird mehrmals und seitdem aktualisiert. Um enthält eine Gerätetreiberarchitektur, die einfache Integration von POS-Hardware mit Windows-basierten POS-Systemen aktiviert. OPOS-Kontrollenziehpunktkommunikation zwischen kompatibler und der Hardware POS-Software. Ein OPOS-Steuerelement besteht aus zwei Teilen:

-   ** Steuerobjekt ** – Das Steuerobjekt für eine Einheitenklasse (z Gerätenamens für) stellt die Schnittstelle zum Softwareprogramm bereit. Monroe-Beratungsdienste www.monroecs.com ([] (http://www.monroecs.com/)) Standardbericht enthält einen Satz OPOS-Steuerobjekte, die als Objekte (CCOs) der gemeinsamen Regelung bezeichnet. Das CCOs werden verwendet, um die POS-Komponente von Microsoft Dynamics 365 für Arbeitsgänge zu testen - Einzelhandel. Daher wird durch die Testshilfen, dass, wenn Microsoft Dynamics 365 für Einzelhandel - Arbeitsgänge unterstützt eine Einheitenklasse um nach, viele Einheitentypen kann unterstützt werden, vorausgesetzt, dass der Hersteller ein Serviceobjekt bereitstellt, um das für erstellt wird. Sie müssen jeden Einheitentyp nicht explizit testen.
-   ** ** Serviceobjekt – Das Serviceobjekt enthält Kommunikation zwischen dem Steuerobjekt () und dem CCO Gerät. Normalerweise wird für das Serviceobjekt ein Gerät aus dem Gerätenhersteller bereitgestellt. Jedoch in bestimmten Fällen müssen Sie möglicherweise das Serviceobjekt aus der Website des Herstellers herunterladen. Beispielsweise kann es sich bei einem Serviceobjekt später verfügbar. Um die Adresse der Website des Herstellers suchen, finden Sie in Hardwaredokumentation.

[Steuerobjekt ![und -Serviceobjekt] ". /media/retail_peripherals_overview01.png)]". - /media/retail_peripherals_overview01.png) Unterstützung für die OPOS-Implementierung von Datenbanken für POS-Hilfen sicherstellen, dass die Gerätenhersteller und POS-Herausgeber der Standardspeicherposition ordnungsgemäß implementieren, und POS-Systemen unterstützte Geräte zusammenarbeiten können, wenn sie zuvor nicht zusammen getestet wurden. ** Hinweis: ** OPOS-Support wird sichergestellt nicht Support für alle Geräte, die OPOS-Fahrer haben. Microsoft Dynamics 365 für Arbeitsgänge Einzelhandel - muss den Einheitentyp oder Klassen, um von zuerst aufgeführt. Darüber hinaus können ggf. Serviceobjekte nicht unbedingt mit der aktuellen Version des CCOs auf dem aktuellen Stand befindet. Sie sollten sich bewusst auch, dass im Allgemeinen auf die Servicequalitätsobjekte unterscheidet.

### <a name="windows"></a>Windows

Bondruck am POS wird für um optimiert wird. Neigt, um als Drucken von Windows viel schneller werden sollen. Daher wird empfohlen, um, insbesondere in der Kleinumgebung zu verwenden, in der 40 Spaltenzugänge gedruckt und Buchungszeiten schnell sein muss. Für die meisten Geräte verwenden Sie OPOS-Kontrollen. Allerdings unterstützen mehrere OPOS-Zugangsdrucker auch Windows-Fahrer. Mithilfe eines Windows-Fahrer verwenden, können Sie die neuesten Schriftarten und den Drucker im Netzwerk eines für mehrere Register zugreifen. Allerdings besteht Nachteile der Verwendung von Windows-Fahrern. Nachfolgend finden Sie einige Beispiele dieser Nachteile:

-   Wenn Windows-Fahrer verwendet werden, Bilder gerendert werden, bevor das Drucken auftritt. Daher neigt das Drucken, langsamer werden soll, wenn sie auf Druckern ist, die OPOS-Kontrollen verwenden.
-   Geräte, die von den Drucker verkettet verbunden sind ("") gearbeitet haben möglicherweise nicht korrekt, wenn Windows-Fahrer verwendet werden. Beispielsweise kann die Geldlade geöffnet hat sich nicht, oder der Kassenbelegdrucker konnte Wort, wie Sie erwarten.
-   Um mehr unterstützt außerdem eine umfangreiche Palette Variablen, die den Kleinzugangsdruckern, wie Papierausschnitt- oder Belegdrucken bestimmt sind.

Wenn für den OPOS-Kontrollen Windows-Drucker verfügbar sind, die Sie bei der Grobterminierung verwenden, sollte der Drucker eingelegt Microsoft Dynamics 365 für Arbeitsgänge noch ordnungsgemäß arbeiten - Einzelhandel.

### <a name="universal-windows-platform"></a>Universal-Zugang Plattform

UWP, bei der Kleinperipheriegeräte, wird zu Windows-Support für bedienungsfertige Geräte zugeordnet. Wenn ein bedienungsfertiges Gerät an eine Windows-Betriebssystemversion verbunden ist, in der diese Art des Geräts unterstützt, ist kein Fahrer erforderlich, damit das Gerät verwendet werden kann, z vorgesehen wurde. Wenn beispielsweise ein Bluetooth-Lautsprechergerät Windows, erkennt weiß das Betriebssystem das Gerät, dass den Lautsprecher ** ** Klassentyp hat. Daher und behandelt dieses Gerät es als Lautsprecher. Es ist keine zusätzliche Einrichtung ist obligatorisch. Im Falle POS-Geräte können viele USB-Geräte verbunden werden, und Windows werden sie als Eingabegeräte (HIDs). Allerdings ist er möglicherweise nicht in der Lage, die Funktion auf, die bestimmen das Gerät, da das Gerät nicht der Klasse angibt, oder der Typ, des Geräts bereitstellt. In Windows 10 ist Einheitenklassen für Strichcodescanner MSR und hinzugefügt. Wenn ein Gerät zu Windows 10 als Gerät aus einer der Klassen sich deklariert, beendet Windows für Ereignisse vom Gerät zu den entsprechenden Uhrzeiten. Modernes POS unterstützt UWP MSR und Scanner. Wenn es zur Eingabe eines dieser Geräte bereit ist, und ein RFID-Gerät, das durch eine der Klassen gehört, wird das Gerät, kann verbunden verwendet werden. Wenn beispielsweise ein UWP-Barcodescanner in einem Windows 10-Computer eingesteckt wird, und Strichcodeanmeldung wird für modernes POS, der konfiguriert Strichcodescanner aktiv wird im Feld Anmeldungsbildschirm. Es ist keine zusätzliche Einrichtung ist obligatorisch. Zusätzliche Klassen von Geräten des UWP POS an Windows hinzugefügt werden. Diese Klassen beinhalten Klassen für Geldladen und Bondrucker. Unterstützung für diese neuen Einheitenklassen das modernem POS ist aussteht.

### <a name="keyboard-wedge"></a>Tastatursektor

Tastatursektorgeräte senden Daten auf den Computer, als ob diese Daten auf der Tastatur eingegeben wurden. Somit erhält standardmäßig das Feld, das am POS aktiv ist, die Daten, die im Lieferumfang oder Karte durch ein Lesegerät gezogen wird. In einigen Fällen kann dieses Verhalten den falschen Typ der Daten führen, in das falsche Feld gescannt werden. Beispielsweise könnte ein Strichcode in ein Feld, das nach möglicherweise für Eingabe aus Kreditkartendaten bezieht. In vielen Fällen besteht Logik am POS, das bestimmt, ob die Daten, die im Lieferumfang oder Karte durch ein Lesegerät gezogen, wird ein Strichcode oder ein Ziehen der Karte durch ein Lesegerät ist. Daher werden die Daten korrekt bearbeitet. Wenn Geräte als um anstelle der Tastatur sektorgeräte eingerichtet sind, gibt es weitere Kontrolle über, wie die Daten aus diesen Geräten verbraucht werden können, da mehr zum Gerät "bezeichnet" dem die Daten stammen aus. Beispielsweise werden Daten von einem Strichcodescanner automatisch als Strichcode erkannt, und der entsprechende Datensatz in der Datenbank ist einfach und schneller als, wenn eine generische Suche nach einer Zeichenfolge verwendet wurden, z im Falle der Tastatur sektorgeräte gefunden.

### <a name="native-printer"></a>Systemeigener Drucker

("Systemeigene Gerät" während der Typ im Hardwareprofil Bezeichnung), Drucker können konfiguriert werden, um den Benutzer aufzufordern, einen Drucker auszuwählen, der den Computer für konfiguriert wird. Wenn ein Gerät ** ** Drucker des Typs wird konfiguriert, wenn modernes POS einen Drucktbefehl kennen, wird der Benutzer aufgefordert, einen Drucker in einer Liste auswählen. Dieses Verhalten unterscheidet sich insofern vom Verhalten für Windows-Fahrer, da der Windows ** ** Drucker im Feld Hardwareprofil enthält keine Liste von Druckern eingeben. Stattdessen es erforderlich, dass ein benannter Drucker im ** Gerätename ** Feld angegeben.

### <a name="windows"></a>Windows

** Windows ** Der Einheitentyp wird nur für Drucker verwendet. Wenn ein Windows-Drucker im Hardwareprofil konfiguriert wurde, muss der Name des jeweiligen Druckers angegeben werden. Wenn POS-Treffen moderne Ereignisse drucken, wenn ein Windows-Drucker konfiguriert ist, wird das Ereignis auf diesen angegebenen Windows-Drucker übergeben. Der Benutzer wird nicht aufgefordert, einen Drucker auszuwählen.

### <a name="network"></a>Netzwerk

Netzwerk-adressierbare, Geldladen Bondrucker und Zahlungsterminals können über ein Netzwerk, die verwendet werden direkt über die Hardwarestation der prozessübergreifenden Kommunikationen IPK "),der im POS für moderne Windows-Anwendung oder von der IIS-Hardwarestation für andere POS-Kunden moderne erstellt wird.

## <a name="hardware-station-deployment-options"></a>Hardwarestationsbereitstellungsoptionen
### <a name="ipc-built-in"></a>(Einbauten IPK"

Die Hardwarestation der prozessübergreifenden Kommunikationen IPK ") wird im POS für moderne Windows-Anwendung erstellt. Um die IPC-Hardwarestation zu verwenden, Zuweisen eines Hardwareprofils zu einem Register zu das das moderne Windows-Anwendung POS für verwendet. Erstellen Sie dann eine Hardwarestation von ** dediziert ** eingeben für den Shop, in dem das Register verwendet wird. Wenn Sie modernes POS beginnen, ist die IPC-Hardwarestation aktiv, und die POS-Peripheriegeräte, die konfiguriert wurden, werden zu. Wenn Sie die nicht die lokale Hardware aus irgendeinem Grund müssen, verwenden Sie den ** Verwalten von Hardwarestationen ** Arbeitsgang, um die Hardwarestationsfunktionen zu deaktivieren. Modernes POS können die IPC-Hardwarestation auch verwenden, um direkt Netzwerkperipheriegeräte verbunden werden sollen.

### <a name="iis"></a>IIS

Sie können das oder IIS die eigenständige Version der Hardwarestation auf zwei verschiedene Arten verwenden. Der Deskriptor "IIS" bedeutet, dass die POS-Bewerbung an die Hardwarestation Microsoft-Internetinformationsdienste zu verbinden. Die POS-Bewerbung Connect die Webdienste zu IIS-Hardwarestation angezeigt, die auf einem Computer ausgeführt werden, in dem die Geräte verbunden werden. Wenn IIS verwendet wird, können die Kleinperipheriegeräte, die mit einer Hardwarestation verbunden werden, von jedem POS-Register verwendet werden, die auf demselben Netzwerk wie die IIS-Hardwarestation ist. Da nur modernes POS für Windows integrierten Unterstützung für Kleinperipheriegeräte umfasst, dann müssen alle anderen modernen POS-Bewerbungen die IIS-Hardwarestation verwenden, um POS-Peripheriegeräte verbunden werden sollen, die im Hardwareprofil konfiguriert werden. Deshalb muss jede Instanz der IIS-Hardwarestation einen Computer, der den Webdienst und die Anwendung ausführen, die die Geräte ist. Die IIS-Hardwarestation ist für alle modernen POS Bewerbungen NichtWindowss erforderlich.

#### <a name="dedicated"></a>Dediziert

Modernes POS verwendet Hardwarestationen von ** dediziert ** eingibt, um zu ermitteln, dass Peripheriegeräte direkt an den Computer herstellen, in dem der Zeit-App verwendet wird. Allerdings kann der ** dediziert ** Typ für IIS-Hardwarestationen auch verwendet werden. In einem herkömmlichen, Fester POS-Szenario, das Cloud POS als die POS-Bewerbung verwendet, wird der Hardwarestationstyp ** dediziert ** für IIS-Hardwarestationen verwendet, die auf demselben Computer bereitgestellt werden, der Cloud POS ausführt. Klicken Sie in einer Kleinperipheriegerätenperspektive kann die dedizierte IIS-Hardwarestation besseren Kleinzusatzsupport für feste traditionelle, POS-Szenarien. Dedizierte Hardwarestationen unterstützen alle Peripheriegeräte das Hardwareprofil, die in unterstützt werden.

#### <a name="shared"></a>Gemeinsam

Freigegebene Hardwarestationen sollen Ihnen, um mehrere POS-Geräte durch den Kurs des Tages verwendet werden. Freigegebene Hardwarestationen optimiert werden, um nur Geldladen Bondrucker, und Zahlungsterminals zu unterstützen. Sie können jedoch Strichcodescanner MSR Gerätenamens für, Skalen oder andere Geräte nicht direkt herstellen. Andernfalls treten Konflikte auf, wenn mehrere POS-Geräte versuchen Peripheriegeräte, diese gleichzeitig zu beanspruchen. Das hier, wie unterstützte Konflikte für Geräte verwaltet werden:

-   ** Geldlade ** – ist die Geldlade geöffnet über ein Ereignis, das dem Gerät gesendet wird. Der einzige Problem, die auftreten kann, wenn eine Geldlade aufgerufen wird, findet statt, wenn die Kassenlade bereits geöffnet ist. Im Falle der freigegebenen Hardwarestationen soll die Kassenlade auf ** freigegeben ** in das Hardwareprofil festgelegt werden. Diese Einstellung wird vom POS zur Überprüfung an, ob bereits die Geldlade geöffnet ist, wenn sie offene Befehle übermittelt.
-   ** Bondrucker ** - wenn zwei Zugangsdruckenbefehle der Hardwarestation gleichzeitig gesendet werden, kann einer der Befehle, je nach spezifischem Gerät "Verloren". Einige Geräte haben internen oder Pooling, Speicherung, die dieses Problem verhindern können. Wenn ein Drucktbefehl nicht erfolgreich ist, erhält der Kassierer eine Fehlermeldung und den Drucktbefehl vom POS versuchen erneut.
-   ** Zahlungsterminal ** – Wenn ein Kassierer Zahlungsmittel eine Buchung an einem Zahlungsterminal versucht, das bereits verwendet wird, um eine Meldung informiert den Kassierer, dass das Terminal verwendet wird und fordert den Kassierer, noch einmal später vorgenommen werden können. Normalerweise Kassierer können sehen, dass bereits ein Terminal verwendet wird und warten wird, bis die andere Buchung abgeschlossen ist, bevor sie Zahlungsmittel noch einmal ausgeführt.

Die Prüfung wird für eine zukünftige Version geplant um zu ermitteln, ob ungestützte Geräte für ein Hardwareprofil eingerichtet werden, die auf eine freigegebene Hardwarestation zugeordnet ist. Werden ungestützte Geräte, der Benutzer einer Meldung wird realisiert, durch die angegeben wird, dass die für freigegebene Hardwarestationen Geräte nicht unterstützt werden. Im Falle der freigegebenen wird die Hardwarestationen ** wählen Sie nach dem Auswählen Anbieten ** Option auf Ja ** ** auf der Registerebene festgelegt. Der POS-Benutzer wird aufgefordert, eine Hardwarestation auszuwählen, wenn ein Zahlungsmittel für eine Buchung am POS aktiviert ist. Wenn die Hardwarestation nur zum Zeitpunkt der Zahlungsmittel ausgewählt wird, wird die Hardwaresenderauswahl direkt an den POS-Workflow mobile für Szenarios hinzugefügt. Wenn zusätzliche Vorteil wird das Zeilendisplay im Feld Zahlungsterminal nicht für freigegebene Szenarien verwendet. Wenn das Zahlungsterminal als Zeilendisplay verwendet wird, können andere Benutzer von Produktionsgemeinkosten mithilfe dieses Terminals gesperrt werden, wenn die Buchung abgeschlossen ist. In den Positionen mobilen Szenarien werden möglicherweise an einer Buchung für einen längeren Zeitraum hinzugefügt. Daher ist die ** wählen Sie nach dem Auswählen Anbieten ** Option obligatorisch, um eine optimale Gerätenverfügbarkeit sicherzustellen.

### <a name="network-peripherals"></a>Netzwerkperipheriegeräte

Die Netzwerkbezeichnung für Geräte Hardwareprofil im aktiviert, Geldladen Bondrucker und die zu einer Netzwerkverbindung verbunden werden, Zahlungsterminals.

#### <a name="modern-pos-for-windows"></a>Modernes POS für Windows

Sie können IP-Adressen für Netzwerkperipheriegeräte in zwei Stellen angeben. Wenn der Kunde moderne POS Windows einen individuellen Satz Netzwerkperipheriegeräte verwendet, sollten Sie die IP-Adressen diese für Geräte festlegen, indem Sie die IP-Konfiguration ** ** Option im Aktivitätsbereich für das Register auch verwenden. Bei der geräte Netzwerk, die unter POS-Registern freigegeben werden, kann ein Hardwareprofil, das vorhanden, die geräte Netzwerk, die ihm zugewiesen werden, direkt auf eine freigegebene Hardwarestation zugeordnet werden. Um IP-Adressen zuzuweisen, wählen Sie diese auf der Hardwarestation ** Einzelhandelsgeschäfte ** Seite aus, und verwenden Sie dann die IP-Konfiguration ** ** Option im Hardwarestationen ** ** Abschnitt den Netzwerkgeräten anzugeben die dieser Hardwarestation zugewiesen werden. Für Hardwarestationen, die nur Netzwerkgeräte haben, müssen Sie die Hardwarestation selbst nicht bereitgestellt. In diesem Fall wird die Hardwarestation, um erforderliche Netzwerk-adressierbare Geräte entsprechend ihrem Lagerplatz im auf Shop Lagermanagement nur begrifflich zu gruppieren.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Sie Bewölken POS, modernes POS für IOS und modernes POS für Android

Logik Die, die physisch verbunden ist und die Netzwerk-adressierbaren Peripheriegeräte wird in der Hardwarestation enthalten. Daher für alle POS-Kunden außer modernes POS für Windows, muss eine IIS-Hardwarestation bereitgestellt und aktiv sein, damit sie das POS zu aktivieren, die mit Peripheriegeräten, unabhängig davon, ob diese die Kommunikation Peripheriegeräte physisch an eine Hardwarestation verknüpft sein oder über dem Netzwerk nicht behoben werden.

## <a name="setup-and-configuration"></a>Einrichtung und Konfiguration
### <a name="hardware-station-installation"></a>Hardwarestationsinstallation

Weitere Informationen finden Sie Kleinhardwarestationskonfiguration Installation und [] (retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modernes POS für Windows-Einstellung und - Konfiguration um

Weitere Informationen finden Sie POS-KleinKonfiguration moderne und Installation [] (retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS-Geräteinstallation und Konfiguration

Weitere Informationen zu OPOS-Komponenten, sehen Sie, dass für die Schnittstellen" Abschnitt dieses Dokuments wird. Normalerweise werden OPOS-Fahrer vom Gerätenhersteller bereitgestellt. Wenn ein OPOS-Gerätetreiber eingerichtet wird, fügt er einem Schlüssel " Windows-Registrierung an einem der folgenden Orte hinzu:

-   ** 32-Bit-System: ** LOKALE VARIABLE \_MACHINESOFTWAREOLEforRetailServiceOPOS HKEY\_
-   ** 64-Bit-System: ** LOKALE VARIABLE \_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS HKEY\_

Innerhalb des ServiceOPOS-Registrierungslagerplatzes konfigurierte werden Geräte entsprechend der OPOS-Einheitenklasse sortiert. Mehrere Gerätetreiber werden gespeichert.

## <a name="supported-scenarios-by-hardware-station-type"></a>Unterstützte Szenarien nach Hardwarestationstyp
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>- IPC-Hardwarestation für IIS-Hardwarestation Kundensupport

Die folgende Tabelle zeigt die Topologien und die Bereitstellungs szenarien an die, unterstützt werden.

| Kunde      | IPC-Hardwarestation | IIS-Hardwarestation |
|-------------|----------------------|----------------------|
| Windows-App | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| IOS         | Nr.                   | Ja                  |

### <a name="network-peripherals"></a>Netzwerkperipheriegeräte

Netzwerkperipheriegeräte können direkt über die Hardwarestation unterstützt werden, der im POS für moderne Windows-Anwendung erstellt wird. Bei allen anderen Client müssen Sie eine IIS-Hardwarestation bereitstellen.

| Kunde      | IPC-Hardwarestation | IIS-Hardwarestation |
|-------------|----------------------|----------------------|
| Windows-App | Ja                  | Ja                  |
| Cloud POS   | Nr.                   | Ja                  |
| Android     | Nr.                   | Ja                  |
| IOS         | Nr.                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Unterstützte Einheitentypen nach Hardwarestationstyp
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modernes POS für Windows mit einer Hardwarestation IPK (Einbauten)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Unterstützte Einheitenklasse</th>
<th>Unterstützte Schnittstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Drucker</td>
<td><ul>
<li>Um</li>
<li>Windows-Treiber</li>
<li>Gerät</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>Um</li>
<li>Windows-Treiber</li>
<li>Gerät</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zeilenanzeige</td>
<td>Um</td>
</tr>
<tr class="even">
<td>Duale Anzeige</td>
<td>Windows-Treiber</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>Um</li>
<li>UWP (keine Einstellung ist erforderlich.)</li>
<li>Tastatursektor (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Aussteller</td>
<td><ul>
<li>Um</li>
<li>Kassenlade Netzwerk <strong>Hinweis:</strong> nur eine Einrichtung werden, wenn <strong>Schicht gemeinsame Verwendung</strong> auf der Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Schublade 2</td>
<td><ul>
<li>Um</li>
<li>Kassenlade Netzwerk <strong>Hinweis:</strong> nur eine Einrichtung werden, wenn <strong>Schicht gemeinsame Verwendung</strong> auf der Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>Um</li>
<li>UWP (keine Einstellung ist erforderlich.)</li>
<li>Tastatursektor (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>Um</li>
<li>UWP (keine Einstellung ist erforderlich.)</li>
<li>Tastatursektor (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skalieren</td>
<td>Um</td>
</tr>
<tr class="odd">
<td>PIN-Feld</td>
<td>Um "Support wird mit Anpassung des Zahlungskonnektors zulässig).</td>
</tr>
<tr class="even">
<td>Signaturerfassung</td>
<td>Um</td>
</tr>
<tr class="odd">
<td>Zahlungsterminal </td>
<td><ul>
<li>Benutzerdefinierter spezifischer Gerätensupport</li>
<li>Netzwerk (weitere Informationen, finden Sie die Zahlungskonnektordokumentation.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle modernen POS-Kunden, die eine IIS-Hardwarestation dedizierte haben

** Hinweis: ** Wenn die " IIS-Hardwarestation dediziert ist, gibt " eine Eins-zu-Eins-Beziehung zwischen dem POS-Kunden und der Hardwarestation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Unterstützte Einheitenklasse</th>
<th>Unterstützte Schnittstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Drucker</td>
<td><ul>
<li>Um</li>
<li>Windows-Fahrer für Windows-Drucker in einem Netzwerk, der der Benutzer Hardwarestation muss über die Berechtigung verfügen, den Drucker zuzugreifen.</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>Um</li>
<li>Windows-Treiber</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zeilenanzeige</td>
<td>Um</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>Um</td>
</tr>
<tr class="odd">
<td>Aussteller</td>
<td><ul>
<li>Um</li>
<li>Netzwerk <strong>Hinweis:</strong> nur eine Kasse pro Hardwareprofil eingerichtet werden kann, wenn <strong>Schicht gemeinsame Verwendung</strong> in der Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Schublade 2</td>
<td><ul>
<li>Um</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner</td>
<td>Um</td>
</tr>
<tr class="even">
<td>Scanner 2</td>
<td>Um</td>
</tr>
<tr class="odd">
<td>Skalieren</td>
<td>Um</td>
</tr>
<tr class="even">
<td>PIN-Feld</td>
<td>Um "Support wird mit Anpassung des Zahlungskonnektors zulässig).</td>
</tr>
<tr class="odd">
<td>Sig. erfassen</td>
<td>Um</td>
</tr>
<tr class="even">
<td>Zahlungsterminal </td>
<td><ul>
<li>Benutzerdefinierter spezifischer Gerätensupport</li>
<li>Netzwerk (weitere Informationen, finden Sie die Zahlungskonnektordokumentation.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle modernen POS-Kunden, die eine gemeinsame IIS-Hardwarestation haben

** Hinweis: ** Wenn die IIS-Hardwarestation " hat, " können die Hardwarestation Geräte mehrere gleichzeitig verwenden. Für dieses Szenario sollten Sie nur die Geräte verwenden, die in der weiter unten dargestellten Tabelle. Wenn Sie versuchen, freizugeben, wenden Geräte, die hier, nicht wie Strichcodescanner und MSR, Fehler aufgeführt werden, aufgeführt, wenn mehrere Geräte versuchen, dasselbe Peripheriegerät zu beanspruchen. In der Zukunft wird eine solche Konfiguration explizit verhindert.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Unterstützte Einheitenklasse</th>
<th>Unterstützte Schnittstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Drucker</td>
<td><ul>
<li>Um</li>
<li>Windows-Fahrer für Windows-Drucker in einem Netzwerk, der der Benutzer Hardwarestation muss über die Berechtigung verfügen, den Drucker zuzugreifen.</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>Um</li>
<li>Windows-Treiber</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Aussteller</td>
<td><ul>
<li>Um</li>
<li>Netzwerk <strong>Hinweis:</strong> nur eine Kasse pro Hardwareprofil eingerichtet werden kann, wenn <strong>Schicht gemeinsame Verwendung</strong> in der Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Schublade 2</td>
<td><ul>
<li>Um</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zahlungsterminal </td>
<td><ul>
<li>Benutzerdefinierter spezifischer Gerätensupport</li>
<li>Netzwerk (weitere Informationen, finden Sie die Zahlungskonnektordokumentation.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfiguration für unterstützte Szenarien
Weitere Informationen dazu, wie Sie Hardwareprofile, finden erstellt [Definieren und Verwalten von Kanalkunden, einschließlich und Register Hardwarestationen] verwalten" define-maintain-channel-clients-registers-hw-stations.md ). ** Hinweis: ** Für Microsoft Dynamics 365 für Arbeitsgangsversion 1611, wird das Hardwarestationsprofil nicht mehr verwendet. Attribute, dass Sie bereits im Vorfeld im Hardwarestationsprofil einrichten, sind jetzt Teil der Hardwarestation selbst.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modernes POS für Windows mit einer Hardwarestation IPK (Einbauten)

Diese Konfiguration ist die typischste Konfiguration für die festen traditionellen, POS-Register. Für dieses Szenario werden die Hardwareprofilinformationen direkt dem Register selbst zugeordnet. Die EFT-Terminalnummer soll auf das Register auch auch festgelegt werden. Um diese Konfiguration einzurichten, führen Sie die folgenden Schritte aus.

1.  Erstellen eines Hardwareprofils, wo alle erforderlichen Peripheriegeräte konfiguriert werden.
2.  Ordnen Sie den dem Hardwareprofil POS-Register zu.
3.  Erstellen Sie eine Hardwarestation von ** dediziert ** eingeben für das auf Shop Lagermanagement, in dem das POS-Register verwendet wird. Eine Beschreibung ist optional. ** Hinweis: ** Sie müssen keine anderen Eigenschaften auf der Hardwarestation festlegen. Alle anderen Informationen, z das Hardwareprofil, aus dem Register selbst.
4.  ** Sie Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
5.  Wählen Sie den Verteilungszeitplan ** ** 1090 aus, um das neue Hardwareprofil dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
6.  Wählen Sie den Verteilungszeitplan ** ** 1040 aus, um die neue Hardwarestation dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
7.  Installieren und aktivieren Sie modernes POS für Windows.
8.  Starten Sie modernes POS für Windows, und starten Sie, um die zugeordneten Peripheriegeräte verwendet werden soll.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Alle modernen POS-Kunden, die eine IIS-Hardwarestation dedizierte haben

Diese Konfiguration kann für alle modernen POS-Kunden verwendet werden, mit denen eine Hardwarestation haben, die ausschließlich durch ein POS-Register verwendet wird. Um diese Konfiguration einzurichten, führen Sie die folgenden Schritte aus.

1.  Erstellen eines Hardwareprofils, wo alle erforderlichen Peripheriegeräte konfiguriert werden.
2.  Erstellen Sie eine Hardwarestation von ** dediziert ** eingeben für das auf Shop Lagermanagement, in dem das POS-Register verwendet wird.
3.  Auf der dedizierten Hardwarestation Legen Sie die folgenden Eigenschaften ein:
    -   ** Hostname ** – Der Name des Hostcomputers, wo die Hardwarestation ausgeführt wird. ** Hinweis: ** Cloud POS können auflösen ** localhost ** um den lokalen Computer zu bestimmen, wo Cloud POS ausgeführt wird. Zuvor müssen die Bescheinigung, die erforderlich ist, um Cloud POS mit der Hardwarestation zuzuordnen, "Localhost" als Computernamen verfügen. Wenn Probleme zu vermeiden, sollten Sie eine Liste Hardwarestation dedizierten jeder Instanz für den Shop, nach Bedarf. Für jede Hardwarestation sollte der Hostname die bestimmte Computernamen werden, in der die Hardwarestation bereitgestellt wird.
    -   ** Port ** – Port, der zu verwenden, damit die Hardwarestation mit dem modernen POS-Kunden dem Sie kommunizieren möchten.
    -   ** Hardwareprofil ** – Wenn das Hardwareprofil nicht auf der Hardwarestation selbst angegeben, das Hardwareprofil, das dem Register zugewiesen ist, wird verwendet.
    -   ** Nummer EFT POS ** – Die EFT-Terminal-ID, das verwendet werden soll, wenn EFT-Autorisierungen übermittelt werden. Diese Kennung wird von der Kreditkartenverarbeitungsstelle bereitgestellt.
    -   ** Paketname ** – Das Hardwarestationspaket, das verwendet werden soll, wenn die Hardwarestation bereitgestellt wird.

4.  ** Sie Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
5.  Wählen Sie den Verteilungszeitplan ** ** 1090 aus, um das neue Hardwareprofil dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
6.  Wählen Sie den Verteilungszeitplan ** ** 1040 aus, um die neue Hardwarestation dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
7.  Richten Sie die Hardwarestation. Weitere Informationen dazu, wie die Hardwarestation, finden Sie unter Kleinhardwarestationskonfiguration Installation und [] (retail-hardware-station-configuration-installation.md).
8.  Installieren und aktivieren Sie modernes POS. Weitere Informationen dazu, wie modernes POS, finden Sie unter POS-KleinKonfiguration moderne und Installation [] (retail-modern-pos-device-activation.md).
9.  Melden Sie sich bei modernem POS, und wählen Sie aus ** führen Sie NichtKassenladearbeitsgänge ** aus.
10. Starten Sie den Hardwarestationen ** verwalten ** Arbeitsgang.
11. ** ** Verwalten Sie auf.
12. Auf der Hardwarestationsverwaltungsseite legen Sie die Option fest, die Hardwarestation zu aktivieren.
13. Wählen Sie die Hardwarestation aus, der verwendet werden soll, und klicken Sie dann Paare ** **.
14. Nachdem die Hardwarestation zugeordnet ist, klicken Sie auf Schließen. ** **
15. Auf der Hardwaresenderauswahlseite klicken Sie auf die Hardwarestation vor kurzem ausgewählte, um diese zu aktivieren.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle modernen POS-Kunden, die eine gemeinsame IIS-Hardwarestation haben

Diese Konfiguration kann für alle modernen POS-Kunden verwendet werden, die mit anderen Hardwarestationen Geräten freigeben. Um diese Konfiguration einzurichten, führen Sie die folgenden Schritte aus.

1.  Erstellen eines Hardwareprofils, in dem die erforderlichen Peripheriegeräte konfiguriert werden.
2.  Erstellen Sie eine Hardwarestation von ** freigegeben ** eingeben für das auf Shop Lagermanagement, in dem das POS-Register verwendet wird.
3.  Auf der freigegebenen Hardwarestation Legen Sie die folgenden Eigenschaften ein:
    -   ** Hostname ** – Der Name des Hostcomputers, wo die Hardwarestation ausgeführt wird.
    -   ** Beschreibung ** – Text, die das Zuweisen, die Hardwarestation zu ermitteln, wie ** Rücklieferungen ** oder ** Vordergrund ** der Filiale.
    -   ** Port ** – Port, der zu verwenden, damit die Hardwarestation mit dem modernen POS-Kunden dem Sie kommunizieren möchten.
    -   ** Hardwareprofil ** – für freigegebene Hardwarestationen, jede Hardwarestation soll ein Hardwareprofil eingerichtet haben. Hardwareprofile können unter Hardwarestationen freigegeben werden, jedoch müssen jeder Hardwarestation zugeordnet werden. Außerdem wird empfohlen, dass von freigegebenen Schichten verwendet, wenn mehrere Geräte identisch freigegebene Hardwarestation verwenden. Um eine freigegebene Schicht einrichten, klicken Sie Einzelhandel und ** Handel ** &gt; ** auf installierten Kanal ** &gt; ** POS eingerichtet ** &gt; ** POS-Profile ** &gt; ** Hardwareprofile **. Für jede gemeinsame Hardwareprofil Auswählen der Kassenlade aus und legen Sie die Schichtkassenlade ** freigegebene ** Option fest ** Ja **.
    -   ** Nummer EFT POS ** – Die EFT-Terminal-ID, das verwendet werden soll, wenn EFT-Autorisierungen übermittelt werden. Diese Kennung wird von der Kreditkartenverarbeitungsstelle bereitgestellt.
    -   ** Paketname ** – Das Hardwarestationspaket, das verwendet werden soll, wenn die Hardwarestation bereitgestellt wird.

4.  Wiederholen Sie die Schritte 2 und 3 für jede weitere Hardwarestation, die im Shop erforderlich ist.
5.  ** Sie Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitplan **.
6.  Wählen Sie den Verteilungszeitplan ** ** 1090 aus, um das neue Hardwareprofil dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
7.  Wählen Sie den Verteilungszeitplan ** ** 1040 aus, um die neue Hardwarestation dorthin synchronisieren. ** Auf Ausführung nun ** um die Änderungen am POS zu synchronisieren.
8.  Richten Sie die Hardwarestation auf jedem Hostcomputer, den Sie in Schritt 2. und 3 eingerichtet. Weitere Informationen dazu, wie die Hardwarestation, finden Sie unter Kleinhardwarestationskonfiguration Installation und [] (retail-hardware-station-configuration-installation.md).
9.  Installieren und aktivieren Sie modernes POS. Weitere Informationen dazu, wie modernes POS, finden Sie unter POS-KleinKonfiguration moderne und Installation [] (retail-modern-pos-device-activation.md).
10. Melden Sie sich bei modernem POS, und wählen Sie aus ** führen Sie NichtKassenladearbeitsgänge ** aus.
11. Starten Sie den Hardwarestationen ** verwalten ** Arbeitsgang.

12. ** ** Verwalten Sie auf.
13. Auf der Hardwarestationsverwaltungsseite legen Sie die Option fest, die Hardwarestation zu aktivieren.
14. Wählen Sie die Hardwarestation aus, der verwendet werden soll, und klicken Sie dann Paare ** **.
15. Wiederholen Sie Schritt 14 für jede Hardwarestation, die modernes POS verwendet.
16. Zum Abschluss werden die erforderlichen Hardwarestationen, auf zugeordnet ** ** Schließen.
17. Auf der Hardwaresenderauswahlseite klicken Sie auf die Hardwarestation vor kurzem ausgewählte, um diese zu aktivieren. ** Hinweis: ** Wenn Geräte oft unterschiedliche Hardwarestationen verwenden, empfiehlt es sich, modernes POS konfigurieren, um für Kassierer Informationen anzuzeigen, eine Hardwarestation auszuwählen, wenn sie den Zahlungsmittelprozess starten. ** Sie Einzelhandel und Handel ** &gt; ** Kanal eingerichtet ** &gt; ** POS eingerichtet ** &gt; ** Register **. Wählen Sie das Register aus, und legen Sie dann die Zahlungsmittel nach ** wählen Sie aus ** Option fest ** Ja **. Verwenden Sie den Verteilungszeitplan ** ** 1090, um Änderungen an der Kanaldatenbank zu synchronisieren.

## <a name="extensibility"></a>Erweiterbarkeit
Informationen zum Erweiterbarkeitsszenarien für die Hardwarestation, finden Sie Hardware-Stationserweiterbarkeit [](Entwickler-itpro/ hardware-station-extensibility.md).

## <a name="security"></a>Sicherheit
Entsprechend aktuellen Sicherheitsstandards sollten die folgenden Einstellungen in einer Produktionsumgebung verwendet werden: ** Hinweis: ** Das Hardwarestationsinstallationsprogramm nimmt automatisch, an dem diese, bearbeitet Registrierung als Teil der - Installation nach Self-Service.

-   Secure Sockets Layer (SSL) sollte deaktiviert werden.
-   Nur Transport Layer Security (TLS)- Version 1,2 (oder höchste die aktuelle Version) aktiviert werden sollen und verwendet werden. ** Hinweis: ** Standardmäßig SSL werden, und alle TLS außer der Version 1,2 TLS deaktiviert. Wenn diese Werte zu bearbeiten oder zu aktivieren, gehen Sie folgendermaßen vor:
    1.  Drücken Sie key+R, das Windows-Logo einen zu öffnen ** Ausführung ** Fenster.
    2.  Wählen Sie im ** offen ** Feld geben Sie Regedit ** ** ein, und klicken Sie anschließend auf OK ** **.
    3.  Ist Benutzerkontensteuerung ** ** Meldungsfeld angezeigt wird, klicken Sie auf Ja ** **.
    4.  Im Registrierungs-Editor ** ** Fenster navigieren Sie LOKALE VARIABLE **\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols\_HKEY **. Die folgenden Konfigurationsschlüssel werden automatisch eingegeben wurden, um TLS 1,2 nur erstellt:
        -   TLS 1.2Server: Enabled=1
        -   TLS 1.2Server: DisabledByDefault=0
        -   TLS 1.2Client: Enabled=1
        -   TLS 1.2Client: DisabledByDefault=0
        -   TLS 1.1Server: Enabled=0
        -   TLS 1.1Client: Enabled=0
        -   TLS 1.0Server: Enabled=0
        -   TLS 1.0Client: Enabled=0
        -   SSL 3.0Server: Enabled=0
        -   SSL 3.0Client: Enabled=0
        -   SSL 2.0Server: Enabled=0
        -   SSL 2.0Client: Enabled=0
-   Keine zusätzlichen Netzwerkporte sollen offen sein, es sei denn, sie ist für dieses bekannt sind obligatorisch, angegebene Gründe.
-   Kreuz-Ursprungsressourcenfreigabe muss deaktiviert werden und muss den zulässigen Ursprüngen angeben, die akzeptiert werden.
-   Nur Zertifizierungsstellen vertrauenswürdige verwendet werden sollen, die Bescheinigungen verschaffen, die auf Computern verwendet werden, die Hardwarestation ausführen.

** Hinweis: ** Es ist außerordentlich wichtig, dass Sie die IIS und Sicherheitsrichtlinien für Zahlungs-Karten-Industrie (PCI)- Anforderungen prüfen.

## <a name="peripheral-simulator"></a>Peripheriesimulator
Weitere Informationen finden Sie Kleinzusatzsimulator [] (retail-peripheral-simulator.md ).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested Peripheriegeräte
### <a name="ipc-built-in-hardware-station"></a>Hardwarestation IPK (Einbauten)

Die folgenden Peripheriegeräte getestet wurden, indem die IPC-Hardwarestation verwendete, die in modernes POS für Windows erstellt wird.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | Um      |                         |
| Epson        | TM-T88V  | Um      |                         |
| Stern         | TSP650II | Um      |                         |
| Stern         | TSP650II | Benutzerdefiniert    | Angeschlossen Netzwerk zu   |
| Stern         | mPOP     | Um      | Angeschlossen zu Bluetooth |
| HP           | F7M67AA  | Um      | Betriebenes USB             |

#### <a name="bar-code-scanner"></a>Strichcodescanner

| Hersteller  | Modell         | Schnittstelle | Kommentare |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | Um      |          |
| Honeywell     | 1900          | UWP       |          |
| <b>Symbol</b>        | LS2208        | Um      |          |
| HP integrierte | E1L07AA       | Um      |          |
| Datalogic     | Magellan 8400 | Um      |          |

#### <a name="pin-pad"></a>PIN-Feld

| Hersteller | Modell  | Schnittstelle | Kommentare                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | Um      | Erfordert Anpassung des Zahlungskonnektors |

#### <a name="payment-terminal"></a>Zahlungsterminal 

| Hersteller | Modell | Schnittstelle | Kommentare                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors                                |
| VeriFone     | MX925 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |
| VeriFone     | MX915 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare                |
|--------------|-----------|-----------|-------------------------|
| Stern         | mPOP      | Um      | Angeschlossen zu Bluetooth |
| APG          | Atwood    | Benutzerdefiniert    | Angeschlossen Netzwerk zu   |
| Stern         | SMD2-1317 | Um      |                         |
| HP           | QT457AA   | Um      |                         |

#### <a name="line-display"></a>Zeilenanzeige

| Hersteller  | Modell   | Schnittstelle | Kommentare |
|---------------|---------|-----------|----------|
| HP integrierte | G6U79AA | Um      |          |
| Epson         | M58DC   | Um      |          |

#### <a name="signature-capture"></a>Signaturerfassung

| Hersteller | Modell  | Schnittstelle | Kommentare |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | Um      |          |

#### <a name="scale"></a>Skalieren

| Hersteller | Modell         | Schnittstelle | Kommentare |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | Um      |          |

#### <a name="msr"></a>MSR

| Hersteller | Modell       | Schnittstelle | Kommentare |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | Um      |          |
| HP           | IDRA-334133 | Um      |          |

### <a name="dedicated-iis-hardware-station"></a>Dedizierte IIS-Hardwarestation

Die folgenden Peripheriegeräte getestet, wurden, indem eine dedizierte (nicht freigegebenen) IIS-Hardwarestation zusammen mit modernem POS für Windows werden und bewölken POS.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | Um      |                           |
| Epson        | TM-T88V  | Um      |                           |
| Stern         | TSP650II | Um      |                           |
| Stern         | TSP650II | Benutzerdefiniert    | Angeschlossen Netzwerk zu     |
| Stern         | TSP100   | Um      | Erfordert TSP650II-Fahrer |
| HP           | F7M67AA  | Um      | Betriebenes USB               |

#### <a name="bar-code-scanner"></a>Strichcodescanner

| Hersteller  | Modell   | Schnittstelle | Kommentare |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | Um      |          |
| <b>Symbol</b>        | LS2208  | Um      |          |
| HP integrierte | E1L07AA | Um      |          |

#### <a name="pin-pad"></a>PIN-Feld

| Hersteller | Modell  | Schnittstelle | Kommentare                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | Um      | Erfordert Anpassung des Zahlungskonnektors |

#### <a name="payment-terminal"></a>Zahlungsterminal 

| Hersteller | Modell | Schnittstelle | Kommentare                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors                                |
| VeriFone     | MX925 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |
| VeriFone     | MX915 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Benutzerdefiniert    | Angeschlossen Netzwerk zu |
| Stern         | SMD2-1317 | Um      |                       |
| HP           | QT457AA   | Um      |                       |

#### <a name="line-display"></a>Zeilenanzeige

| Hersteller  | Modell   | Schnittstelle | Kommentare |
|---------------|---------|-----------|----------|
| HP integrierte | G6U79AA | Um      |          |
| Epson         | M58DC   | Um      |          |

#### <a name="signature-capture"></a>Signaturerfassung

| Hersteller | Modell  | Schnittstelle | Kommentare |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | Um      |          |

#### <a name="scale"></a>Skalieren

| Hersteller | Modell         | Schnittstelle | Kommentare |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | Um      |          |

#### <a name="msr"></a>MSR

| Hersteller | Modell       | Schnittstelle | Kommentare |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | Um      |          |
| HP           | IDRA-334133 | Um      |          |

### <a name="shared-iis-hardware-station"></a>Freigegebene IIS-Hardwarestation

Die folgenden Peripheriegeräte getestet, wurden, indem eine freigegebene IIS-Hardwarestation zusammen mit modernem POS für Windows werden und bewölken POS. ** Hinweis: ** Nur ein Drucker, ein Zahlungsterminal und eine Geldlade werden unterstützt.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | Um      |                           |
| Epson        | TM-T88V  | Um      |                           |
| Stern         | TSP650II | Um      |                           |
| Stern         | TSP650II | Benutzerdefiniert    | Angeschlossen Netzwerk zu     |
| Stern         | TSP100   | Um      | Erfordert TSP650II-Fahrer |
| HP           | F7M67AA  | Um      | Betriebenes USB               |

#### <a name="payment-terminal"></a>Zahlungsterminal 

| Hersteller | Modell | Schnittstelle | Kommentare                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |
| VeriFone     | MX915 | Benutzerdefiniert    | Erfordert Anpassung des Zahlungskonnektors; Netzwerk verbunden zu und USB |

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Benutzerdefiniert    | Angeschlossen Netzwerk zu |
| Stern         | SMD2-1317 | Um      |                       |
| HP           | QT457AA   | Um      |                       |

## <a name="troubleshooting"></a>Problembehandlung
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modernes POS können die Hardwarestation in seiner Liste zur Auswahl erkennen, die Angabe kann die Zuordnung nicht abschließen

** Lösung: ** Überprüfen Sie die nächste Liste möglicher Schwachstellen:

-   Der Computer, der manuell ist, modernes POS vertraut der Bescheinigung, die auf dem Computer verwendet wird, der die Hardwarestation ausführt.
    -   Wenn Sie diese Einstellung, in einem Webbrowser zu überprüfen, fahren der folgenden URL: https://Computer-&lt;Name&gt;:&lt;IP-Adresse&gt;/HardwareStation/Ping.
    -   Diese URL wird ein Ping, um sicherzustellen, dass der Computer zugegriffen werden kann, und der Browser gibt an, ob die Bescheinigung vertraut wird. (Wenn Sie z, in Internet Explorer, wird ein Schlosssymbol in die Adressenleiste verwenden. Wenn Sie auf dieses Symbol klicken, überprüft Internet Explorer, ob die Bescheinigung derzeit vertraut wird. Sie können das Zertifikat auf dem lokalen Computer, indem Sie die Details der Bescheinigung anzeigen, die angezeigt wird).
-   Auf dem Computer, der die Hardwarestation ausführt, ist der Anschluss, der von der Hardwarestation verwendet wird, an der Firewall geöffnet.
-   Die Hardwarestation wurde ordnungsgemäß Handelskontoinformationen durch das installierenshandelsinformationenstool eingerichtet, dem ausgeführten am Ende der Hardware Installationsprogramm stationieren.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modernes POS können die Hardwarestation in seiner Liste zur Auswahl nicht ermitteln

** Lösung: ** Jedes der folgenden Faktoren kann dieses Problem führen:

-   Die Hardwarestation ist nicht ordnungsgemäß in den Headquartern eingerichtet. Verwenden Sie die Schritte oben in diesem Thema aus, um zu überprüfen, dass das Hardwarestationsprofil und die Hardwarestation richtig eingegeben werden.
-   Die Einzelvorgänge sind, die nicht für Kanalkonfigurationen aktualisieren aktiviert. In diesem Fall können Sie den Einzelvorgang für Kanalkonfigurationen 1070.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modernes Point-of-Sale keine neuen Geldladeneinstellungen

** Lösung: ** Schließt die aktuelle Charge. Änderungen der Geldlade werden nicht in modernem POS aktualisiert, bis der aktuelle Stapel geschlossen wurde.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modernes POS Berichte ein Problem mit einem Kleinperipheriegerät

** Lösung: ** Nachfolgend sind einige typische Ursachen dieses Abgang:

-   Überprüfen Sie, ob andere Gerätetreiberkonfigurationsprogramme geschlossen werden. Wenn diese Hilfsprogramme offen sind, verhindern könnten sie möglicherweise modernes POS oder die Hardwarestation am Beanspruchen des Geräts.
-   Wenn das Kleinperipheriegerät mit mehreren POS-Geräten freigegeben ist, prüfen Sie, ob es bis eine der folgenden Kategorien gehören:
    -   Geldlade
    -   <b>Belegdrucker</b>
    -   Zahlungsterminal 

    Wenn das Peripheriegerät erst einer dieser Kategorien angehört, ist die Hardwarestation nicht so entworfen, dass das auf mehrere POS-Geräten freizugebenden Peripheriegerät zu aktivieren.
-   Manchmal können Gerätetreiber die Objekte (CCOs) veranlassen der gemeinsamen Regelung einwandfrei, die Arbeit einzustellen. Wenn ein Gerät vor kurzem eingerichtet wurde, jedoch nicht ordnungsgemäß funktioniert, oder Sie wegen anderer Probleme erkennen, können Sie das Problem häufig auflösen, indem Sie das CCOs erneut installieren. Um das CCOs herunterzuladen, besuchen Sie < http://monroecs.com/oposccos_current.htm>.
-   Wenn Sie häufig Zusatzänderungen während der Prüfung oder der Problembehandlung vornehmen, müssen Sie möglicherweise IIS zurücksetzen, anstatt, in den Cache zu verwalten, zu aktualisieren. Wenn Sie IIS zurückzusetzen, führen Sie die folgenden Schritte aus:
    1.  ** Im Menü Start ** Typ ** CMD **.
    2.  In den Suchergebnissen klicken Rechtsklick ** Eingabeaufforderung ** und dann ausgeführt ** geworden als Administrator **.
    3.  Im ** Eingabeaufforderung ** Fenster drücken Typ ** /Restart und iisreset ** EINGABETASTE.
    4.  Nachdem IIS neu gestartet hat, starten Sie modernes POS neu.
-   Während Sie bei der Lösung häufiger Änderungen an den Peripheriegeräten vornehmen, wenn auch häufig den POS-Kunden starten und enden, darf der dllhost Prozess aus einer vorherigen POS-Sitzung die aktuelle Sitzung entstehen. In diesem Fall könnte ein Gerät nicht verwendbar, bis der Dynamic Link Library (DLL)- Host schließen, der die frühere Sitzung verwaltet. Um den DLL-Host zu schließen, die folgenden Schritte aus:
    1.  ** Im Menü Start ** Eingeben Task-Manager ** **.
    2.  In den Suchergebnissen klicken Sie Task-Manager ** **.
    3.  Im Task-Manager ** ** Details auf der Registerkarte, klicken Sie auf der Spaltenkopf, die ** Name wird als bezeichnet ** um die Tabelle zu sortieren alphabetisch nach Name.
    4.  Navigieren Sie nach unten, bis Sie dllhost.exe suchen.
    5.  Wählen Sie jeden DLL-Host aus, und klicken Sie dann Enden-Aufgabe ** **.
    6.  Nachdem die DLL-Hosts geschlossen wurden, starten Sie neu modernes POS.


<a name="see-also"></a>Siehe auch
--------

Kleinzusatzsimulator [] (retail-peripheral-simulator.md )


