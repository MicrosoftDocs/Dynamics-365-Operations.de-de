---
title: Die Chargennummer wird gelöscht, wenn eine neue Loskennung ausgewählt wird
description: Wenn Sie eine Erfassungsposition für eine Kommissionierliste überprüfen, wird der Wert im Feld „Chargennummer“ gelöscht, wenn Sie im Feld „Loskennung“ einen neuen Wert auswählen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738818"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Die Chargennummer wird gelöscht, wenn eine neue Loskennung ausgewählt wird

KB-Nummer: 4613107

## <a name="symptoms"></a>Symptome

Wenn Sie eine Erfassungsposition für eine Kommissionierliste überprüfen, wird der Wert im Feld **Chargennummer** gelöscht, wenn Sie im Feld **Loskennung** einen neuen Wert auswählen.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Wenn Sie die Loskennung ändern, ändern Sie den Artikelkontext. Daher wird die Chargennummer zurückgesetzt.

Um die Chargennummer einer Loskennung zuzuordnen, müssen Sie zuerst die Loskennung festlegen.
