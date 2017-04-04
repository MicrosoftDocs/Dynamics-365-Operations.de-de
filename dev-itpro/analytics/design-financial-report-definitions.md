---
title: Berichtsdefinitionen im Finanzberichtdesigner
description: "Dieser Artikel enthält Informationen zu Berichtsdefinitionen. Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 58 - 18
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81ac503410e51672c2f97a76d37d4c567832912f
ms.lasthandoff: 03/29/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Berichtsdefinitionen im Finanzberichtdesigner

Dieser Artikel enthält Informationen zu Berichtsdefinitionen. Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts. 

Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Eine Berichtsdefinition enthält auch Optionen und Einstellungen, die Sie verwenden können, um Anpassen eines Berichts. Nachdem Sie Zeilendefinitionen und Spaltendefinitionen definieren, müssen Sie sie in einer Berichtsdefinition kombinieren. An diesem Punkt definieren Sie auch andere Aspekte der Definitionen wie die Detailebene und das Berichtsdatum. Sie können einen Bericht dann speichern und generieren. Die Finanzberichterstellung bietet die folgenden Detailebenen an:

-   Wertmäßig
-   Finanzen und Konto
-   Finanzen, Konto und Transaktion

Je nachdem jedoch, wie Daten im Microsoft Dynamics ERP-System gespeichert werden, können Buchungsdetails in den Berichten nicht verfügbar sein.

## <a name="create-a-report-definition"></a>Erstellen einer Berichtsdefinition
1.  Wählen Sie im Berichts-Designer im Menü **Datei** **Neu** und dann **Berichtsdefinition**.
2.  Geben Sie die entsprechenden Informationen auf den Registerkarten **Bericht**, **Ausgabe und Verteilung**, **Kopf- und Fußzeilen** und **Einstellungen** an.

## <a name="contents-of-a-report-definition"></a>Inhalt einer Berichtsdefinition
In der folgenden Tabelle werden die Registerkarten in einer Berichtsdefinition und die Art, wie die Informationen verwendet werden, beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registerkarte</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bericht</td>
<td>Erstellen eines Berichts, Konfigurieren eines Berichts oder Ändern eines vorhandenen Bericht.</td>
</tr>
<tr class="even">
<td>Ausgabe- und Verteilung</td>
<td>Ändern Sie den Ausgabetyp und das Ziel des Berichts.</td>
</tr>
<tr class="odd">
<td>Kopf- und Fußzeilen</td>
<td>Definieren und formatieren Sie die Überschriften und die Fußzeilen für den Bericht. So können Sie Text oder Bilder zur Kopf- oder der Fußzeile hinzufügen. Die Finanzberichterstellung unterstützt BMP-, JPG- und .png-Dateien für Bilder. Sie können auch Autotext-Codes hinzufügen, um weitere Informationen wie einen Unternehmensnamen, Berichtsnamen oder eine Seitenzahl einzufügen.</td>
</tr>
<tr class="even">
<td>Einstellungen</td>
<td>Geben Sie Berichtsdefinitionseinstellungen wie die folgenden Einstellungen an:
<ul>
<li>Formatierung und Rundungsbeträge</li>
<li>Formatdetailberichte</li>
<li>Berichtsbaumstrukturen formatieren</li>
<li>Generieren eines Ausnahmeberichts</li>
<li>Angabe zur Währungsumrechnung</li>
<li>Details zu Zwischensummen und Filterung von Konten</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Siehe auch
--------

[Finanzberichterstellung für Microsoft Dynamics 365 für Arbeitsgänge financial-reporting-intro.md] ()


