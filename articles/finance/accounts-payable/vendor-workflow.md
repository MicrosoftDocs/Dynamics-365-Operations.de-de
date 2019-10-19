---
title: Lieferantenworkflow
description: Ändern Sie Kreditordatendaten und Nutzen Sie zur Genehmigung Workflow.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: afda0ead11ec1adac2d436511eef8165a7f0aed2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189268"
---
# <a name="vendor-workflow"></a>Lieferantenworkflow

[!include [banner](../includes/banner.md)]

Wenn der Kreditorenworkflow verwendet wird, werden Änderungen, die zu bestimmten Feldern vorgenommen werden, zur Genehmigung an den Workflow gesendet, bevor sie dem Kreditor hinzugefügt werden.

## <a name="set-up-the-vendor-workflow"></a>Lieferantenworkflow einrichten

Die Funktion Workflow kann erst nach der Aktivierung verwendet werden.

1. Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2. Legen Sie auf der Registerkarte **Genehmigter Kreditor** im Inforegister **Allgemein** die Option **Genehmigter Kretitor aktivieren** auf **Ja** fest.
3. Im Feld **Datenentitätsverhalten** wählen Sie das Verhalten aus, das verwendet werden soll, wenn Daten importiert werden:

    - **Ermöglichen von Änderungen ohne Genehmigung** – Die Datenentität kann den Kreditorendatensatz aktualisieren, ohne ihn mit dem Standardworkflow verarbeitet.
    - **Weisen Sie Änderungen zurück** – Änderungen können vorgenommen nicht auf dem Kreditorendatensatz vorgenommen werden. Der Import schlägt für die Felder fehl, die für Importe Workflow aktiviert werden.
    - **Änderungsvorschläge erstellen** – Alle Felder werden mit Ausnahme der Felder geändert, die für den Workflow aktiviert werden. Die neuen Werte für diese Felder werden an den Kreditor hinzugefügt, da vorgeschlagene Änderungen und der Workflow automatisch gestartet werden.

4. In der Liste mit Kreditorenfeldern aktivieren Sie das Kästchen **Aktivieren** für jedes aus, das genehmigt werden muss, damit die Änderungen vorgenommen werden können.
5. Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenworkflows**.
6. Wählen Sie **Neu** aus.
7. Wählen Sie **Workflow zu vorgeschlagenen Lieferantenänderungen**. 
8. Einrichten des Workflows, so dass er mit demn Genehmigungsprozess übereinstimmt. Das Workflowgenehmigungselement **Workflowgenehmigungen für vorgeschlagene Kreditorenänderung** übernimmt die Änderung des Kreditors.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Ändern Sie Kreditoreninformationen und übermitteln Sie die Änderungen an den Workflow

Wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird die Seite **Vorgeschlagene Änderungen** angezeigt. Diese zeigt den ursprünglichen Feldwert und den neu eingegebenen Wert. Das Feld, das Sie ändern, wird auf den ursprünglichen Wert zurückgesetzt. Eine Statusmeldung informiert Sie auch, dass die Änderungen nicht übermittelt wurden. 

Immer wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird dieses Feld der Liste auf der Seite **Vorgeschlagene Änderungen** hinzugefügt. Um den vorgeschlagenen Wert für ein Feld zu verwerfen, verwenden Sie die Schaltfläche **Verwerfen** neben dem Feld in der Liste. Um sämtliche Änderungen zu verwerfen, verwenden Sie die Schaltfläche **Alle Änderungen verwerfen** am unteren Seitenrand. Klicken Sie auf **OK**, um die Seite zu schließen.

Nachdem Sie mindestens eine vorgeschlagene Änderung haben, werden zwei zusätzliche Registerkarten im Aktivitätsbereich: **Vorgeschlagene Änderungen** und **Workflow** angezeigt.

1. Wählen Sie **Vorgeschlagene Änderungen**, um die Seite **Vorgeschlagene Änderungen** zu öffnen und die Änderungen zu prüfen.
2. Wählen Sie **Workflow\>Übermitteln, um die Änderungen für den Workflow zu ändern**.

    Der Status auf der Seite ändert sich in **Änderungen mit ausstehender Genehmigung**.

Der Workflow erfolgt gemäß dem Standardworkflowprozess. Die genehmigende Person wird auf die Seite **Kreditor** verwiesen, auf der sie die Änderungen auf der Seite Überprüfen **Vorgeschlagene Änderungen** und dann **Workflow \> Genehmigen** auswählen können, um den Workflow zu genehmigen. Sind alle Genehmigungen bearbeitet, werden die Felder mit den vorgeschlagenen Werten aktualisiert.
