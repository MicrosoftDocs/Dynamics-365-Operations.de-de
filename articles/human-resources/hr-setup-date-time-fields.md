---
title: Datums- und Zeitfelder verstehen
description: Verstehen, was zu erwarten ist, wenn Sie Datums- und Zeitfelder in Microsoft Dynamics 365 Human Resources verwenden. Erhalten Sie Klarheit, was Sie erwartet, wenn Sie mit Datums- und Zeitdaten in einem Formular in Human Resources, als externe Quelle, oder in Common Data Service interagieren.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529851"
---
# <a name="understand-date-and-time-fields"></a>Datums- und Zeitfelder verstehen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datum und Uhrzeit** Felder sind ein grundlegendes Konzept in Dynamics 365 Human Resources. Es ist wichtig, zu verstehen, wie **Datum und Uhrzeit** Daten in einem Dynamics 365 Human Resources Formular, Common Data Service und externen Quellen arbeiten.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Differenz zwischen Datum sowie Datums- und Zeitfeld Datentypen verstehen

**Datum und Uhrzeit** Felder enthalten Zeitzoneninformationen, wohingegen **Datum** Felder nicht. Felder **Datum** werden die gleichen Informationen in jeder beliebigen elektronischen Adresse anzeigen. Wenn Sie ein Datum in ein Feld **Datum** eingeben, schreibt Human Resources das gleiche Datum mit der Datenbank.

Wenn Daten in einem Feld **Datum und Uhrzeit** angezeigt werden, wird Human Resources das Datum und die Uhrzeit auf der Zeitzone des Benutzers anpassen, die im Formular **Benutzeroptionen** eingestellt sind (**Allgemein > Einstellungen > Benutzeroptionen**). Die Datums- und Uhrzeitinformationen, die Sie im Feld eingeben, sind die gleichen wie die Informationen, die in die Datenbank geschrieben werden.

[![Formular Benutzeroptionen](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Datums- und Zeitfelder in Formularen verstehen 

Wenn sie Daten in einem Feld **Datum und Uhrzeit** eingeben, sind die Daten, die auf dem Bildschirm angezeigt werden, nicht die gleichen wie die Daten, die in der Datenbank gespeichert werden, wenn die Zeitzone des Benutzers nicht in der koordinierten Weltzeit (UTC) festgelegt wird. Daten in **Datum und Uhrzeit** Felder werden immer als UTC gespeichert.

[![Formular Arbeitskraft](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datums- und Zeitfelder in Formularen verstehen 

Wenn Human Resources **Datum und Uhrzeit** Wert in die Datenbank schreibt, werden die Daten in UTC gespeichert. Dies ermöglicht es Benutzern, alle **Datum und Uhrzeit** Daten in der Zeitzone anzuzeigen, die in ihren Benutzeroptionen definiert wird.
 
Im Beispiel oben ist die Startzeit ein Zeitpunkt, kein bestimmtes Datum. Durch das Ändern der Zeitzone des angemeldeten Benutzers für +12 GMT: 00 zu GMT UTC, wird dieselbe Anzeige erstellt die  04/30/2019 12:00: 00 statt 05/01/2019 12:00: 00 anzeigt.
  
Im Beispiel weiter unten wird das Beschäftigungsverhältnis des Mitarbeiters 000724 aktiv, unabhängig von der Zeitzone. Der Mitarbeiter wird auf 04/30/2019 in der GMT-Zeitzone aktiv, die gleich ist wie 05/01/2019 in GMT+12:00 Zeitzone. Beide beziehen sich auf den gleichen Zeitpunkt und nicht auf ein bestimmtes Datum. 

[![Formular Arbeitskraft](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Datums- und Uhrzeitdaten im Datenverwaltungsframework, Excel, Common Data Service und Power BI 

Datenverwaltungs-Framework, Excel-Add-In, Common Data Service, und Power BI sind Berichte sind alle dazu entworfen, um mit Daten direkt in der Datenbankebene zu interagieren. Da es keinen Clients auftritt, **Datum und Uhrzeit** Daten auf der Zeitzone des Benutzers angepasst, sind alle **Datum und Uhrzeit**-Werte in UTC, das auf mehrere falsche Annahmen führen kann, wenn Daten ein oder anzeigt.  
 
**Datum und Uhrzeit** Daten, die zu DMF, Excel oder Common Data Service übermittelt werden, werden wohl auch in UTC von der Datenbank verwendet. Dies kann einige Unklarheiten verursachen, wenn der **Datum und Uhrzeit** Wert nicht wie erwartete angezeigt wird, weil der Benutzer, der die Daten anzeigt, nicht die Zeitzone des Benutzers anzeigt, die in UTC festgelegt ist. 
 
Dasselbe kann umgekehrt auftreten, wenn Daten exportiert werden. Die **Datum und Uhrzeit** Daten in der exportierten DMF-Entität können sich davon unterscheiden, was im Dynamics-Client angezeigt wird. 
 
Wenn externe Quellen wie DMF verwendet werden, um Daten anzuzeigen oder zu erstellen, ist es wichtig, daran zu denken, dass **Datum und Uhrzeit**-Werte standardmäßig in UTC berücksichtigt werden, unabhängig von der Zeitzone des Computers des Benutzers oder der aktuellen Benutzerzeitzoneneinstellung. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Beispiele desselben Datensatzes, der in verschiedenen Produktbereichen angezeigt wird 

**Human Resources mit Benutzerzeitzone ist auf UTC festgelegt**

[![Formular Arbeitskraft](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources mit Benutzerzeitzone ist auf GMT + 12.00 festgelegt** 

[![Formular Arbeitskraft](./media/worker-form4.png)](./media/worker-form4.png)

**Excel über ODaten**

[![Excel über ODaten](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**D;F Staging:-**

[![DMF Staging:-](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF Export**

[![DMF Staging:-](./media/DMFexport.png)](./media/DMFexport.png)

**Excel zu Common Data Service**

[![Excel zu Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Siehe auch

[Datum und Uhrzeit](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Bevorzugte Zeitzone des Benutzers](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]