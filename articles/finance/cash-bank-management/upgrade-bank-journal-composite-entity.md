---
title: Die zusammengefasste Entität der Bankerfassung aktualisieren
description: In diesem Artikel werden die erforderlichen Schritte zum Hinzufügen des zusätzlichen Felds „BankTransactionType“ zum zusammengesetzten BankJournalEntity beschrieben.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715202"
---
# <a name="update-the-bank-journal-composite-entity"></a>Die zusammengefasste Entität der Bankerfassung aktualisieren

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die erforderlichen Schritte zum Hinzufügen des zusätzlichen Felds „BankTransactionType“ zum zusammengesetzten BankJournalEntity beschrieben.

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
