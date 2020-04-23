---
title: Lagererfassungen
description: In diesem Thema wird beschrieben, wie Sie Lagererfassungen verwenden können, um verschiedene Typen von physischen Bestandstransaktionen zu buchen.
author: perlynne
manager: tfehr
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d184b34ec33184d730d5b6eed3db144f1433f1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212778"
---
# <a name="inventory-journals"></a>Lagererfassungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Lagererfassungen verwenden können, um verschiedene Typen von physischen Bestandstransaktionen zu buchen.

Die Lagererfassungen in Supply Chain Management werden verwendet, um physische Lagerbuchungen unterschiedlicher Arten, wie Abgangs-und Zugangsbuchungen Lagerumlagerungen, die Erstellung von Stücklisten (BOMs) zu buchen und zur Abstimmung des physischen Bestands. Alle diese Lagererfassungen werden auf ähnliche Weise verwendet, sie werden jedoch in verschiedene Arten unterteilt.

## <a name="types-of-inventory-journals"></a>Arten der Lagererfassung
Die folgenden Lagererfassungstypen stehen zur Verfügung:

-   Bewegung
-   Lagerregulierung
-   Umlagerung
-   Stückliste
-   Wareneingang
-   Produktions-Wareneingang
-   Inventur
-   Markierungen zählen

### <a name="movement"></a>Bewegung

Wenn Sie eine Lagerumlagerungserfassung verwenden, können Sie einem Artikel Kosten hinzufügen, wenn Sie einen Bestand hinzufügen. Sie müssen jedoch die zusätzlichen Kosten manuell einem bestimmten Hauptbuchkonto zuweisen, indem Sie ein Hauptbuchgegenkonto angeben, wenn Sie die Erfassung erstellen. Dieser Lagererfassungstyp ist hilfreich, wenn Sie die Standardbuchungskonten überschreiben möchten.

### <a name="inventory-adjustment"></a>Lagerregulierung

Wenn Sie eine Lagerregulierungserfassung verwenden, können Sie einem Artikel Kosten hinzufügen, wenn Sie einen Bestand hinzufügen. Die Kosten werden automatisch auf ein bestimmten Hauptbuchkonto, basierend auf den Einstellungen des Buchungsprofils der Artikelgruppe gebucht. Verwenden Sie diesen Lagererfassungstyp, um Gewinne und Verluste bei Lagermengen zu aktualisieren, wenn der Artikel weiterhin im standardmäßigen Hauptbuchgegenkonto geführt werden soll. Beim Buchen einer Lagerregulierungserfassung wird ein Lagerzugang oder -abgang gebucht, der Lagerwert wird geändert, und Sachkontobuchungen werden erstellt.

### <a name="transfer"></a>Umlagerung

Sie können Umlagerungserfassungen verwenden, um Artikel zwischen Lagerplätzen, Chargen oder Produktvarianten ohne Kostenauswirkungen zu übertragen. So können Sie beispielsweise Artikel aus einem Lagerort an einen anderen Lagerort innerhalb des gleichen Unternehmens übertragen. Wenn Sie eine Umlagerungserfassung verwenden, müssen Sie sowohl die "von" als auch die "nach" Lagerungsdimensionen angeben (beispielsweise für Standort und Lagerort). Der verfügbare Lagerbestand für die definierten Lagerungsdimensionen ändert sich entsprechend. Bestandumlagerungen beziehen sich auf die direkte Bewegung des Materials. Transportierter Lagerbestand wird nicht nachverfolgt. Wenn der transportierte Lagerbestand nachverfolgt werden muss, sollten Sie stattdessen einen Umlagerungsauftrag verwenden. Beim Buchen einer Umlagerungserfassung werden für jede Erfassungsposition jeweils zwei Lagerbuchungen erstellt:

-   Ein Lagerabgang am Lagerplatz „Von”.
-   Ein Lagerzugang am Lagerplatz „Nach”.

### <a name="bom"></a>Stückliste

Bei der Fertigmeldung einer Stückliste, können Sie eine Stücklistenerfassung erstellen. Wenn Sie eine Stücklistenerfassung verwenden, können Sie die Stückliste direkt buchen. Diese Buchung generiert einen Lagerzugang des Produkts, zusammen mit einer zugeordneten Stückliste und einem Lagerabgang der Produkte, die die Stückliste umfasst. Dieser Lagererfassungstyp ist in Einzel-oder Großserienproduktionsszenarien hilfreich, in denen keine Arbeitspläne erforderlich sind.

### <a name="item-arrival"></a>Wareneingang

Sie können die Wareneingangserfassung verwenden, um die Erfassung von Artikelzugängen zu registrieren (beispielsweise aus Bestellungen). Eine Wareneingangserfassung kann im Rahmen der Eingangsverwaltung auf der Seite **Wareneingangsübersicht** erstellt werden, oder Sie können manuell einen Erfassungseintrag auf der Seite **Wareneingang** erstellen. Wenn Sie die Wareneingangserfassung aktivieren, um nach Entnahmeorte zu suchen, überprüft Supply Chain Management die Lagerplätze für eingegangene Artikel und generiert Lagerplatzziele für die eingehenden Artikel, wenn es Platz findet.

### <a name="production-input"></a>Produktions-Wareneingang

Produktions-Wareneingangserfassungen arbeiten wie Wareneingangserfassungen, werden jedoch für Produktionsaufträge verwendet.

### <a name="counting"></a>Inventur

Mit Inventurerfassungen können Sie den aktuell verfügbaren Lagerbestand korrigieren, der für Artikel oder Gruppen von Artikel erfasst wird, und dann können Sie die tatsächliche physische Zählung buchen, um die Regulierungen vorzunehmen, die zur Abstimmung der Abweichungen erforderlich sind. Sie können Inventurrichtlinien Inventurgruppen zuordnen, um die Gruppierung von Artikeln zu unterstützen, die verschiedene Merkmale haben, sodass diese Artikel in eine Inventurerfassung einbezogen werden können. So können Sie beispielsweise Inventurgruppen einrichten, um Artikel zu zählen, die eine bestimmte Häufigkeit haben, oder um Artikel zu zählen, wenn Bestand unter eine bestimmte Menge sinkt. Informationen darüber, wie Sie Inventurgruppen definieren, finden Sie unter [Lagerinventurprozesse definieren](tasks/define-inventory-counting-processes.md) definieren.

### <a name="tag-counting"></a>Markierungen zählen

Markierungsinventurerfassungen werden verwendet, um eine nummerierte Markierung einem Inventurlos zuzuweisen. Die Markierung sollte eine Markeriungsnummer, eine Artikelnummer und eine Artikelmenge enthalten. Zur Sicherstellung dass eine Markierung nur einmal verwendet wird und alle Markierungen verwendet werden, sollte jede Artikelnummer über einen eindeutige Satz Markierungen verfügen, der einen eigenen Nummernkreis enthält. Drei Statuswerte können für jede Markierung festgelegt werden:

-   **Verwendet** – Die Artikelnummer für diese Markierung wird gezählt.
-   **Storniert** – Die Artikelnummer für diese Markierung wird storniert.
-   **Fehlt** – Die Artikelnummer für diese Markierung fehlt.

Beim Buchen der Markierungs-Inventurerfassung wird auf der Grundlage der Markierungs-Inventurerfassungpositionen eine neue Inventurerfassung erstellt. Weitere Informationen zu Markierungszählung, finden Sie unter [Inventurmarkierungszählung](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Arbeiten mit Erfassungen
Auf eine Erfassungsposition kann zu einem gegebenen Zeitpunkt jeweils nur ein Benutzer zugreifen. Wenn mehrere Benutzer gleichzeitig auf die Erfassungen zugreifen müssen, um Erfassungspositionen zu erstellen, müssen die Benutzer Erfassungen auswählen, die aktuell nicht verwendet werden, um das Überschreiben von Informationen zu verhindern. In den Fällen, in denen mehrere Abteilungen den gleichen Erfassungstyp verwenden, ist es hilfreich, mehrere Erfassungen (beispielsweise eine pro Abteilung) erstellen. Außerdem ist es nützlich, Erfassungen zu unterteilen, sodass jede Buchungsroutine in ihre eigene, eindeutige Lagererfassung eingegeben wird. Erstellen Sie für Buchungsroutinen, die mit Lagerbuchungen zusammenhängen, eine Erfassung für periodische Lagerregulierungen und eine weitere für Bestandszählungen.

## <a name="posting-journal-lines"></a>Buchungserfassungspositionen
Sie können die Erfassungspositionen, die Sie erstellt haben, jederzeit buchen, bis Sie einen Artikel aus weiteren Buchungen sperren. Daten, die Sie in eine Erfassung eingeben, bleiben selbst dann in der Erfassung, wenn Sie die Erfassung schließen, ohne die Positionen zu buchen.

## <a name="data-entity-support-for-inventory-journals"></a>Datenentitätsunterstützung für Lagererfassungen

Datenentitäten unterstützen die folgenden Arten von Integrationsszenarien:
-    Synchroner Dienst (OData)
-  Asynchrone Integration

Weitere Informationen finden Sie unter [Datenentitäten](../../dev-itpro/data-entities/data-entities.md).

> [!NOTE]
> Nicht bei allen Bestandserfassungen ist OData aktiviert. Deshalb können Sie nicht den Excel-Datenkonnektor verwenden, damit Daten veröffentlicht, aktualisiert und zurück in Supply Chain Management importiert werden. 

Ein weiterer Unterschied zwischen den Erfassungsdatenentitäten ist die Fähigkeit, zusammengesetzte Entitäten zu verwenden, die sowohl die Kopfzeilen- als auch Positionsdaten enthalten. Aktuell können Sie die zusammengesetzten Entitäten verwenden für:
-   Lagerregulierungserfassung
-   Lagerbestands-Umlagerungserfassung

Diese beiden Lagererfassungen unterstützen nur das Szenario *Bestand initialisieren* als Teil eines Datenverwaltungs-Importprojekts:
-  Wenn keine Erfassungskopfzeilennummer angegeben ist, aber ein Nummernkreis für den Erfassungstyp angegeben ist, erstellt der Importeinzelvorgang automatisch Erfassungskopfzeilen pro 1000 Positionen. Beispielsweise führt das Importieren von 2020 Positionen zu den folgenden drei Erfassungskopfzeilen:
    -  Kopfzeile 1: enthält 1000 Positionen
    -  Kopfzeile 2: enthält 1000 Positionen
    -  Kopfzeile 3: enthält 20 Positionen
-  Es wird angenommen, dass eindeutige Positionsinformationen pro Bestandsdimension vorhanden sind, was ein Produkt, ein Speicher und Rückverfolgungsangaben sein können. Deshalb ist es nicht möglich, Erfassungspositionen zu importieren, in denen sich nur das Datumsfeld auf den Positionen innerhalb des gleichen Importprojekts unterscheidet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datenentitäten](../../dev-itpro/data-entities/data-entities.md)
