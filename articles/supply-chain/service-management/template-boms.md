---
title: "Vorlagenstücklisten"
description: "Mit einer Vorlagenstückliste verfügen Sie über eine standardisierte Liste von Komponenten für Serviceobjekte, die regelmäßig verwaltet werden."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e3a16b9938f6d4222e0a95078356f457e71a1bb
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="template-boms"></a>Vorlagenstücklisten    

[!include [banner](../includes/banner.md)]


Mit einer Vorlagenstückliste verfügen Sie über eine standardisierte Liste von Komponenten für Serviceobjekte, die regelmäßig verwaltet werden. Die in der Vorlagenstückliste aufgeführten Komponenten stellen die einzelnen Unterkomponenten des Serviceobjekts dar. Indem Sie eine Vorlagenstückliste auf ein Serviceobjekt anwenden, können Sie die verfolgen, welche Unterkomponenten im Serviceobjekt ersetzt wurden.

Um eine Vorlagenstückliste auf eine Servicevereinbarung oder einen Serviceauftrag anzuwenden, ordnen Sie sie einer Serviceobjektbeziehung zu.


> [!NOTE]
> <P>Einem Serviceobjekt kann nur eine Vorlagenstückliste zugeordnet werden.</P>

## <a name="create-a-template-bom"></a>Erstellen einer Vorlagenstückliste

Die folgende Tabelle enthält Informationen zu den verschiedenen Methoden, die Sie zum Erstellen einer Vorlagenstückliste verwenden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Produktion</p></td>
<td><p>Die Vorlagenstückliste basiert auf einem Produktionsauftrag. Diese Option kann nur angewendet werden, wenn Sie innerhalb einer Produktionsumgebung agieren. Der Vorteil besteht darin, dass Sie über eine aktuelle und umfassende Auflistung der Komponenten eines Artikels verfügen.</p></td>
</tr>
<tr class="even">
<td><p>Artikel BOM</p></td>
<td><p>Die Vorlagenstückliste basiert auf einer Artikelstückliste. Die Artikelstückliste ist im Gegensatz zur Produktionsstückliste eine statische Liste der Komponenten, die einen Artikel bilden.</p></td>
</tr>
<tr class="odd">
<td><p>Vorhandene Vorlage</p></td>
<td><p>Die Vorlage basiert auf einer vorhandenen Vorlagenstückliste.</p></td>
</tr>
<tr class="even">
<td><p>Manuell</p></td>
<td><p>Wenn Sie genau wissen, welche Ersatzteile in der Regel in einem Serviceobjekt ersetzt werden, können Sie die Vorlagenstückliste manuell erstellen. Mit dieser Methode können leichter Sie sicherstellen, dass die in der Vorlage enthaltenen Komponenten die tatsächlichen Anforderungen des Arbeitsplatzes widerspiegeln.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Wenden Sie die Vorlagenstückliste auf eine Servicevereinbarung oder einen Serviceauftrag an

Die Vorlagenstückliste kann auf eine Servicevereinbarung, einen Serviceauftrag oder beides angewendet werden. Die Servicevereinbarung deckt in der Regel eine langfristige Beziehung zu einem Debitor ab. Bei dem in der Vorlagenstückliste aufgezeichnete Verlauf von Ersetzungen handelt es sich um nützliche Daten für die Servicevereinbarung.

Vorlagenstücklisten können auch auf einen Serviceauftrag angewendet werden, um den Verlauf der Dienstleistung erfassen, die an einem Serviceobjekt erbracht wurde.

## <a name="copy-the-history-of-a-service-bom"></a>Kopieren des Verlaufs einer Servicestückliste

Der Verlauf einer Servicestücklistenposition kann zwischen Servicevereinbarungen kopiert werden. Durch das Kopieren des Serviceverlaufs zwischen Servicevereinbarungen kann der Datensatz zu Ersetzungen für einen Artikel erhalten werden.

**Beispiel**

Sie haben eine Servicevereinbarung über drei Jahre für das Auto eines Kunden eingerichtet. Während dieser Periode gewöhnt sich der Debitor an den guten Service, die das Unternehmen anbietet. Nach dem Ablauf der Vereinbarung möchte der Debitor daher eine neue Vereinbarung treffen. Sie können nun eine günstigere Vereinbarung für das Unternehmen aushandeln. Da der Datensatz ersetzter Komponenten in der Zukunft nützlich sein kann, kopieren Sie den Verlauf der Servicestückliste in die neue Vereinbarung.

## <a name="modify-the-template-bom"></a>Ändern der Vorlagenstückliste

Wenn eine Vorlagenstückliste keinem Serviceobjekt zugeordnet wurde, können Sie sie ändern oder Positionen daraus löschen. Nach der Zuordnung der Vorlagenstückliste zu einem Serviceobjekt kann nur die lokale Version der Stückliste geändert werden. Zum Duplizieren der Einstellungen der lokalen Version einer Vorlagenstückliste kann eine neue Vorlagenstückliste auf Grundlage der der lokalen Version erstellt werden. Weitere Informationen zu Serviceintervallen finden Sie unter [Ändern einer Servicestückliste](modify-service-bom.md).

Wenn Sie einen Artikel in der Stückliste ersetzen, können Sie die Ersetzung in der Stücklistenposition im Stücklisten-Designer erfassen. Optional können Sie eine Serviceauftragsposition für das Ersetzungsobjekt erstellen. Wenn Sie eine Serviceauftragsposition erstellen, können Sie den Ersetzungsartikel fakturieren. Wenn keine Serviceauftragsposition für eine Ersetzung erstellt wird, wird die Ersetzungserfassung zum Nachverfolgen des Verlaufs des Serviceobjekts in den Datensätzen beibehalten.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Ändern, wie Informationen zu Stücklistenposition angezeigt werden

Die Anzeige der Stücklistenpositionsdaten kann für alle Vorlagen- und Servicestücklisten geändert werden. Die Änderungen werden auf alle Vorlagen- und Servicestücklisten angewendet. Hierzu gehören auch diejenigen, die Serviceobjekten zugeordnet sind.

## <a name="set-up-number-sequences-for-template-boms"></a>Einrichten von Nummernkreisen für die Vorlagenstückliste

Um Vorlagenstücklisten verwenden möchten, müssen Sie zwei Nummernkreise einrichten. Richten Sie einen Nummernkreis für die Vorlagenstückliste und einen die für die Positionsnummer des Stücklistenverlaufs ein.


> [!NOTE]
> <P>Nummernkreise werden in Microsoft Dynamics AX verwendet, um Datensätzen, die dies erfordern, Kennungen zuzuweisen. Bevor Sie einen Nummernkreis einer Vorlagenstückliste oder Positionsnummer des Stücklistenverlaufs zuweisen können, müssen Sie Nummernkreiscodes einrichten.</P>


## <a name="set-up-number-sequences"></a>Nummernkreise einrichten

1.  Erstellen Sie auf der Listenseite **Nummernkreise** Nummernkreise für Vorlagenstücklisten und die Positionsnummer des Stücklistenverlaufs. 

2.  Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.

3.  Klicken Sie auf **Nummernkreise**, und wählen Sie dann einen Nummernkreiscode für Nummernkreisreferenzen aus, die Sie im Formular **Nummernkreise** erstellt haben.

4.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.


> [!NOTE]
> <P>Die Positionsnummer des Stücklistenverlaufs wird verwendet, um die Buchungen im Stücklistenverlauf einem Servicevertrag oder Serviceauftrag zuzuordnen. Die Nummer wird nicht in der Benutzeroberfläche angezeigt.</P>



## <a name="see-also"></a>Siehe auch

[Erstellen einer Vorlagenstückliste](create-template-bom.md)

[Verwalten von Vorlagenstücklisten für Objektbeziehungen](manage-template-boms-on-object-relations.md)

[Ändern einer Servicestückliste](modify-service-bom.md)

 



