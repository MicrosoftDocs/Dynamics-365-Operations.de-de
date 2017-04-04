---
title: Konfigurieren Sie App-Feldnamen in der Warehousing-App
description: "In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Dynamics 365 für Arbeitsgänge definiert und konfiguriert."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurieren Sie App-Feldnamen in der Warehousing-App

In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Dynamics 365 für Arbeitsgänge definiert und konfiguriert. 

** Hinweis: ** Dieses Thema bezieht sich auf Funktionen in der Lager- zu. Es gilt nicht auf Funktionen in der Lagerverwaltung zu. Dynamics 365 für Arbeitsgänge Warehousing - handelt es sich um eine Anwendung, die Sie verwenden können, um Lagerortaufgaben auszuführen. Sie können die und konfigurieren Feldnamen definieren, die in der Zeit-App verwendet werden, sowie die Priorität konfigurieren, der die Feldnamen zugewiesen werden sollen. In diesem Thema wird erläutert, wie Sie diese Lagerort-App-Feldnamen und -Prioritäten definiert und konfiguriert und wie sie in Dynamics 365 - Warehousing für Arbeitsgänge verwendet werden. Ausführliche Informationen dazu, wie der Verbindung zu Dynamics 365 für Arbeitsgänge - Warehousing, erhalten Sie unter " Referenten an [Installieren und Konfigurieren Sie Dynamics 365 für Arbeitsgänge - Warehousing] (install-configure-warehousing-app.md) konfiguriert.

<a name="configure-warehouse-app-field-names"></a>Konfigurieren Sie Lagerort-App-Feldnamen
===================================

Wenn Sie Arbeitsgänge für Dynamics 365 auf dem - Warehousing mobilen Gerät, Sie konfigurieren können, z Metadaten für das Gerät in angezeigt werden sollen Lagerort-App-Feldnamen ** ** Seite. In ein neues Unternehmen in Dynamics 365 für Arbeitsgänge, wählen Sie ** erstellen Sie Standardeinstellungen aus ** um alle Feldnamen zu generieren, die im Workflow des geräts mobilen Lagerort verwendet werden, und weisen Sie diese dann eines bevorzugten Eingabemodus und geben Sie einen Typ zugewiesen. Nachdem Sie alle Feldnamen generiert wurde, können folgende Eingabeoptionen auswählen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mit der folgenden Option...</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bevorzugter Eingabemodus</td>
<td>Mit dieser Option wird definiert, ob eine Bildfläche oder ein Eingabefeld der manuellen Eingabe für den Feldnamen ausgewählten angezeigt werden sollen. Dies ist nützlich, Optionen entsprechend den von Strichcodes zu unterscheiden, wenn für das Feld verwendet werden. <strong>Hinweis:</strong> Für Feldnamen mit das bevorzugte Eingabemodus, der auf festgelegt ist, können Informationen manuell eingeben, wenn der Strichcode nicht lesbar oder beschädigt wird.</td>
</tr>
<tr class="even">
<td>Eingabetyp</td>
<td>Diese Option definiert, welche eingegebener Typ des ausgewählten Feldnamen verwendet werden soll. Vier Optionen sind verfügbar:
<ul>
<li><strong>Auswahl</strong> - enthält eine Liste der Optionen aus, um auszuwählen. Feldnamen mit dieser Option sind nicht bearbeitet werden.</li>
<li><strong>Datum</strong> - Feldnamen, die ab der das Datum angegeben werden, wird ein mit Datumsformat der Beschriftung an. Damit schaffen Lagerarbeitern, in dem Format anzuzeigen, um das Datum zu geben. Feldnamen mit dieser Option sind nicht bearbeitet werden.</li>
<li><strong>Alphanumerische</strong> -, wenn es, die Gerätentastatur aktiviert ist, wird verwendet, wenn die manuelle Informationen in der Zeit-App eingibt. Die Tastaturerfahrung kann geändert werden, je nach Gerät verwendet wird.</li>
<li><strong>Numerisch</strong> Feldnamen für  -, nur die Eingabe numerische verwenden, können Sie diese Option auswählen, um eine benutzerdefinierte Zehnertastatur dem Eingabefeld anstelle der Gerätentastatur anzuzeigen.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurieren Sie Lagerort-App-Feldpriorität
======================================

Auf der Seite Lagerort-App-Feldpriorität ** ** können Sie Tabellen- und andere Prioritätsgruppen zu sperren. Auf diese Weise ist es möglich, entscheiden, welche Informationen auf der Hauptaufgabenseite angezeigt werden sollen, wenn Lagerarbeiter Aufgaben mithilfe der Zeit-App ausführen. Beim Klicken auf… ** erstellen Sie Standardeinstellungen **, wird ein Standardsatz Prioritätsgruppen generiert. Es ist möglich, durch sich nach Bedarf erstellen, aber nur drei Prioritätsgruppen werden der auf die angezeigt. Wenn Dynamics 365 für Arbeitsgänge und Metadaten Zeit-App sendet, weist diese jedes der Felder einen relativen Priorität abhängig von seiner Prioritätsstufe zu, und der Zeit-App werden die ersten drei an, die sich in den Metadaten auf der Aufgabenseite enthalten sind. Der Rest der überfließenden Metadaten werden auf einer sekundären Detailseite angezeigt. Die folgende Tabelle enthält ein Beispiel der fünf sich an.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritätsstufe</th>
<th>Zugewiesene Felder</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Priorität 10</td>
<td><ul>
<li>Artikel</li>
<li>Leistung</li>
<li>Maßeinheit</li>
</ul></td>
</tr>
<tr class="even">
<td> Priorität 20</td>
<td><ul>
<li>Clusterposition</li>
<li>Cluster</li>
</ul></td>
</tr>
<tr class="odd">
<td> Priorität 30</td>
<td><ul>
<li>Artikelbeschreibung</li>
</ul></td>
</tr>
<tr class="even">
<td> Priorität 40</td>
<td><ul>
<li>Variante</li>
<li>Farbe</li>
<li>Größe</li>
<li>Formatvorlage</li>
</ul></td>
</tr>
<tr class="odd">
<td> Priorität 50</td>
<td><ul>
<li>Ziel</li>
<li>Ladungsträger</li>
</ul></td>
</tr>
</tbody>
</table>

Wenn beispielsweise ein Lagerarbeiter eine Aufgabe auf einem mobilen Gerät ausführt, wenn die Metadaten, die in der Zeit-App angezeigt werden, besteht aus den folgenden Feldern:

-   Artikel
-   Leistung
-   Maßeinheit
-   Artikelbeschreibung
-   Größe und Lagerplatz

Basierend auf den Lagerort-App-Feldpriorität, die in der Tabelle) eingerichtet wird, werden die folgenden Zeilen 3 von der Informationen auf die angezeigt:

-   Zeile 1: Artikel, Menge, Einheit
-   Zeile 2: Artikelbeschreibung
-   Zeile 3: Größe

Die verbleibenden Metadaten beispielsweise Lagerplatz, werden nicht auf der Aufgabenseite angezeigt, sondern werden auf einer Detailseite angezeigt. Um Weitere Informationen und Beispiele der Benutzeroberfläche anzuzeigen, finden Sie in der Blogbeitrag an an [Dynamics 365 für Arbeitsgänge ankündigend - Warehousing] (https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Siehe auch
--------

[Installieren und Konfigurieren von Microsoft Dynamics 365 für Arbeitsgänge – Warehousing] (install-configure-warehousing-app.md)


