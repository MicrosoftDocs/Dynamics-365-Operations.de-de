---
title: Mithilfe von Workflows, um Mitarbeiter verwalten
description: "In diesem Thema wird erläutert, wie die Workflowfunktion verwenden können, für Personalverwaltung Mitarbeiterdaten verwaltet. So können Sie einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, die gestartet wird, wenn Mitarbeiter gegenüber Datensatz ändern."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Mithilfe von Workflows, um Mitarbeiter verwalten

In diesem Thema wird erläutert, wie die Workflowfunktion verwenden können, für Personalverwaltung Mitarbeiterdaten verwaltet. So können Sie einen Workflow einer Position zuordnen und einen Genehmigungsworkflow konfigurieren, die gestartet wird, wenn Mitarbeiter gegenüber Datensatz ändern.

Die Workflowfunktion für Personalverwaltung beinhaltet zahlreiche Workflow zur Verwaltung von Personalverwaltungsaktivitäten bereit. Darüber hinaus wurden zahlreiche Optionen zur Verfügung, und Sie können bestimmte Workflows ändern und mit einer Berichterstellungshierarchie zuordnen können. Workflow sind verfügbar zu unterstützen, Änderungen an einigen standardmäßigen Arten Mitarbeiterinformationen verwalten. Sie können einen Workflow einer Position zuordnen. Wenn Mitarbeiter gegenüber Mitarbeiterdatensatz ändern, wird ein Workflow gestartet, der eine Genehmigung erforderlich, bevor die neuen Informationen gespeichert werden. Workflows werden vordefiniert, sodass die folgenden Informationsarten Ihnen effizient, Änderungen verwalten Hilfe sowie Daten- genau der Mitarbeiter verwalten:

-   Kennnummern
-   Kurse
-   Ausbildung
-   Bild
-   Ausgeliehene Artikel
-   Berufserfahrung
-   Projekterfahrung
-   Qualifikationen
-   Vertrauensposition
-   Personalverwaltungsaktivitäten
-   Kurserfassung

Wenn Mitarbeiter eingestellt, übertragen oder beendet werden, kann der Workflow einem Prüfprozess enthalten. Auf diese Weise kann ein Dokument geprüft werden, oder die Anforderungen einer Aktivität können im Rahmen des Workflows definiert werden. Wenn der Prüfprozess durchlaufen, wird das Dokument oder die Aktivität, der Workflow abgeschlossen und wechselt zu einem Schritt der Genehmigungsprozedur aus.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Weisen Sie einen Workflow einer zu Positionshierarchie
Sie können einen Workflow einer beliebigen Hierarchie beziehen, den Sie konfigurieren. Wird beispielsweise eine Position mit einer Matrixberichterstellungshierarchie konfigurierten zugeordnet ist, kann eine Arbeitsplanausgaben diesen Workflow für ein bestimmtes Projekt an Projektleiter anstelle des Managers des Mitarbeiters, der mit dieser Position zugeordnet ist. So erstellen Sie einen neuen Workflow erstellen oder einen vorhandenen Workflow, auf der Personalverwaltungsworkflow ** ** Seite zu ändern, klicken ** ** neu. Wählen Sie einen Workflow in der Liste aus, um den Workflowdesigner zu starten. Sie können den Designer verwenden, um einen neuen Workflow erstellen oder die Schritte in einem vorhandenen Workflow zu ändern. Wenn Sie einen vorhandenen Workflow ändern, werden die Änderungen als neue Version gespeichert. Daher können Sie wieder zu einer früheren Version immer wechseln, falls notwendig.

## <a name="configure-a-human-resources-workflow"></a>Konfigurieren eines Personalverwaltungsworkflow
Um einen grundlegenden Workflow konfigurieren der statt wenn Mitarbeiteranforderung zu ihrer persönlichen Kennung wird, führen Sie die folgenden Schritte aus.

1.  ** Auf der Seite klicken Sie Personalverwaltungsworkflow ** ** ** neu.
2.  In der Liste verfügbarer Workflow, Auswählen ** Kennnummern **.
3.  ** Auf Ausführung ** um das Workflowdesigners an, und geben Sie dann den Benutzernamen und Kennwort ein, wenn Sie dazu aufgefordert werden.
4.  Ziehen Sie das Genehmigen ** Kennnummer ** Element aus der Liste von Workflowelementen auf die Designercanvas.
5.  Schließt das Genehmigungselement an ** Start ** anzeigen und Ende ** **.
6.  ** Doppelklick Genehmigen Element ** und klicken Sie dann mit der rechten Maustaste und Auswählen aus ** Eigenschaften **.
7.  Gehen Sie folgendermaßen vor, um Arbeitsaufgabenanweisungen hinzuzufügen:
    1.  ** Zuweisung ** Wählen Sie aus, und wählen Sie dann ** Hierarchie ** unter dem Zuweisungstyp aus.
    2.  ** Unter der Hierarchie ** Auswahl wählen Sie aus ** konfigurierbare ** Hierarchie.
    3.  Fügen Sie eine Beendigungsbedingung, und schließen Sie die Seite.

8.  Schließen Sie alle zusätzliche Anweisungen stornieren "keine weiteren Warnungen müssen vorhanden sein).
9.  Klicken Sie auf **Speichern und schließen**. Aktivieren des neuen Workflow, wenn das Dialogfeld geöffnet wird, und wählen Sie aus ** aktivieren Sie die Version aktiv **.
10. Wechseln ** Personalverwaltung ** &gt; ** Positionen ** &gt; ** Positionshierarchietypen **.
11. Wählen Sie aus ** Matrix **.
12. Fügen Sie das Arbeitskraftkennnummer ** ** Workflow der Liste.



