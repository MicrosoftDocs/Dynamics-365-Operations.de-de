---
title: "Serviceaufträge kombinieren"
description: "Sie können Serviceaufträge kombinieren."
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
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a>Serviceaufträge kombinieren   

[!include [banner](../includes/banner.md)]


Beim automatischen Erstellen von Serviceauftragspositionen im Formular **Serviceverträge** können Sie eine der folgenden Optionen wählen, um die Art der Gruppierung anzugeben:

  - **Nach Servicevertrag**

  - **Nach Serviceaufgabe**

  - **Nach Mitarbeiter**

  - **Nach Serviceobjekt**

## <a name="example"></a>Beispiel

Sie erstellen eine Servicevereinbarung mit dem Startdatum 31.03.2007. Wählen Sie im Feld **Serviceaufträge kombinieren** **Nach Serviceobjekte** aus. Anschließend erstellen Sie die folgenden Servicevertragspositionen:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Vereinbarungspositionsnummer</p></th>
<th><p>Buchungsart</p></th>
<th><p>Beschreibung</p></th>
<th><p>Intervall</p></th>
<th><p>Serviceobjekt</p></th>
<th><p>Eintrittstermin</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Stunde</strong></p></td>
<td><p>SVP1</p></td>
<td><p>Wöchentlich</p></td>
<td><p>X-1</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Stunde</strong></p></td>
<td><p>SVP2</p></td>
<td><p>Zweiwöchentlich</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Stunde</strong></p></td>
<td><p>SVP3</p></td>
<td><p>Wöchentlich</p></td>
<td><p>X-2</p></td>
<td><p>01.04.2007</p></td>
</tr>
</tbody>
</table>


Sie geben keine Zeitfenster für die Servicevertragspositionen an. Daher werden die Serviceauftragspositionen nicht vom berechneten Tag, auf den sie fallen, verschoben.

Nun erstellen Sie mit dem Formular **Erstellen von Serviceaufträgen** Serviceauftragspositionen vom 01.04.2007 bis zum 30.04.2007.

Insgesamt werden 10 Serviceaufträge erstellt. Da Sie **Nach Serviceobjekt** als Einstellung für die Zusammenfassung ausgewählt haben, verfügen alle erstellten Serviceaufträge nur über Serviceauftragspositionen mit einem bestimmten Serviceobjekt. Aus der Servicevereinbarung generierte Serviceauftragspositionen mit gleichem Servicedatum und Objekt werden im gleichen Serviceauftrag zusammengefasst.


> [!NOTE]
> <P>In diesem Beispiel hat der im Formular <STRONG>Serviceverwaltungsparameter</STRONG> angegebene Kalender keine geschlossenen Tage.</P>



Die weitere Gruppierung von Serviceauftragspositionen in Serviceaufträge erfolgt gemäß den einzelnen Zeitfenstern, die in den Servicevertragspositionen jeweils angegeben sind.

## <a name="see-also"></a>Siehe auch

[Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md)

  



