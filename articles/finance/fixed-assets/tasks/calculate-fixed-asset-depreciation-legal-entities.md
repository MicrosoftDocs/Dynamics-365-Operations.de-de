---
title: Anlagenabschreibung über juristische Personen hinweg berechnen
description: Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ca54a45b81b66fdcdd5e43ad6b8c408cb764fb9
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712117"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Anlagenabschreibung über juristische Personen hinweg berechnen

[!include [banner](../../includes/banner.md)]

Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden. Dieses Verfahren beschreibt, wie Sie den Prozess für mehrere juristische Personen einrichten und ausführen können. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Einrichten unternehmensübergreifender Abschreibungs-Ausführungserfassungen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".
2. Erweitern Sie den Anlagenvorschlagsabschnitt.
3. Klicken Sie auf Hinzufügen.
4. Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wiederholen die Erfassungseinrichtung auf der Anlagenparameterseite in jeder juristischen Person.  

## <a name="depreciation-run"></a>Abschreibungsausführung
1. Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen.
2. Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Journalname ist standardmäßig von den Anlagenparametern. Er kann für die aktuelle juristische Person hier geändert werden.  
3. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Dient zum Auswählen der in der Abschreibungsausführung einzubeziehenden juristischen Personen.  
    * Nur juristische Personen mit Erfassungen, die für Anlagenvorschläge auf der Anlagenparameterseite eingerichtet werden, werden in der Liste angezeigt.  
4. Wählen Sie "Ja" im Feld "Erfassungen buchen" aus.
    * Filterungsfelder enthalten alle Anlagen und Bücher, Gruppen für die juristischen Personen, die für diese Abschreibungsausführung ausgewählt werden.  
    * Die Stapelverarbeitungsoption ist standardmäßig aktiviert. Wenn diese Option aktiviert ist, werden die Abschreibungserfassungserstellung und Buchung im Hintergrund ausgeführt.  
5. Klicken Sie auf "Erfassung erstellen".
6. Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
