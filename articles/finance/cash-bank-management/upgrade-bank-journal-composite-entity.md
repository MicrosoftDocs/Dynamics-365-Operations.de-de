---
title: Die zusammengefasste Entität der Bankerfassung aktualisieren
description: In diesem Thema werden die erforderlichen Schritte zum Hinzufügen des zusätzlichen Felds „BankTransactionType“ zum zusammengesetzten BankJournalEntity beschrieben.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 730e6bd10b0cdd1587c915bb9ec8d6a4792435d9
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727257"
---
# <a name="update-the-bank-journal-composite-entity"></a>Die zusammengefasste Entität der Bankerfassung aktualisieren

[!include [banner](../includes/banner.md)]

In diesem Thema werden die erforderlichen Schritte zum Hinzufügen des zusätzlichen Felds „BankTransactionType“ zum zusammengesetzten BankJournalEntity beschrieben.

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
