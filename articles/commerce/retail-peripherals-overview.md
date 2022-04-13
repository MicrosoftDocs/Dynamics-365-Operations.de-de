---
title: Peripheriegeräte
description: In diesem Thema werden einige Konzepte in Verbindung mit Commerce-Peripheriegeräten beschrieben.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 76ce17777a2d13b46e5faed96dbde5e0d93782eb
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462240"
---
# <a name="peripherals"></a>Peripheriegeräte

[!include[banner](includes/banner.md)]

In diesem Thema werden die Konzepte erläutert, die sich auf Speicherperipheriegeräte beziehen. Es werden die verschiedenen Arten Peripheriegeräte beschrieben, die mit der Verkaufsstelle (POS) verbunden werden können und die Komponenten, die für das Verwalten der Verbindung mit dem POS zuständig sind.

## <a name="concepts"></a>Konzepte

### <a name="pos-registers"></a>POS-Register

Zur Navigation: Gehen Sie zu **Retail und Commerce \> Kanal Einrichtung \> POS Einrichtung \> Register**. Das POS-Register ist eine Entität, die verwendet wird, um die Merkmale einer bestimmten Instanz des POS zu definieren. Diese umfassen das Hardwareprofil bzw. die Einrichtung für Peripheriegeräte, die für das Register verwendet werden, die Filiale, der das Register zugeordnet ist, und die Sichterfahrung für den Benutzer, der sich an dem Register anmeldet.

### <a name="devices"></a>Geräte

Navigation: Gehen Sie zu **Einzelhandel und Commerce \> Einrichtung der Kanäle \> Einrichtung der Kassen \> Geräte**. Ein Gerät ist eine Entität, die eine physische Instanz eines Gerätes darstellt, das dem POS-Register zugeordnet ist. Wenn ein Gerät eingerichtet wird, wird es einem POS-Register zugeordnet. Die Geräteentität verfolgt Informationen darüber, ob ein POS-Register aktiviert ist, welcher Client verwendet wird und das Anwendungspaket, das für ein bestimmtes Gerät bereitgestellt wurde. 

Geräte können den folgenden Anwendungstypen zugeordnet werden: Retail Modern POS, Retail Cloud POS, Retail Modern POS - Android, und Retail Modern POS - iOS.

### <a name="modern-pos"></a>Modern POS

Modern POS ist das POS-Programm für Microsoft Windows. Es kann auf den Betriebssystemen Windows 10 und Windows 11 bereitgestellt werden.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS ist eine browserbasierte Version des Modern POS-Programms, das in einem Webbrowser zugegriffen werden kann.

### <a name="modern-pos-for-ios"></a>Modern POS für iOS

Modern POS für iOS ist eine iOS-basierte Version des Modern POS-Programms, das auf iOS-Geräten bereitgestellt werden kann.

### <a name="modern-pos-for-android"></a>Modern POS für Android

Modern POS für Android ist eine Android-basierte Version des Modern POS-Programms, das auf Android-Geräten bereitgestellt werden kann.

### <a name="pos-peripherals"></a>POS-Peripheriegeräte

POS-Peripheriegeräte sidn Geräte, die für POS-Funktionen explizit unterstützt werden. Diese Peripheriegeräte werden in der Regel in bestimmten Klassen aufgeteilt. Weitere Informationen über diese Klassen lesen Sie den Abschnitt "Geräteklasse" dieses Themas.

### <a name="hardware-station"></a>Hardwarestation

Zur Navigation: Gehen Sie zu **Einzelhandel und Commerce \> Kanäle \> Stores \> Alle Stores**. Wählen Sie einen Store und dann das Inforegister **Hardware-Stationen**. Die Einstellung **Hardware-Station** ist eine Einstellung auf Kanalebene, die zur Definition von Instanzen verwendet wird, in denen die Peripherielogik eingesetzt wird. Diese Einstellung auf der Kanalebene wird verwendet, um die Merkmale der Hardwarestation zu bestimmen. Sie wird außerdem zum Auflisten von Hardwarestationen verwendet, die für eine Modern POS-Instanz eine moderne in einem bestimmten Shop verfügbar sind. Die Hardwarestation ist in die Modern POS-Programme für Windows und Android integriert. Die Hardwarestation kann auch unabhängig bereitgestellt werden als ein eigenständiges Microsoft-Internetinformationsdienste-Programm (IIS). In diesem Fall können Sie über ein Netzwerk zugreifen.

### <a name="hardware-profile"></a>Hardwareprofil

Zur Navigation: Gehen Sie zu **Einzelhandel und Commerce \> Kanal Einrichtung \> POS Einrichtung \> POS Profile \> Hardware Profile**. Das Hardwareprofil identifiziert die Geräte, die für eine POS-Register oder einer Hardwarestation konfiguriert sind. Das Hardwareprofile kann direkt zu einer POS-Register oder einer Hardwarestation zugewiesen werden.

## <a name="devices-classes"></a>Geräteklassen
POS-Peripheriegeräte werden in der Regel in Klassen aufgeteilt. Dieser Abschnitt beschreibt und gibt einen Überblick der Geräte, die Modern POS unterstützt.

### <a name="printer"></a>Drucker

Drucker umfassen traditionelle POS-Bondrucker und ganzseiten Drucker. Drucker werden über Object Linking and Embedding for Retail POS (OPOS) und Microsoft Windows-Treiber-Schnittstellen unterstützt. Bis zu zwei Drucker können gleichzeitig verwendet werden. Diese Funktion unterstützt Szenarien, in denen die Barbelege von Kunden auf Bondruckern gedruckt werden, und in den Kundenaufträge, die mehr Informationen enthalten, über einen ganzseiten Drucker gedruckt werden. Bondrucker können direkt mit einem Computer per USB verbunden werden, per Ethernet über ein Netzwerk verbunden werden, oder per Bluetooth verbunden werden.

### <a name="scanner"></a>Scanner

Bis zu zwei Barcodescanner können gleichzeitig verwendet werden. Diese Funktion unterstützt Szenarien, in denen ein Scanner, der mobiler ist, erforderlich ist, um die sehr schwere Artikel zu scannen, oder ein fester eingebetteter Scanner für die meisten Standard-skalierten Artikel verwendet wird, um die Auscheckenzeiten zu beschleunigen. Scanner können über OPOS, Universal Windows Platform (UWP) oder Tastatur-Wedge-Schnittstellen unterstützt werden. USB oder Bluetooth können verwendet werden, um eine Scanner-Verbindung mit einem Computer herstellen.

### <a name="msr"></a>MSR

Ein USB-Magnetstreifenleser (MSR) kann über OPOS-Treiber eingerichtet werden. Wenn Sie ein eigenständiges MSR für Zahlungsbuchungen für elektronische Überweisungen verwenden möchten, muss einen MSR (Magnetstreifenleser) durch einen Zahlungskonnektor verwaltet werden. Ein eigenständiger MSR kann für einen Kundentreueeintrag, Mitarbeiteranmeldung und Geschenkkarteeintrag verwendet werden – unabhängig vom Zahlungskonnektor.

### <a name="cash-drawer"></a>Kassenlade

Zwei Kassenladen können pro Hardwareprofil unterstützt werden. Diese Funktion ermöglicht zwei aktive Schichten pro Register, die verfügbar ist gleichzeitig. Im Falle einer gemeinsamen Schicht oder einer Kassenlade, die durch mehrere Geräte des mobilen POS gleichzeitig verwendet wird, ist nur eine Kassenlade pro Hardwareprofil zulässig. Kassenladen können direkt mit einem Computer per USB verbunden werden, über ein Netzwerk verbunden werden, oder per RJ12-Schnittstelle mit einem Bondrucker verbunden werden. In einigen Fällen können Kassenladen auch per Bluetooth verbunden werden.

### <a name="line-display"></a>Zeilenanzeige

Zeilendisplays werden zur Anzeige von Produkten, Buchungssaldos und andere Informationen während einer Transaktion verwendet. Ein Zeilendisplay kann an den Computer per USB über OPOS-Treiber verbunden werden.

### <a name="signature-capture"></a>Signaturerfassung

Unterschriftenaufnahmegeräte können direkt mit einem Computer per USB über den OPOS-Treiber verbunden verwendet. Wenn die Unterschriftaufnahme konfiguriert ist, wird der Kunde aufgefordert, um über das Gerät zu unterschreiben. Nachdem die Unterschrift bereitgestellt wird, wird sie dem Kassierer zur Abnahme dargestellt.

### <a name="scale"></a>Waage

Eine Waage kann an den Computer per USB über OPOS-Treiber verbunden werden. Wenn ein Produkt, das als "gewogenes Produkt" markiert wird, einer Buchung hinzugefügt wird, erfasst das POS das Gewicht von der Waage, fügt das Produkt der Buchung hinzu und verwendet die Menge der Waage.

### <a name="pin-pad"></a>PIN-Feld

Geheimzahl (PIN)-Pads werden über OPOS unterstützt, müssen aber zu über ein Zahlungskonnektor verwaltet werden.

### <a name="secondary-display"></a>Sekundäre Anzeige

Wenn eine sekundäre Anzeige wird konfiguriert, wird die zweite Windows-Anzeige verwendet, um grundlegende Informationen anzuzeigen. Die sekundäre Anzeige ist standardmäßig nicht konfigurierbar und zeigt nur begrenzte Inhalte an. Der Zweck der sekundären Anzeige ist die Unterstützung einer unabhängigen Softwareanbieter-Erweiterung (ISV). 

### <a name="payment-device"></a>Zahlungsgerät

Der Zahlungsgerätensupport wird durch den Zahlungskonnektor implementiert. Zahlungsgeräte können eine oder mehrere der Funktionen ausführen, die über andere Einheitenklassen bereitgestellt werden. So kann ein Zahlungsgerät als MSR-/Kartenleser, Zeilendisplay, oder Gerät für elektronische Unterschriften oder PIN-Pad arbeiten. Unterstützung für Zahlungsgeräte wird unabhängig des eigenständigen Gerätensupports implementiert, der für andere Geräte zulässig ist, die im Hardwareprofil enthalten sind.

## <a name="supported-interfaces"></a>Unterstützte Schnittstellen
### <a name="opos"></a>OPOS

Um zu gewährleisten, dass die größte Bandbreite an Geräten mit Commerce verwendet werden kann, ist der Industriestandard OLE für POS die primäre unterstützte Peripheriegeräteplattform. Der OLE for POS-Standard wurde von der National Retail Federation (NRF) erstellt, die Industriestandard-Kommunikationsprotokolle für Peripheriegeräte festlegt. OPOS ist eine weithin anerkannte Implementierung des OLE für POS-Standards. Es wurde Mitte der 1990er entwickeltes und wurde mehrmals und aktualisiert. OPOS enthält eine Gerätetreiberarchitektur, die eine einfache Integration von POS-Hardware mit Windows-basierten POS-Systemen ermöglicht. OPOS steuert die Kommunikation zwischen kompatibler Hardware und der POS-Software. Ein OPOS-Steuerelement besteht aus zwei Teilen:

-   **Steuerelementobjekt** – Das Steuerelementobjekt für eine Einheitenklasse (z.B. Gerätenamen) stellt die Schnittstelle zum Softwareprogramm bereit. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) bietet einen Satz OPOS-Steuerobjekte, die Common Control Objects (CCOs) heißen. Mit den CCOs wird die POS-Komponente von Commerce getestet. Wenn Commerce eine Geräteklasse über OPOS unterstützt, wird mit den Tests sichergestellt, dass viele Gerätetypen unterstützt werden, vorausgesetzt, dass der Hersteller ein Serviceobjekt bereitstellt, das für OPOS entwickelt wurde. Sie müssen jeden Einheitentyp nicht explizit testen.
-   **Serviceobjekt** – Das Serviceobjekt bietet die Kommunikation zwischen dem Steuerobjekt (CCO) und dem Gerät. Normalerweise wird das Serviceobjekt für ein Gerät von dem Gerätenhersteller bereitgestellt. Jedoch in bestimmten Fällen müssen Sie möglicherweise das Serviceobjekt von der Website des Herstellers herunterladen. Beispielsweise kann ein neueres Serviceobjekt verfügbar sein. Um die Adresse der Website des Herstellers suchen, prüfen Sie die Hardwaredokumentation.

[![Steuerobjekt und -Serviceobjekt.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Steuerobjekt- und Serviceobjekt-Unterstützung für die OPOS-Implementierung von Datenbanken für POS stellen sicher, dass die Gerätenhersteller und POS-Herausgeber der Standardspeicherposition ordnungsgemäß implementieren, und POS-Systemen unterstützte Geräte zusammenarbeiten können, wenn sie zuvor nicht zusammen getestet wurden. 

> [!NOTE]
> OPOS-Support wird sichergestellt für alle Geräte, die OPOS-Treiber haben. Der Handel muss diesen Gerätetyp bzw. diese Geräteklasse zunächst über OPOS unterstützen. Darüber hinaus können ggf. Serviceobjekte nicht unbedingt mit der aktuellen Version des CCOs auf dem aktuellen Stand befindet. Sie sollten sich bewusst sein, dass sich im Allgemeinen die Servicequalitätsobjekte unterscheidet.

### <a name="windows"></a>Windows

Bondruck am POS sind für OPOS optimiert. OPOS neigt zum schnelleren Drucken über Windows. Daher ist es eine gute Idee, OPOS zu verwenden, insbesondere in Umgebungen, in denen 40-Spalten-Belege gedruckt werden und die Transaktionszeiten schnell sein müssen. Für die meisten Geräte verwenden Sie OPOS-Steuerelemente. Allerdings unterstützen mehrere OPOS-Bondrucker auch Windows-Treiber. Mithilfe eines Windows-Treibers können Sie die neuesten Schriftarten und den Drucker im Netzwerk für mehrere Registern unterstützen. Allerdings besteht Nachteile bei der Verwendung von Windows-Treibern. Beispiele für Nachteile:

-   Wenn Windows-Treiber verwendet werden, werden Bilder gerendert bevor das Drucken auftritt. Daher neigt das Drucken dazu langsamer zu werden als bei Druckern mit OPOS-Steuerung.
-   Geräte, die mit dem Drucker verbunden sind ("Daisy-Chained") funktionieren möglicherweise nicht korrekt, wenn Windows-Treiber verwendet werden. Es kann z.B. sein, dass sich die Kassenschublade nicht öffnet oder dass der Quittungsdrucker nicht so funktioniert, wie Sie es erwarten.
-   OPOS unterstützt auch einen umfangreicheren Satz von Variablen, die spezifisch für Quittungsdrucker sind, wie z.B. das Ausschneiden von Papier oder das Drucken von Belegen.
-   Windows-Drucker werden nicht von der IIS-Hardwarestation unterstützt. 

Wenn OPOS-Steuerungen für Windows-Drucker verfügbar sind, sollte der Drucker trotzdem korrekt mit Commerce funktionieren.

### <a name="plug-and-play-devices"></a>Plug and Play-Geräte

Wenn ein Plug&Play-Gerät an eine Windows-Betriebssystemversion angeschlossen wird, die diesen Gerätetyp unterstützt, ist kein Treiber erforderlich, damit das Gerät wie vorgesehen verwendet werden kann. Wenn Windows beispielsweise ein Bluetooth-Lautsprechergerät erkennt, weiß das Betriebssystem, dass das Gerät den Klassentyp „Lautsprecher“ hat und behandelt dieses Gerät als Lautsprecher. Es sind keine zusätzlichen Einrichtung erforderlich. 

Im Falle von POS-Peripheriegeräten können viele USB-Geräte eingesteckt und vom Windows-Betriebssystem als Human Interface Devices (HIDs) erkannt werden. Es kann sein, dass Windows die Funktionalitäten, die das Gerät bietet, nicht ermitteln kann, da das Gerät die Klasse oder den Typ des Geräts nicht angibt. In Windows 10 sind Einheitenklassen für Strichcodescanner MSR und hinzugefügt. Wenn ein Gerät unter Windows 10 sich als Gerät aus einer der Klassen deklariert, hört Windows auf Ereignisse vom Gerät zu den entsprechenden Uhrzeiten.

Modern POS unterstützt UWP MSR und Scanner. Wenn Modern POS für die Eingabe von einem dieser Geräte bereit ist und ein Gerät, das zu einer der Geräteklassen gehört, angeschlossen ist, kann dieses Gerät verwendet werden. Wenn z.B. ein Plug&Play-Barcodescanner an einen Windows 10 Computer angeschlossen ist und die Barcode-Anmeldung für Modern POS konfiguriert ist, wird der Barcodescanner auf der Anmeldeseite aktiv. Es sind keine zusätzlichen Einrichtung erforderlich.

Zusätzliche Klassen von POS-Peripheriegeräten werden zu Windows hinzugefügt, wie z.B. Klassen für Kassenschubladen und Belegdrucker. Unterstützung für diese neuen Einheitenklassen für Modern POS ist aussteht.

### <a name="keyboard-wedge"></a>Tastaturweiche

Tastaturweichengeräte senden Daten auf den Computer, als ob diese Daten auf der Tastatur eingegeben wurden. Somit erhält standardmäßig das Feld, das am POS aktiv ist, die Daten, die eingelesen werden. In einigen Fällen kann dieses Verhalten zum falschen Typ der Daten führen, die in das falsche Feld gescannt werden. Beispielsweise könnte ein Strichcode in ein Feld eingefügt werden, das sich möglicherweise auf Kreditkartendaten bezieht. In vielen Fällen legt die Logik am POS fest, ob die gescannten Daten ein Strichcode oder ein Kartendaten sind. Daher werden die Daten korrekt bearbeitet. Wenn Geräte als Tastaturweichengeräte eingerichtet sind, gibt es mehr Kontrolle darüber, wie die Daten aus diesen Geräten genutzt werden können, da mehr zum Gerät "bekannt" ist. Beispielsweise werden Daten von einem Strichcodescanner automatisch als Strichcode erkannt, und der entsprechende Datensatz in der Datenbank ist einfach und schneller als, wenn eine generische Suche nach einer Zeichenfolge verwendet wurden, z.B. im Falle der Tastaturweichen.

> [!NOTE]
> Wenn am POS Keyboard-Wedge-Scanner verwendet werden, müssen sie so programmiert sein, dass sie einen Wagenrücklauf oder ein **Eingeben**-Ereignis nach dem zuletzt gescannten Zeichen senden. Wenn diese Konfiguration nicht vorgenommen wird, funktionieren Keyboard-Wedge-Scanner nicht ordnungsgemäß. Weitere Informationen zum Anfügen des Wagenrücklaufereignisses finden Sie in der Dokumentation Ihres Geräteherstellers.  

### <a name="device-printers"></a>Gerätedrucker

Drucker des Typs „Gerät“ können so konfiguriert werden, dass der Benutzer aufgefordert wird, einen Drucker auszuwählen, der für den Computer konfiguriert ist. Wenn ein Drucker vom Typ „Gerät“ konfiguriert ist und Modern POS auf einen Druckbefehl stößt, wird der Benutzer aufgefordert, einen Drucker aus einer Liste auszuwählen. Dieses Verhalten unterscheidet sich von dem Verhalten für Windows Fahrer, da der Druckertyp „Windows“ im Hardwareprofil dem Benutzer keine Liste von Druckern anzeigt. Stattdessen es erforderlich, dass ein benannter Drucker im **Gerätename** Feld angegeben wird.

### <a name="network"></a>Netzwerk

Netzwerk-Kassenladen, -Bondrucker und -Zahlungsterminals können über ein Netzwerk verwendet werden, entweder direkt über die Hardwarestation die prozessübergreifenden Kommunikationen (Interprocess Communications, IPK), der in die Modern POS für Windows-Anwendung integriert ist oder von der IIS-Hardwarestation für andere Modern POS-Clients erstellt wird.

## <a name="hardware-station-deployment-options"></a>Hardware Station-Bereitstellungsoptionen

### <a name="dedicated"></a>Dediziert

Moderne POS-Clients für Windows und Android umfassen **dedizierte** oder eingebaute Hardwarestationen. Diese Clients können mithilfe der in die Anwendungen integrierten Geschäftslogik direkt mit Peripheriegeräten kommunizieren. Die Android-Anwendung unterstützt nur Netzwerkgeräte. Weitere Informationen über die Unterstützung von Peripheriegeräten für die Android finden Sie im Artikel [POS-Hybridanwendung einrichten auf Android und iOS](./dev-itpro/hybridapp.md).

Um die dedizierte Hardwarestation zu verwenden, folgen Sie diesen Schritten.

1. Weisen Sie einer Kasse, die die Anwendung Modern POS for Windows oder Android verwenden wird, ein Hardwareprofil zu.
1. Erstellen Sie eine Hardwarestation vom Typ „Dedicated“ für den Store, in dem die Kasse verwendet werden soll. 
1. Öffnen Sie Modern POS im Nicht-Schubladenmodus und verwenden Sie den Vorgang **Hardware-Stationen verwalten**, um die Funktionalitäten der Hardware-Stationen zu aktivieren. Die dedizierte Hardwarestation ist standardmäßig aktiv. 
1. Melden Sie sich bei Modern POS ab. Melden Sie sich dann wieder an und öffnen Sie eine Schicht. Die Peripheriegeräte, die im Hardwareprofil konfiguriert sind, können nun verwendet werden. 

### <a name="shared"></a>Freigegeben

Manchmal auch als „IIS“-Hardware-Station bezeichnet, wobei „IIS“ bedeutet, dass die POS-Anwendung über Microsoft Internet Information Services mit der Hardware-Station verbunden ist. Die POS-Anwendung verbindet sich mit der IIS-Hardwarestation über Webdienste, die auf einem Computer ausgeführt werden, mit dem die Geräte verbunden werden. Wenn die gemeinsam genutzte Hardware-Station verwendet wird, können die Peripheriegeräte, die an eine Hardware-Station angeschlossen sind, von jeder POS-Kasse verwendet werden, die sich im selben Netzwerk wie die IIS-Hardware-Station befindet. Da nur Modern POS for Windows und Android eine integrierte Unterstützung für Peripheriegeräte enthalten, müssen alle anderen Modern POS-Anwendungen die IIS-Hardware-Station zur Kommunikation mit den im Hardwareprofil konfigurierten POS-Peripheriegeräten verwenden. Deshalb muss jede Instanz der IIS-Hardwarestation einen Computer haben, der den Webdienst und die Anwendung ausführen. 

Die gemeinsam genutzte Hardwarestation kann verwendet werden, um mehreren Point of Sale Clients die gemeinsame Nutzung von Peripheriegeräten zu erlauben oder um eine festgelegte Anzahl von Peripheriegeräten für einen einzelnen Point of Sale zu verwalten. 

Wenn eine Hardwarestation für die gemeinsame Nutzung von Peripheriegeräten zwischen mehreren POS-Clients genutzt wird, sollten nur Kassenladen, Belegdrucker und Zahlungsterminals verwendet werden. Sie können Strichcodescanner, MSRs, Zeilendisplays, Skalen oder andere Geräte nicht direkt verbinden. Andernfalls treten Konflikte auf, wenn mehrere POS-Geräte versuchen, Peripheriegeräte gleichzeitig zu beanspruchen. So werden Konflikte für unterstützt Geräte verwaltet:

-   **Kassenlade** – Die Kassenlade wird über ein Ereignis geöffnet, das dem Gerät gesendet wird. Es kann zu Problemen kommen, wenn eine Kassenschublade aufgerufen wird, während die Schublade bereits geöffnet ist. Eine Kassenschublade, die in einer gemeinsamen Hardware-Stationskonfiguration verwendet wird, sollte im Hardwareprofil auf **Gemeinsam** festgelegt werden. Diese Einstellung verhindert, dass der POS prüft, ob bereits die Kassenlade geöffnet ist, wenn sie offene Befehle übermittelt.
-   **Bondrucker** - Wenn zwei Bondruckerbefehle der Hardwarestation gleichzeitig gesendet werden, kann einer der Befehle, je nach Gerät, verloren gehen. Einige Geräte haben internen Speicherpool, der dieses Problem verhindern können. Wenn ein Druckbefehl nicht erfolgreich ist, erhält der Kassierer eine Fehlermeldung und kann den Druckbefehl vom POS erneut versuchen.
-   **Zahlungsterminal** – Wenn ein Kassierer eine Buchung an einem Zahlungsterminal versucht, das bereits verwendet wird, informiert eine Meldung den Kassierer, dass das Terminal verwendet wird und fordert den Kassierer, noch einmal später vorgenommen werden können. Normalerweise können Kassierer sehen, dass ein Terminal bereits verwendet wird und warten, bis die andere Buchung abgeschlossen ist, bevor sie Zahlungsmittel noch einmal ausgeführt.

Für eine zukünftige Version ist eine Prüfung geplant, um zu ermitteln, ob nicht unterstützte Geräte für ein Hardwareprofil eingerichtet sind, die auf eine freigegebene Hardwarestation zugeordnet ist. Werden nicht unterstützt Geräte erkannt werden, erhält der Benutzer einer Meldung, durch die angegeben wird, dass die freigegebene Hardwarestationen Geräte nicht unterstützt werden. Im Falle der freigegebenen Hardwarestationen ist die Option **Bei Angebot auswählen** auf Registernebene auf **Ja** festgelegt. Der POS-Benutzer wird aufgefordert, eine Hardwarestation auszuwählen, wenn ein Zahlungsmittel für eine Buchung am POS aktiviert ist. Wenn die Hardwarestation nur zum Zeitpunkt der Zahlungsmittel ausgewählt wird, wird die Hardwarestationsauswahl direkt an den POS-Workflow für mobile Szenarios hinzugefügt. Als zusätzliche Vorteil wird das Zeilendisplay im Feld Zahlungsterminal nicht für freigegebene Szenarien verwendet. Wenn das Zahlungsterminal als Zeilendisplay verwendet wird, können andere Benutzer für dieses Terminals gesperrt werden, bis die Buchung abgeschlossen ist. In mobilen Szenarien werden möglicherweise Positionen an einer Buchung für einen längeren Zeitraum hinzugefügt. Daher ist die Option **Bei Angebot wählen** obligatorisch, um eine optimale Gerätenverfügbarkeit sicherzustellen.

### <a name="network-peripherals"></a>Netzwerkperipheriegeräte

Die Netzwerkbezeichnung für Geräte im Hardwareprofil sorgt dafür, das Kassenladen, Bondrucker und Zahlungsterminals per Netzwerkverbindung verbunden werden können.

#### <a name="modern-pos-for-windows"></a>Modern POS für Windows

Sie können IP-Adressen für Netzwerkperipheriegeräte in zwei Stellen angeben. Wenn der Modern POS Windows-Client einen individuellen Satz Netzwerkperipheriegeräte verwendet, sollten Sie die IP-Adressen diese für Geräte festlegen, indem Sie die **IP-Konfiguration** Option im Aktivitätsbereich für die Register verwenden. Bei der Netzwerkgeräten, die unter POS-Registern freigegeben werden, kann ein Hardwareprofil, dem Netzwerkgeräte zugewiesen werden, direkt auf eine freigegebene Hardwarestation zugeordnet werden. Um IP-Adressen zuzuweisen, wählen Sie die Hardwarestation auf der Seite **Filialen** aus. Verwenden Sie dann die Option **IP-Konfiguration** im Abschnitt **Hardwarestationen**, um die Netzwerkgeräte anzugeben, die dieser Hardwarestation zugewiesen werden. Für Hardwarestationen, die nur Netzwerkgeräte haben, müssen Sie die Hardwarestation selbst nicht bereitstellen. In diesem Fall ist die Hardware-Station nur erforderlich, um netzwerkadressierbare Geräte konzeptionell nach ihrem Standort in der Filiale zu gruppieren.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS und Modern POS für iOS

Die Logik für physisch verbundene und über das Netzwerk-adressierbaren Peripheriegeräte ist in der Hardwarestation enthalten. Daher muss für alle POS-Clients außer Modern POS für Windows und Android eine IIS-Hardwarestation bereitgestellt und aktiv sein, damit der POS mit Peripheriegeräten kommunizieren kann, unabhängig davon, ob diese Peripheriegeräte physisch mit einer Hardwarestation verbunden sind oder die Kommunikation über das Netzwerk verläuft.

## <a name="setup-and-configuration"></a>Einrichtung und Konfiguration
### <a name="hardware-station-installation"></a>Installation der Hardwarestation

Eine Anleitung zur Installation einer IIS-Hardware-Station finden Sie unter [Hardware-Station konfigurieren und installieren](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS für Windows-Einstellung und -Konfiguration

Weitere Informationen finden Sie unter [Konfigurieren, Installieren und Aktivieren von Modern POS (MPOS)](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Modern POS für Android und iOS – Einrichtung und Konfiguration

Weitere Informationen finden Sie unter [POS-Hybridanwendung auf Android und iOS](./dev-itpro/hybridapp.md) einrichten.

### <a name="opos-device-setup-and-configuration"></a>OPOS-Geräte Einrichtung und Konfiguration

Weitere Informationen zu OPOS-Komponenten, finden Sie unter "Unterstützte Schnittstellen" dieses Dokuments. Normalerweise werden OPOS-Treiber vom Gerätenhersteller bereitgestellt. Wenn ein OPOS-Gerätetreiber eingerichtet wird, fügt er der Windows-Registrierung einem Schlüssel an einem der folgenden Orte hinzu:

-   **32-Bit-System:** HKEY\_LOCAL\_MACHINE\SOFTWARE\OLEforRetail\ServiceOPOS
-   **64-Bit-System:** HKEY\_LOCAL\_MACHINE\SOFTWARE\WOW6432Node\OLEforRetail\ServiceOPOS

Innerhalb des ServiceOPOS-Registrierungsspeicherortes werden konfigurierte Geräte entsprechend der OPOS-Einheitenklasse sortiert. Mehrere Gerätetreiber werden gespeichert.

## <a name="supported-scenarios-by-hardware-station-type"></a>Unterstützte Szenarien nach Hardwarestationstyp
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Client-Support - IPC-Hardwarestation vs. IIS-Hardwarestation

Die folgende Tabelle zeigt die Topologien und die Bereitstellungsszenarien an die, unterstützt werden.

| Kunde      | IPC-Hardwarestation | IIS-Hardwarestation |
|-------------|----------------------|----------------------|
| Windows-App | Ja                  | Ja                  |
| Cloud POS   | Nein                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nein                   | Ja                  |

### <a name="network-peripherals"></a>Netzwerkperipheriegeräte

Netzwerkperipheriegeräte können direkt über die Hardwarestation unterstützt werden, die in Modern POS für Windows- und Android-Anwendungen integriert ist. Bei allen anderen Clients müssen Sie eine IIS-Hardwarestation bereitstellen.

| Kunde      | IPC-Hardwarestation | IIS-Hardwarestation |
|-------------|----------------------|----------------------|
| Windows-App | Ja                  | Ja                  |
| Cloud POS   | Nein                   | Ja                  |
| Android     | Ja                  | Ja                  |
| iOS         | Nein                   | Ja                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Unterstützte Gerätetypen nach Hardwarestationstyp
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS für Windows mit einer IPC-Hardwarestation (integriert)

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
<li>OPOS</li>
<li>Windows-Treiber</li>
<li>Gerät</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-Treiber</li>
<li>Gerät</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zeilenanzeige</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Duale Anzeige</td>
<td>Windows-Treiber</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Keine Einstellung erforderlich)</li>
<li>Tastaturweiche (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Schublade</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk </br><strong>Hinweis:</strong> Es kann nur eine Kassenlade eingerichtet werden, wenn das <strong>Verwenden der freigegebenen Schicht</strong> für die Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Schublade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk </br><strong>Hinweis:</strong> Es kann nur eine Kassenlade eingerichtet werden, wenn das <strong>Verwenden der freigegebenen Schicht</strong> für die Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Scanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Keine Einstellung erforderlich)</li>
<li>Tastaturweiche (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Keine Einstellung erforderlich)</li>
<li>Tastaturweiche (keine Einstellung ist erforderlich.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skalieren</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-Feld</td>
<td>OPOS (Support wird mit Anpassung des Zahlungskonnektors bereigestellt).</td>
</tr>
<tr class="even">
<td>Signaturerfassung</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Zahlungsterminal</td>
<td><ul>
<li>Benutzerdefinierter Gerätensupport</li>
<li>Netzwerk (Weitere Informationen finden Sie in der Zahlungskonnektordokumentation).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-Clients mit festgeschriebener freigegebener IIS-Hardwarestation

> [!NOTE]
> Wenn die IIS-Hardware-Station „gebunden“ ist, besteht eine Eins-zu-Eins-Beziehung zwischen dem POS Client und der Hardware-Station.

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
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Positionsanzeige</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Schublade</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk </br><strong>Hinweis:</strong> Nur eine Kassenlade pro Hardwareprofil kann eingerichtet werden, wenn <strong>Verwenden der freigegebenen Schicht</strong> für die Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Schublade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Scanner</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Scanner 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Skalieren</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN-Feld</td>
<td>OPOS (Support wird mit Anpassung des Zahlungskonnektors bereigestellt).</td>
</tr>
<tr class="odd">
<td>Sig. erfassen</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Zahlungsterminal</td>
<td><ul>
<li>Benutzerdefinierter Gerätensupport</li>
<li>Netzwerk (Weitere Informationen finden Sie in der Zahlungskonnektordokumentation).</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Alle Modern POS Clients, die sich eine IIS-Hardware-Station teilen

> [!NOTE]
> Wenn die IIS-Hardwarestation "freigegeben" ist, können die Hardwarestation Geräte von mehreren gleichzeitig verwenden. Für dieses Szenario sollten Sie nur die Geräte verwenden, die in der weiter unten dargestellten Tabelle. Wenn Sie versuchen Geräte freizugeben, die hier nicht aufgeführt sind, wie Strichcodescanner und MSR, treten Fehler auf, wenn mehrere Geräte versuchen, dasselbe Peripheriegerät zu beanspruchen. In der Zukunft wird eine solche Konfiguration explizit verhindert.

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
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="even">
<td>Drucker 2</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Schublade</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk </br><strong>Hinweis:</strong> Nur eine Kassenlade pro Hardwareprofil kann eingerichtet werden, wenn <strong>Verwenden der freigegebenen Schicht</strong> für die Kassenlade konfiguriert wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Schublade 2</td>
<td><ul>
<li>OPOS</li>
<li>Netzwerk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zahlungsterminal</td>
<td><ul>
<li>Benutzerdefinierter Gerätensupport</li>
<li>Netzwerk (Weitere Informationen finden Sie in der Zahlungskonnektordokumentation).</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfiguration für unterstützte Szenarien
Weitere Informationen zum Erstellen von Hardwareprofilen finden Sie unter [Peripheriegeräte an den Point of Sale (POS)](define-maintain-channel-clients-registers-hw-stations.md) anschließen. 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS für Windows mit einer IPC-Hardwarestation (integriert)

Diese Konfiguration ist die typischste Konfiguration für die traditionelle, feste POS-Registern. Für dieses Szenario werden die Hardwareprofilinformationen direkt der Register selbst zugeordnet. Die EFT-Terminalnummer soll auf die Register selbst festgelegt werden. Führen Sie zum Eirnichten dieser Konfiguration die folgenden Schritte durch.

1.  Erstellen eines Hardwareprofils, bei dem alle erforderlichen Peripheriegeräte konfiguriert werden.
2.  Ordnen Sie den dem Hardwareprofil POS-Registern zu.
3.  Erstellen Sie eine Hardware-Station vom Typ **Dediziert** für das Geschäft, in dem die POS-Kasse verwendet werden soll. Die Beschreibung ist optional. 

    > [!NOTE]
    > Sie müssen keine anderen Eigenschaften auf der Hardwarestation festlegen. Alle anderen Informationen, z.B. das Hardwareprofil, kommt von der Register selbst.

4.  Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
5.  Wählen Sie den Verteilungszeitplan **1090** aus, um das neue Hardwareprofil zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
6.  Wählen Sie den Verteilungszeitplan **1040** aus, um die neue Hardwarestation zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
7.  Installieren und aktivieren von Modern POS für Windows.
8.  Starten Sie Modern POS für Windows, und starten Sie die zugeordneten Peripheriegeräte zu verwenden.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS für Android mit einer IPC-Hardwarestation (integriert)

**Neu für 10.0.8** - Epson Netzwerkdrucker und Kassenschubladen, die mit diesen Druckern über An Hafen verbunden sind, werden jetzt von der App Modern POS für Android unterstützt. Einzelheiten finden Sie im Artikel [POS-Hybridanwendung einrichten auf Android und iOS](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Alle Modern POS-Clients mit festgeschriebener freigegebener IIS-Hardwarestation

Diese Konfiguration kann für alle Modern POS-Clients verwendet werden, die eine Hardwarestation hat, die ausschließlich durch eine POS-Register verwendet wird. Führen Sie zum Eirnichten dieser Konfiguration die folgenden Schritte durch.

1.  Erstellen eines Hardwareprofils, bei dem alle erforderlichen Peripheriegeräte konfiguriert werden.
2.  Erstellen Sie eine Hardware-Station vom Typ **Dediziert** für das Geschäft, in dem die POS-Kasse verwendet werden soll.
3.  Auf dedizierten Hardwarestationen legen Sie die folgenden Eigenschaften fest:
    -   **Hostname** – Der Name des Hostcomputers, wo die Hardwarestation ausgeführt wird. 
    
        > [!NOTE]
        > Cloud POS kann **localhost** für den lokalen Computer auflösen, um zu bestimmen, wo Cloud POS ausgeführt wird. Das Zertifikat für das koppeln von Cloud POS mit der Hardwarestation muss jedoch auch "Localhost" als Computernamen nutzen. Um Probleme zu vermeiden, sollten Sie eine Liste aller Instanzen jeder dedizierten Hardwarestation für den Shop führen. Für jede Hardwarestation sollte der Hostname der Computernamen sein, für den die Hardwarestation bereitgestellt wird.
    
    -   **Port** – Der Port, der verwendet wird, damit die Hardwarestation mit dem Modern POS-Client kommunizieren kann.
    -   **Hardwareprofil** – Wenn das Hardwareprofil nicht auf der Hardwarestation selbst angegeben ist, wird das Hardwareprofil, das der Register zugewiesen ist, verwendet.
    -   **EFT POS-Nummer** – Die EFT-Terminal-ID, das verwendet werden soll, wenn EFT-Autorisierungen übermittelt werden. Diese Kennung wird von der Kreditkartenverarbeitungsstelle bereitgestellt.
    -   **Paketname** – Das Hardwarestationspaket, das verwendet werden soll, wenn die Hardwarestation bereitgestellt wird.

4.  Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
5.  Wählen Sie den Verteilungszeitplan **1090** aus, um das neue Hardwareprofil zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
6.  Wählen Sie den Verteilungszeitplan **1040** aus, um die neue Hardwarestation zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
7.  Installation der Hardwarestation Weitere Informationen zur Installation der Hardware-Station finden Sie unter [Konfiguration und Installation der Retail-Hardware-Station](retail-hardware-station-configuration-installation.md).
8.  Installieren und aktivieren von Modern POS Weitere Informationen über die Installation von Modern POS finden Sie unter [Konfiguration, Installation und Aktivierung von Modern POS (MPOS)](retail-modern-pos-device-activation.md).
9.  Melden Sie sich bei Modern POS, und wählen Sie aus **Ausführen von Vorgängen ohne Kassenlade**.
10. Starten Sie den **Hardwarestationen verwalten** Arbeitsgang.
11. Wählen Sie **Verwalten** aus.
12. Auf der Hardwarestationsverwaltungsseite legen Sie die Option fest, um die Hardwarestation zu aktivieren.
13. Wählen Sie die zu verwendende Hardwarestation aus und wählen Sie dann **Paar**.
14. Nachdem die Hardware-Station gekoppelt wurde, wählen Sie **Schließen**.
15. Wählen Sie auf der Seite Auswahl der Hardwarestation die kürzlich ausgewählte Hardwarestation aus, um sie zu aktivieren.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Alle Modern POS-Clients, die eine freigegebene IIS-Hardwarestation haben

Diese Konfiguration kann für alle Modern POS-Clients verwendet werden, die die Hardwarestationen mit anderen Geräten teilen. Führen Sie zum Eirnichten dieser Konfiguration die folgenden Schritte durch.

1.  Erstellen eines Hardwareprofils, bei dem die erforderlichen Peripheriegeräte konfiguriert werden.
2.  Erstellen Sie eine Hardware-Station vom Typ **Shared** für das Geschäft, in dem die POS-Kasse verwendet werden soll.
3.  Auf freigegebenen Hardwarestationen legen Sie die folgenden Eigenschaften fest:
    -   **Hostname** – Der Name des Hostcomputers, wo die Hardwarestation ausgeführt wird.
    -   **Beschreibung** – Text, der die Erkennung der Hardwarestation unterstützt (z. B. **Rücklieferungen** oder **Vorne im Laden**).
    -   **Port** – Der Port, der verwendet wird, damit die Hardwarestation mit dem Modern POS-Client kommunizieren kann.
    -   **Hardwareprofil** – Für freigegebene Hardwarestationen, jede Hardwarestation soll ein Hardwareprofil eingerichtet haben. Hardwareprofile können unter Hardwarestationen freigegeben werden, jedoch müssen sie jeder Hardwarestation zugeordnet werden. Außerdem wird empfohlen, dass sie freigegebenen Schichten verwendet, wenn mehrere Geräte gleiche freigegebene Hardwarestation verwenden. Um eine gemeinsame Schicht festzulegen, gehen Sie auf **Einzelhandel und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Hardware-Profile**. Für jedes freigegebene Hardwareprofil wählen Sie die Kassenlade aus und legen Sie die **Schichtkassenlade** Option auf **Ja**.
    -   **EFT POS-Nummer** – Die EFT-Terminal-ID, das verwendet werden soll, wenn EFT-Autorisierungen übermittelt werden. Diese Kennung wird von der Kreditkartenverarbeitungsstelle bereitgestellt.
    -   **Paketname** – Das Hardwarestationspaket, das verwendet werden soll, wenn die Hardwarestation bereitgestellt wird.

4.  Wiederholen Sie die Schritte 2 und 3 für jede zweite Hardwarestation im Shop.
5.  Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
6.  Wählen Sie den Verteilungszeitplan **1090** aus, um das neue Hardwareprofil zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
7.  Wählen Sie den Verteilungszeitplan **1040** aus, um die neue Hardwarestation zu synchronisieren. Wählen Sie **Jetzt ausführen**, um Änderungen mit dem POS zu synchronisieren.
8.  Installieren Sie die Hardwarestation auf jedem Hostcomputer, den Sie in Schritt 2. und 3 eingerichtet haben. Weitere Informationen zur Installation der Hardware-Station finden Sie unter [Konfiguration und Installation der Retail-Hardware-Station](retail-hardware-station-configuration-installation.md).
9.  Installieren und aktivieren von Modern POS Weitere Informationen über die Installation von Modern POS finden Sie unter [Konfigurieren, Installieren und Aktivieren von Modern POS (MPOS)](retail-modern-pos-device-activation.md).
10. Melden Sie sich bei Modern POS, und wählen Sie aus **Ausführen von Vorgängen ohne Kassenlade**.
11. Starten Sie den **Hardwarestationen verwalten** Arbeitsgang.

12. Wählen Sie **Verwalten** aus.
13. Auf der Hardwarestationsverwaltungsseite legen Sie die Option fest, um die Hardwarestation zu aktivieren.
14. Wählen Sie die zu verwendende Hardwarestation aus und wählen Sie dann **Paar**.
15. Wiederholen Sie Schritt 14 für jede Hardwarestation, die Modern POS verwendet.
16. Nachdem alle erforderlichen Hardwarestationen gekoppelt sind, wählen Sie **Schließen**.
17. Wählen Sie auf der Seite Auswahl der Hardwarestation die kürzlich ausgewählte Hardwarestation aus, um sie zu aktivieren. 

> [!NOTE]
> Wenn Geräte oft unterschiedliche Hardwarestationen verwenden, empfiehlt es sich, Modern POS zu konfigurieren, um den Kassierer zur Auswahl einer Hardwarestation aufzufordern, wenn sie den Zahlungsmittelprozess starten. Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einstellungen \> Kassen**. Wählen Sie das Register aus, und legen Sie dann die Option **Bei Angebot auswählen** auf **Ja** fest. Verwenden Sie den Verteilungszeitplan **1090**, um Änderungen an der Kanaldatenbank zu synchronisieren.

## <a name="extensibility"></a>Erweiterbarkeit
Informationen zu Erweiterbarkeitsszenarien für die Hardwarestation finden Sie unter [Den POS mit einem neuen Hardwaregerät integrieren und Installationsprogramm für die Erweiterung generieren](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Sicherheit
Entsprechend aktuellen Sicherheitsstandards sollten die folgenden Einstellungen in einer Produktionsumgebung verwendet werden: 

### <a name="hardware-station-installer"></a>Hardware-Station-Installationsprogramm
Das Hardwarestationsinstallationsprogramm macht automatisch diese Eintragsanpassungen als Teil der Installation über Self-Service.

-   Secure Sockets Layer (SSL) sollte deaktiviert werden.
-   Nur Transport Layer Security (TLS)- Version 1.2 (oder die höchste aktuelle Version) sollte aktiviert und verwendet werden. 

### <a name="ssl-and-tls"></a>SSL und TLS
Standardmäßig sind SSL und alle Versionen von TLS außer TLS 1.2 deaktiviert. Um diese Werte zu bearbeiten oder zu aktivieren, gehen Sie folgendermaßen vor:
    1.  Drücken Sie Windows-Taste+R, um das **Ausführen** Fenster zu öffnen.
    2.  Geben Sie im Feld **Öffnen** **Bearbeiten** ein und wählen Sie anschließend **OK**.
    3.  Wenn ein Nachrichtenfeld **Benutzerkontensteuerung** erscheint, wählen Sie **Ja**.
    4.  Im **Registrierungs-Editor** Fenster navigieren Sie zu **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Die folgenden Konfigurationsschlüssel werden automatisch eingegeben, um nur TLS 1.2 zuzulassen:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Keine zusätzlichen Netzwerkporte sollen offen sein, es sei denn, sie ist für dieses bekannte obligatorische Gründe erforderlich.
-   Cross-Origin-Resource-Sharing muss deaktiviert werden und es müssen die zulässigen Ursprünge angeben werden.
-   Nur vertrauenswürdige Zertifizierungsstellen dürfen verwendet werden, um Zertifikate für Computern mit Hardwarestation zu erstellen.

> [!NOTE]
> Es ist außerordentlich wichtig die Sicherheitsrichtlinien für IIS und die PCI--Anforderungen zu lesen (Payment Card Industry).

## <a name="peripheral-simulator"></a>Peripheriesimulator
Weitere Informationen finden Sie unter [Peripheriesimulator für den Handel](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Von Microsoft getestete Peripheriegeräte
### <a name="ipc-built-in-hardware-station"></a>IPC-Hardwarestation (integriert)

Die folgenden Peripheriegeräte wurden getestet, indem die IPC-Hardwarestation verwendete wurde, die in Modern POS für Windows integriert ist.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB             |
| Star         | TSP650II | Angepasst    | Per Netzwerk verbunden   |
| Star         | mPOP     | OPOS      | Angeschlossen per Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Der Drucker Star TSP 100 wird für die integrierte Hardwarestation nicht unterstützt. Die integrierte Hardwarestation verwendet einen 64-Bit-Prozess, der nicht mit vorhandenen Star-TP-100-Treibern kompatibel ist. 

#### <a name="bar-code-scanner"></a>Strichcodescanner

| Hersteller  | Modell         | Schnittstelle | Kommentare |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Zahlungsterminals und PIN-Pads

Dynamics 365 Commerce bietet eine standardmäßige Lösung für die Integration mit Adyen für Zahlungsdienste. Der [Dynamics 365 Payment Connector für Adyen](dev-itpro/adyen-connector.md) verwendet die geräteunabhängige [Adyen Payment Terminal Application Programming Interface (API)](https://www.adyen.com/blog/introducing-the-terminal-api) und kann mit allen Zahlungsterminals interagieren, die diese API unterstützt. Eine vollständige Liste der unterstützten Zahlungsterminals finden Sie unter [Adyen POS Terminals](https://www.adyen.com/pos-payments/terminals).

Sie können auch andere Zahlungsanbieter mit Dynamics 365 Commerce verwenden, indem Sie einen angepassten Konnektor erstellen. Jedes vom Zahlungsanbieter unterstützte Terminal kann mit Dynamics 365 Commerce verwendet werden. Ebenso lässt Dynamics 365 Commerce jedes Integrationsmodell für Zahlungsgeräte zu, das vom Zahlungsanbieter unterstützt wird, wie z.B. lokale IP, Cloud API oder eine direkte Verbindung (z.B. über USB) mit dem POS. Weitere Informationen finden Sie unter [Erstellen Sie eine End-to-End-Zahlungsintegration für ein Zahlungsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Angeschlossen per Bluetooth |
| APG          | Atwood    | Benutzerdefiniert    | Per Netzwerk verbunden   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Benutzerdefiniert    | Über DK-Port mit dem Netzwerk verbundener Epson-Drucker |

#### <a name="line-display"></a>Positionsanzeige

| Hersteller | Modell    | Schnittstelle | Kommentare |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T-series | OPOS      |          |

#### <a name="signature-capture"></a>Signaturerfassung

| Hersteller | Modell  | Schnittstelle | Kommentare |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skalieren

| Hersteller | Modell         | Schnittstelle | Kommentare |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Hersteller | Modell       | Schnittstelle | Kommentare |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Deditzierte IIS-Hardwarestation

Die folgenden Peripheriegeräte wurden getestet, indem eine dedizierte (nicht freigegebenen) IIS-Hardwarestation zusammen mit Modern POS für Windows und Cloud POS verwendet wurde.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB             |
| Star         | TSP650II | Angepasst    | Per Netzwerk verbunden   |
| Star         | mPOP     | OPOS      | Angeschlossen per Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Strichcodescanner

| Hersteller  | Modell         | Schnittstelle | Kommentare |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Symbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Zahlungsterminals und PIN-Pads

Dynamics 365 Commerce bietet eine standardmäßige Lösung für die Integration mit Adyen für Zahlungsdienste. Der [Dynamics 365 Payment Connector für Adyen](dev-itpro/adyen-connector.md) verwendet die geräteunabhängige [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) und kann mit allen Zahlungsterminals interagieren, die diese API unterstützt. Eine vollständige Liste der unterstützten Zahlungsterminals finden Sie unter [Adyen POS Terminals](https://www.adyen.com/pos-payments/terminals).

Sie können auch andere Zahlungsanbieter mit Dynamics 365 Commerce verwenden, indem Sie einen angepassten Konnektor erstellen. Jedes vom Zahlungsanbieter unterstützte Terminal kann mit Dynamics 365 Commerce verwendet werden. Ebenso lässt Dynamics 365 Commerce jedes Integrationsmodell für Zahlungsgeräte zu, das vom Zahlungsanbieter unterstützt wird, wie z.B. lokale IP, Cloud API oder eine direkte Verbindung (z.B. über USB) mit dem POS. Weitere Informationen finden Sie unter [Erstellen Sie eine End-to-End-Zahlungsintegration für ein Zahlungsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Benutzerdefiniert    | Per Netzwerk verbunden |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Benutzerdefiniert    | Über DK-Port mit dem Netzwerk verbundener Epson-Drucker |

#### <a name="line-display"></a>Positionsanzeige

| Hersteller  | Modell   | Schnittstelle | Kommentare |
|---------------|---------|-----------|----------|
| HP Integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Signaturerfassung

| Hersteller | Modell  | Schnittstelle | Kommentare |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Skalieren

| Hersteller | Modell         | Schnittstelle | Kommentare |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Hersteller | Modell       | Schnittstelle | Kommentare |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Freigegebene IIS-Hardwarestation

Die folgenden Peripheriegeräte wurden getestet, indem eine freigegeben IIS-Hardwarestation zusammen mit Modern POS für Windows und Cloud POS verwendet wurde. 

> [!NOTE]
> Nur ein Drucker, ein Zahlungsterminal und eine Kassenlade werden unterstützt.

#### <a name="printer"></a>Drucker

| Hersteller | Modell    | Schnittstelle | Kommentare                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | USB             |
| Star         | mPOP     | OPOS      | Angeschlossen per Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Zahlungsterminal

Dynamics 365 Commerce bietet eine standardmäßige Lösung für die Integration mit Adyen für Zahlungsdienste. Der [Dynamics 365 Payment Connector für Adyen](dev-itpro/adyen-connector.md) verwendet die geräteunabhängige [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) und kann mit allen Zahlungsterminals interagieren, die diese API unterstützt. Eine vollständige Liste der unterstützten Zahlungsterminals finden Sie unter [Adyen POS Terminals](https://www.adyen.com/pos-payments/terminals).

Sie können auch andere Zahlungsanbieter mit Dynamics 365 Commerce verwenden, indem Sie einen angepassten Konnektor erstellen. Jedes vom Zahlungsanbieter unterstützte Terminal kann mit Dynamics 365 Commerce verwendet werden. Ebenso lässt Dynamics 365 Commerce jedes Integrationsmodell für Zahlungsgeräte zu, das vom Zahlungsanbieter unterstützt wird, wie z.B. lokale IP, Cloud API oder eine direkte Verbindung (z.B. über USB) mit dem POS. Weitere Informationen finden Sie unter [Erstellen Sie eine End-to-End-Zahlungsintegration für ein Zahlungsterminal](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Geldlade

| Hersteller | Modell     | Schnittstelle | Kommentare              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Benutzerdefiniert    | Per Netzwerk verbunden |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Benutzerdefiniert    | Über DK-Port mit dem Netzwerk verbundener Epson-Drucker |


## <a name="troubleshooting"></a>Problembehandlung
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kann die Hardwarestation in seiner Liste zur Auswahl erkennen, kann aber nicht die Koppelung abschließen

**Lösung**: Überprüfen Sie die folgende Liste möglicher Schwachstellen:

-   Der Computer, der Modern POS ausführt, vertraut dem Zertifikat, das auf dem Computer verwendet wird, der die Hardwarestation ausführt.
    -   Um diese Einrichtung in einem Webbrowser zu überprüfen, rufen Sie die folgende URL auf: https://&lt;Computername&gt;:&lt;Portnummer&gt;/Hardwarestation/ping.
    -   Diese URL nutzt ein Ping, um sicherzustellen, dass auf den Computer zugegriffen werden kann, und der Browser gibt an, ob dem Zertifikat vertraut wird. (Bei Internet Explorer erscheint zum Beispiel ein Schloss-Symbol in der Adressleiste. Wenn Sie dieses Symbol auswählen, prüft Internet Explorer, ob das Zertifikat derzeit vertrauenswürdig ist. Sie können das Zertifikat auf dem lokalen Computer installieren, indem Sie die Details des Zertifikats anzeigen).
-   Auf dem Computer, der die Hardwarestation ausführt, ist der Port, der von der Hardwarestation verwendet wird, in der Firewall geöffnet.
-   Die Hardwarestation hat ordnungsgemäß installierte Handelskontoinformationen über das Handelsinformations-Installationstool, das zum Ende der Installationsprogramms für die Hardwarestation ausgeführt wird.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS kann die Hardwarestation in seiner Liste für die Auswahl nicht ermitteln

**Lösung**: Jeder der folgenden Faktoren kann dieses Problem führen:

-   Die Hardwarestation ist in der Zentrale nicht korrekt festgelegt worden. Weitere Informationen finden Sie unter [Konfigurieren und Installieren einer Retail Hardware Station](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Die Jobs für die Aktualisierung der Kanalkonfigurationen wurden nicht ausgeführt. In diesem Fall können Sie den Einzelvorgang für Kanalkonfigurationen 1070 aus.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS zeigt neuen Kassenladeneinstellungen nicht an

**Lösung:** Schließt den aktuellen Stapel. Änderungen der Kassenlade werden nicht in Modern POS aktualisiert, bis der aktuelle Stapel geschlossen wurde.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS zeigt ein Problem mit einem Peripheriegerät an

**Lösung:** Nachfolgend sind einige typische Ursachen dieses Problems:

-   Überprüfen Sie, ob andere Gerätetreiberkonfigurationsprogramme geschlossen sind. Wenn diese Hilfsprogramme offen sind, verhindern könnten sie möglicherweise, das Modern POS oder die Hardwarestation das Gerät nutzen kann.
-   Wenn das Peripheriegerät von mehreren POS-Geräten gemeinsam genutzt wird, stellen Sie sicher, dass es zu einer der folgenden Kategorien gehört:
    -   Kassenlade
    -   Belegdrucker
    -   Zahlungsterminal

    Wenn das Peripheriegerät nicht einer dieser Kategorien angehört, ist die Hardwarestation nicht so entworfen, dass die Peripherie auf mehrere POS-Geräten genutzt werden kann.
-   Manchmal können Gerätetreiber die CCOs (Common Control Objects) veranlassen, die Arbeit einzustellen. Wenn ein Gerät vor kurzem eingerichtet wurde, jedoch nicht ordnungsgemäß funktioniert, oder Sie anderer Probleme erkennen, können Sie das Problem häufig auflösen, indem Sie die CCOs erneut installieren. Um die CCOs herunterzuladen, besuchen Sie <http://monroecs.com/oposccos_current.htm>.
-   Wenn Sie häufig Peripheriänderungen während Prüfungen oder der Problembehandlung vornehmen, müssen Sie möglicherweise IIS zurücksetzen, anstatt auf die Aktualisierung des Cache von selbst zu warten. Gehen Sie hierzu folgendermaßen vor:
    1.  Im Menü **Start** geben Sie **CMD** ein.
    2.  Klicken Sie in den Suchergebnissen mit der rechten Maustaste auf **Befehlszeile** und wählen Sie dann **Als Administrator ausführen**.
    3.  Geben Sie Im **Eingabeaufforderung** Fenster **iisreset /Restart** ein und drücken Sie Eingabe.
    4.  Nachdem IIS neu gestartet hat, starten Sie Modern POS neu.
-   Während Sie häufiger Änderungen an den Peripheriegeräten vornehmen, oder häufig den POS-Clients starten und beenden, kann der dllhost Prozess aus einer vorherigen POS-Sitzung die aktuelle Sitzung stören. In diesem Fall könnte Geräte nicht verwendbar sein, bis der Dynamic Link Library (DLL)- Host der früheren Sitzung geschlossen ist. Um den DDL-Host zu schließen, führen Sie folgende Schritte aus:
    1.  Im Menü **Start** geben Sie **Task-Manager** ein.
    2.  Wählen Sie in den Suchergebnissen **Aufgabenmanager**.
    3.  Wählen Sie im Manager auf der Registerkarte **Details** die Spaltenüberschrift mit der Bezeichnung **Name**, um die Tabelle alphabetisch nach Namen zu sortieren.
    4.  Navigieren Sie nach unten, bis Sie dllhost.exe finden.
    5.  Markieren Sie jeden DLL-Host und wählen Sie dann **Aufgabe beenden**.
    6.  Nachdem die DLL-Hosts geschlossen wurden, starten Sie neu Modern POS.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Peripheriesimulator für den Handel](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
