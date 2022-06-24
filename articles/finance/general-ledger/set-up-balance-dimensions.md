---
title: Wie richte ich ausgleichende Finanzdimensionen ein?
description: Dieser Artikel beschreibt die Optionen zum Einrichten und Verwenden der Funktion Ausgleichsfinanzdimension.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: dd859629b0eb9f14fa4907699613382f3897d21d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878011"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Wie richte ich ausgleichende Finanzdimensionen ein?

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Optionen zum Einrichten und Verwenden der Funktion Ausgleichsfinanzdimension.

## <a name="symptom"></a>Symptom

Es gibt zwei Möglichkeiten, um ausgleichende Finanzdimensionen einzurichten. Die erste Möglichkeit besteht darin, das Feld **Ausgleich der finanziellen Dimension** im **Ledger** auf der Einrichtungsseite (**Hauptbuch \> Ledger-Einrichtung \> Ledger**) zu verwenden. Die zweite Option besteht darin, das Feld **Erforderliche Dimension für den Ausgleich** auf der Seite **Finanzdimension** (**Hauptbuch > Kontenplan \> Dimension \> Finanzdimension**) zu verwenden. In diesem Artikel wird der Unterschied zwischen diesen beiden Optionen erläutert.

## <a name="resolution"></a>Lösung

Organisationen verwenden in der Regel Ausgleichsdimensionen, um eine Bilanz zu erstellen, die auf der Ebene der Finanzdimension ausgeglichen ist. Durch Aktivieren einer der beiden Funktionen werden gebuchte, unausgeglichene Bemaßungen nicht ausgeglichen. Sie müssen zuerst manuell Korrekturbuchungen eingeben, um die Bilanz auszugleichen, bevor Sie eine der beiden Funktionen aktivieren.

Die zwei Optionen sind einheitlich exklusiv. Die Option, die Ihre Organisation verwendet, sollte auf Ihren Geschäftsanforderungen basieren. Wir hören oft von Kunden, die die Ausgleichsdimension sowohl in der Ledger-Einrichtung als auch in der Finanzdimensions-Einrichtung definieren und dann einige oder alle der zusätzlichen erforderlichen Einstellungen abschließen. Aufgrund eines Ungleichgewichts auf der Ebene der Finanzdimension können sie jedoch immer noch nicht buchen.

In den folgenden Abschnitten werden die beiden Optionen beschrieben und deren Einrichtung erläutert.

### <a name="ledger--balancing-financial-dimension"></a>Sachkonto - Ausgleichende Finanzdimension

Die ausgleichende Finanzdimension auf der **Hauptbuch** Einrichtungsseite wird verwendet, um die Abrechnung zwischen Einheiten zu aktivieren. Folgen Sie diesen Schritten, um die Funktionalität zu aktivieren.

1. Bestimmen Sie, welche Finanzdimension die Ausgleichsdimension sein soll.

    - Mit dieser Funktion können Sie nur eine Finanzdimension als Ausgleichsdimension auswählen.
    - Wählen Sie die Dimension noch nicht auf der Einrichtungsseite **Ledger**.
    - Stellen Sie sicher, dass Ihre Bilanz für die ausgewählte Finanzdimension bereits ausgeglichen ist.

2. Aktualisieren Sie die Kontenstruktur für die ausgleichende Finanzdimension.

    - Sie müssen eine ausgleichende Finanzdimension auswählen, die in allen Kontostrukturen enthalten ist, die dem Sachkonto zugeordnet werden.
    - Die Finanzdimension darf keine Leerzeichen in der Kontostruktur zulassen. Diese Einschränkung stellt sicher, dass jeder Buchhaltungseintrag, der in das Hauptbuch gebucht wird, einen Finanzdimensionswert enthält. Eine leere Dimension ist nicht gültig, wenn ausgleichende Finanzdimensionen verwendet werden.

3. Auf der Seite **Konten für automatische Transaktionen** (**Hauptbuch \> Buchungs-Einrichtung \> Konten für automatische Transaktionen**), definieren Sie die einheitsübergreifenden Soll- und Habenhauptkonten.
4. Auf der Einstellungsseite **Ledger** (**Hauptbuch \> Hauptbuch einrichten \> Ledger**) im Feld **Ausgelichende Finanzdimension** wählen Sie eine Finanzdimension, die Sie für den Ausgleich verwenden können.

Wenn die ausgewählte Finanzdimension beim Erfassen und Buchen von Transaktionen nicht ausgeglichen ist, fügt das System automatisch die Soll- oder Habenbuchungen hinzu, die zum Ausgleichen der Buchungsbuchung beim Buchen erforderlich sind. Die Soll- und Habenkonten für die einheitsübergreifende Transaktion werden auf dem gebuchten Beleg im Hauptbuch angezeigt. Sie werden jedoch nicht in den Journalen oder Quellbelegen angezeigt, für die die Buchhaltungsbuchungen gebucht wurden.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finanzielle Dimensionen – Erfordern, dass die Dimension ausgeglichen ist

Obwohl die ausgleichende Dimension auf der Seite **Finanzdimension** normalerweise von Unternehmen des öffentlichen Sektors verwendet wird, ist die Funktionalität nicht mit einem Konfigurationsschlüssel des öffentlichen Sektors verknüpft. Da es im System keine Einschränkungen gibt, können Sie diese Funktionalität auch dann verwenden, wenn Ihre Organisation keine Einrichtung des öffentlichen Sektors ist.

Diese Funktionalität wird normalerweise im Kundenstamm des öffentlichen Sektors verwendet, da sie erfordert, dass Buchungsdefinitionen verwendet werden, um jede Transaktion automatisch auszugleichen. Es verwendet nicht die einheitenübergreifenden Soll- und Habenkonten, die auf der Seite **Konten für automatische Transaktionen** definiert sind, um die Buchhaltungsbuchungen automatisch auszugleichen. Wenn ein Buchungsposten nach Anwendung der Buchungsdefinitionen auf Dimensionsebene nicht ausgeglichen ist, wird die Transaktion nicht gebucht, selbst wenn die Soll- und Habenkonten zwischen Einheiten definiert sind.

Wir hören oft von Kunden, die die Ausgleichsdimension sowohl in der Ledger-Einrichtung als auch in der Finanzdimensions-Einrichtung definieren. In diesem Fall verwendet das System die Funktionalität der Finanzdimensionen. Die Einrichtung zum Ausgleich von Dimensionen auf Finanzdimensionsebene hat beim Buchen Vorrang. Die Buchung schlägt fehl, wenn die Buchungsdefinition keinen ausgeglichenen Buchungsposten auf Finanzdimensionsebene erstellt.

Führen Sie diese Schritte aus, um die Verwendung einer Ausgleichsdimension auf Finanzdimensionsebene zu aktivieren.

1. Bestimmen Sie, welche Finanzdimensionen die ausgleichende Dimension sein soll.

    - Sie können mehr als eine Finanzdimension als ausgleichende Dimension festlegen.
    - Legen Sie noch nicht die finanziellen Dimensionen fest, die erforderlich sind, um eine Transaktion auf der Seite **Finanzdimension** auszugleichen.

2. Definieren Sie die Buchungsdefinitionen für jede Art von Journal oder Quelldokument, die von Ihrer Organisation verwendet wird. Buchungsdefinitionen verwenden die Sachkonten aus einem nicht gebuchten Journal oder Quellbeleg als Übereinstimmungskriterien. Die Buchungsdefinition gibt dann die generierten Buchungen zurück, die zur Buchhaltungsbuchung werden. Wenn die Buchungsdefinition korrekt eingerichtet ist, enthält der generierte Eintrag die Übereinstimmungskriterien Sachkonten sowie zusätzliche Konten, um den Buchhaltungseintrag auf Dimensionsebene auszugleichen. Weitere Informationen unter [Buchungsdefinitionen](posting-definitions.md). 
   
   Buchungsdefinitionen werden nicht bei jedem Transaktionstyp unterstützt. Buchungsdefinitionen können beispielsweise nicht für Buchungen definiert werden, die über das allgemeine Journal oder das Anlagenjournal eingegeben werden. Wenn für eine Erfassung oder einen Quellbeleg keine Buchungsdefinition definiert werden kann, muss die Transaktion manuell mit dem Finanzdimensionswert ausgeglichen werden. Wenn beispielsweise ein allgemeiner Journaleintrag vorgenommen wird und die Dimension Abteilung die Ausgleichsdimension ist, müssen Sie sicherstellen, dass jeder Abteilungswert ausgeglichen ist.  Wenn die Dimension nicht für jeden Abteilungswert ausgeglichen ist, wird der Beleg erst verbucht, wenn das Ungleichgewicht korrigiert wird, indem dem Beleg manuell eine einheitenübergreifende Belastung oder Gutschrift hinzugefügt wird. 

    > [!IMPORTANT]
    > Wenn eine übermäßige Anzahl von Transaktionen manuell ausgeglichen werden muss, sollten Sie die ausgleichende Dimensionsfunktionalität **nicht** auf der Seite **Finanzdimension** verwenden. Verwenden Sie stattdessen die Funktion zum ausgleichen der Dimensionsfunktionalität auf der Einrichtungsseite **Ledger**.

3. Nachdem die Buchungsdefinitionen definiert wurden, können die Finanzdimensionen als für den Ausgleich erforderlich markiert werden.

Beim Erfassen und Buchen von Transaktionen werden die Buchungsdefinitionen beim Buchen aufgerufen, um die Buchungsbuchungen zu ermitteln. Wenn die Finanzdimensionen ausgeglichen sind, erfolgt die Validierung nach der Ermittlung der Buchhaltungsbuchungen. Wenn die Finanzdimensionen nicht ausgeglichen sind, wird die Transaktion nicht gebucht und Sie erhalten eine Nachricht, die besagt, dass die Belastungen nicht den Gutschriften für eine bestimmte Dimension entsprechen.
