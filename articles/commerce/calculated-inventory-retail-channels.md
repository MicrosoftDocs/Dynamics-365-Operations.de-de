---
title: Lagerverfügbarkeit für Retail Channels berechnen
description: In diesem Thema wird beschrieben, wie ein Unternehmen Microsoft Dynamics 365 Commerce verwenden kann, um die geschätzte Verfügbarkeit von Produkten im Online- und Shop-Kanal anzuzeigen.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 1b1e0ea264dd74f6583d3b7fd3ecce551c73fbae
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674674"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Lagerverfügbarkeit für Retail Channels berechnen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Unternehmen Microsoft Dynamics 365 Commerce verwenden kann, um die geschätzte Verfügbarkeit von Produkten im Online- und Shop-Kanal anzuzeigen.

## <a name="accuracy-of-inventory-availability"></a>Genauigkeit der Bestandsverfügbarkeit

Commerce verwendet mehrere Server und Datenbanken, um Skalierbarkeit und Leistung zu gewährleisten. Daher ist es wichtig, dass Sie verstehen, dass die verfügbaren Bestandswerte, die über die Point of Sale (POS)-Anwendung, die E-Commerce-Bestandsverfügbarkeits-APIs (Application Programming Interfaces) und die Seiten für den Lagerbestand in der Commerce-Zentrale bereitgestellt werden, in Echtzeit möglicherweise nicht zu 100 Prozent genau sind. Wenn Transaktionen, die für Produkte im Online- oder Store-Kanal erstellt werden, noch nicht mit der Zentrale synchronisiert wurden, zeigen die Seiten mit dem Lagerbestand in der Zentrale möglicherweise keinen genauen Echtzeit-Bestandswert für diese Produkte an. Wenn Sie Ihre Firma dagegen so konfiguriert haben, dass Benutzer in der Zentrale oder in anderen integrierten Anwendungen Bestände aus einem Geschäft oder einem Lagerort verkaufen, empfangen, zurückgeben oder anderweitig anpassen können, verfügt der POS- oder Online-Kanal möglicherweise nicht über alle Informationen, die erforderlich sind, um genaue Echtzeitwerte für Artikel anzuzeigen.

Es ist wichtig zu verstehen, dass alle Daten zum Lagerbestand, die während des Vorgangs bereitgestellt werden, als Schätzwert gelten. Wenn Sie also versuchen, die Informationen zum Lagerbestand, die die Anwendung liefert, mit dem tatsächlichen physischen Bestand in den Regalen zu vergleichen, oder wenn Sie versuchen, die Lagerbestände, die in POS angezeigt werden, mit den Lagerbestandsdaten zu vergleichen, die Sie für denselben Lagerort in der Zentrale finden, können die Werte abweichen. Diese Differenz wird während des Betriebstages erwartet und sollte nicht als Problem betrachtet werden. Wenn Sie Daten prüfen und sicherstellen möchten, dass die in POS, APIs und der Zentrale angegebenen Werte mit den tatsächlichen physischen Einheiten übereinstimmen, die Sie in Ihrem Geschäft oder Lagerort vorfinden, ist der beste Zeitpunkt dafür, nachdem die Vorgänge in den Kanälen für den Tag beendet wurden und alle Transaktionen korrekt zwischen der Zentrale und den Kanälen synchronisiert wurden.

## <a name="channel-side-inventory-calculation"></a>Kanalseitige Bestandsberechnung

Die kanalseitige Bestandsberechnung ist ein Mechanismus, der die letzten bekannten kanalseitigen Bestandsdaten in der Commerce-Zentrale als Basis nimmt und dann zusätzliche Bestandsänderungen auf der Kanalseite berücksichtigt, die nicht in dieser Basis enthalten sind, um einen geschätzten Lagerbestand nahezu in Echtzeit zu berechnen. 

Die folgenden Bestandsänderungen werden derzeit in der kanalseitigen Bestandsberechnungslogik berücksichtigt:

- Bestand, der durch Cash-and-Carry-Bestellungen in der Filiale verkauft wurde
- Bestand, der durch Kundenbestellungen im Geschäft oder im Online-Kanal verkauft wurde
- Bestand zurück in die Filiale
- Erfüllter Bestand (entnehmen, verpacken, versenden) vom Lagerort der Filiale

Um die kanalseitige Bestandsberechnung zu verwenden, müssen Sie die Funktion **Optimierte Produktverfügbarkeitsberechnung** aktivieren.

Wenn sich Ihre Commerce-Umgebung in Version **10.0.8 bis 10.0.11** befindet, führen Sie die folgenden Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung zu **Retail und Commerce** \> **Gemeinsame Commerce-Parameter**.
1. Wählen Sie auf der Registerkarte **Bestand** im Feld **Produktverfügbarkeitsjob** die Option **Optimiertes Verfahren für Produktverfügbarkeitsjob verwenden** aus.

Wenn sich Ihre Commerce-Umgebung in Version **10.0.12 oder höher** befindet, führen Sie die folgenden Schritte aus.

1. Gehen Sie in der Commerce-Zentralverwaltung zu **Arbeitsbereiche \> Funktionsverwaltung** und aktivieren Sie die Funktion **Optimierte Produktverfügbarkeitsberechnung**.
1. Wenn Ihre Online- und Store-Kanäle dieselben Lagerorte für die Auftragserfüllung verwenden, müssen Sie auch die Funktion **Erweiterte kanalseitige E-Commerce-Bestandsberechnungslogik** aktivieren. Auf diese Weise berücksichtigt die kanalseitige Berechnungslogik die nicht gebuchten Transaktionen, die im Store-Kanal erstellt werden. (Bei diesen Transaktionen kann es sich um Abholungstransaktionen, Debitorenaufträge und Rücksendungen handeln.)
1. Führen Sie den Job **1070** (**Kanalkonfiguration**) aus.

Wenn Ihre Commerce-Umgebung von einer früheren Commerce-Version als 10.0.8 aktualisiert wurde, müssen Sie nach dem Aktivieren der Funktion **Optimierte Produktverfügbarkeitsberechnung** außerdem **Commerce-Planer initialisieren** ausführen, damit die Funktion wirksam wird. Um die Initialisierung auszuführen, gehen Sie zu **Retail und Commerce** \> **Zentralverwaltungseinrichtung** \> **Commerce-Planer**.

Um die kanalseitige Bestandsberechnung zu verwenden, muss als Voraussetzung eine periodische Momentaufnahme der Bestandsdaten aus der Zentrale, erstellt durch den Job **Produktverfügbarkeit**, an die Kanaldatenbanken gesendet werden. Die Momentaufnahme stellt die Informationen dar, die die Zentrale über die Verfügbarkeit des Bestands für eine bestimmte Kombination aus einem Produkt oder einer Produktvariante und einem Lagerort hat. Sie enthält nur die Bestandstransaktionen, die zum Zeitpunkt der Momentaufnahme in der Zentrale verarbeitet und gebucht wurden, und ist aufgrund der konstanten Verkaufsverarbeitung, die auf verteilten Servern stattfindet, in Echtzeit möglicherweise nicht zu 100 Prozent genau.

- Wenn der Bestand für ein Produkt in einer Filiale über einen Cash-and-Carry-Verkauf oder einen asynchronen Debitor-Auftrag in der POS-Anwendung verkauft wurde, hat die Zentrale nicht sofort Informationen über die zugehörige Transaktion zur Bestandsausgabe für diesen Verkauf. Die Zentrale verfügt erst dann über Informationen über den Bestand, der für diese Arten von Filialverkäufen verkauft wird, wenn der P-Job die zugehörige Transaktion aus der Kanaldatenbank der Filiale in die Zentrale hochlädt und die zugehörigen Verkaufsaufträge durch die Auszugsbuchung oder die Trickle-Feed-Buchungsprozesse erstellt werden. Der Prozess des Erstellens der Aufträge in der Zentrale erstellt die zugehörigen Transaktionen für den Bestand. 
- Bei Bestellungen über den E-Commerce-Kanal verfügt die Zentrale erst dann über Informationen zu den Bestandstransaktionen, wenn die Transaktionen über den P-Job an die Zentrale gesendet wurden und der Auftragssynchronisationsprozess abgeschlossen ist.

Um eine Momentaufnahme des Bestands in der Commerce-Zentrale zu machen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Produkte und Bestand \> Produktverfügbarkeit**.
1. Wählen Sie **OK**, um den Job **Produktverfügbarkeit** auszuführen. Sie können diesen Job auch so planen, dass er im Batch ausgeführt wird.

Nachdem der **Produktverfügbarkeit**-Job ausgeführt wurde, müssen die erfassten Daten in die Kanaldatenbanken übertragen werden, damit die neueste Momentaufnahme der Zentrale bei der kanalseitigen Berechnung des geschätzten Lagerbestands berücksichtigt werden kann.

So synchronisieren Sie Momentaufnahmen von der Zentrale mit Ihren Channel-Datenbanken.

1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
1. Führen Sie den Job **1130** (**Produktverfügbarkeit**) aus, um die Momentaufnahmen, die der Job **Produktverfügbarkeit** von der Zentrale erstellt hat, mit den Channel-Datenbanken zu synchronisieren.

## <a name="inventory-availability-apis-for-e-commerce"></a>Bestandsverfügbarkeit APIs für E-Commerce

Commerce bietet die folgenden APIs für E-Commerce-Szenarien, um die Bestandsverfügbarkeit eines Produkts abzufragen:

- **GetEstimatedAvailability** – Verwenden Sie diese API, um den Bestand für ein Produkt oder eine Produktvariante im Lagerort des Online-Kanals oder in Lagerorten abzufragen, die mit der Fulfillment-Gruppe des Online-Kanals verknüpft sind.
- **GetEstimatedProductWarehouseAvailability** – Verwenden Sie diese API, um den Bestand für ein Produkt oder eine Produktvariante aus einem bestimmten Lagerort abzufragen.

> [!NOTE]
> Diese APIs ersetzen die **GetProductAvailabilities** und **GetAvailableInventoryNearby** APIs in Commerce Version 10.0.7 und früher.

Beide APIs verwenden intern die kanalseitige Berechnungslogik und geben die geschätzte **physikalisch verfügbare** Menge, **gesamte verfügbare** Menge, **Maßeinheit (UoM)** und **Bestand** für das angefragte Produkt und Lagerort zurück. Die zurückgegebenen Werte können auf Ihrer E-Commerce-Site angezeigt werden, wenn Sie dies wünschen, oder sie können verwendet werden, um andere Geschäftslogiken auf Ihrer E-Commerce-Site auszulösen. Sie können z. B. den Kauf von Produkten verhindern, deren Bestand „nicht vorrätig“ ist.

Obwohl andere APIs, die in Commerce verfügbar sind, direkt zur Zentrale gehen können, um Lagerbestände für Produkte abzurufen, empfehlen wir nicht, diese in einer E-Commerce Umgebung zu verwenden, wegen möglicher Leistungsprobleme und der Auswirkungen, die diese häufigen Anfragen auf die Server Ihrer Zentrale haben können. Zusätzlich können die beiden oben genannten APIs mit der kanalseitigen Berechnung eine genauere Schätzung zur Verfügbarkeit eines Produkts liefern, indem sie die Transaktionen berücksichtigen, die in den der Zentrale noch nicht bekannten Kanälen erstellt wurden.

Um zu definieren, wie die Produktmenge in der API-Ausgabe zurückgegeben werden soll, führen Sie diese Schritte aus.

1. Gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**.
1. Wählen Sie die Registerkarte **Bestand** und legen Sie dann auf dem Inforegister **Bestandsverfügbarkeit APIs für E-Commerce** den Wert der Einstellung **Menge in API-Ausgabe** fest.
1. Führen Sie den Job **1070** (**Kanalkonfiguration**) aus, um die neueste Einstellung auf die Kanäle zu synchronisieren.

Die Einstellung **Quantität in API-Ausgabe** bietet drei Optionen:

- **Bestandsmenge zurückgeben** – Physisch verfügbare und insgesamt verfügbare Menge eines angeforderten Produkts werden in der API-Ausgabe zurückgegeben.
- **Rückgabe Bestandsmenge abzüglich Bestandspuffer** – Die in der API-Ausgabe zurückgegebene Menge wird durch Subtraktion des Bestandspufferwerts angepasst. Weitere Informationen über den Bestandspuffer finden Sie unter [Konfigurieren von Bestandspuffern und Bestandsebenen](inventory-buffers-levels.md).
- **Bestandsmenge nicht zurückgeben** – Nur der Bestand wird in der API-Ausgabe zurückgegeben. Weitere Informationen über Bestände finden Sie unter [Konfigurieren von Bestandspuffern und Beständen](inventory-buffers-levels.md).

Sie können den API-Parameter `QuantityUnitTypeValue` verwenden, um die Art der Einheit anzugeben, in der die APIs die Menge zurückgeben sollen. Dieser Parameter unterstützt die Optionen **Bestand Einheit** (Standard), **Kauf Einheit** und **Verkauf Einheit**. Die zurückgegebene Menge wird auf die definierte Genauigkeit der entsprechenden Maßeinheit (UOM) in der Zentrale gerundet.

Die **GetEstimatedAvailability** API bietet die folgenden Eingabeparameter, um verschiedene Abfrageszenarien zu unterstützen:

- `DefaultWarehouseOnly` – Verwenden Sie diesen Parameter, um den Bestand für ein Produkt am Standardlagerort des Online-Kanals abzufragen. 
- `FilterByChannelFulfillmentGroup` und `SearchArea` – Verwenden Sie diese beiden Parameter, um den Bestand für ein Produkt von allen Abholorten innerhalb eines bestimmten Suchbereichs abzufragen, basierend auf `longitude`, `latitude` und `radius`. 
- `FilterByChannelFulfillmentGroup` und `DeliveryModeTypeFilterValue` – Verwenden Sie diese beiden Parameter, um den Bestand für ein Produkt von bestimmten Lagerorten abzufragen, die mit der Erfüllungsgruppe eines Online-Kanals verknüpft und so konfiguriert sind, dass sie bestimmte Lieferarten unterstützen. Der Parameter `DeliveryModeTypeFilterValue` unterstützt die Optionen **Alle** (Standard), **Versand** und **Abholung**. In einem Szenario, in dem eine Online-Bestellung von mehreren Versandlagern aus erfüllt werden kann, können Sie diese beiden Parameter verwenden, um die Verfügbarkeit des Bestands eines Produkts in allen diesen Versandlagern abzufragen. Die API gibt in diesem Fall den Lagerbestand des Produkts und den Lagerbestand in jedem der Versandlager zurück, plus eine aggregierte Menge und einen aggregierten Bestand aus allen Versandlagern im Abfragebereich.
 
Die Commerce-Module „Buy Box“, „Store Selector“, „Wishlist“, „Cart“ und „Cart Symbol“ verwenden die oben genannten APIs und Parameter, um Nachrichten über den Bestand auf der E-Commerce-Website anzuzeigen. Commerce Site Builder bietet verschiedene Einstellungen für den Bestand, um das Verhalten beim Verkauf und Kauf festzulegen. Weitere Informationen finden Sie unter [Bestandeinstellungen anwenden](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>POS-Nachschlagefeld mit kanalseitiger Berechnung

In der Commerce-Version 10.0.9 und früher verwendete der Vorgang **Nachschlagefeld** in POS einen Echtzeit-Serviceaufruf an die Zentrale, um Bestandsinformationen für das ausgewählte Produkt sowohl für die aktuelle Filiale des Benutzers als auch für alle anderen Filialen abzurufen, die für die Erfüllungsgruppe als Teil der Kanalkonfiguration für die Filiale konfiguriert sind. In Commerce Version 10.0.10 und später können Sie Echtzeit-Serviceaufrufe an die Zentrale abschalten und stattdessen die kanalseitige Berechnung auf dem Commerce-Server verwenden, um den physisch verfügbaren Lagerbestand für die Filiale und alle anderen Lagerplätze zu ermitteln, die in der Fulfillment-Gruppe definiert sind. Diese kanalberechnete Bestandskonfiguration ist auch für Lagerplätze nützlich, an denen die Internetverbindung unzuverlässig ist, da Sie nicht online sein müssen, um Nachschlagefelder für den Bestand in der Zentrale zu erhalten.

Wenn die kanalseitige Berechnung richtig konfiguriert und verwaltet wird, kann sie eine zuverlässigere Schätzung des aktuellen Bestands im Lager liefern, da sie die Transaktionsdaten verwendet, die sich in der Datenbank des Commerce-Kanals befinden, über die die Zentrale aber möglicherweise noch keine Informationen hat. Wenn Sie z. B. den vorhandenen Echtzeit-Serviceaufruf für Nachschlagefelder im POS verwenden, hat die Zentrale wahrscheinlich noch keine Informationen über einen Cash-and-Carry-Verkauf, der gerade für ein Produkt stattgefunden hat. Daher wird der Wert des Lagerbestands, den die Zentrale für dieses Produkt zurückgibt, wahrscheinlich den tatsächlichen Lagerbestand der Filiale um eine Einheit übersteigen. Wenn Sie jedoch die kanalseitige Berechnung verwenden, kann der Mitnahmeverkauf in die Berechnung einbezogen und vom angezeigten Bestandswert abgezogen werden. Obwohl die Werte, die sowohl die kanalseitige Berechnung als auch der Echtzeit-Serviceabruf liefern, nur Schätzungen des aktuellen Bestands sind, ist der Wert, den die kanalseitige Berechnung liefert, für das aktuelle Geschäft viel wahrscheinlicher.

Um den Vorgang der POS-**Bestandssuche** in der Commerce-Zentralverwaltung zu konfigurieren, sodass Sie die kanalseitige Berechnungslogik und die Echtzeitserviceaufruf verwenden zu können, müssen Sie zuerst die Option **Optimierte Berechnung der Produktverfügbarkeit** über den Arbeitsbereich **Funktionsverwaltung** über die Commerce-Zentralverwaltung aktivieren und dann den folgenden Schritten folgen.

1. Gehen Sie zu **Einzelhandel und Handel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**.
1. Wählen Sie ein Funktionsprofil aus.
1. Auf der Registerkarte **Funktionen** Inforegister, im Abschnitt **Bestandsverfügbarkeitsberechnung**, ändern Sie den Wert von **Bestandsverfügbarkeitsberechnungsmodus** von **Echtzeitservice** auf **Kanal**. Standardmäßig verwenden alle Funktionsprofile Echtzeit-Serviceabrufe. Sie müssen den Wert dieses Feldes ändern, wenn Sie eine kanalseitige Berechnungslogik verwenden wollen. Jedes Einzelhandelsgeschäft, das mit dem ausgewählten Funktionsprofil verknüpft ist, ist von dieser Änderung betroffen.

Anschließend müssen Sie die Änderungen mit den Kanälen über den Prozess „Verteilungsplan“ in der Zentrale synchronisieren, indem Sie diese Schritte ausführen.

1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
1. Führen Sie den Job **1070** (**Kanalkonfiguration**) aus.

Nach Abschluss der Konfiguration verwenden die Informationen, die über den physisch verfügbaren Bestand bereitgestellt werden, keinen Echtzeit-Serviceabruf mehr, wenn ein Benutzer in der POS-Anwendung den Vorgang **Bestandssuche** verwendet (Standard- und Matrixansicht). Stattdessen werden die Daten über den physisch verfügbaren Bestand für die aktuelle Filiale und alle Filialen in der Erfüllungsgruppe auf der Grundlage des letzten bekannten Snapshots berechnet, der von Headquarters an die Kanaldatenbank geliefert wurde. Der Momentaufnahmewert wird durch die kanalseitige Berechnung weiter verfeinert, um den physisch verfügbaren Wert auf der Grundlage zusätzlicher Verkaufs- oder Retourentransaktionen anzupassen, die für das ausgewählte Produkt in der Kanaldatenbank vorhanden sind und die in der letzten synchronisierten Momentaufnahme aus dem Auftrag 1130 nicht enthalten waren. Wenn die Vertriebskanal-Datenbank keine Transaktionsdaten für eines der Lager oder Geschäfte in der Erfüllungsgruppe enthält, enthält sie keine zusätzlichen Transaktionen, die in eine Neuberechnung des Wertes einbezogen werden können. Die beste Schätzung des verfügbaren Bestands, der für diese Lager oder Geschäfte angezeigt werden kann, sind daher die Daten aus dem letzten bekannten Snapshot von Commerce Headquarters.

Die Bildschirme **Auftragserfüllung** von POS nutzen auch die Berechnung auf der Kanalseite, um den verfügbaren Bestand für Artikel anzuzeigen, wenn eine Zeile zur Auftragserfüllung ausgewählt wird und ein Benutzer das Panel **Details** für den verfügbaren Bestand für den ausgewählten Artikel anzeigt.

## <a name="optimize-your-inventory-data"></a>Optimieren Sie Ihre Bestandsdaten

Um die bestmögliche Schätzung des Bestands zu gewährleisten, ist es wichtig, dass Sie die folgenden Commerce-Batch-Jobs verwenden und diese häufig ausführen:

- **P-Job** - Der P-Job ist auf der Seite **Verteilungspläne** zu finden und sollte häufig ausgeführt werden. Dieser Job bringt e-Commerce-Bestellungen, asynchrone Kundenbestellungen, die von POS erstellt wurden, und Cash-and-Carry-Bestellungen, die von POS aus den Channel-Datenbanken erstellt wurden, in Commerce Headquarters, damit sie weiter verarbeitet werden können. Solange diese Daten nicht vom Channel zu Commerce Headquarters synchronisiert sind, verfügt Commerce Headquarters über keine Informationen über Bestandsanpassungen der Produkte in den Lagern, die sich aus diesen Transaktionen ergeben.
- **Bestellungen synchronisieren** - Dieser Job verarbeitet die rohen Transaktionsdaten in Commerce Headquarters, die der P-Job zur Verfügung stellt, und konvertiert E-Commerce- und asynchrone Kundenbestellungstransaktionen in Kundenaufträge in Commerce Headquarters. Bis dieser Job verarbeitet und die Kundenaufträge erstellt sind, werden keine Bestandstransaktionen erstellt. Daher werden die Transaktionen bei der Bestandsaufnahme in Commerce Headquarters nicht berücksichtigt.
- **Transaktionsaufstellungen im Batch berechnen** - Bei Cash-and-Carry-Transaktionen, die im Geschäft erstellt werden, stellt der Einzelzulaufsbuchungsprozess sicher, dass der Bestand, der mit den Verkäufen in Zusammenhang steht, effizient aktualisiert wird. Um die effizienteste Verarbeitung von Bestandstransaktionen für Cash-and-Carry-Bestellungen zu erhalten, stellen Sie sicher, dass Sie Ihr System so konfigurieren, dass [Einzelzulaufsbuchung](./trickle-feed.md) verwendet wird.
- **Posttransaktionsauszüge im Batch** - Dieser Job ist auch für die Einzelzulaufsbuchung erforderlich. Er folgt auf den Job **Transaktionale Anweisungen im Batch** berechnen. Dieser Job bucht die berechneten Auszüge systematisch, sodass Kundenaufträge für Cash-and-Carry-Verkäufe in Commerce Headquarters erstellt werden, und Commerce Headquarters den Bestand Ihres Geschäfts genauer widerspiegeln.
- **Produktverfügbarkeit** - Dieser Job erstellt die Momentaufnahme des Bestands in Commerce Headquarters.
- **1130 (Produktverfügbarkeit)** - Dieser Job ist auf der Seite **Vertriebspläne** zu finden und sollte unmittelbar nach dem Job **Produktverfügbarkeit** ausgeführt werden. Mit diesem Job werden die Bestandsdaten von Commerce Headquarters zu den Vertriebskanal-Datenbanken transportiert.

> [!NOTE]
> - Es ist ein bewährtes Verfahren, die Jobs **Produktverfügbarkeit** und **1130** stündlich auszuführen und P-Job, Auftragssynchronisation und buchungsbezogene Jobs mit der gleichen oder einer höheren Frequenz zu planen.
> - Aus Leistungsgründen wird bei kanal-seitigen Bestandsverfügbarkeitsberechnungen für eine Bestandsverfügbarkeitsabfrage über die E-Commerce API's oder die kanal-seitige POS-Bestandslogik ein Zwischenspeicher verwendet, um festzustellen, ob genug Zeit vergangen ist, um ein erneutes Ausführen der Berechnungslogik zu rechtfertigen. Der Standard-Cache ist auf 60 Sekunden eingestellt. Sie haben beispielsweise die kanalseitige Berechnung für Ihr Geschäft aktiviert und den verfügbaren Bestand für ein Produkt auf der Seite **Bestandssuche** angezeigt. Wenn dann eine Einheit des Produkts verkauft wird, zeigt die Seite **Bestandsabfrage** den reduzierten Bestand erst dann an, wenn der Cache geleert wurde. Nachdem Benutzer Transaktionen in POS gebucht haben, sollten sie 60 Sekunden warten, bevor sie überprüfen, ob der verfügbare Bestand reduziert wurde.

Wenn Ihr Unternehmensszenario eine kleinere Zwischenspeicherzeit erfordert, wenden Sie sich an Ihren Produkt-Support-Mitarbeiter, um Unterstützung zu erhalten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
