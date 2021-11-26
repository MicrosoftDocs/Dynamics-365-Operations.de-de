---
title: Datums- und Zeitfelder verstehen
description: Dieses Thema erklärt, was zu erwarten ist, wenn Sie Datums- und Zeitfelder in Microsoft Dynamics 365 Human Resources verwenden.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728588"
---
# <a name="understand-date-and-time-fields"></a>Datums- und Zeitfelder verstehen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datum und Uhrzeit** Felder sind ein grundlegendes Konzept in Microsoft Dynamics 365 Human Resources. Es ist wichtig, dass Sie verstehen, wie Sie mit **Datum und Uhrzeit**-Daten auf Seiten in Dataverse und in externen Quellen arbeiten.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Differenz zwischen Datum sowie Datums- und Zeitfeld Datentypen verstehen

**Datum und Uhrzeit**-Felder enthalten Zeitzoneninformationen, **Datum**-Felder dagegen nicht. **Datum**-Felder zeigen die gleichen Informationen in jeder beliebigen elektronischen Adresse. Wenn Sie ein Datum in ein **Datum**-Feld eingeben, wird das gleiche Datum in die Datenbank geschrieben.

Wenn Daten in einem **Datum und Uhrzeit**-Feld angezeigt werden, werden das Datum und die Uhrzeit auf der Zeitzone des Benutzers angepasst, die auf der Seite **Benutzeroptionen** eingestellt ist (**Allgemein \> Einstellungen \> Benutzeroptionen**). Datums- und Uhrzeitinformationen, die Sie im Feld eingeben, sind die gleichen wie die Informationen, die in die Datenbank geschrieben werden.

[![Seite „Benutzeroptionen“.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Datums- und Zeitfelder auf Seiten verstehen 

**Datum und Uhrzeit**-Daten, die auf dem Bildschirm angezeigt werden, sind nicht die gleichen wie die Daten, die in der Datenbank gespeichert werden, wenn die Zeitzone des Benutzers nicht in der koordinierten Weltzeit (UTC) festgelegt wird. Daten in **Datum und Uhrzeit** Felder werden immer als UTC gespeichert.

[![UTC Seite „Arbeitskraft“.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datums- und Zeitfelder in Formularen verstehen 

Wenn ein **Datum und Uhrzeit**-Wert in die Datenbank geschrieben wird, werden die Daten als UTC gespeichert. Dadurch können Benutzer sehen, alle **Datum und Uhrzeit** Daten in der Zeitzone sehen, die in ihren Benutzeroptionen definiert wird.
 
Im Beispiel oben ist die Startzeit ein Zeitpunkt, kein bestimmtes Datum. Durch das Ändern der Zeitzone des angemeldeten Benutzers für +12 GMT: 00 zu GMT UTC, zeigt derselbe Datensatz 04/30/2019 12:00: 00 statt 05/01/2019 12:00: 00.

Im Beispiel weiter unten wird das Beschäftigungsverhältnis des Mitarbeiters 000724 unabhängig von der Zeitzone aktiv. Der Mitarbeiter wird auf 04/30/2019 in der GMT-Zeitzone aktiv, die gleich ist wie 05/01/2019 in GMT+12:00 Zeitzone. Beide beziehen sich auf den gleichen Zeitpunkt und nicht auf ein bestimmtes Datum. 

[![GMT Seite „Arbeitskraft“.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datums- und Uhrzeitdaten im Datenverwaltungsframework, Excel, Dataverse und Power BI 

Das Datenverwaltungsframework (DMF), Excel-Add-In, Dataverse, und Power BI sind Berichte sind alle dazu entworfen, um mit Daten direkt in der Datenbankebene zu interagieren. Da es keinen Clients auftritt, **Datum und Uhrzeit** Daten auf der Zeitzone des Benutzers angepasst, sind alle **Datum und Uhrzeit**-Werte in UTC, das auf mehrere falsche Annahmen führen kann, wenn Daten ein oder anzeigt.
 
Wenn **Datum und Uhrzeit**-Daten, die zu DMF, Excel oder Dataverse übermittelt werden, geht die Datenbank davon aus, dass sie in UTC sind. Wenn jedoch Benutzer, die die Daten anzeigen, ihre Benutzerzeitzone nicht auf UTC eingestellt haben, wird der übermittelte **Datum und Uhrzeit**-Wert nicht wie erwartet angezeigt, was für die Benutzer verwirrend sein kann. 
 
Dasselbe kann umgekehrt auftreten, wenn Daten exportiert werden. Die **Datum und Uhrzeit** Daten in der exportierten DMF-Entität können sich davon unterscheiden, was im Dynamics-Client angezeigt wird. 
 
Wenn externe Quellen wie DMF verwendet werden, um Daten anzuzeigen oder zu erstellen, müssen Sie daran zu denken, dass **Datum und Uhrzeit**-Werte standardmäßig in UTC berücksichtigt werden, unabhängig von der Zeitzone des Computers des Benutzers oder der aktuellen Benutzerzeitzoneneinstellung. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Beispiele desselben Datensatzes, der in verschiedenen Produktbereichen angezeigt wird 

**Human Resources mit Benutzerzeitzone ist auf UTC festgelegt**

[![Auf UTC festgelegte Arbeitskraftseite.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources mit Benutzerzeitzone ist auf GMT + 12.00 festgelegt** 

[![Auf GMT festgelegte Arbeitskraftseite.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel über ODaten**

[![Excel über OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**D;F Staging:-**

[![DMF-Staging.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF Export**

[![DMF-Export.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel zu Dataverse**

[![Excel über Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Siehe auch

[Datum und Uhrzeit](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Bevorzugte Zeitzone des Benutzers](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
