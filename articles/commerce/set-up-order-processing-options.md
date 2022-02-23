---
title: Einrichten von Callcenterkanälen
description: Die Themen dieses Abschnitts enthalten Informationen zum Verarbeiten von Bestellungen für Callcenter mit Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28954eab857a06da3978ca362081dfc3c525354d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412641"
---
# <a name="set-up-call-center-channels"></a>Einrichten von Callcenterkanälen

[!include [banner](includes/banner.md)]

Ein Unternehmen kann Callcenter-Kanäle in Dynamics 365 Commercedefinieren. Callcenterkanäle werden bei **Retail und Commerce** \> **Kanäle** \> **Callcenter** \> **Alle Callcenter** konfiguriert, und sie sind für eine juristische Person bestimmt.

Wenn ein neuer Callcenterkanal erstellt wird, wird er systematisch einer Organisationseinheitsnummer zugewiesen. Da Callcenter als Organisationseinheiten erstellt werden, können Benutzer den Callcenterkanal mit verschiedenen Commerce-Funktionen, z. B. Sortimente, Kataloge und bestimmte Lieferarten, verknüpfen.

Ein Standardlagerort kann im Feld Callcenterkanal konfiguriert werden. Wenn Aufträge in diesem Kanal erstellt werden, wird der Standardlagerort automatisch im Auftragskopf eingegeben, es sei denn, dass ein anderer Lagerort für den Debitor definiert wurde, der für den Auftrag ausgewählt wird. In diesem Fall wird standardmäßig der Lagerort des Debitors eingegeben.

Benutzer müssen mit einem Callcenterkanal verknüpft werden, um die Funktionen des Callcenters zu verwenden. Jeder Auftrag, den ein Benutzer erstellt, wird automatisch mit dem Callcenterkanal dieses Benutzers verknüpft. So wird ein einzelner Benutzer möglicherweise nicht mit mehreren Callcenterkanlälen gleichzeitig verknüpft.

Ein E-Mail-Benachrichtigungsprofil kann im Callcenterkanal auch so konfiguriert werden. Das Profil definiert den Satz von E-Mail-Vorlagen, der verwendet wird, wenn eine E-Mail an den Debitor gesendet wird, die Aufträge nach den Callcenterkanal aufgeben. Die E-Mail-Trigger können anhand von Systemereignissen, wie Auftragsunterordnung oder Auftragslieferung konfiguriert werden.

Bevor Vertrieb korrekt durch einen Callcenterkanal verarbeitet werden kann, müssen korrekte [Zahlungsmethoden](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) und Lieferarten für den Kanal definiert werden.

Auf der Ebene des Callcenterkanals, können andere Standardwerte definiert werden, die Finanzdimensionen zugeordnet werden, die mit Aufträgen verknüpft werden, die in diesem Kanal erstellt werden.

## <a name="options-for-order-processing-behavior"></a>Optionen für Auftragsverarbeitungsverhalten

Drei Einstellungen in der Konfiguration eines Callcenters haben einen Haupteffekt auf die Funktionen, die für Aufträge verfügbar sind, die anhand dieser Callcenter erstellt werden: **Aktivieren Sie Auftragsabschluss**, **Aktivieren des Direktverkauf** und **Aktivieren Sie Auftrags-Preiskontrolle**.

### <a name="enable-order-completion"></a>Auftragsabschluss aktivieren

Die Einstellung im Feld **Aktivieren Sie Auftragsabschluss** im Callcenterkanal hat einen Haupteffekt auf den Auftrag, der den Flow von Aufträgen verarbeitet, die für diesen Kanal eingegeben werden. Wenn diese Einstellung aktiviert ist, müssen alle Aufträge eine Reihe von Validierungsregeln durchlaufen, bevor diese bestätigt werden können. Sie führen diese Regeln aus, indem Sie die Schaltfläche **Vollständig** auswählen, die im Aktivitätsbereich der Seite "Aufträge" hinzugefügt wird. Alle Aufträge, die erstellt werden, wenn die Einstellung **Aktivieren Sie Auftragsabschluss** aktiviert ist, müssen den Auftragsabschlussprozess durchlaufen. Dieses Verfahren setzt das Aufzeichnen der Zahlungs- und Zahlungsprüfungslogik durch. Zusätzlich zur Zahlungsdurchführung kann der Auftragsunterordnungsprozess starten, der [Betrugsschecks](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts) auslösen kann, die im System konfiguriert sind. Aufträge, die Zahlungs- oder Betrugsprüfungen nicht erfolgreich durchlaufen, werden gesperrt und können nicht freigegeben werden zur späteren Bearbeitung (wie Entnahme oder Versand) bis das Problem, das die Sperre auslöste, behoben ist.

Wenn die Einstellung **Aktivieren Sie Auftragsabschluss** für den Callcenterkanal aktiviert ist, wenn Positionen in einen Auftrag eingegeben werden und der Kanalbenutzer versucht, das Auftragsformular zu schließen oder vom Auftragsformular wegzunavigieren, ohne zuerst **Vollständig** zu wählen, setzt das System den Auftragsabschlussprozess fest, indem die Auftragsrekapitulationsseite geöffnet wird und verlangt, dass der Benutzer den Auftrag korrekt versendet. Wenn der Auftrag nicht zusammen mit der Zahlung korrekt übermittelt werden kann, kann er die Funktionen [Auftragssperre](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) verwenden, um die Reihenfolge zu sperren. Wenn der Benutzer versucht, die Reihenfolge zu deaktivieren, muss er ihn richtig stornieren, indem entweder die Abbrechen-Funktion oder die Löschfunktion abhängig von der Funktion verwendet wird, die die Sicherheit des Benutzers zulässt.

Wenn die Einstellung **Aktivieren Sie Auftragsabschluss** für den Callcenterkanal aktiviert ist, wird der **Zahlungsstatus** für den Auftrag nachverfolgt. Das System berechnet **Zahlungsstatus** wenn der Auftrag übermittelt wird. Nur Aufträge, die einen genehmigten Zahlungsstatus haben, werden für die Verschiebung vom System für weiteren Auftrag zugelassen, wie Entnahme und Versand. Wenn Zahlungen abgelehnt werden, ist die Markierung **nicht verarbeiten** in dem detaillierten Auftragsstatus aktiviert. Dies sperrt den Auftrag, bis der Zahlungsabgang behoben ist.

Wenn darüber hinaus die Einstellung **Aktivieren Sie Auftragsabschluss** aktiviert ist, wenn Benutzer Aufträge erstellen und im Eintragsmodus sind, ist das Feld **Quelle** verfügbar im Hauptauftragskopf. Das Feld **Quelle** wird verwendet, um einen [Katalogquellcode](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) in einer Direktvertriebsbranche aufzuzeichnen, die Szenario verkauft. Dieser Code kann dann Sonderpreise und Aktionen treiben.

Auch wenn die Einstellung **Aktivieren Sie Auftragsabschluss** deaktiviert ist, können Benutzer einen Quellcode noch in einen Auftrag übernehmen. Allerdings müssen sie zuerst Auftragskopfdetails öffnen, um auf das Feld **Quelle** zuzugreifen. Das bedeutet, es sind einige zusätzliche Klicks notwendig. Dasselbe Verhalten bezieht sich auf Funktionen wie vollständige und beschleunigte Aufträge von Versand. Diese Funktionalität ist für alle Aufträge verfügbar, die in dem Callcenter erstellt werden. Wenn die Einstellung **Aktivieren Sie Auftragsabschluss** aktiviert ist, können Benutzer die Konfiguration dieser Funktionen im Auftragskopf finden, die im Formular Positionseintragsansicht sind. Sie müssen nicht in die Auftragskopfdetails gehen, um die erforderlichen Einstellungen und Felder zu suchen.

### <a name="enable-direct-selling"></a>Direktverkauf aktivieren

Wenn die Einstellung **Direktverkauf aktivieren** für den Callcenterkanal aktiviert ist, können Benutzer die Upsell- und Cross-Sell-Funktionen von Commerce nutzen. In diesem Fall erscheint ein Popupfenster bei der Auftragserfassung und schlägt andere Produkte vor, die der Callcenterbenutzer dem Debitor anbieten kann. Die Produkte, die vorgeschlagen werden, basieren auf dem Produkt, das derzeit für die Auftragsposition bestellt wurde. Derzeit sind die Upsell und die Cross-Sell-Vorschläge auf Artikelebene auf Produkte oder Kataloge konfiguriert. Wenn die Einstellung **Aktivieren des Direktverkauf** für den Callcenterkanal deaktiviert ist, werden Popupfenster nicht in der Verkaufserfassung angezeigt, selbst wenn ein gültiger Upsell oder Cross-Sell für einen Artikel definiert wurden, der bestellt ist.

Wenn die Einstellung **Aktivieren des Direktverkauf** aktiviert ist, werden die Skript- und Bildfunktionen der Auftragseintragsseite auch aktiviert. In diesem Fall ist eine Informationsleiste rechts der Seite bei der Auftragserfassung verfügbar. Dieser Bereich kann die Skripts anzeigen, die mit dem generischen Auftragserfassungsprozess verknüpft sind, den Katalogquellcode, der angewendet wurde, oder die Skripts, die den Artikeln zugeordnet werden, die bestellt wurden. Darüber hinaus kann der Bildbereich ein Produktbild für die Artikel anzeigen, die bestellt wurden, wenn ein Bild für den Artikel in der Produkteinstellung definiert wurde.

### <a name="enable-order-price-control"></a>Auftragspreissteuerung aktivieren

Wenn die Einstellung **Aktivieren Sie Auftrags-Preiskontrolle** gedreht wird, können nur berechtigte Benutzer den Verkaufspreis eines Artikel während der Verkaufserfassung ändern. Die Änderungen müssen innerhalb der angegebenen Toleranzen liegen. Benutzer, die nicht die korrekte Autorisierung haben, müssen stattdessen eine Anforderung für eine Preisänderung übermitteln. Die Anforderung wird dann durch den Systemworkflow zur Prüfung und Genehmigung verarbeitet.

## <a name="channel-users"></a>Kanalbenutzer

Wenn Sie das Callcenterkanal definieren, müssen Sie Kanalbenutzer mit dem Callcenter verknüpfen. Andernfalls kann das Callcenter nicht im System verwendet werden. Wenn Benutzer sich bei Commerce anmelden und Aufträge oder Rücklieferungen auf einer Seite eingeben, die der Auftragserfassung zugeordnet sind, wird die Benutzerkennung für die Konfiguration des Callcenterkanals geprüft. Wenn ein Benutzer mit einem bestimmten Callcenterkanal verknüpft wird, erben Aufträge, die der Benutzer erstellt hat, die Eigenschaften und Standardwerte des Kanals.

Standardmäßig wird die Markierung **Verkauf** im Auftragskopf für alle Aufträge aktiviert, die Callcenterbenutzer erstellen. Hierbei können Aufträge von den Commerce-spezifischen Funktionen von Preis- und verkaufsfördernden Maßnahmen profitieren.


Benutzer, die nicht mit einem Callcenterkanal verknüpft sind, verwenden die Standardauftragserfassungsfunktionen von Microsoft Dynamics 365 Finance. Aufträge, die diese Benutzer durch das Auftragserfassungsformular eingeben, werden nicht systematisch als Commerce-Aufträge identifiziert. Darüber hinaus sind diese Aufträge, die von diesen Benutzern eingegeben werden, nicht Auftragsabschlussregeln, Preislogik oder anderen Auftragsprüfungen unterworfen, die in der Callcenterkanalkonfiguration oder im Systemparameter des Callcenters definiert werden können.

Nachdem Sie die Konfiguration des Callcenters abgeschlossen und Kanalbenutzer definiert haben, um das gewünschte Systemverhalten sicherzustellen, überprüfen Sie, ob alle erforderlichen Callcenter-Parameter bei **Retail und Commerce** \> **Kanaleinrichtung** \> **Callcenter-Einrichtung** \> **Callcenter-Parameter** definiert sind. Überprüfen Sie, ob auch zugehörige Nummernkreise definiert sind.

> [!NOTE]
> Um die Funktionen des Callcenters nutzen zu können, muss der Konfigurationsschlüssel für **Mehrere Lieferadressen** aktiviert sein. Diesen Konfigurationsschlüssel finden Sie in den Konfigurationsschlüsseln **Handel** unter **Systemverwaltung**\> **Einstellungen** \> **Lizenzkonfiguration**. Dies ist aufgrund der Call Center-Funktionalität erforderlich, die verschiedene Überprüfungen basierend auf der Lieferadresse durchführt, die auf der Ebene der Auftragspositionen konfiguriert wurde. 

