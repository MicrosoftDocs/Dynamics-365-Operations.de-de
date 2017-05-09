---
title: Sperrung von Lagerbestand
description: "Dieser Artikel gibt einen Überblick über die Sperrung von Lagerbestand, die Teil des Qualitätsprüfungsprozesses in Microsoft Dynamics AX ist. Sie können die Sperrung von Lagerbestand verwenden, um die Verarbeitung oder den Verbrauch von Artikeln zu verhindern."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0d7e37de63e6c63b5d7942a84de60ef8f3984cde
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-blocking"></a>Sperrung von Lagerbestand

[!include[banner](../includes/banner.md)]


Dieser Artikel gibt einen Überblick über die Sperrung von Lagerbestand, die Teil des Qualitätsprüfungsprozesses in Microsoft Dynamics AX ist. Sie können die Sperrung von Lagerbestand verwenden, um die Verarbeitung oder den Verbrauch von Artikeln zu verhindern.

Sie können Lagerartikel auf die folgenden Arten sperren:
-   Manuell
-   Per Erstellung eines Qualitätsprüfungsauftrags
-   Per Nutzung eines Vorgangs, bei dem ein Qualitätsprüfungsauftrag generiert wird
-   Mithilfe der Lagerstatussperrung

## <a name="blocking-items-manually"></a>Manuelle Sperrung von Artikeln
Sie können eine bestimmte Menge eines Artikels sperren, indem Sie auf der Seite **Sperrung von Lagerbestand** eine Transaktion erstellen. Es können nur Artikel manuell gesperrt werden, die als verfügbarer Lagerbestand vorhanden sind. Bei manuell gesperrten Mengen müssen Sie entscheiden, ob Planungsaktivitäten erwartete Zugänge als eine zu erwartende verfügbare Menge einbeziehen. Bei erwarteten Zugängen handelt es sich um gesperrte Artikel, von denen Sie erwarten, dass sie nach Abschluss der Prüfung als verfügbarer Lagerbestand vorhanden sind. Sie können das erwartete Datum beibehalten. Standardmäßig ist die Option **Erwartete Zugänge** für Artikel ausgewählt, die durch eine Testbestellung gesperrt sind. Sie können eine manuelle Sperre für eine Menge stornieren, indem Sie die Transaktion auf der Seite **Sperrung von Lagerbestand** löschen.

## <a name="blocking-items-by-creating-a-quality-order"></a>Sperren von Artikeln per Erstellung einer Testbestellung
Sie können Artikel angeben, die überprüft werden müssen, indem Sie eine Testbestellung auf der Seite **Testbestellungen** erstellen. Wenn Sie eine Testbestellung erstellen, wird die Menge, die Sie für einen Artikel angeben, gesperrt. Der Musteraufnahmeplan, der einer Testbestellung zugeordnet ist, steuert nur die Menge der Artikel, die überprüft werden müssen, nicht die Menge, die gesperrt wird. Die Menge, die in der Testbestellung eingegeben wird, ist die Menge, die gesperrt wird, ungeachtet der Menge, die gemäß der Angaben des Musteraufnahmeplans zur Prüfung eingereicht werden sollte.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Sperrung von Artikeln mithilfe eines Prozesses, bei dem eine Testbestellung generiert wird
Wenn ein Qualitätsprozess angibt, dass ein Artikel überprüft werden muss, wird eine Menge des Artikels automatisch gesperrt. Wenn daher eine Testbestellung automatisch generiert wird, steuert der der Testbestellung zugeordnete Musteraufnahmeplan sowohl die Menge der Artikel, die gesperrt wird, als auch die Menge, die geprüft werden muss. Wenn die Option **Vollständige Sperrung** auf der Seite **Artikelmusteraufnahme** ausgewählt ist, wird die gesamte Menge beispielsweise einer Bestellposition während der Überprüfung gesperrt, unabhängig von der Menge der Artikelmusteraufnahme.
### <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Qualitätsprüfungsauftrag generiert, wenn ein Lieferschein für eine Bestellung gebucht wird. Auf der Seite **Qualitätszuordnungen** haben Sie angegeben, dass das Buchen eines Lieferscheins für eine Bestellung der Prozess ist, der eine Testbestellung aktiviert.

|Einrichten                                                                     |Benutzeraktivität                 |Ergebnis             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Eine Qualitätszuordnung gibt an, dass beim Buchen eines Lieferscheins für eine Bestellung eine Testbestellung generiert werden muss. In den Einstellungen für die Artikelmusteraufnahme der Testbestellung ist angegeben, dass 10 Prozent der Menge der Bestellposition geprüft werden müssen. Weil darüber hinaus die Option **Vollständige Sperrung** bei den Einstellungen für die Artikelmusteraufnahme ausgewählt ist, muss die gesamte Menge der Bestellposition während der Prüfung unabhängig von der zur Prüfung eingereichten Menge gesperrt werden. | Der Lieferschein wird gebucht. | Ein Qualitätsprüfungsauftrag wird generiert. Zehn Prozent der Bestellmenge für den Artikel wird Prüfung eingereicht. Die Gesamtmenge der Bestellposition wird gesperrt. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Sperrung von Artikeln mithilfe der Lagerstatussperrung
Sie können angeben, welche Lagerstatus Sperrenstatus sind, indem Sie den Parameter **Sperrung von Lagerbestand** auf der Seite **Lagerstatus** verwenden.  Sie können Lagerstatus nicht als Sperrenstatus für Produktionsaufträge, Aufträge, Umlagerungsaufträge, ausgehende Transaktionen oder Projektintegrationen verwenden. Für ausgehende Arbeit verwenden Sie Artikel, die den Bestandsstatus "verfügbar" aufweisen. Wenn Artikel den Status **Kaputt** haben und der Produktprogrammplan für diese Artikel ausgeführt wird, werden die Artikel als fehlend betrachtet und der Bestand wird automatisch aufgefüllt.



<a name="see-also"></a>Siehe auch
--------

[Erstellen und Verwalten einer Sperrung von Lagerbestand (Aufgabenleitfaden)](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Qualitätsmanagementprozesse](quality-management-processes.md)

[Überprüfen Sie die Qualität von Waren (Aufgabenleitfaden)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)




