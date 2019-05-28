---
title: Interaktion zwischen Servicestatus und Statusfeld
description: Im Formular "Serviceauftärge wird im Feld "Fortschritt" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "Statusberichte" wird der Status der einzelnen Serviceauftragspositionen angegeben.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570785"
---
# <a name="service-status-and-progress-field-interaction"></a>Interaktion zwischen Servicestatus und Statusfeld 

[!include [banner](../includes/banner.md)]


Im Formular "**Serviceauftärge** wird im Feld "**Fortschritt**" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "**Statusberichte**" wird der Status der einzelnen Serviceauftragspositionen angegeben.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Position 1 Status</p></th>
<th><p>Position 2 Status</p></th>
<th><p>Position 3 Status</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>In Bearbeitung</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>In Bearbeitung</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>In Bearbeitung</strong></p></td>
<td><p><strong>Erstellt</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Gebucht</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Gebucht</strong></p></td>
<td><p><strong>Gebucht</strong></p></td>
<td><p><strong>Gebucht</strong></p></td>
<td><p><strong>Gebucht</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Gebucht</strong></p></td>
<td><p><strong>Gebucht</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
<td><p><strong>Storniert</strong></p></td>
</tr>
</tbody>
</table>


Der Fortschritt eines Serviceauftrags vollzieht sich, wenn alle Positionen den Status **Erstellt** besitzen. Er ist nach wie vor aktiv, wenn einige der Positionen den Status **Storniert** oder **Gebucht** besitzen.

Werden alle Positionen in einem Serviceauftrag als **Gebucht** markiert, lautet der Fortschritt des Statusauftrags **Gebucht**. Gilt für einige Positionen der Status **Gebucht** und für andere **Storniert**, gilt für den Fortschritt nach wie vor der Status **Gebucht**.

  


