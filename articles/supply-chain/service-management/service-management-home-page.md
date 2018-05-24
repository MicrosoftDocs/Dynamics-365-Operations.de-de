---
title: Serviceverwaltung
description: "Mit der Serviceverwaltung können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
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
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: de-de
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a>Serviceverwaltung 

[!include [banner](../includes/banner.md)]


Mit der **Serviceverwaltung** können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren. In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden. Zudem können Sie in Serviceverträgen festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen. Ein Servicevertrag kann auch eine Vereinbarung zum Servicelevel enthalten, die Standardantwortzeiten festlegt und Tools zum Erfassen der tatsächlichen Zeit anbietet.

Sie können Serviceaufträge erstellen, um Informationen zu geplanten und nicht geplanten Besuchen von einem Servicetechniker am Kundenstandort zu verwalten. Serviceaufträge enthalten beispielsweise folgende Informationen:

1.  Die Arbeitsstunden, die der Servicetechniker ausführt

2.  Der Typ des Service oder der Reparatur

3.  Der zu reparierende Gegenstand, einschließlich Details zu Symptomen und Diagnose

4.  Ausgaben und Gebühren in Bezug auf den Service oder die Reparatur

Debitoren können Serviceanforderungen mit Enterprise Portal über das Internet übermitteln. Sie können diese Anforderungen empfangen, verarbeiten und versenden. Nachdem Sie einen Serviceauftrag erstellt haben, können Sie mithilfe von Servicephasen den Fortschritt überwachen und anhand von Regeln steuern, welche Aktivitäten in jeder Phase aktiviert sind. Wenn ein Serviceauftrag abgeschlossen ist, können Sie den Auftrag abzeichnen, um dessen Vollständigkeit zu bestätigen. Dann können Sie den Auftrag buchen, um den Rechnungsprozess zu starten.

Mithilfe der Berichtstools können Sie Gewinnspannen für Serviceaufträge und Dauerauftragsbuchungen überwachen sowie Arbeitsbeschreibungen und Arbeitsquittungen drucken.

## <a name="business-processes"></a>Geschäftsprozesse

Im folgenden Diagramm werden die Geschäftsprozesse auf oberer Ebene für **Serviceverwaltung** dargestellt. Das Diagramm veranschaulicht, wo Serviceprozesse in andere Module in Microsoft Dynamics 365 for Finance and Operations integriert werden.

[![Geschäftsprozessdiagramm für Serviceverwaltung](./media/sm_home_page.gif)](./media/sm_home_page.gif)

## <a name="service-management-at-a-glance"></a>Serviceverwaltung auf einen Blick

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wichtige Aufgaben</p></th>
<th><p>Primäre Formulare</p></th>
<th><p>Häufig verwendete Berichte</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Serviceverträge erfüllen</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Formular "Servicevereinbarungen"</a></p></td>
<td><p><strong>Gewinnspanne für Serviceauftrag</strong></p></td>
</tr>
<tr class="even">
<td><p>Debitorenabfragen behandeln</a></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Formular "Serviceaufträge"</a></p></td>
<td><p><strong>Arbeitsbeschreibung</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Einsatzplanung (Formular)</a></p></td>
<td><p><strong>Buchung - Dauerauftrag</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><strong>Buchungen von Dauerauftragsgebühren</strong></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a>Integration der Serviceverwaltung

Die Serviceverwaltung kann in die folgenden Module in Microsoft Dynamics 365 for Finance and Operations integriert werden:

  - [Vertrieb und Marketing](../sales-marketing/overview-sales-marketing.md)

  - [Personalverwaltung](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


