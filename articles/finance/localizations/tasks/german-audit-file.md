---
title: Generieren Sie deutsche Protokolldatei
description: Diese Prozedur führt Sie durch das Generieren einer deutschen Protokolldatei.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426e7dc08f7930728cde7a96d0ee529e66bc6cd0fdd5972ae66cc27d6d6c3128
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757948"
---
# <a name="generate-german-audit-file"></a>Generieren Sie deutsche Protokolldatei

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren sehen Sie, wie die deutsche Protokolldatei generiert wird. Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.

1. Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Datenexport".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    - Wenn die Liste leer ist, bedeutet dies, dass es kein deutsches Protokolldateiexportformat und keine aktive Debitorenzahlungs-Exportformatkonfiguration gibt. Sie müssen eine deutsche Protokolldateiexportformatkonfiguration importieren, bevor Sie den Vorgang fortsetzen können.  
3. Klicken Sie auf "OK".
4. Geben Sie im Feld "Kommentar" einen Wert ein.
5. Geben Sie im Feld "Medien" einen Wert ein.
6. Geben Sie im Feld "Version" einen Wert ein.
7. Geben Sie im Feld "Tabellengruppe" einen Wert ein oder wählen Sie einen Wert aus.
    - Wählen Sie beispielsweise "Kunden", um den Masterdaten und Transaktionen von Debitoren zu buchen.  
8. Geben Sie ein Datum in das Feld "Periode - Von Datum" ein.
9. Geben Sie in das Feld "Periode - Bis Datum" ein Datum ein.
10. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]