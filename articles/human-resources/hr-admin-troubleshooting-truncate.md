---
title: Vermeiden Sie abgeschnittenen Text in der Positionshierarchie und beim Exportieren in Visio
description: Dieser Artikel erklärt, wie Sie das Problem der abgeschnittenen Namen von Personen und Positionen in der Positionshierarchie in Microsoft Dynamics 365 Human Resources beheben können.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3663f5689fc0109caad01a285185f9f4ffa6fcca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865381"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Vermeiden Sie abgeschnittenen Text in der Positionshierarchie und beim Exportieren in Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Abgang**

Wenn ein Kunde die Positionshierarchie in Microsoft Dynamics 365 Human Resources anzeigt, werden die Namen von Einzelpersonen und Positionen abgeschnitten. Daher kann es schwierig sein, ein Screenshot zu erstellen oder die Hierarchie zu drucken oder zu verteilen.

![Positionshierarchie.](media/position-h.png)

**Ursache**

Dieses Verhalten ist beabsichtigt.

**Lösung**

Leider können Benutzer die Größe des Texts nicht einfach ändern. Sie können jedoch die Positionshierarchie von Human Resources heraus exportieren und sie dann in Microsoft Visio importieren. Obwohl der folgende Artikel für Microsoft Dynamics AX 2012 verfasst wurde, gilt der Prozess nach wie vor für Human Resources: [Exportieren einer Positionshierarchie nach Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Gehen Sie folgendermaßen vor beim Export nach Visio.

1. Öffnen Sie in Human Resources die Listenseite **Positionen**.

    Um mehr Informationen in das Organisationsstrukturdiagramm aufzunehmen, fügen Sie der Liste **Positionen** Felder hinzu, so dass diese verfügbar sind, wenn Sie später in dieser Prozedur den **Organigramm-Assistenten** verwenden.

2. Wählen Sie im Aktionsbereich die Schaltfläche **In Microsoft Office öffnen** aus, und wählen Sie dann unter **Nach Excel exportieren** die Option **Positionen** aus. Alternativ drücken Sie STRG+T.

    ![Exportieren der Listenseite „Positionen“ nach Excel.](media/org-admin.png)

3. Speichern Sie die Excel-Datei, die exportiert wurde.

    ![Dialogfeld „Nach Excel exportieren“.](media/export-excel.png)

4. Wählen Sie in Visio **Visio – Neue erstellen** und wählen Sie die Vorlagenkategorie **Unternehmen** aus.

    ![Neues Diagramm.](media/new.png)

5. Wählen Sie **Organigramm-Assistent** und dann **Erstellen** aus.

    ![Dialogfeld „Organigramm-Assistent“.](media/orgchart-wizard.png)

6. Wählen Sie **Informationen, die bereits in einer Datei oder Datenbank gespeichert sind** aus, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 1.](media/orgchart-wizard7.png)

7. Wählen Sie **Ein Text, Organisation Plus (\*.txt) oder Excel-Datei** aus, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 2.](media/orgchart-wizard3.png)

8. Navigieren Sie zur Auswahl der exportierten Excel-Datei, die die Positionshierarchie enthält, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 3.](media/orgchart-wizard2.png)

9. Legen Sie das Feld **Name** auf **Position** fest, legen Sie das Feld **Vorgesetzter** auf **Position des Vorgesetzten** fest, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 4.](media/orgchart-wizard1.png)

10. Wählen Sie die Felder aus, die in jedem Knoten angezeigt werden sollen, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 5.](media/orgchart-wizard5.png)

11. Fügen Sie die Spalte **Position** der Liste **Formdatenfelder** hinzu, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 6.](media/orgchart-wizard6.png)

12. Bilder sind aktuell nicht vorhanden. Daher wählen Sie auf der nächsten Seite **Weiter** aus.
13. Wählen Sie **Ich möchte, dass der Assistent mein Organigramm über mehrere Seiten hinweg darstellt** aus.

    ![Organigramm-Assistent 7.](media/orgchart-wizard4.png)

14. Wählen Sie **Fertig stellen** aus.

    Wenn es Positionen gibt, die sich nicht in der Struktur befinden, werden Sie dazu aufgefordert, sie im Diagramm einzuschließen.

Das in Visio generierte Diagramm zeigt jeden Manager auf einem getrennten Arbeitsblatt an.

Anhand der Felder, die Sie ausgewählt haben, um sie ins Diagramm einzubeziehen, zeigt jeder Knoten die entsprechenden Informationen an, wenn die Visio-Datei generiert wird.

![Hierarchiediagramm.](media/hierarchy.png)

**Zusätzliche Option**

In Human Resources sind Sie möglicherweise auch in der Lage, den Arbeitsbereich **Personen** zu verwenden, um der Hierarchie zugehörige Informationen anzuzeigen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
