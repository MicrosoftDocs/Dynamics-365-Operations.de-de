---
title: Konfigurieren Sie App-Feldnamen in der Warehousing-App
description: "In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d029481d31a0064a193e2cb9eeaf79df28bfa159
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurieren Sie App-Feldnamen in der Warehousing-App

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden. 

**Hinweis:** Dieser Artikel gilt für Funktionen im Modul "Lagerortverwaltung". Er gilt nicht für Funktionen im Modul "Bestandverwaltung". Finance and Operations - Warehousing ist eine Anwendung, die Sie verwenden können, um Lagerortaufgaben auszuführen. Sie können die Feldnamen definieren und konfigurieren, die in der App verwendet werden und die Priorität konfigurieren, der die Feldnamen zugewiesen werden sollen. In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden. Ausführliche Informationen dazu, wie die Verbindung zu Finance and Operations - Warehousing konfiguriert wird, finden Sie im Lernprogramm [Installieren und Konfigurieren von Finance and Operations - Warehousing](install-configure-warehousing-app.md).

## <a name="configure-warehouse-app-field-names"></a>Konfigurieren von Lagerort-Feldnamen in der App

Wenn Sie Arbeitsgänge für Finance and Operations - Warehousing auf Ihrem mobilen Gerät nutzen, können Sie auf der Seite **Lagerort-App-Feldnamen** konfigurieren, wie Metadaten für das Gerät angezeigt werden sollen. In einem neuen Unternehmen in Finance and Operations wählen Sie **Standardeinstellungen erstellen** aus, um alle Feldnamen zu generieren, die im Workflow des mobilen Geräts für Lagerort verwendet werden, und weisen Sie diesen dann einen bevorzugten Eingabemodus zu, und geben Sie einen Typ ein. Nachdem Sie alle Feldnamen generiert haben, können folgende Eingabeoptionen auswählen.

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
<td>Mit dieser Option wird definiert, ob eine Bildfläche oder ein Eingabefeld oder eine manuelle Eingabe für den Feldnamen ausgewählt und angezeigt werden sollen. Dies ist nützlich, um Felder entsprechend den Strichcodes zu unterscheiden, wenn solche für das Feld verwendet werden. <strong>Hinweis:</strong> Für Feldnamen mit bevorzugtem Eingabemodus wählen Sie <strong>Durchsuchen</strong>. Sie können Informationen manuell eingeben, wenn der Strichcode nicht lesbar oder beschädigt wird.</td>
</tr>
<tr class="even">
<td>Eingabetyp</td>
<td>Diese Option definiert, welcher eingegebene Typ des ausgewählten Feldnamen verwendet werden soll. Es sind vier Optionen verfügbar:
<ul>
<li><strong>Auswahl</strong> - Enthält eine Liste der Optionen zum Auszuwählen. Feldnamen mit dieser Option können nicht bearbeitet werden.</li>
<li><strong>Datum </strong> -Feldnamen, definiert als Datum zeigen das Datumsformat der Beschriftung an. Damit können Lagerarbeiter sehen, welches Datumsformat sie eingeben müssen. Feldnamen mit dieser Option können nicht bearbeitet werden.</li>
<li><strong>Alphanumerisch</strong> - Wenn ausgewähltes, wird die Gerätentastatur verwendet, um die Informationen manuell in de App einzugeben. Die Tastaturerfahrung kann geändert werden, je nach Gerät, das verwendet wird.</li>
<li><strong>Numerisch</strong> - Für Feldnamen, die nur numerische Eingaben verwenden; Sie könne diese Option auswählen, um eine benutzerdefinierte Zehnertastatur dem Eingabefeld anstelle der Gerätentastatur anzuzeigen.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Feldpriorität in Lagerortanwendung konfigurieren

Auf der Seite L **agerort-App-Feldpriorität** können Sie Feldnamen anderen Prioritätsgruppen zuweisen. Auf diese Weise ist es möglich, zu entscheiden, welche Informationen auf der Hauptaufgabenseite angezeigt werden sollen, wenn Lagerarbeiter Aufgaben mithilfe der App ausführen. We nn Sie auf **Standardeinstellungen erstellen** klicken, wird ein Standardsatz von Prioritätsgruppen generiert. Es ist möglich, beliebig viele Prioritätsgruppen zu erstellen, aber es werden nur drei Prioritätengruppen auf der Aufgabenseite angezeigt. Wenn Finance and Operations Metadaten an die App sendet, weist diese jedem der Felder eine relative Priorität abhängig von seiner Prioritätsstufe zu, und die App zeigt die ersten drei Prioritätengruppen an, die in den Metadaten auf der Aufgabenseite enthalten sind. Der Rest der überfließenden Metadaten wird auf einer sekundären Detailseite angezeigt. Die folgende Tabelle enthält ein Beispiel der fünf Prioritätengruppen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritätsgruppe</th>
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

Ein Lagerarbeiter führt beispielsweise eine Aufgabe auf einem mobilen Gerät aus, wenn die Metadaten, die angezeigt werden, folgende Felder aufweisen:

-   Artikel
-   Leistung
-   Maßeinheit
-   Artikelbeschreibung
-   Größe und Standort

Basierend auf der Lagerort-App-Feldpriorität, die in der Tabelle oben eingerichtet wird, werden die folgenden 3 Zeilen der Informationen auf der Aufgabenseite angezeigt:

-   Zeile 1: Artikel, Menge, Maßeinheit
-   Reihe 2: Artikelbeschreibung
-   Zeile 3: Größe

Die verbleibenden Metadaten beispielsweise Lagerplatz, werden nicht auf der Aufgabenseite angezeigt, sondern werden auf einer Detailseite angezeigt. Weitere Informationen und Beispiele der Benutzeroberfläche finden Sie im Blogbeitrag [Ankündigung Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Installieren und Konfigurieren von Microsoft Dynamics 365 for Finance and Operations – Warehousing](install-configure-warehousing-app.md)




