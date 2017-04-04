---
title: "Erweiterter Bankabstimmung MT940 Import – zusammengesetzte Datenentitätsaktualisierung"
description: "Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: 3a4868045a12f7210a4d3924b4a335a52206341a
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Erweiterter Bankabstimmung MT940 Import – zusammengesetzte Datenentitätsaktualisierung

Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen. 

Gehen Sie folgendermaßen vor, um die Bankauszugs-Importentität hinzuzufügen, um das Format MT940 zu unterstützen.

1.  Kompilieren und synchronisieren Sie Folgendes:
    -   " Zusammengesetzt (\\BankStatementImportEntity Entität
    -   \\BankStatementBalanceEntity Entität
    -   \\BankStatementDocumentEntity Entität
    -   \\BankStatementEntity Entität
    -   \\BankStatementLineEntity Entität
    -   Tabellen BankStatementStaging \\

2.  Datenverwaltungs-\\Datenprojekte.
    1.  Laden Sie MT940-Importprojekt(e)
        1.  Ändern Sie XSLT.
            -   Klicken Sie auf **Zuordnung anzeigen**.
            -   Klicken Sie auf **Zuordnung anzeigen** auf dem Bankauszugsdokument.
            -   Klicken Sie auf **Umwandlungen**
            -   Löschen Sie die Datei „BankReconiliation-to-Composite.xslt”.
            -   Fügen Sie die neue Version von „BankReconiliation-to-Composite.xsl” hinzu.

        2.  Machen Sie die **Sequenznummer** im Layout **Quelldaten** verfügbar.
            1.  Quelldatenformat = XML-Element.
            2.  Entitätsname = Bankauszüge.
            3.  Laden Sie die Datendatei hoch = neue Version „SampleBankCompositeEntity.xml”.
            4.  Klicken Sie auf **Ja**, um die vorhandene Datei zu überschreiben.
            5.  Klicken Sie auf **Ja**, um eine neue Zuordnung zu generieren.
            6.  Überprüfen Sie, ob S**equenceNumber** zugeordnet ist.
                -   Klicken Sie auf **Zuordnung anzeigen** auf der Auszugsentität.
                -   Überprüfen Sie, dass **SequenceNumber** von der Quelle zum Bereitstellen zugeordnet ist.

3.  Importieren Sie den neuen Auszug.



