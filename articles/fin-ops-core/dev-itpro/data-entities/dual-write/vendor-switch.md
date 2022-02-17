---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird beschrieben, wie Sie die Integration von Kreditor-Daten zwischen Apps für Finanzen und Betrieb und Dataverse umschalten.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 80de21b5e46e4f274626fa311f16e81312a2f5ab
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062749"
---
# <a name="switch-between-vendor-designs"></a>Wechsel zwischen Kreditorendesigns

[!include [banner](../../includes/banner.md)]





## <a name="vendor-data-flow"></a>Kreditorendatenfluss 

Wenn Sie die Tabelle **Konto** zum Speichern von Lieferanten vom Typ **Organisation** und die Tabelle **Kontakt** zum Speichern von Lieferanten vom Typ **Person** verwenden, konfigurieren Sie die folgenden Workflows. Andernfalls ist diese Konfiguration nicht erforderlich.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Erweiterte Kreditorendesign für Kreditoren vom Typ „Organisation“ verwenden

Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen. Sie erstellen für jede Vorlage einen Workflow.

+ Lieferanten in der Kontotabelle erstellen
+ Lieferanten in der Lieferantentabelle erstellen
+ Lieferanten in der Kontotabelle aktualisieren
+ Lieferanten in der Lieferantentabelle aktualisieren

Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:

1. Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle erstellen** aus. Wählen Sie dann **OK** aus. Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Tabelle **Konto**.

    ![Workflowprozess „Lieferanten in der Kontotabelle erstellen“.](media/create_process.png)

2. Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle aktualisieren** aus. Wählen Sie dann **OK** aus. Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Tabelle **Konto**.
3. Erstellen Sie einen Workflowprozess für die Tabelle **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle erstellen** aus.
4. Erstellen Sie einen Workflowprozess für die Tabelle **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle aktualisieren** aus.
5. Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren. Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.

    ![Schaltfläche „In einen Hintergrundworkflow konvertieren“.](media/background_workflow.png)

6. Aktivieren Sie die Workflows, die Sie für die Tabellen **Konto** und **Lieferant** erstellt haben, um die Tabelle **Konto** für das Speichern von Informationen vom Typ **Organisation** zu verwenden.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Erweiterte Kreditorendesign für Kreditoren vom Typ „Person“ verwenden

Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen. Sie erstellen für jede Vorlage einen Workflow.

+ Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen
+ Lieferanten vom Typ „Person“ in der Kontakttabelle erstellen
+ Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren
+ Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren

Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:

1. Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus. Wählen Sie dann **OK** aus. Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Tabelle **Kontakt**.
2. Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren** aus. Wählen Sie dann **OK** aus. Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Tabelle **Kontakt**.
3. Erstellen Sie einen Workflowprozess für die Tabelle **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus.
4. Erstellen Sie einen Workflowprozess für die Tabelle **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren** aus.
5. Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren. Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.
6. Aktivieren Sie die Workflows, die Sie für die Tabellen **Kontakt** und **Lieferant** erstellt haben, um die Tabelle **Kontakt** für das Speichern von Informationen vom Typ **Person** zu verwenden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]