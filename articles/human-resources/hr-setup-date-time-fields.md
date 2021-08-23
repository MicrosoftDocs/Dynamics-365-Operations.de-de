---
title: Datums- und Zeitfelder verstehen
description: Verstehen, was zu erwarten ist, wenn Sie Datums- und Zeitfelder in Microsoft Dynamics 365 Human Resources verwenden.
author: andreabichsel
ms.date: 02/03/2020
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
ms.openlocfilehash: cb011ca7b5f4c036b2f49875a256885182564c391c6dd263a0bfa70bbd29f4a7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733539"
---
# <a name="understand-date-and-time-fields"></a>Datums- und Zeitfelder verstehen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datum und Uhrzeit** Felder sind ein grundlegendes Konzept in Dynamics 365 Human Resources. Es ist wichtig, zu verstehen, wie Sie mit **Datum und Uhrzeit**-Daten in Formularen, Dataverse und externen Quellen arbeiten.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Differenz zwischen Datum sowie Datums- und Zeitfeld Datentypen verstehen

**Datum und Uhrzeit** Felder enthalten Zeitzoneninformationen, wohingegen **Datum** Felder nicht. Felder **Datum** werden die gleichen Informationen in jeder beliebigen elektronischen Adresse anzeigen. Wenn Sie ein Datum in ein Feld **Datum** eingeben, schreibt Human Resources das gleiche Datum mit der Datenbank.

Wenn Daten in einem Feld **Datum und Uhrzeit** angezeigt werden, wird Human Resources das Datum und die Uhrzeit auf der Zeitzone des Benutzers anpassen, die im Formular **Benutzeroptionen** eingestellt sind (**Allgemein > Einstellungen > Benutzeroptionen**). Die Datums- und Uhrzeitinformationen, die Sie im Feld eingeben, sind die gleichen wie die Informationen, die in die Datenbank geschrieben werden.

[![Formular Benutzeroptionen.](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Datums- und Zeitfelder in Formularen verstehen 

**Datum und Uhrzeit**-Daten, die auf dem Bildschirm angezeigt werden, sind nicht die gleichen wie die Daten, die in der Datenbank gespeichert werden, wenn die Zeitzone des Benutzers nicht in der koordinierten Weltzeit (UTC) festgelegt wird. Daten in **Datum und Uhrzeit** Felder werden immer als UTC gespeichert.

[![Arbeitskraftformular UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datums- und Zeitfelder in Formularen verstehen 

Wenn Human Resources **Datum und Uhrzeit** Wert in die Datenbank schreibt, werden die Daten in UTC gespeichert. Dies ermöglicht es Benutzern, alle **Datum und Uhrzeit** Daten in der Zeitzone anzuzeigen, die in ihren Benutzeroptionen definiert wird.
 
Im Beispiel oben ist die Startzeit ein Zeitpunkt, kein bestimmtes Datum. Durch das Ändern der Zeitzone des angemeldeten Benutzers für +12 GMT: 00 zu GMT UTC, zeigt derselbe Datensatz 04/30/2019 12:00: 00 statt 05/01/2019 12:00: 00.
  
Im Beispiel weiter unten wird das Beschäftigungsverhältnis des Mitarbeiters 000724 aktiv, unabhängig von der Zeitzone. Der Mitarbeiter wird auf 04/30/2019 in der GMT-Zeitzone aktiv, die gleich ist wie 05/01/2019 in GMT+12:00 Zeitzone. Beide beziehen sich auf den gleichen Zeitpunkt und nicht auf ein bestimmtes Datum. 

[![Arbeitskraftformular GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datums- und Uhrzeitdaten im Datenverwaltungsframework, Excel, Dataverse und Power BI 

Datenverwaltungs-Framework, Excel-Add-In, Dataverse, und Power BI sind Berichte sind alle dazu entworfen, um mit Daten direkt in der Datenbankebene zu interagieren. Da es keinen Clients auftritt, **Datum und Uhrzeit** Daten auf der Zeitzone des Benutzers angepasst, sind alle **Datum und Uhrzeit**-Werte in UTC, das auf mehrere falsche Annahmen führen kann, wenn Daten ein oder anzeigt.  
 
**Datum und Uhrzeit** Daten, die zu DMF, Excel oder Dataverse übermittelt werden, werden wohl auch in UTC von der Datenbank verwendet. Dies kann einige Unklarheiten verursachen, wenn der **Datum und Uhrzeit** Wert nicht wie erwartete angezeigt wird, weil der Benutzer, der die Daten anzeigt, nicht die Zeitzone des Benutzers anzeigt, die in UTC festgelegt ist. 
 
Dasselbe kann umgekehrt auftreten, wenn Daten exportiert werden. Die **Datum und Uhrzeit** Daten in der exportierten DMF-Entität können sich davon unterscheiden, was im Dynamics-Client angezeigt wird. 
 
Wenn externe Quellen wie DMF verwendet werden, um Daten anzuzeigen oder zu erstellen, müssen Sie daran zu denken, dass **Datum und Uhrzeit**-Werte standardmäßig in UTC berücksichtigt werden, unabhängig von der Zeitzone des Computers des Benutzers oder der aktuellen Benutzerzeitzoneneinstellung. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Beispiele desselben Datensatzes, der in verschiedenen Produktbereichen angezeigt wird 

**Human Resources mit Benutzerzeitzone ist auf UTC festgelegt**

[![Auf UTC festgelegtes Arbeitskraftformular.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources mit Benutzerzeitzone ist auf GMT + 12.00 festgelegt** 

[![Auf GMT festgelegtes Arbeitskraftformular.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel über ODaten**

[![Excel über OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**D;F Staging:-**

[![DMF-Staging.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF Export**

[![DMF-Export.](./media/DMFexport.png)](./media/DMFexport.png)

**Excel zu Dataverse**

[![Excel über Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Siehe auch

[Datum und Uhrzeit](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Bevorzugte Zeitzone des Benutzers](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]