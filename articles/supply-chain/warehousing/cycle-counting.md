---
title: Permanente Inventur
description: In diesem Artikel wird beschrieben, wie Sie Zykluszählungen mit der Warehousing-Lösung verwenden können, die in der Warehouse-Verwaltung verfügbar ist. Dieser Artikel gilt nicht für die Warehousing-Lösung, die in der Lagerverwaltung verfügbar ist.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca5ae06a2a6cbe410fadf464bc49071122d0342b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973809"
---
# <a name="cycle-counting"></a>Permanente Inventur

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Zykluszählungen mit der Warehousing-Lösung verwenden können, die in der Warehouse-Verwaltung verfügbar ist. Dieser Artikel gilt nicht für die Warehousing-Lösung, die in der Lagerverwaltung verfügbar ist.

Zykluszählung ist ein Lagerortprozess, den Sie verwenden können, um Artikel des verfügbaren Lagerbestands zu überwachen. Der Zykluszählprozess kann in drei Schritten beschrieben werden:

1.  **Erstellen von Zykluszählungsarbeit** Zykluszählungsarbeit wird automatisch auf Grundlage von Schwellenwertparametern für Artikel oder durch die Verwendung eines Zykluszählungsplans erstellt. Alternativ können Sie Zykluszählungsarbeit auch manuell erstellen, indem Sie die Artikel- oder Lagerortparameter auf der Seite **Zykluszählungsarbeit nach Artikel** oder **Zykluszählungsarbeit nach Lagerplatz** verwenden.
2.  **Zykluszählung verarbeiten** Nachdem Sie Zykluszählungsarbeit erstellt haben, führen Sie die Zykluszählungsarbeit aus, indem Sie Artikel in einem Lagerort zählen und dann ein mobiles Gerät verwenden, um das Ergebnis in Dynamics 365 Supply Chain Management einzugeben. Alternativ können Sie Artikel in einem Lagerort zählen ohne Zykluszählungsarbeit zu erstellen. Dieser Prozess wird als *Stichprobenzykluszählung* bezeichnet.
3.  **Beheben einer Differenz im gezählten Wert** – Nach einer Zykluszählung haben alle Artikel, die Unterschiede im gezählten Wert aufweisen, auf der Seite **Alle Arbeit** den Arbeitsstatus **Prüfung ausstehend**. Sie können diese Differenz auf der Seite **Ausstehende Prüfung der Zykluszählungsarbeit** beheben.

Die folgende Abbildung zeigt den Zykluszählprozess. ![Prozessfluss für Zykluszählung](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Zykluszählung-Voraussetzungen
In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie die Zykluszählung verwenden können.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Artikel</td>
<td>Der Artikel muss für Lagerortverwaltungsprozesse aktiviert werden.</td>
</tr>
<tr class="even">
<td>Lagerort</td>
<td>Der Lagerort muss für Lagerortverwaltungsprozesse aktiviert werden. Um den Lagerort für Lagerortverwaltungsprozesse auf der Seite <strong>Lagerorte</strong> zu aktivieren, wählen Sie den Lagerort aus und wählen dann die Option <strong>Lagerortverwaltungsprozesse verwenden</strong>. Wenn Sie darüber hinaus Arbeitskräften ermöglichen möchten, während einer Zykluszählung Paletten zu bewegen, wählen Sie auf dem Inforegister <strong>Lagerortverwaltung</strong> die Option <strong>Palettenumlagerungen während der Zykluszählung zulassen</strong>.</td>
</tr>
<tr class="odd">
<td>Arbeitspools</td>
<td>Optional: Erstellen eines Arbeitspool, um die Lagerortarbeit, basierend auf der Art der Arbeit (in diesem Fall Zykluszählarbeit) zu trennen.</td>
</tr>
<tr class="even">
<td>Lagerplätze</td>
<td>Aktivieren Sie Zykluszählungen für Lagerplätze. Wählen Sie auf der Seite <strong>Lagerplatzprofile</strong> die Option <strong>Zykluszählungen zulassen</strong> aus, um Zykluszählung für den Lagerort-Lagerplatz zuzulassen.</td>
</tr>
<tr class="odd">
<td>Parameter für Lagerortverwaltung</td>
<td>Richten Sie Parameter für Zykluszählungen ein. Geben Sie auf der Seite <strong>Lagerortverwaltungsparameter</strong> den standardmäßigen Regulierungstypencode, die Arbeitsklassenkennung und die Arbeitspriorität für die Zykluszählung an.</td>
</tr>
<tr class="even">
<td>Mobiles Gerät</td>
<td><ul>
<li>Erstellen Sie ein Menüelement für eine der folgenden Methoden auf der Seite <strong>Menüelemente des mobilen Geräts</strong>:
<ul>
<li>Vom Benutzer geleitete Zykluszählung</li>
<li>Vom System geleitete Zykluszählung</li>
<li>Permanente Inventur-Gruppierung</li>
<li>Permanente Lagerplatzinventur</li>
</ul>
</li>
<li>Richten Sie ein Menü für das mobile Gerät ein.</li>
<li>Erstellen Sie ein Arbeitsbenutzerkonto, und weisen Sie ein Menü des mobilen Geräts der Arbeitsbenutzerkennung zu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zugehörige Einrichtungsaufgabe</td>
<td>Richten Sie einen Zykluszählungsplan für einen Lagerortlagerplatz ein.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Zykluszählungsarbeit automatisch erstellen
Es gibt zwei Möglichkeiten, um die Serienerstellung der Zykluszählungsarbeit zu planen: richten Sie Zyklusinventurschwellenwerte oder Zyklusinventurpläne ein.

-   Ein Zykluszählungsschwellenwert gibt die Mengen- oder Prozentsatzgrenze von Lagerartikeln an. Zykluszählungsarbeit wird automatisch erstellt, wenn der Schwellenwert erreicht wird.
-   Ein Zykluszählungsplan erstellt Zykluszählungsarbeit umgehend oder regelmäßig über einen Batchauftrag. Wenn Zykluszählungsarbeit erstellt wird, enthält die Position der Zykluszählarbeit Informationen dazu, welcher Lagerplatz zu zählen ist. Der verfügbare Lagerbestand, der diesem Lagerplatz zugeordnet ist, wird nicht gesperrt und ist daher für Reservierung und ausgehende Verarbeitungen verfügbar, auch wenn offene Zählarbeit vorhanden ist.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Zykluszählungsarbeit auf der Basis der Schwellenwertparameter für Artikel erstellen

Die Zykluszählungsarbeit kann erstellt werden, wenn die Anzahl der Artikel unter einem bestimmten Schwellenwert an einem Lagerplatz liegt. Beispielsweise gibt es 60 Artikel an einem Ort, der einen Zykluszählungsschwellenwert von 40 hat. Während einer Auftragsbuchung werden 25 Artikel vom Lagerplatz entnommen und in den Staginglagerplatz gelegt. Da die Menge des neuen Artikels mit 35 geringer ist als die Schwellenmenge, wird automatisch Zykluszählungsarbeit für den Speicherort erstellt.

### <a name="schedule-cycle-counting-work"></a>Zykluszählungsarbeit planen

Ein Zykluszählungsplan terminieren, um Zykluszählungsarbeit umgehend oder regelmäßig zu erstellen. Indem Sie Zyklusinventurpläne einrichten, können Sie den Arbeitspool für den die Zyklusinventurarbeit erstellt wird, die maximale Anzahl von Zykluszählungen, die für Artikel an unterschiedlichen Standorten erstellt werden, und die Anzahl der Tage bevor ein Lagerort erneut gezählt, steuern. Beispielsweise ist ein Artikel in drei Lagerplätzen am Lagerort verfügbar, während die maximale Anzahl von Zykluszählungen auf **2** festgelegt ist. Wenn Sie den Zykluszählungsplan ausführen, erstellt er zwei Zykluszählungen für die beiden Lagerplätze, in denen die Artikel vorhanden sind. Ein weiteres Beispiel ist, Sie legen die Anzahl der Tage zwischen den Zykluszählungen auf **5** fest. In diesem Fall wird Zykluszählungsarbeit alle fünf Tage erstellt. Wenn jedoch eine Zykluszählungsarbeit an Tag drei verarbeitet wird, wird die nächste Zykluszählungsarbeit fünf Tage nachdem die letzte Zykluszählung verarbeitet wurde, erstellt, am Tag acht.

## <a name="create-cycle-counting-work-manually"></a>Zykluszählung manuell erstellen
Um Zykluszählungsarbeit manuell zu erstellen, können Sie die Seite **Zykluszählungsarbeit nach Artikel** oder **Zykluszählungsarbeit nach Lagerplatz** verwenden. Sie können die Höchstanzahl der zu erstellenden Zykluszählungen angeben. Wenn beispielsweise der Lagerortleiter einen Wert von **5** angibt, dann wird die Zyklusinventurarbeit für fünf Lagerplätze erstellt, auch wenn der Artikel in 10 verschiedenen Lagerplätzen vorhanden ist. Sie können auch eine Arbeitspool-ID auswählen, der die erstellen Zykluszählungsarbeit-IDs zugewiesen werden. Wenn eine Arbeitspool-ID für die Zykluszählung verarbeitet wird, werden die Zykluszählungsarbeit-IDs, die diesem Arbeitspool zugewiesen sind, als Gruppe verarbeitet.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Zykuszählung mithilfe eines mobilen Geräts ausführen
Es gibt mehrere Möglichkeiten, die Zykluszählungsarbeit mittels Supply Chain Management auf einem mobilen Gerät zu verarbeiten:

-   **Benutzergeleitet** – Die Arbeitskraft kann eine Zykluszählungsarbeit-ID angeben, die im Status **Offen** ist.
-   **Systemgeleitet** – Supply Chain Management weist der Arbeitskraft eine Zykluszählungsarbeit-ID zu.
-   **Zykluszählungs-Gruppierung** - Die Arbeitskraft kann Zykluszählungsarbeit-IDs gruppieren, die für einen bestimmten Lagerplatz, eine bestimmte Zone oder einen Arbeitspool spezifisch sind.
-   **Stichprobenzykluszählung** – Die Arbeitskraft kann Artikel in einem Lagerortlagerplatz jederzeit zählen, ohne Zykluszählungsarbeit zu erstellen. Um eine Stichprobenzykluszählung in einem Lagerplatz auszuführen, gibt die Arbeitskraft die Lagerplatzkennung ein.

Das folgende Beispiel zeigt, wie Sie Stichprobenzykluszählungen ausführen können, indem Sie ein mobiles Gerät verwenden. Die Anweisungen, die die Arbeitskraft auf dem Gerät sieht, variieren abhängig von den Einstellungen des Menüelements für die Stichprobenzykluszählung.

1.  Wählen Sie auf dem mobilen Gerät die Menüoption für die Verarbeitung der Stichprobenzyklusinventurarbeit aus.
2.  Erfassen Sie den Lagerplatz, für den Sie die Stichprobenzykluszählung ausführen wollen.
3.  Erfassen und bestätigen Sie die Artikelnummer und die gezählte Artikelmenge. **Hinweis:** Der Status der Zykluszählungsarbeit wird entweder mit **Prüfung ausstehend** oder **Geschlossen** auf der Seite **Alle Arbeit** aktualisiert, abhängig von den Parametern, die auf der Seite **Arbeitskraft** festgelegt werden.
4.  Optional: Wiederholen Sie Schritt 3 für die übrigen Artikel im Lagerplatz und bestätigen Sie, dass keine zusätzlichen Artikel für die Zählung verfügbar sind.

## <a name="resolve-cycle-counting-differences"></a>Zykluszählungsdifferenzen beheben
Eine Zykluszählungsdifferenz tritt in den folgenden Szenarien auf, wenn die Option **Ist ein Zykluszählungssupervisor** für eine Arbeitsbenutzerkennung auf **Nein** gesetzt ist:

-   Der im Zyklus gezählte Wert befindet sich nicht innerhalb der Abweichungsgrenzen, die in den Feldern **Prozentsatzobergrenze** oder **Mengenobergrenze** auf der Seite **Arbeitsbenutzer** angegeben werden. Beispielsweise ist die Menge des verfügbaren Lagerbestands an einem Ort 50, und die Abweichungsgrenze für den Arbeitsbenutzer ist 10. Wenn der Arbeitsbenutzer einen Wert eingeben, der nicht zwischen 40 und 60 liegt, tritt eine Differenz auf.
-   Der gezählte Wert unterscheidet sich von der Menge des verfügbaren Bestands und es gibt keine festen Abweichungsgrenzen.

Sie können Abweichungen in den gezählten Werten anpassen und dann den gezählten Wert auf der Seite **Ausstehende Prüfung der Zykluszählung** akzeptieren. Sie können die geänderte Anzahl der Artikelmenge auf der Seite **Verfügbarer Lagerbestand nach Lagerplatz** überprüfen. Der gezählte Wert wird abgelehnt, wenn die Differenz nicht genehmigt werden kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Mobile Geräte für Lagerarbeiten einrichten](configure-mobile-devices-warehouse.md)



