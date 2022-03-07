---
title: Aktualisiert die zusammengesetzte Bankerfassungs-Entität
description: Gehen Sie folgendermaßen vor, um das zusätzliche Feld "BankTransactionType" der zusammengesetzten BankJournalEntity hinzuzufügen.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443439"
---
# <a name="update-the-bank-journal-composite-entity"></a>Aktualisiert die zusammengesetzte Bankerfassungs-Entität

[!include [banner](../includes/banner.md)]

Gehen Sie folgendermaßen vor, um das zusätzliche Feld "BankTransactionType" der zusammengesetzten BankJournalEntity hinzuzufügen.

Gehen Sie folgendermaßen vor, um den BankTransactionType-Feld der zusammengesetzten BankJournalEntity hinzuzufügen.

1.  Kompilieren und synchronisieren Sie die folgenden zusammengesetzten Bankerfassungsentitäten, Entitäten und Stagingtabellen:
    -   Zusammengesetzte Entität\\BankJournalEntity
    -   Entität\\BankJournalHeaderEntity
    -   Entität\\BankJournalLineEntity
    -   Tabelle\\BankJournalHeaderStaging
    -   Tabelle\\BankJournalLineStaging

2.  Datenverwaltung\\Datenprojekte
    -   Macht den Typ **Banktransaktion** im Layout **Quelldaten** verfügbar.
        -   Quelldatenformat = XML-Element
        -   Entitätsname j= Bankerfassung
        -   Laden Sie die Datendatei hoch = neue Version SampleBankJournalCompositeEntity.xml
        -   Klicken Sie auf **Ja**, um die vorhandene Datei zu überschreiben.
        -   Klicken Sie auf **Ja**, um eine neue Zuordnung von Beginn her zu generieren.
        -   Überprüfen Sie, dass der Banktransaktionstyp zugeordnet ist.
            -   Klicken Sie auf **Zuordnung anzeigen** auf der Positionsentität.
            -   Überprüfen Sie, dass der Banktransaktionstyp von der Quelle zum Bereitstellen zugeordnet ist.

3.  Importieren Sie den neuen Auszug.




