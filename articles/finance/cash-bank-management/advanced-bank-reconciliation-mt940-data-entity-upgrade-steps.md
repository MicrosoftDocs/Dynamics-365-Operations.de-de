---
title: Erweiterte Bankabstimmung MT940 Import – Zusammengesetzter Datenentitäts-Upgrade
description: Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ee5ad476b10077592c61f6827b5596a1b3e66cd6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217433"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Erweiterte Bankabstimmung MT940 Import – Zusammengesetzter Datenentitäts-Upgrade

[!include [banner](../includes/banner.md)]

Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen. 

Gehen Sie folgendermaßen vor, um die Bankauszugs-Importentität hinzuzufügen, um das Format MT940 zu unterstützen.

1.  Kompilieren und synchronisieren Sie Folgendes:
    -   Zusammengesetzte Entität\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tables\\BankStatementStaging

2.  Datenverwaltung\\Datenprojekte.
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
            6.  Überprüfen Sie, ob S **equenceNumber** zugeordnet ist.
                -   Klicken Sie auf **Zuordnung anzeigen** auf der Auszugsentität.
                -   Überprüfen Sie, dass **SequenceNumber** von der Quelle zum Bereitstellen zugeordnet ist.

3.  Importieren Sie den neuen Auszug.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]