---
title: Projektbudget zum Ende des Geschäftsjahres übertragen
description: Dieser Artikel enthält Informationen darüber, wie verbleibende Budgetbeträge auf zukünftige Jahre übertragen und Details zum Budgetregister erstellt werden können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172329"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektbudget zum Ende des Geschäftsjahres übertragen

[!include [banner](../includes/banner.md)]

Wenn Sie an einem mehrjährigen Projekt arbeiten, haben Sie möglicherweise am Ende des Geschäftsjahres noch verbleibendes Budget. Sie können die Restbudgetbeträge auf ein zukünftiges Jahr übertragen und Budgetregisterdetails für die Beträge in den zugeordneten Hauptbuchkonten erstellen. Bevor Sie die verbleibenden Beträge vortragen, überprüfen und analysieren Sie die verbleibenden Budgetbeträge.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Prüfen und Analysieren der Restbudgetbeträge

Gehen Sie folgendermaßen vor, wenn Sie die Budgetbeträge für Projekte am Jahresende überprüfen, jedoch nicht vortragen möchten.

1. Gehe zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen**. 
2. Überprüfen Sie auf der Seite **Projektbudget-Vortragsprozess** auf der Registerkarte **Optionen am Jahresende**, ob **Verbleibende Projektbudgetbeträge vortragen** nicht aktiviert ist.
3. Wählen Sie auf der Registerkarte **Parameter** im Feld **Projektbudgetjahr** das Geschäftsjahr aus, für das Sie den Restbudgetbetrag anzeigen möchten. 
4. Wählen Sie im Feld **Beginnendes Geschäftsjahr** das Geschäftsjahr aus, für das Sie den Restbudgetbetrag anzeigen möchten. 
5. Wählen Sie im Feld **Aus Prognosemodell** **Restbudget** aus. 
6. Um Projekte einzuschließen, die Ihren ausgewählten Kriterien entsprechen und kein Restbudget mehr haben, wählen Sie **Anzeigen bei Restbudget von null** aus.  
7. Wählen Sie auf der Registerkarte **Budgets auswählen** **Alle Budgets abrufen** aus, um alle Budgets zu laden, die Ihren ausgewählten Kriterien entsprechen, und wählen Sie dann **Verarbeiten**. 
8. Um eine Datenbankabfrage zu entwerfen, die eine bestimmte Reihe von Budgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.

Wählen Sie für weitere Informationen über eine bestimmte Position im Bereich erst die Position und dann **Budgetdetails** oder **Konten anzeigen** aus.

## <a name="carry-forward-remaining-budget-amounts"></a>Restbudgetbeträge vortragen 

Bei der Verarbeitung der Restbudgetbeträge können Sie Transaktionen im Hauptbuch für alle vorgetragenen Beträge erstellen. Um Hauptbuchbuchungen zu erstellen, schließen Sie die Schritte im Abschnitt [Vortragen von Budgetbeträgen und Erstellen von Hauptbuchbuchungen](#carry-forward) ab. 

> [!NOTE]
> Vorgetragene Budgetbeträge werden in das Planzahlenmodell übertragen, das auf der Seite **Vortragsmodelle** als Vortragsbudgetmodell ausgewählt ist..  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Vortragen von Budgetbeträgen und Erstellen von Hauptbuchbuchungen

1.  Wählen Sie **Projektverwaltung und Buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen**. 
2. Wählen Sie auf der Seite **Projektbudget-Vortragsprozess** **Jahresende** aus und aktivieren Sie dann **Verbleibende Projektbudgetbeträge vortragen** und **Budgeterfassungseinträge im Hauptbuch erstellen**. 
3. Wählen Sie auf der Registerkarte **Parameter** in der Feldgruppe **Projektparameter** Folgendes aus:

   - **Projektbudgetjahr**: Wählen Sie den Beginn des Geschäftsjahrs aus, für das Sie die Restbudgetbeträge anzeigen möchten. 
   - **Gewinn und Verlust**: Erstellen Sie Gewinn- und Verlusttransaktionen im Hauptbuch. 
   -  **RIF**: Erstellen Sie RIF-Transaktionen im Hauptbuch.
   -  **Lohnabrechnung** : Erstellen Sie Abrechnungszuordnungstransaktionen im Hauptbuch. 

5. Geben Sie in der Feldgruppe **Hauptbuch** die folgenden Informationen an: 

   - Wählen Sie im Feld **Beginnendes Geschäftsjahr** das Geschäftsjahr aus, in das Sie die Restbudgetbeträge für die Projekte übertragen möchten. Ein Jahr nach dem Wert im Feld **Projektbudgetjahr** ist der Standardwert.
   -  Wählen Sie im Feld **Vortragsperiode** die Periode aus, in der die Budgetregisterdetails im Hauptbuch erstellt werden sollen. Dies ist in der Regel die erste Periode im eröffneten Geschäftsjahr.

6. Geben Sie in der Feldgruppe **Kopieren aus/nach** die folgenden Informationen an:

   - Wählen Sie im Feld **Aus Prognosemodell** das Budget-Planzahlenmodell aus, das den Restbudgetbeträgen zugeordnet ist, die Sie für die Projekte übertragen möchten. 
   - Wählen Sie im Feld **in Sachkontobudgetmodell** das Sachkontobudgetmodell aus, das den Budgetbeträgen zugeordnet ist, die Sie in das Hauptbuch übertragen möchten. 
   -  Wählen Sie **Verkaufswährung übertragen** aus, um die Projektverkaufswährung für die Hauptbuchbuchungen zu verwenden, die beim Übertragen der Budgetbeträge für das Projekt erstellt werden. Wenn die Option nicht ausgewählt ist, verwenden die Transaktionen die Buchhaltungswährung. 
   -  Wählen Sie **Anzeigen bei Restbudget von null** aus, um Projekte einzuschließen, die keine verbleibenden Budgetbeträge haben, aber die anderen Kriterien erfüllen, die Sie in den im unteren Bereich angezeigten Projekten auswählen.

7. Wählen Sie auf der Registerkarte **Budgets auswählen** **Alle Budgets abrufen** aus, um alle Budgets zu laden, die den ausgewählten Kriterien entsprechen. Um eine Datenbankabfrage zu entwerfen, die eine bestimmte Reihe von Projektbudgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.
8. Aktivieren Sie für jedes zu verarbeitende Projekt die Option am Beginn der Projektposition.

    > [!TIP]
    > Um alle oder die meisten Projekte auszuwählen, aktivieren Sie das Häkchen in der oberen oberen linken Ecke. Deaktivieren Sie das Häkchen für dieses Projekt, um die Verarbeitung eines Projekts auszuschließen.

9. Klicken Sie auf **Verarbeiten**, um die Restbudgetbeträge für die ausgewählten Projekte in das ausgewählte Geschäftsjahr zu übertragen und Budgetregisterdetails im Hauptbuch zu erstellen.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Vortragen von Budgetbeträgen ohne Erstellen von Hauptbuchbuchungen

1. Gehe zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen**.
2. Wählen Sie auf der Seite **Projektbudget-Vortragsprozess** im Feld **Optionen am Jahresende** **Verbleibende Projektbudgetbeträge vortragen** aus.
3. Wählen Sie in der Gruppe **Parameter** im Feld **Projektbudgetjahr** das Geschäftsjahr aus, für das Sie Restbudgetbeträge anzeigen möchten.
4. Geben Sie in der Feldgruppe **Kopieren aus/nach** die folgenden Informationen an:

   - Wählen Sie im Feld **Aus Prognosemodell** das Budget-Planzahlenmodell aus, das den Restbudgetbeträgen zugeordnet ist, die Sie für die Projekte übertragen möchten. 
   - Wählen Sie **Anzeigen bei Restbudget von null** aus, um Projekte einzuschließen, die Ihren ausgewählten Kriterien entsprechen und kein Restbudget mehr haben.
   - Wählen Sie in der Gruppe **Budgets auswählen** **Alle Budgets abrufen** aus, um alle Budgets zu laden, die den ausgewählten Kriterien entsprechen. Um eine Datenbankabfrage zu entwerfen, die eine bestimmte Reihe von Projektbudgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.

5. Aktivieren Sie für jedes zu verarbeitende Projekt die Option am Beginn der Projektposition. 
6. Wählen Sie **Verarbeiten** aus, um die Restbudgetbeträge für die ausgewählten Projekte in das ausgewählte Geschäftsjahr zu übertragen.

