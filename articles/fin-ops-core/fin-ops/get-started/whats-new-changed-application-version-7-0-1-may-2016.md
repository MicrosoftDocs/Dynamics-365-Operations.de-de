---
title: Neuheiten und Änderungen in Dynamics AX 7.0.1 (Mai 2016)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0.1 entweder neu oder geändert sind. Diese Version wurde im Mai 2016 veröffentlicht und hat die Build-Nummer 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6bd40873d6890bc837188cba1aa1125d874f6bda
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178029"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Neuheiten und Änderungen in Dynamics AX 7.0.1 (Mai 2016)

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0.1 entweder neu oder geändert sind. Diese Version wurde im Mai 2016 veröffentlicht und hat die Build-Nummer 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronische Berichterstellung (ER, Elektronic Reporting)

| Wie können Sie vorgehen? | Warum ist dieses wichtig? |
|------------------|------------------------|
| Konfigurieren Sie ein Laufzeit-Dialogfeld für die elektronische Berichterstellung, über das der Benutzer die gewünschten Finanzdimensionen auswählen kann. | Zur Laufzeit können die Benutzer im Dialogfeld für die Ausführung eines ER-Berichts mehrere Finanzdimensionen auswählen. Die Details der ausgewählten Finanzdimensionen werden im generierten elektronischen Dokument angezeigt. |
| Konfigurieren des Zugriffs auf mehrere Finanzdimensionen beim Entwurf eines ER-Berichts über eine einzelne Zuordnung zur gewünschte Datenquelle. | Die selbe ER Berichtskonfiguration kann verwendet werden, um elektronische Dokumente zu generieren, die Buchungsdaten mit Details zu Finanzdimensionen anzeigen – und zwar unabhängig von der Anzahl der Finanzdimensionen die vom Benutzer ausgewählt oder für die aktuelle juristische Person oder Instanz konfiguriert sind. |
| Konfigurieren eines Er-Berichts zur Eingabe von Daten in dynamisch generierten Spalten eines elektronischen Dokuments, dass im OPENXML-Arbeitsblattformat erstellt wurde. | Ein ER-Bericht kann über horizontal replizierte spalten Daten in einem generierten OPENXML-Arbeitsblatt eingeben. Daher kann eine ER Berichtskonfiguration zur Generierung von elektronischen Dokumenten genutzt werden, die unterschiedlich viele dynamisch generierte Spalten haben. |
| Konfigurieren von ER-Zielen für die Umleitung des Ausgabeergebnisses eines Formats an ein bestimmtes Ziel: Datei, E-Mail und Archivierung (Microsoft SharePoint-Ordner oder Microsoft Azure Storage). | Zuvor wurde bei der Ausführung einer ER-Konfiguration ein Meldungsfeld angezeigt, bei dem eine Benutzeraktion zum Speichern oder Öffnen einer Datei erforderlich war. Sie können nun ein separates Ziel für jede Formatkonfiguration und für jede Ausgabenkomponente (einen Ordner oder eine Datei) vorkonfigurieren. Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail

| Wie können Sie vorgehen? | Warum ist dieses wichtig? |
|------------------|------------------------|
| Verwenden des Google Chrome-Browsers. | Einzelhändler können nun Cloud POS über den Chrome-Browser nutzen und alle Funktionen verwenden, die in der Microsoft Edge und Internet Explorer über Cloud POS verfügbar sind. |

## <a name="financial-reporting"></a>Finanzberichterstellung

| Wie können Sie vorgehen? | Warum ist dieses wichtig? |
|------------------|------------------------|
| Neu Erstellen der Finanzberichterstellungs-Data Mart-Datenbank. | Wenn Sie Dynamics AX-Datenbanken zwischen Umgebungen verschieben oder andere invasive Änderungen an der Umgebung vornehmen, muss möglicherweise die Finanzberichterstellungsdatenbank neu erstellt werden. Ein Windows PowerShell-Skript wird nun bereitgestellt, mit dem die Datenbank für Sie neu erstellt wird. |
| Sie können nicht mehr ungültige Designer Berichtsoptionen auswählen. | Mehrere Designer-Optionen, die in den veröffentlichten Versionen von Management Reporter verwendeten wurden, gelten nicht für diese Version von Dynamics AX. Diese Optionen betrafen das Finanzberichtsdesign, die Ausgabe und das Verknüpfen. Diese Optionen wurden aus dem Finanzberichtsdesigner entfernt, um Benutzerfehler zu verhindern. |

## <a name="financial-management"></a>Finanzverwaltung

| Wie können Sie vorgehen? | Warum ist dieses wichtig? |
|------------------|------------------------|
| Generieren positiver Lohndateien für Kreditorenkontozahlungen. | Um Scheckbetrug zu verhindern können positive Lohndateien generiert werden. |

## <a name="warehouse-and-production"></a>Lagerort und Produktion

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definieren Sie eine Lagerortrichtlinie, die die Erstellung der Arbeit für eine Reihe von Produkten an bestimmten Lagerorten steuert.</td>
<td>Lagerortprozesse enthalten nicht immer Arbeit. Wenn Sie die neue Lagerortarbeitsrichtlinie verwenden, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern.</td>
</tr>
<tr>
<td>Geben Sie an, dass ein Warenausgangslagerplatz nicht über Ladungsträger gesteuert wird.</td>
<td>Sie können nun festlegen, dass ein Produktausgangslagerplatz nicht über Ladungsträger gesteuert wird. Diese Funktion eignet sich beispielsweise, wenn Upstream-Fertigungsauftrag Artikel direkt an einen Lagerort als fertiggestellt meldet der als Produktionseingangslagerort für einen Downstream-Produktionsauftrag agiert.</td>
</tr>
<tr>
<td>Unterstützung für Stücklisten, die Artikel mit unterschiedlichen Produktdimensionen desselben Artikels umfassen.</td>
<td>Wenn Sie eine oder mehrere der Produktdimensionen in der Produktion verwenden, treten Situationen auf, in denen Sie einen Artikel auf Basis einer Variante des gleichen Artikels produzieren möchten. Weitere Informationen finden Sie <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">in diesem Blog</a>.</td>
</tr>
<tr>
<td>Fertigungsaufträge mit Zirkularitätsstrukturen auf der ersten Ebene ihrer Stücklisten sind von der Kalkulation der Materialressourcenplanung auf Stücklistenebene ausgeschlossen.</td>
<td>Es ist nicht möglich, korrekte Stücklistenebenen zu Produktvarianten für Fertigungsaufträge zuzuweisen die einen in der Stücklistenhierarchie einen Verweis auf sich selbst darstellen.</td>
</tr>
<tr>
<td>Berechnen separater Stücklistenebenen für die Materialressourcenplanung und Kostenkalkulation:
<ul>
<li>Für die Materialressourcenplanung werden Stücklistenebenen in der neuen Tabelle <strong>ReqItemLevel</strong> kalkuliert. Beendete Fertigungsaufträge werden bei der Berechnung ignoriert.</li>
<li>Für die Berechnung der Produktionskosten werden Stücklistenebenen in der Tabelle <strong>InventTable</strong> berechnet. Beendete Fertigungsaufträge werden bei der Berechnung einbezogen.</li>
</ul>
</td>
<td>
<ul>
<li>Bei der Ausführung der Materialressourcenplanung (beispielsweise die Produktprogrammplanplanung und -auflösung) müssen nur Stücklistenebenen neu berechnet werden, die zur Materialressourcenplanung genutzt werden. Es ist also nicht erforderlich die zur Produktionskostenberechnung verwendeten Stücklistenebenen neu zu berechnen.</li>
<li>Bei der Ausführung von Nachkalkulationsvorgängen (beispielsweise der Lagerabschluss) müssen nur zur Produktionskostenkalkulation verwendete Stücklistenebenen neu berechnet werden.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neuheiten und Änderungen](whats-new-changed.md)

[Neue oder aktualisierte Aufgabenleitfäden (Mai 2016)](new-updated-task-guides-available-may-2016.md)
