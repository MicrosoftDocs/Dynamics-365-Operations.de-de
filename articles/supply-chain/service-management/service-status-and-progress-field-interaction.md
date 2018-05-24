---
title: Interaktion zwischen Servicestatus und Statusfeld
description: "Im Formular \"Serviceauftärge wird im Feld \"Fortschritt\" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter \"Statusberichte\" wird der Status der einzelnen Serviceauftragspositionen angegeben."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

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

  



