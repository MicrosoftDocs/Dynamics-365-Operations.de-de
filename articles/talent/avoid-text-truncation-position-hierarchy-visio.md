---
title: Vermeiden Sie das Abschneiden von Text in der Positionshierarchie und beim Export nach Visio
description: In diesem Thema wird erläutert, wie ein Problem gelöst wird, bei dem Namen von Einzelpersonen und Positionen abgeschnitten werden, wenn Kunden die Positionshierarchie in Microsoft Dynamics 365 Talent anzeigen. Das Abschneiden von Text erschwert das Erstellen von Screenshots oder das Drucken der Hierarchie.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 22e8570ccb53e8a7be2c57d3f14fe8034bdb699b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898895"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Vermeiden Sie das Abschneiden von Text in der Positionshierarchie und beim Export nach Visio

**Abgang**

Wenn ein Kunde die Positionshierarchie in Microsoft Dynamics 365 Talent anzeigt, werden die Namen von Einzelpersonen und Positionen abgeschnitten. Daher kann es schwierig sein, ein Screenshot zu erstellen oder die Hierarchie zu drucken oder zu verteilen.

![Positionshierarchie](media/position-h.png)

**Ursache**

Dieses Verhalten ist beabsichtigt.

**Auflösung**

Leider können Benutzer die Größe des Texts nicht einfach ändern. Sie können jedoch die Positionshierarchie von Talent heraus exportieren und sie dann in Microsoft Visio importieren. Obwohl der folgende Artikel für Microsoft Dynamics AX 2012 verfasst wurde, gilt der Prozess nach wie vor für Talent: [Exportieren einer Positionshierarchie nach Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Gehen Sie folgendermaßen vor beim Export nach Visio.

1. Öffnen Sie in Talent die Listenseite **Positionen**.

    Um weitere Informationen im Organisationsstrukturdiagramm einzubeziehen, fügen Sie der Liste **Positionen** Felder hinzu, damit sie verfügbar sind, wenn Sie den Assistenten später in dieser Prozedur verwenden.

2. Wählen Sie im Aktionsbereich die Schaltfläche **In Microsoft Office öffnen** aus, und wählen Sie dann unter **Nach Excel exportieren** die Option **Positionen** aus. Alternativ drücken Sie STRG+T.

    ![Exportieren der Listenseite „Positionen” nach Excel](media/org-admin.png)

3. Speichern Sie die Excel-Datei, die exportiert wurde.

    ![Dialogfeld „Nach Excel exportieren”](media/export-excel.png)

4. Wählen Sie in Visio **Visio – Neue erstellen** und wählen Sie die Vorlagenkategorie **Unternehmen** aus.

    ![Neues Diagramm](media/new.png)

5. Wählen Sie **Organigramm-Assistent** und dann **Erstellen** aus.

    ![Dialogfeld „Organigramm-Assistent”](media/orgchart-wizard.png)

6. Wählen Sie **Informationen, die bereits in einer Datei oder Datenbank gespeichert sind** aus, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 1](media/orgchart-wizard7.png)

7. Wählen Sie **Ein Text, Organisation Plus (\*.txt) oder Excel-Datei** aus, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 2](media/orgchart-wizard3.png)

8. Navigieren Sie zur Auswahl der exportierten Excel-Datei, die die Positionshierarchie enthält, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 3](media/orgchart-wizard2.png)

9. Legen Sie das Feld **Name** auf **Position** fest, legen Sie das Feld **Vorgesetzter** auf **Position des Vorgesetzten** fest, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 4](media/orgchart-wizard1.png)

10. Wählen Sie die Felder aus, die in jedem Knoten angezeigt werden sollen, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 5](media/orgchart-wizard5.png)

11. Fügen Sie die Spalte **Position** der Liste **Formdatenfelder** hinzu, und wählen Sie dann **Weiter** aus.

    ![Organigramm-Assistent 6](media/orgchart-wizard6.png)

12. Bilder sind aktuell nicht vorhanden. Daher wählen Sie auf der nächsten Seite **Weiter** aus.
13. Wählen Sie **Ich möchte, dass der Assistent mein Organigramm über mehrere Seiten hinweg darstellt** aus.

    ![Organigramm-Assistent 7](media/orgchart-wizard4.png)

14. Wählen Sie **Fertig stellen** aus.

    Wenn es Positionen gibt, die sich nicht in der Struktur befinden, werden Sie dazu aufgefordert, sie im Diagramm einzuschließen.

Das in Visio generierte Diagramm zeigt jeden Manager auf einem getrennten Arbeitsblatt an.

Anhand der Felder, die Sie ausgewählt haben, um sie ins Diagramm einzubeziehen, zeigt jeder Knoten die entsprechenden Informationen an, wenn die Visio-Datei generiert wird.

![Hierarchiediagramm](media/hierarchy.png)

**Zusätzliche Option**

In Talent sind Sie möglicherweise auch in der Lage, den Arbeitsbereich **Personen** zu verwenden, um der Hierarchie zugehörige Informationen anzuzeigen.
