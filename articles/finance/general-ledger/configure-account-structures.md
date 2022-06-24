---
title: Kontostrukturen konfigurieren
description: Dieser Artikel enthält Informationen zu Kontostrukturen und Finanzdimensionen.
author: aprilolson
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0a3febf8d269caec847ad879f60ac042e5fec9e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907979"
---
# <a name="configure-account-structures"></a>Kontostrukturen konfigurieren

[!include[banner](../includes/banner.md)]

Kontostrukturen verwenden die Hauptkonten und Finanzdimensionen, um eine Gruppe von Regeln zu erstellen, die die Reihenfolge und die Werte festlegt, die bei der Eingabe der Kontonummer verwendet werden. Sie können so viele Kontenstrukturen einrichten, wie Sie für Ihr Unternehmen benötigen. Die Kontostrukturen sind den Sachkonto-Einstellungen zugeordnet, so dass sie gemeinsam genutzt werden können.

Beim Anlegen einer Kontostruktur ist die maximale Anzahl der Segmente 11. Wenn Sie mehr Segmente als diese benötigen, sollten Sie Ihre Einstellungen und Ihre Anforderungen gründlich auswerten, da dies Auswirkungen auf die Benutzerfreundlichkeit hat. Überlegen Sie, ob ein Segment in einem Berichterstellungsszenario über eine Hierarchie anstelle der Dateneingabe oder über ein benutzerdefiniertes Feld abgeleitet werden könnte. Wenn Sie z.B. am Lagerplatz berichten möchten, aber den Lagerplatz nach Abteilung oder Kostenstelle darstellen können, benötigen Sie den Lagerplatz nicht als Finanzdimension. Wenn Sie nach der Auswertung mehr als 11 Segmente benötigen, können Sie über erweiterte Regeln weitere Segmente hinzufügen.

Kontostrukturen benötigen das Hauptkonto. Das Hauptkonto muss nicht das erste Segment in der Struktur sein, aber es identifiziert, welche Kontostruktur bei der Eingabe der Kontonummer verwendet wird. Aus diesem Grund kann ein Hauptkontowert nur in einer dem Sachkonto zugeordneten Struktur existieren, damit sie sich nicht überlappen. Nachdem die Kontostruktur identifiziert wurde, wird die Liste der zulässigen Werte gefiltert, um den Benutzer durch die Auswahl nur gültiger Dimensionswerte zu führen, wodurch die Möglichkeit eines falschen Journaleintrag verringert wird.

> [!NOTE] 
> Wenn Sie planen, gegen eine Finanzdimension zu budgetieren, muss diese Teil einer Kontostruktur sein. Die Budgetierung verwendet derzeit keine erweiterten Regeln.

## <a name="example"></a>Beispiel
Um eine bewährte Methode für den Aufbau einer Kontostruktur zu veranschaulichen, nehmen wir an, dass ein Unternehmen seine Bilanzkonten (100000..399999) auf der Ebene der Finanzdimension der Konten- und Unternehmenseinheit verfolgen möchte. Für Umsatzerlöse und Ausgabenkonten (400000..999999) verfolgen sie die Finanzdimensionen Unternehmenseinheit, Abteilung und Kostenstelle. Wenn sie einen Verkauf machen, verfolgen sie auch gerne den Debitor. In diesem Szenario empfiehlt es sich, dem Unternehmenssachkonto zwei Kontostrukturen zuzuordnen - eine für Bilanzkonten und eine für GuV-Konten. Um die Benutzerfreundlichkeit und Prüfung zu optimieren, sollte Debitor eine erweiterte Regel sein, die nur bei Verwendung eines Verkaufskontos genutzt wird.

**Bilanzkontostruktur**

|Hauptkonto          | Unternehmenseinheit    |
|----------------------|-----------|
|100000..399999 | *;” “|

**GuV-Kontostruktur**

|Hauptkonto          | Unternehmenseinheit    |Abteilung          | Kostenstelle    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;„ “| \*;„ “| \*;„ “| \*;„ “|

**Erweiterte Regel für das Hinzufügen eines Debitors**

Kriterien: Wenn das Hauptkonto zwischen 400000 und 499999 liegt, dann fügen Sie einen Debitor hinzu. Es kann nicht leer gelassen werden.

|Kunde         |
|-----------------|
|* |

In diesem vereinfachten Beispiel sind alle Werte und Leerzeichen erlaubt, so dass * und " " verwendet werden.

## <a name="segments-and-allowed-values"></a>Segmente und zulässige Werte
Der Abschnitt **Segmente** und **Details zu zulässigem Wert** bietet eine Rastererfahrung für die Eingabe der Regeln, die bei der Prüfung während der Buchung befolgt werden. Sie können in den Zellen direkt im Raster eingeben, aus Excel importieren oder den Abschnitt **Details zu zulässigem Wert** verwenden, um Sie durch das Raster zu führen.

Der Abschnitt **Details zu zulässigem Wert** führt Sie durch das Erstellen von Kriterien mit **Operatoren** wie z.B. Beginnt mit, ist zwischen, umfasst und viele andere.

[![Werte zulassen.](./media/account.png)](./media/account.png) 

Zulässige Werte werden standardmäßig auf einer Erfassungs- oder Buchhaltungsverteilungseintrags-Seite angezeigt, wenn gemäß der Kontostruktureinrichtung keine anderen möglichen Werte gibt, die ausgewählt werden können

Dies ist ein Beispiel der **Gewinn- und Verlust-Kontostruktur**.

|Hauptkonto          | Unternehmenseinheit    |Abteilung          | Kostenstelle    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Beim Eingeben einer Erfassung und dem Auswählen eines Kontos im Gewinn- und Verlustbereich, führt die Auswahl von Unternehmenseinheit „002“ dazu, dass Werte 022 und 014 standardmäßig in der Kontosteuerung angezeigt werden. Dieses Verhalten tritt auch auf der Buchhaltungsverteilungsseite auf. 

## <a name="more-than-7-criteria-needed"></a>Mehr als 7 Kriterien erforderlich

Wenn Sie mehr als 7 Kriterien benötigen, können Sie diese in der nächsten Zeile hinzufügen. Bei der Arbeit im Abschnitt **Details zu zulässigem Wert** werden Sie feststellen, dass das Kriterium **+Neue hinzufügen** nach der Eingabe des siebten Kriteriums nicht mehr aktiv ist. Dies ist auf viele Faktoren zurückzuführen, wie zum Beispiel: 
 - Spaltenbreite 
 - Wie die Daten gespeichert werden 
 - Leistung des Steuerelements **Zulässige Wertdetails**
 - Benutzerfreundlichkeit  
 
Um weitere Kriterien hinzuzufügen, klicken Sie auf **Duplizieren im Segment** und **Details zu zulässigem Wert**. Dies kopiert die Kriterien an eine neue Position. Sie können dann den Abschnitt **Details zu zulässigem Wert** überschreiben oder ändern.

## <a name="best-practices"></a>Optimale Verfahren
Bei der Einrichtung Ihrer Kontostruktur gibt es einige bewährte Methoden, die Sie befolgen können. Dies ist jedoch nur eine Orientierungshilfe, so dass eine ganzheitliche Diskussion über Ihr Unternehmen, Ihren Wachstumsplan und Ihren Wartungsplan als Teil dieser Diskussion betrachtet werden sollte.

- Erstellen Sie das Hauptkonto zuerst oder so weit wie möglich vorne in der Kontostruktur, damit die Benutzer die bestmögliche geführte Erfahrung während der Kontoeingabe erhalten.

- Verwenden Sie die Kontostrukturen so weit wie möglich wieder, um die Pflege Ihrer juristischen Personen zu reduzieren.

- Bei Abweichungen zwischen den einzelnen juristischen Personen sollten Sie die Verwendung erweiterter Regeln in Betracht ziehen, damit die Kontostrukturen wiederverwendet werden können.

- Verwenden Sie bei der Definition der zulässigen Werte möglichst viele Bereiche und Platzhalter. So können Sie nicht nur ohne Wartung wachsen und ändern, sondern das System arbeitet auch mit dieser Konfiguration besser.

- Setzen Sie nicht nur ein Sternchen für jedes Segment in der Kontostruktur und verlassen Sie sich dann ausschließlich auf die erweiterten Regeln. Dies kann schwierig zu handhaben sein und führt häufig zu Fehlern bei der Wartung, die dazu führen können, dass das System nicht buchen kann.

## <a name="account-structure-activation"></a>Kontostrukturaktivierung
Wenn Sie mit Ihrer neuen Einrichtung oder einer Änderung der Kontostruktur zufrieden sind, müssen Sie diese aktivieren. Wenn eine Kontostruktur einem Sachkonto zugeordnet ist, kann diese Aktivierung ein langwieriger Prozess sein, da alle nicht gebuchten Vorgänge im System mit der neuen Struktur synchronisiert werden müssen. Gebuchte Transaktionen werden nicht durch Kontostrukturänderungen beeinflusst.

Weitere Informationen finden Sie unter [Ihren Kontenplan planen](plan-chart-of-accounts.md), [Finanzdimensionen](financial-dimensions.md), [Eingeben von Konto- und Dimensionskombinationen (segmentierte Eintragssteuerung)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
