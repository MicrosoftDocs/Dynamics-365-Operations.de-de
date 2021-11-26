---
title: Lieferantenworkflow
description: Ändern Sie Kreditordatendaten und Nutzen Sie zur Genehmigung Workflow.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 48d81c727de29a285e5e33672e8f6d2eccef6249
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753921"
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

Der Workflow erfolgt gemäß dem Standardworkflowprozess. Die genehmigende Person wird an die Seite **Kreditor** weitergeleitet. Dort können die Änderungen auf der Seite **Vorgeschlagene Änderungen** geprüft und der Workflow anschließend über **Workflow \> Genehmigen** genehmigt werden. Sind alle Genehmigungen bearbeitet, werden die Felder mit den vorgeschlagenen Werten aktualisiert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
