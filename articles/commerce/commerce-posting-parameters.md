---
title: Commerce-Buchungsparameter
description: In diesem Thema werden die Parameter beschrieben, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen in Microsoft Dynamics 365 Commerce sind.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649202"
---
# <a name="commerce-posting-parameters"></a>Commerce-Buchungsparameter

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema werden die Parameter beschrieben, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen in Microsoft Dynamics 365 Commerce sind. Commerce-Buchungsparameter befinden sich in der Commerce-Zentralverwaltung unter **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter \> Buchung**.

## <a name="periodic-discount-parameters"></a>Periodische Rabattparameter

Die folgende Tabelle listet die periodischen Rabattparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Periodischen Rabatt buchen | Diese Option steuert, ob periodische Angeboten auf Sachkonten gebucht werden. Periodische Rabatte umfassen Angebots-Sortimentsrabatte, Mengenrabatte und Rabattangebote. Wenn dieser Parameter aktiviert ist, können zusätzliche Felder im Abschnitt **Periodische Rabatte** eingestellt werden. |
| Sachkontenart | <p>Wählen Sie den Typ des Kontos aus, das verwendet wird, um periodische Rabatte zu buchen:</p><ul><li>**Standard** – Das System verwendet die rabattbezogenen Felder auf dieser Seite nicht. Stattdessen werden die Konten verwendet, die auf der **Buchung**-Seite in der Commerce-Zentralverwaltung (**Bestandsverwaltung \> Einrichtung \> Buchung \> Buchungsformulare**) definiert sind.</li><li>**Periodisch** – Das System verwendet die Commerce-Rabattkonten, die in den rabattbezogenen Feldern auf dieser Seite angegeben sind. Wenn Sie diese Option auswählen, müssen Sie das Hauptbuchkonto (GL) für jeden Angebotstyp angeben (Rabatt, Angebots-Sortiment, Menge und Schwellenwert). Wenn Sie jeden Rabatt einrichten, können Sie ein Konto definieren. Wenn die Rabattkontobuchungsfunktion auf der Rabatteinrichtungsseite verwendet wird, wird eine zusätzliche Belastungsbuchung und Gutschriftbuchung vorgenommen, um die Rabattbuchung vom Commerce-Rabatt-GL-Konto auf das Rabatt-GL-Konto umzuklassifizieren. Weitere Informationen finden Sie unter [Einzelhandelsrabatte](retail-discounts-overview.md).</li></ul> |
| Infocode-Rabatt buchen | Diese Option wird in der Standard-Commerce-Lösung nicht mehr verwendet und ist veraltet. |
| Periodischen Rabatt für Aufträge buchen | Diese Option steuert, ob periodische Einzelhandelsrabatte auf das Sachkonto für Kundenaufträge und Callcenteraufträge gebucht werden. |

## <a name="inventory-update-parameters"></a>Lageraktualisierungsparameter

Die folgende Tabelle listet die Lageraktualisierungsparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Standard-Chargen-ID verwenden, wenn Chargennummern nicht gefunden werden | Diese Option steuert, ob eine Standard-Chargen-ID für chargenaktivierte Artikel verwendet wird, falls Chargennummern nicht gefunden werden und ein negativer Bestand zulässig ist. |
| Standard-Chargen-ID | Die Chargennummer, die verwendet werden soll, wenn Chargennummern für Artikel nicht gefunden werden und der Parameter **Standard-Chargen-ID verwenden, wenn Chargennummern nicht gefunden werden** aktiviert ist. |

## <a name="aggregation-parameters"></a>Aggregationsparameter

Die folgende Tabelle listet die Aggregationsparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Sichere Einzahlung | Aktivieren Sie diesen Parameter, um alle Transaktionen während der Auszugsbuchung zu aggregieren und eine einzelne Zeile in der Erfassung für die Buchung zu erstellen, anstatt eine separate Zeile für jede Einzahlung. |
| Bankeinzahlung | Aktivieren Sie diesen Parameter, um alle Transaktionen während der Auszugsbuchung zu aggregieren und eine einzelne Zeile in der Erfassung für die Buchung zu erstellen, anstatt eine separate Zeile für jede Einzahlung. |
| Verkaufsbuchungen | Aktivieren Sie diesen Parameter, um die Transaktionen als Teil des Transaktionsauszugsbuchungsprozesses zu konsolidieren. Wir empfehlen Ihnen, diesen Parameter zu aktivieren. Er wurde zuvor **Belegbuchungen** genannt. |
| Rückgaben nicht aggregieren | Wenn diese Option aktiviert ist, wird jede Rückgabebuchung als separater Auftrag gebucht, wenn ein Einzelhandelsauszug gebucht wird. |

## <a name="batch-processing-parameters"></a>Chargenverarbeitungsparameter

Die folgende Tabelle listet die Chargenverarbeitungsparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Maximale Anzahl paralleler Aufstellungen | Dieses Feld definiert die Anzahl der Batchaufgaben, die verwendet werden, um mehrere Auszüge zu buchen. |
| Maximaler Thread für die Auftragsverarbeitung pro Auszug | Dieses Feld stellt die maximale Anzahl der Threads dar, die vom Batchauftrag für die Auszugsbuchung verwendet wird, um Aufträge für einen einzelnen Auszug zu erstellen und zu fakturieren. Die Gesamtanzahl der Threads, die bei der Buchung von Auszügen verwendet werden, wird durch Multiplizierung des Werts dieses Parameters mit dem Wert des Parameters **Maximale Anzahl paralleler Aufstellungsbuchung** berechnet. Wenn der Wert dieses Parameters zu hoch ist, kann dies die Leistung des Auszugsbuchungsprozesses negativ beeinflussen. |
| Maximale Transaktionspositionen, die in der Aggregation enthalten sind | Dieses Feld definiert die Anzahl von Transaktionspositionen, die in einer einzelnen zusammengefassten Transaktion eingeschlossen sind, bevor eine neue Transaktion erstellt wird. Aggregierte Transaktionen werden auf Grundlage unterschiedlicher Aggregationskriterien erstellt, beispielsweise Debitor, Geschäftsdatum oder Finanzdimensionen. Beachten Sie, dass die Positionen einer einzelnen Transaktion nicht auf verschiedene aggregierte Transaktionen aufgeteilt werden. Deshalb kann die Anzahl der Positionen in einer aggregierten Transaktion möglicherweise etwas höher oder niedriger sein, je nach Faktoren wie die Anzahl der eindeutig identifizierbaren Produkte. |
| Maximale Anzahl von Threads für Überprüfung von Geschäftbuchungen | Dieses Feld definiert die maximale Anzahl von Threads, die für das Überprüfen von Buchungen verwendet werden. Die Prüfung von Transaktionen ist ein erforderlicher Schritt, der durchgeführt werden muss, bevor die Transaktionen in die Aufstellungen gezogen werden können. Sie müssen auch ein Geschenkkartenprodukt auf dem Inforegister **Geschenkkarte** auf der Registerkarte **Buchung** der Seite **Commerce-Parameter** definieren, selbst wenn die Organisation keine Geschenkkarten verwendet. |

In der folgenden Tabelle sind die empfohlenen Werte für die Parameter in der vorstehenden Tabelle aufgeführt. Diese Werte sollten getestet und an die Bereitstellungskonfiguration und die verfügbare Infrastruktur angepasst werden. Werte, die empfohlene Werte überschreiten, können sich negativ auf andere Batch-Verarbeitungen auswirken und sollten daher validiert werden.

| Parameter | Empfohlener Wert | Informationen |
|-----------|-------------------|---------|
| Maximale Anzahl paralleler Aufstellungsbuchung | <p>Legen Sie diesen Parameter auf die Anzahl der Batch-Aufgaben fest, die für die Batch-Gruppe verfügbar sind, die den **Auftrag** ausführt.</p><p>**Allgemeine Regel:** Multiplizieren Sie die Anzahl der virtuellen Server von Application Object Server (AOS) mit der Anzahl der Batch-Aufgaben, die pro virtuellem AOS-Server verfügbar sind.</p> | Dieser Parameter ist nicht anwendbar, wenn die Funktion **Einzelhandelsauszüge - Trickle feed** aktiviert ist. |
| Maximaler Thread für die Auftragsverarbeitung pro Auszug | Beginnen Sie, Werte bei **4** zu testen. In der Regel sollte der Wert **8** nicht überschreiten. | Dieser Parameter definiert die Anzahl der Threads, die zum Erstellen und Buchen von Aufträgen verwendet werden. Sie gibt die Anzahl der Threads an, die pro Anweisung für die Buchung zur Verfügung stehen. |
| Maximale Transaktionspositionen, die in der Aggregation enthalten sind | Beginnen Sie, Werte bei **1000** zu testen. Je nach Konfiguration der Commerce-Zentralverwaltung können kleinere Aufträge für die Leistung vorteilhafter sein. | Dieser Parameter definiert die Anzahl der Positionen, die bei der Auszugsbuchung in jeden Auftrag aufgenommen werden. Nachdem diese Anzahl erreicht ist, werden die Zeilen in eine neue Reihenfolge aufgeteilt. Die Anzahl der Verkaufspositionen wird der von Ihnen angegebenen Anzahl nicht exakt entsprechen, da die Aufteilung auf der Ebene des Auftrags erfolgt. Trotzdem wird die Anzahl nahe an der festgelegten Anzahl liegen. Dieser Parameter wird verwendet, um Verkaufsaufträge für Transaktionen im Einzelhandel zu generieren, die keinen benannten Debitor haben. |
| Maximale Anzahl von Threads für Überprüfung von Geschäftbuchungen | Wir empfehlen Ihnen, diesen Parameter auf **4** festzulegen und ihn nur dann zu erhöhen, wenn Sie keine akzeptable Leistung erreichen. Die Anzahl der Threads, die dieser Prozess verwendet, darf die Anzahl der Prozessoren, die dem Batch-Server zur Verfügung stehen, nicht überschreiten. Wenn die Anzahl der Threads zu hoch ist, werden möglicherweise andere Batchverarbeitungen beeinträchtigt. | Dieser Parameter steuert die Anzahl der Transaktionen, die gleichzeitig für einen bestimmten Store validiert werden können. |

> [!NOTE]
> Alle Einstellungen und Parameter, die sich auf Auszugsbuchungen beziehen und die in den Geschäften und auf der Seite **Commerce-Parameter** definiert sind, sind auf die verbesserte Funktion zur Auszugsbuchung anwendbar.

## <a name="invoice-parameters"></a>Rechnungsparameter

Die folgende Tabelle listet die Rechnungsparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Erfassungsname | Der Zahlungserfassungsname, der verwendet wird, wenn Debitorenzahlungserfassungen für Auftragszahlungen erstellt werden. Diese Einstellung gilt für alle Auftragszahlungen, die für Bestellungen über Verkaufsstellen (POS), Callcenter und E-Commerce-Kanäle gebucht werden. |
| Kontoname | Der Name des Zahlungskontos. |
| Priorisierung von Dimensionen aus der Zahlungsmethode | Wenn dieses Kennzeichen aktiviert ist, werden Dimensionen aus der Zahlungsmethode anstelle der Dimensionen aus dem Geschäft von den Zahlungserfassungen priorisiert. |
| Steuerberechnungsverhalten | Dieser Parameter gibt das Verhalten an, wenn Aufträge, die während der Auszugsbuchung erstellt werden, fakturiert werden:<ul><li>**Neu berechnen** – Steuern neu berechnen.</li><li> **Nicht neu berechnen** – Die Steuerbeträge verwenden, die in POS berechnet werden.</li></ul> |
| Erfassungsname | Der Erfassungsname, der verwendet wird, wenn eine Debitorenzahlungserfassung für Rückerstattungen erstellt wird. Diese Einstellung gilt für alle Auftragszahlungen, die für POS-, Callcenter- und E-Commerce-Kanal-Bestellungen gebucht werden. |

## <a name="statement-parameters"></a>Aufstellungsparameter

Die folgende Tabelle listet die Aufstellungsparameter auf, die spezifisch für die Buchung von wertmäßigen und physischen Buchungen sind.

| Parameter | Description |
|-----------|-------------|
| Bestand bei der Berechnung reservieren | Wenn dieser Parameter aktiviert ist, reserviert die Auszugsberechnung vorübergehend Bestand, bis der Auszug gebucht wird. Dieser Parameter ist standardmäßig deaktiviert, um die Leistung der Auszugsberechnung zu verbessern. Aktualisierte Bestandsinformationen können mithilfe des Batchauftrags **Lager buchen** berechnet werden. Beachten Sie, dass der Batchauftrag zum **Buchen** des Bestands nicht mehr verwendet wird, wenn die auf [Einzelzulauf](trickle-feed.md) basierte Auftragserstellung für Einzelhandelsgeschäftbuchungen aktiviert ist. |
| Deaktivieren der Zählung erforderlich | Mit dieser Kennzeichnung wird die Zählung beim Buchen in der Commerce-Zentralverwaltung deaktiviert. |
| Finanzdimensionen bei Fehler neu berechnen | Wenn dieser Parameter aktiviert ist, werden Finanzdimensionen bei nachfolgenden Auszugsbuchungen neu bewertet, wenn die Auszugsbuchung fehlschlägt. |
| Finanzdimensionen der Rückgabefiliale verwenden | Wenn dieser Parameter aktiviert ist, können verknüpfte Retourenaufträge erstellt werden, die die Finanzdimensionen des Geschäfts anstelle der Finanzdimensionen aus der ursprünglichen Buchung verwenden. |
| Verknüpfung für Retouren aufheben | Wenn dieser Parameter aktiviert ist, kann der Auszug Retouren von nicht gebuchten Verkäufen als Blindretouren erstellen. Dieser Parameter ist standardmäßig deaktiviert, und wir empfehlen, ihn deaktiviert zu lassen. |
| Buchung der Rundungsdifferenz deaktivieren | Dieser Parameter deaktiviert die Buchung der Rundungsdifferenz zwischen einer Transaktionszahlung und dem Bruttobetrag während der Zahlungsverarbeitung. |
| Debitoreneinzahlungen automatisch ausgleichen | Wenn dieser Parameter aktiviert ist, werden Debitoreneinzahlungen, die während der Buchung der Einzelhandelsaufstellung gebucht werden, mit offenen Debitorenbuchungen ausgeglichen. |
| Bargeldverwaltungsabstimmung von POS aktivieren und verwenden | Wenn dieser Parameter aktiviert ist, erfolgt die Bargeldverwaltungsabstimmung in POS, und die Werte werden an die Buchung der Finanzauszüge für den Einzelhandel weitergeleitet, um Auszugspositionen zu erstellen. |
| Detailebene des Sachkontobelegs | Dieser Parameter definiert den Detaillierungsgrad, der im Sachkontobeleg für ausgewählte Transaktionen enthalten ist, die vom POS stammen. Zu den Transaktionstypen gehören Einnahmen, Ausgaben und Rabatte. Bei Rabatten wird dieser Parameter nur berücksichtigt, wenn die Kontonummer für einen periodischen Rabatt und die Kontonummer für einen regelmäßigen Rabatt nicht identisch sind. Sofern keine Angaben erforderlich sind, ist **Zusammenfassung** der empfohlene Wert für diese Buchungen. Wenn Buchungen auf Zusammenfassungsebene definiert sind, wird **TransactionDiscountTrans.RecID** nicht ausgefüllt. In der Commerce-Version 10.0.27 wurde dieses Kennzeichen umbenannt und verschoben. Es wurde zuvor **Detailebene** genannt und befand sich im Abschnitt **Lageraktualisierung**. |
