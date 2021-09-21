---
title: Die maximale Anzahl der Dezimalstellen für die Lagermengeneinheit beträgt 0
description: 'Wenn Sie versuchen, eine Bestandstransaktion oder eine Bestandsreservierung zu buchen, wird die folgende Fehlermeldung angezeigt: Die maximale Anzahl von Dezimalstellen für die Lagermengeneinheit beträgt 0.'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476483"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Die maximale Anzahl der Dezimalstellen für die Lagermengeneinheit beträgt 0


## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Bestandstransaktion oder eine Bestandsreservierung zu buchen, erhalten Sie die folgende Fehlermeldung:

> Die maximale Anzahl der Dezimalstellen für die Lagermengeneinheit beträgt 0.

Dieses Problem tritt auf, wenn die Bestandstransaktionsmenge als Dezimalwert angegeben wird, der unter der vom Feld unterstützten Genauigkeit liegt. Beispiel: Für eine Bestandstransaktion wurde eine Menge von *0,5* angegeben, es werden jedoch nur ganzzahlige Mengen unterstützt. Daher sollte der Wert *1* statt *0,5* sein.

## <a name="resolution"></a>Lösung

1. Führen Sie das folgende Skript auf Ihrer SQL Server-Instanz aus, um Mengen in den Bestandstransaktionen zu runden. Dieses Skript korrigiert Werte in der Tabelle **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Führen Sie eine Konsistenzprüfung des verfügbaren Bestands durch, bei der die Option **Fehler beheben** aktiviert ist. Diese Überprüfung korrigiert Werte in der Tabelle **inventSum**.

> [!IMPORTANT]
> Wir empfehlen dringend, dass Sie das Skript entsprechend Ihrer Umgebung sorgfältig bearbeiten, es in einer Testumgebung testen und dann die resultierenden Daten überprüfen, bevor Sie das Skript in einer Produktionsumgebung ausführen.
