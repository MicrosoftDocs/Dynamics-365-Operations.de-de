---
title: Kontostrukturen konfigurieren
description: Dieser Artikel enthält Informationen zu Kontostrukturen und Finanzdimensionen.
author: aprilolson
ms.date: 10/14/2022
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
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713942"
---
# <a name="configure-account-structures"></a>Kontostrukturen konfigurieren

[!include[banner](../includes/banner.md)]

Kontostrukturen verwenden die Hauptkonten und Finanzdimensionen, um eine Gruppe von Regeln zu erstellen, die die Reihenfolge und die Werte festlegt, die bei der Eingabe der Kontonummer verwendet werden. Sie können so viele Kontenstrukturen einrichten, wie Sie für Ihr Unternehmen benötigen. Die Kontostrukturen werden dem Sachkonto einer Firma zugewiesen, sodass sie gemeinsam genutzt werden können.

Beim Anlegen einer Kontostruktur ist die maximale Anzahl der Segmente 11. Wenn Sie mehr als 11 Segmente benötigen, sollten Sie Ihre Einrichtung und Ihre Anforderungen gründlich prüfen, da dies Auswirkungen auf die Benutzerfreundlichkeit hat. Überlegen Sie, ob ein Segment in einem Berichterstellungsszenario über eine Hierarchie anstelle der Dateneingabe oder über ein benutzerdefiniertes Feld abgeleitet werden könnte. Wenn Sie z.B. über den Standort berichten möchten, aber den Standort nach Abteilung oder Kostenstelle abbilden können, benötigen Sie den Standort nicht als finanzielle Dimension. Wenn Sie nach der Auswertung mehr als 11 Segmente benötigen, können Sie über erweiterte Regeln weitere Segmente hinzufügen.

Kontostrukturen benötigen das Hauptkonto. Das Hauptkonto muss nicht das erste Segment in der Struktur sein, aber es zeigt an, welche Kontostruktur bei der Eingabe der Kontonummer verwendet wird. Aus diesem Grund kann ein Hauptkontowert nur in einer dem Sachkonto zugeordneten Struktur vorhanden sein, damit sich diese nicht überschneiden. Nachdem die Kontostruktur identifiziert wurde, wird die Liste der zulässigen Werte gefiltert, um den Benutzer durch die Auswahl nur gültiger Dimensionswerte zu führen, wodurch die Möglichkeit eines falschen Journaleintrag verringert wird.

> [!NOTE] 
> Wenn Sie planen, gegen eine Finanzdimension zu budgetieren, muss diese Teil einer Kontostruktur sein. Die Budgetierung verwendet derzeit keine erweiterten Regeln.

## <a name="example"></a>Beispiel
Um eine bewährte Methode für den Aufbau einer Kontostruktur zu veranschaulichen, nehmen wir an, dass ein Unternehmen seine Bilanzkonten (100000..399999) auf der Ebene der Finanzdimension der Konten- und Unternehmenseinheit verfolgen möchte. Für Umsatzerlöse und Ausgabenkonten (400000..999999) verfolgen sie die Finanzdimensionen Unternehmenseinheit, Abteilung und Kostenstelle. Wenn sie einen Verkauf machen, verfolgen sie auch gerne den Debitor. In diesem Szenario wäre es empfehlenswert, dem Hauptbuch der Firma zwei Kontostrukturen zuzuweisen - eine für Bilanzkonten und eine für Gewinn- und Verlustkonten. Um die Benutzerfreundlichkeit und Prüfung zu optimieren, sollte Debitor eine erweiterte Regel sein, die nur bei Verwendung eines Verkaufskontos genutzt wird.

**Bilanzkontostruktur**

|Hauptkonto          | Unternehmenseinheit    |
|----------------------|-----------|
|100000..399999 | *;„&nbsp;“|

**GuV-Kontostruktur**

|Hauptkonto          | Unternehmenseinheit    |Abteilung          | Kostenstelle    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;„&nbsp;“| \*;„&nbsp;“| \*;„&nbsp;“| \*;„&nbsp;“|

**Erweiterte Regel für das Hinzufügen eines Debitors**

Kriterien: Wenn das Hauptkonto zwischen 400000 und 499999 liegt, dann fügen Sie einen Debitor hinzu. Es kann nicht leer gelassen werden.

|Kunde         |
|-----------------|
|\* |

In diesem vereinfachten Beispiel sind alle Werte und Leerzeichen zugelassen, also werden \* und „&nbsp;“ verwendet.

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

## <a name="more-than-seven-criteria-needed"></a>Mehr als sieben Kriterien erforderlich

Wenn Sie mehr als sieben Kriterien benötigen, können Sie diese in der nächsten Zeile hinzufügen. Bei der Arbeit im Abschnitt **Details zu zulässigem Wert** werden Sie feststellen, dass das Kriterium **+Neue hinzufügen** nach der Eingabe des siebten Kriteriums nicht mehr aktiv ist. Dies ist auf viele Faktoren zurückzuführen, wie zum Beispiel: 
 - Spaltenbreite 
 - Wie die Daten gespeichert werden 
 - Leistung des Steuerelements **Zulässige Wertdetails**
 - Benutzerfreundlichkeit  

> [!NOTE]
> Ein Upgrade von Microsoft Dynamics AX 2012, bei dem mehr als sieben Kriterien angegeben werden, wird nicht unterstützt. Es muss korrigiert werden, bevor Sie das Upgrade auf Finance und Vorgänge Apps abschließen. 

Um weitere Kriterien hinzuzufügen, klicken Sie auf **Duplizieren im Segment** und **Details zu zulässigem Wert**. Dies kopiert die Kriterien an eine neue Position. Sie können dann den Abschnitt **Details zu zulässigem Wert** überschreiben oder ändern.

## <a name="best-practices"></a>Bewährte Vorgehensweisen
Beim Festlegen Ihrer Kontostrukturen gibt es einige bewährte Verfahren, die Sie befolgen können. Dies ist jedoch nur eine Orientierungshilfe, so dass eine ganzheitliche Diskussion über Ihr Unternehmen, Ihren Wachstumsplan und Ihren Wartungsplan als Teil dieser Diskussion betrachtet werden sollte.

- Stellen Sie das Hauptkonto an die erste Stelle oder so nah wie möglich an die Spitze der Kontostruktur, damit die Benutzer bei der Kontoerfassung die bestmögliche Anleitung erhalten.
  
  - Vergewissern Sie sich, dass alle Lösungen von Drittanbietern, die Sie verwenden möchten, das Hauptkonto an erster Stelle unterstützen.

- Verwenden Sie die Kontostrukturen so weit wie möglich wieder, um die Pflege Ihrer juristischen Personen zu reduzieren.

- Bei Abweichungen zwischen den einzelnen juristischen Personen sollten Sie die Verwendung erweiterter Regeln in Betracht ziehen, damit die Kontostrukturen wiederverwendet werden können.

- Verwenden Sie bei der Definition der zulässigen Werte möglichst viele Bereiche und Platzhalter. So können Sie nicht nur ohne Wartung wachsen und ändern, sondern das System arbeitet auch mit dieser Konfiguration besser.

- Setzen Sie nicht nur ein Sternchen für jedes Segment in der Kontostruktur und verlassen Sie sich dann ausschließlich auf die erweiterten Regeln. Dies kann schwierig zu handhaben sein und führt häufig zu Fehlern bei der Wartung, die dazu führen können, dass das System nicht buchen kann.

## <a name="account-structure-activation"></a>Kontostrukturaktivierung
Wenn Sie mit Ihrer neuen Einrichtung oder einer Änderung der Kontostruktur zufrieden sind, müssen Sie diese aktivieren. Wenn eine Kontostruktur einem Sachkonto zugeordnet ist, kann diese Aktivierung ein langwieriger Prozess sein, da alle nicht gebuchten Vorgänge im System mit der neuen Struktur synchronisiert werden müssen. Gebuchte Transaktionen werden von Änderungen der Kontenstruktur nicht beeinflusst. Ab Anwendungsversion 10.0.31 steht in der Funktionsverwaltung eine neue Funktion mit der Bezeichnung **Leistungssteigerung bei der Aktivierung der Kontenstruktur** zur Verfügung. Weitere Informationen zu dieser neuen Funktion für die Aktivierung der Kontenstruktur finden Sie unter [Leistungssteigerung bei der Aktivierung der Kontenstruktur](account-structure-improvement.md). 

Weitere Informationen finden Sie unter [Planen Sie Ihren Kontenplan](plan-chart-of-accounts.md), [Finanzielle Dimensionen](financial-dimensions.md) und [Erfassen Sie Konto- und Dimensionskombinationen (segmentierte Erfassungssteuerung)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
