---
title: Berechnen der Bestandsverfügbarkeit für Einzelhandelskanäle
description: In diesem Thema werden die Optionen beschrieben, die für die Anzeige des verfügbaren Bestands für das Geschäft und die Online-Kanäle zur Verfügung stehen.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: de4ee98198f441b8f42a8a55aa5ff1015f485234
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412552"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Berechnen der Bestandsverfügbarkeit für Einzelhandelskanäle

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Unternehmen Microsoft Dynamics 365 Commerce verwenden kann, um die geschätzte Verfügbarkeit von Produkten im Online- und Shop-Kanal anzuzeigen.

## <a name="accuracy-of-calculation"></a>Genauigkeit der Berechnung

Commerce verwendet mehrere Server und Datenbanken, um Skalierbarkeit und Leistung zu gewährleisten. Daher ist es wichtig, dass Sie sich darüber im Klaren sind, dass die verfügbaren Bestandswerte, die über die POS-Anwendung (Point of Sale), die Anwendungs-Programmierschnittstellen (APIs) für die Verfügbarkeit des E-Commerce-Bestands und die verfügbaren Bestandsseiten in Commerce Headquarters bereitgestellt werden, möglicherweise nicht zu 100 Prozent in Echtzeit korrekt sind. Wenn Transaktionen, die für Produkte im Online- oder Store-Kanal erstellt werden, noch nicht mit dem Server und der Datenbank von Commerce Headquarters synchronisiert wurden, zeigen die Seiten für den vorliegenden Bestand in Commerce Headquarters möglicherweise keinen genauen Echtzeit-Bestandswert für diese Produkte an. Wenn Sie Ihr Unternehmen umgekehrt so konfiguriert haben, dass Benutzer in Commerce Headquarters oder in anderen integrierten Anwendungen den Bestand in einem Geschäft oder einem Online-Lager verkaufen, empfangen, zurückgeben oder anderweitig anpassen können, verfügt die Verkaufsstelle oder der Online-Kanal möglicherweise nicht über alle Informationen, die erforderlich sind, um einen genauen Echtzeit-Bestandswert für Artikel anzuzeigen.

In diesem Thema werden die Datensynchronisationsprozesse erläutert, die häufig ausgeführt werden können, um die Latenzzeit der Daten zwischen Anwendungen oder Kanälen zu begrenzen. Es ist jedoch wichtig, dass Sie verstehen, dass alle verfügbaren Daten, die während des Betriebstages zur Verfügung gestellt werden, als Schätzwert betrachtet werden. Wenn Sie daher versuchen, die von der Anwendung bereitgestellten Bestandsinformationen mit dem tatsächlichen physischen Bestand in den Regalen zu vergleichen, oder wenn Sie versuchen, die in der Kasse angezeigten Bestandswerte mit den Bestandsdaten zu vergleichen, die Sie für dasselbe Lager in Commerce Headquarters finden, können die Werte abweichen. Diese Differenz wird während des Betriebstages erwartet und sollte nicht als Problem betrachtet werden. Wenn Sie Daten prüfen und sicherstellen möchten, dass die Werte, die in den Bestandsverfügbarkeits-APIs und in Commerce Headquarters bereitgestellt werden, mit den tatsächlichen physischen Einheiten übereinstimmen, die Sie in Ihrem Geschäft oder in den Regalen Ihres Lagers vorfinden, sollten Sie dies am besten tun, nachdem die Channel-Operationen für den Tag gestoppt und alle Transaktionen zwischen Commerce Headquarters und dem Channel korrekt synchronisiert wurden.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Verwenden Sie APIs zur Bestandsabfrage für Anfragen zur Verfügbarkeit von E-Commerce-Beständen.

Sie können die folgenden APIs verwenden, um die Bestandsverfügbarkeit für ein Produkt anzuzeigen, wenn Ihre Kunden auf einer E-Commerce-Website einkaufen.

- **GetEstimatedAvailabilty** – Verwenden Sie diese API, um die Bestandsverfügbarkeit für den Artikel im Lager des E-Commerce-Kanals oder in allen Lagern anzuzeigen, die mit der Konfiguration der Erfüllungsgruppe für den E-Commerce-Kanal verknüpft sind. Diese API kann auch für Lager in einem bestimmten Suchbereich oder Radius verwendet werden, basierend auf Längen- und Breitengraddaten.
- **GetEstimatedProductWarehouseAvailability** - Verwenden Sie diese API, um den Bestand für einen Artikel aus einem bestimmten Lager anzufordern. Sie können sie beispielsweise verwenden, um die Bestandsverfügbarkeit in Szenarien anzuzeigen, die eine Auftragsabholung beinhalten.

> [!NOTE]
> Diese APIs ersetzen die APIs **GetProductAvailabilities** und **GetAvailableInventoryNearby** in Dynamics 365 Retail Version 10.0.7 und früher.

Beide APIs rufen Daten vom Commerce-Server ab und liefern eine Schätzung des verfügbaren Bestands für eine bestimmte Kombination aus einem Produkt oder einer Produktvariante und einem Lager. Obwohl andere APIs, die auf dem Commerce-Server verfügbar sind, direkt an Commerce Headquarters gehen können, um vorrätige Mengen für Produkte abzurufen, empfehlen wir nicht, dass sie in einer E-Commerce-Umgebung verwendet werden, da diese häufigen Anfragen potenzielle Leistungsprobleme und die damit verbundenen Auswirkungen auf die Commerce Headquarters Server haben können. Wenn der vorrätige Bestand über den Commerce-Server berechnet wird, ist es wahrscheinlicher, dass die Berechnung den Bestand einschließt, der in den letzten E-Commerce-Transaktionen verkauft wurde, die noch nicht mit Commerce Headquarters synchronisiert wurden. Auch wenn Commerce Headquarters möglicherweise nicht über Informationen über diese Transaktionen verfügt, sind die Daten auf dem Commerce-Server und in der Channel-Datenbank vorhanden. Daher werden die Daten berücksichtigt und können dazu beitragen, eine genauere Schätzung des verfügbaren Bestands eines Produkts zu liefern.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Beginnen Sie mit der berechneten Verfügbarkeit des E-Commerce-Bestands

Bevor Sie die beiden zuvor genannten APIs verwenden, müssen Sie die Funktion **Optimierte Berechnung der Produktverfügbarkeit** über den Arbeitsbereich **Funktionsverwaltung** in der Handelszentrale aktivieren.

Bevor die APIs die bestmögliche Schätzung der Bestandsverfügbarkeit für einen Artikel berechnen können, muss ein periodischer Snapshot der Bestandsverfügbarkeit von Commerce Headquarters verarbeitet und an die Datenbank des Vertriebskanals gesendet werden, die die E-Commerce Commerce Scale Unit verwendet. Der Snapshot stellt die Informationen dar, die Commerce Headquarters über die Bestandsverfügbarkeit für eine bestimmte Kombination aus einem Produkt oder einer Produktvariante und einem Lager hat. Er kann Bestandsanpassungen oder -bewegungen enthalten, die durch Lagereingänge oder durch Lieferungen oder andere Prozesse in Commerce Headquarters verursacht werden und über die der E-Commerce-Kanal nur aufgrund des Synchronisierungsprozesses Informationen hat.

Der Datenbank-Snapshot, den der Job **Produktverfügbarkeit** erstellt, berechnet nur die Bestandstransaktionen, die zum Zeitpunkt der Erstellung des Snapshots in Commerce Headquarters verarbeitet und gebucht wurden. Wenn der Bestand für ein Produkt in einem Ladenlager durch einen Cash-and-Carry- oder asynchronen Kundenauftragsverkauf in der POS-Anwendung verkauft wurde, verfügt Commerce Headquarters nicht sofort über Informationen über die entsprechende Bestandsausgabetransaktion für den Verkauf. Informationen über den Bestand, der für diese Art von Ladenverkäufen verkauft wird, liegen erst dann vor, wenn der P-Job die entsprechende Transaktion aus der Vertriebskanal-Datenbank des Ladens in Commerce Headquarters hochlädt und der entsprechende Kundenauftrag durch die Auszugsbuchung oder die Einzelzulaufbuchungsvorgänge erstellt wird. Durch den Prozess der Auftragserstellung in Commerce Headquarters werden die zugehörigen Bestandstransaktionen erstellt. Bei Bestellungen über den E-Commerce-Kanal verfügt Commerce Headquarters erst dann über Informationen zu den Bestandstransaktionen, wenn die Transaktionen über den P-Job an Commerce Headquarters gesendet werden und der Bestellsynchronisationsprozess abgeschlossen ist. Daher ist es wichtig, dass Sie sich darüber im Klaren sind, dass der Wert der Bestandsaufnahme, der im Job **Produktverfügbarkeit** bereitgestellt wird, aufgrund der konstanten Verkaufsverarbeitung, die über verteilte Server erfolgt, möglicherweise nicht zu 100 Prozent in Echtzeit korrekt ist.

Führen Sie die folgenden Schritte aus, um einen Snapshot des Inventars in Commerce Headquarters zu erstellen.

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Produkte und Bestand \> Produktverfügbarkeit**.
1. Wählen Sie **OK**, um den Job **Produktverfügbarkeit** auszuführen. Sie können diesen Job auch so einplanen, dass er im Batch ausgeführt wird.

Nachdem der Job **Produktverfügbarkeit** ausgeführt wurde, müssen die erfassten Daten an die Datenbanken des E-Commerce-Kanals weitergeleitet werden, sodass der neueste Bestandsabgleich von Commerce Headquarters bei der Berechnung des geschätzten Lagerbestands berücksichtigt werden kann.

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Führen Sie den Job **1130** (**Produktverfügbarkeit**) aus, um die Momentaufnahmedaten, die der Job **Produktverfügbarkeit** von Commerce Headquarters erstellt hat, mit Ihren Kanaldatenbanken zu synchronisieren.

Wenn die Bestandsverfügbarkeit von der API **GetEstimatedAvailabilty** oder **GetEstimatedProductWarehouseAvailability** angefordert wird, wird eine Berechnung durchgeführt, um die bestmögliche Schätzung des Bestands für das Produkt zu erhalten. Die Berechnung bezieht sich auf alle E-Commerce-Kundenbestellungen, die in der Kanaldatenbank enthalten sind, aber nicht in den Momentaufnahmedaten enthalten waren, die der 1130-Job geliefert hat. Diese Logik wird ausgeführt, indem die zuletzt verarbeitete Bestandstransaktion von Commerce Headquarters verfolgt und mit den Transaktionen in der Kanaldatenbank verglichen wird. Sie liefert eine Basislinie für die kanalseitige Berechnungslogik, sodass die zusätzlichen Bestandsbewegungen, die bei Verkaufstransaktionen von Kundenbestellungen in der E-Commerce-Kanaldatenbank aufgetreten sind, in den geschätzten Bestandswert, den die API liefert, einbezogen werden können.

Die kanalseitige Berechnungslogik liefert einen geschätzten physisch verfügbaren Wert und einen verfügbaren Gesamtwert für das angeforderte Produkt und das Lager. Die Werte können auf Ihrer E-Commerce-Site angezeigt werden, wenn Sie dies wünschen, oder sie können verwendet werden, um andere Geschäftslogik auf Ihrer E-Commerce-Site auszulösen. So können Sie beispielsweise eine Meldung „nicht vorrätig“ anstelle der tatsächlich verfügbaren Menge anzeigen, die die API übergeben hat.

Die Berechnungslogik, die die kanalseitigen e-Commerce-APIs für den geschätzten Bestandswert verwenden, kann den Bestand nur auf der Grundlage von Kundenbestellungen bewerten, die in der Kanaldatenbank erstellt, aber noch nicht synchronisiert und in Commerce Headquarters gebucht wurden. Wenn Ihre Vertriebskanal-Datenbank auch Transaktionsdaten für Cash-and-Carry-Verkäufe für filialspezifische Läger enthält, werden die Cash-and-Carry-Verkäufe nicht in die kanalseitige E-Commerce-Berechnung für diese Lager berücksichtigt.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigurieren Sie den Bestandssuchevorgang im POS-Kanal.

In Retail Version 10.0.9 und früher verwendete die Operation **Bestandsabfrage** von POS aus einen Echtzeit-Serviceaufruf an Commerce Headquarters, um Bestandsinformationen für das ausgewählte Produkt zu erhalten, und zwar sowohl für den aktuellen Laden des Benutzers als auch für alle anderen Läden, die als Teil der Channel-Konfiguration für den Laden für die Fulfillment-Gruppe konfiguriert sind. In der Commerce-Version 10.0.10 und höher können Sie die Echtzeit-Serviceanrufe an Commerce Headquarters ausschalten. Stattdessen können Sie die kanalseitige Berechnung auf dem Commerce-Server verwenden, um den physisch verfügbaren Bestand für die Filiale und alle anderen Standorte zu ermitteln, die in der Auftragserfüllungsgruppe definiert sind. Diese kanalseitig berechnete Bestandskonfiguration ist auch für Standorte nützlich, an denen die Internetverbindung unzuverlässig ist, da Sie nicht online sein müssen, um Bestandsabfragen von Commerce Headquarters zu erhalten.

Wenn die kanalseitige Berechnung korrekt konfiguriert und verwaltet wird, kann sie eine zuverlässigere Schätzung des aktuellen Ladenbestands liefern, da sie die Transaktionsdaten verwendet, die in der Datenbank des Commerce-Kanals enthalten sind, über die Headquarters aber möglicherweise noch keine Informationen hat. Wenn Sie beispielsweise den vorhandenen Echtzeit-Serviceabruf für Bestandsabfragen in POS verwenden, verfügt Commerce Headquarters wahrscheinlich noch nicht über Informationen über einen Cash-and-Carry-Verkauf, der gerade für ein Produkt stattgefunden hat. Daher wird der aktuelle Bestandswert, den Commerce Headquarters für dieses Produkt zurückgibt, wahrscheinlich den aktuellen Bestand des Ladens um eine Einheit übersteigen. Wenn Sie jedoch die kanalseitige Berechnung verwenden, kann der Mitnahmeverkauf in die Berechnung einbezogen und vom angezeigten Bestandswert abgezogen werden. Obwohl die Werte, die sowohl die kanalseitige Berechnung als auch der Echtzeit-Serviceabruf liefern, nur Schätzungen des aktuellen Bestands sind, ist der Wert, den die kanalseitige Berechnung liefert, für das aktuelle Geschäft viel wahrscheinlicher.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Beginnen Sie mit der kanalseitigen Berechnung der Bestandsverfügbarkeit am POS

Um die kanalseitige Berechnungslogik zu verwenden und Echtzeitserviceaufrufe für Bestandssuchen in der POS-Anwendung zu deaktivieren, müssen Sie zuerst die Option **Optimierte Berechnung der Produktverfügbarkeit** über den Arbeitsbereich **Funktionsverwaltung** in der Handelszentrale aktivieren. Zusätzlich zur Aktivierung der Funktion müssen Sie Änderungen am **Funktionsprofil** vornehmen.

Führen Sie die folgenden Schritte aus, um das **Funktionsprofil** zu ändern:

1. Gehen Sie zu **Retail und Commerce \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**.
1. Wählen Sie ein Funktionsprofil aus.
1. Ändern Sie auf den Inforegister **Funktionen** im Abschnitt **Verfügbarkeitsberechnung** von **Verfügbarkeitsberechnungsmodus** von **Echtzeitdienst** auf **Kanal**. Standardmäßig verwenden alle Funktionsprofile Echtzeit-Serviceabrufe. Daher müssen Sie den Wert dieses Feldes ändern, wenn Sie die kanalseitige Berechnungslogik verwenden möchten. Jedes Einzelhandelsgeschäft, das mit dem ausgewählten Funktionsprofil verknüpft ist, ist von dieser Änderung betroffen.

Anschließend müssen Sie die Änderungen am Kanal über den Verteilungsplanungsprozess synchronisieren, indem Sie die folgenden Schritte ausführen:

1. Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
1. Führen Sie den Job **1070** (**Kanalkonfiguration**) aus.

Nach Abschluss der Konfiguration verwenden die Informationen, die über den physisch verfügbaren Bestand bereitgestellt werden, keinen Echtzeit-Serviceabruf mehr, wenn ein Benutzer in der POS-Anwendung den Vorgang **Bestandssuche** verwendet (Standard- und Matrixansicht). Stattdessen werden die Daten über den physisch verfügbaren Bestand für die aktuelle Filiale und alle Filialen in der Erfüllungsgruppe auf der Grundlage des letzten bekannten Snapshots berechnet, der von Headquarters an die Kanaldatenbank geliefert wurde. Der Momentaufnahmewert wird durch die kanalseitige Berechnung weiter verfeinert, um den physisch verfügbaren Wert auf der Grundlage zusätzlicher Verkaufs- oder Retourentransaktionen anzupassen, die für das ausgewählte Produkt in der Kanaldatenbank vorhanden sind und die in der letzten synchronisierten Momentaufnahme aus dem Auftrag 1130 nicht enthalten waren. Wenn die Vertriebskanal-Datenbank keine Transaktionsdaten für eines der Lager oder Geschäfte in der Erfüllungsgruppe enthält, enthält sie keine zusätzlichen Transaktionen, die in eine Neuberechnung des Wertes einbezogen werden können. Die beste Schätzung des verfügbaren Bestands, der für diese Lager oder Geschäfte angezeigt werden kann, sind daher die Daten aus dem letzten bekannten Snapshot von Commerce Headquarters.

Die Bildschirme **Auftragserfüllung** von POS nutzen auch die Berechnung auf der Kanalseite, um den verfügbaren Bestand für Artikel anzuzeigen, wenn eine Zeile zur Auftragserfüllung ausgewählt wird und ein Benutzer das Panel **Details** für den verfügbaren Bestand für den ausgewählten Artikel anzeigt.

## <a name="optimize-your-inventory-data"></a>Optimieren Sie Ihre Bestandsdaten

Um die bestmögliche Schätzung des Bestands zu gewährleisten, ist es wichtig, dass Sie die folgenden Commerce-Batch-Jobs verwenden und diese häufig ausführen:

- **P-Job** - Der P-Job ist auf der Seite **Verteilungspläne** zu finden und sollte häufig ausgeführt werden. Dieser Job bringt e-Commerce-Bestellungen, asynchrone Kundenbestellungen, die von POS erstellt wurden, und Cash-and-Carry-Bestellungen, die von POS aus den Channel-Datenbanken erstellt wurden, in Commerce Headquarters, damit sie weiter verarbeitet werden können. Solange diese Daten nicht vom Channel zu Commerce Headquarters synchronisiert sind, verfügt Commerce Headquarters über keine Informationen über Bestandsanpassungen der Produkte in den Lagern, die sich aus diesen Transaktionen ergeben.
- **Bestellungen synchronisieren** - Dieser Job verarbeitet die rohen Transaktionsdaten in Commerce Headquarters, die der P-Job zur Verfügung stellt, und konvertiert E-Commerce- und asynchrone Kundenbestellungstransaktionen in Kundenaufträge in Commerce Headquarters. Bis dieser Job verarbeitet und die Kundenaufträge erstellt sind, werden keine Bestandstransaktionen erstellt. Daher werden die Transaktionen bei der Bestandsaufnahme in Commerce Headquarters nicht berücksichtigt.
- **Transaktionsaufstellungen im Batch berechnen** - Bei Cash-and-Carry-Transaktionen, die im Geschäft erstellt werden, stellt der Einzelzulaufsbuchungsprozess sicher, dass der Bestand, der mit den Verkäufen in Zusammenhang steht, effizient aktualisiert wird. Um die effizienteste Verarbeitung von Bestandstransaktionen für Cash-and-Carry-Bestellungen zu erhalten, stellen Sie sicher, dass Sie Ihr System so konfigurieren, dass [Einzelzulaufsbuchung](https://docs.microsoft.com/dynamics365/commerce/trickle-feed) verwendet wird.
- **Posttransaktionsauszüge im Batch** - Dieser Job ist auch für die Einzelzulaufsbuchung erforderlich. Er folgt auf den Job **Transaktionale Anweisungen im Batch** berechnen. Dieser Job bucht die berechneten Auszüge systematisch, sodass Kundenaufträge für Cash-and-Carry-Verkäufe in Commerce Headquarters erstellt werden, und Commerce Headquarters den Bestand Ihres Geschäfts genauer widerspiegeln.
- **Produktverfügbarkeit** - Dieser Job erstellt die Momentaufnahme des Bestands in Commerce Headquarters.
- **1130 (Produktverfügbarkeit)** - Dieser Job ist auf der Seite **Vertriebspläne** zu finden und sollte unmittelbar nach dem Job **Produktverfügbarkeit** ausgeführt werden. Mit diesem Job werden die Bestandsdaten von Commerce Headquarters zu den Vertriebskanal-Datenbanken transportiert.

Es wird empfohlen, diese Batchaufträge nicht zu häufig (alle paar Minuten) auszuführen. Häufige Ausführungen überlasten die Commerce-Zentralverwaltung (HQ) und können möglicherweise die Leistung beeinträchtigen. Im Allgemeinen empfiehlt es sich, die Produktverfügbarkeit und 1130 Jobs stündlich auszuführen und P-Jobs zu planen, Aufträge zu synchronisieren und Aufträge im Zusammenhang mit Feeding-Posts mit derselben oder einer höheren Häufigkeit durchzuführen.

> [!NOTE]
> Wenn die kanalseitige Bestandsverfügbarkeitsberechnung verwendet wird, um eine Bestandsverfügbarkeitsanforderung mit Hilfe der E-Commerce-APIs oder der neuen kanalseitigen POS-Bestandslogik zu stellen, verwendet die Berechnung aus Leistungsgründen einen Cache, um festzustellen, ob genügend Zeit verstrichen ist, um die erneute Ausführung der Berechnungslogik zu rechtfertigen. Der Standard-Cache ist auf 60 Sekunden eingestellt. Sie haben beispielsweise die kanalseitige Berechnung für Ihr Geschäft aktiviert und den verfügbaren Bestand für ein Produkt auf der Seite **Bestandssuche** angezeigt. Wenn dann eine Einheit des Produkts verkauft wird, zeigt die Seite **Bestandsabfrage** den reduzierten Bestand erst dann an, wenn der Cache geleert wurde. Nachdem Benutzer Transaktionen in POS gebucht haben, sollten sie 60 Sekunden warten, bevor sie überprüfen, ob der verfügbare Bestand reduziert wurde.

Wenn Ihr Geschäftsszenario eine geringere Cache-Zeit erfordert, wenden Sie sich an Ihren Produktsupportvertreter, um Hilfe zu erhalten.
