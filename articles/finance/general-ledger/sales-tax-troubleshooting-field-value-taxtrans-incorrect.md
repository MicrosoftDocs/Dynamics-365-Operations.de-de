---
title: Falscher Feldwert in TaxTrans
description: Dieses Thema enthält Informationen zur Fehlerbehebung bei falschen Feldwerten in TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947642"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Falscher Feldwert in TaxTrans

[!include [banner](../includes/banner.md)]

Wenn ein Feldwert in **TaxTrans** falsch ist, verwenden Sie die Informationen in diesem Thema, um zu versuchen, das Problem zu lösen.

## <a name="overview-of-values"></a>Übersicht der Werte
Die folgende Auflistung zeigt, dass **TaxTrans**, **TaxUncommitted** und **TmpTaxWorkTrans** ähnliche Datensätze sind, aber unterschiedlich funktionieren.

  - **TaxTrans** ist das endgültige Ergebnis der gebuchten steuerlichen Transaktion, das in der Datenbank persistiert wird.
  - **TaxUncommitted** ist das in der Datenbank persistierte Zwischenergebnis der Steuerberechnung (falls zutreffend), das später für die Buchung verwendet wird.
  - **TmpTaxWorkTrans** ist das temporäre berechnete Steuerergebnis in der In-Memory-Tabelle (Table Type = InMemory).

Wenn Sie die Ursache für eine fehlerhafte **SteuerTrans** Spalte finden, haben Sie auch die Ursache für eine fehlerhafte **SteuerUnverbindlich** oder **SteuerWerkTrans** Spalte gefunden. Dies liegt daran, dass die drei Spalten voneinander kopiert werden.

Typischerweise wird bei der Steuerberechnung **TmpTaxWorkTrans** erzeugt, und dann, falls zutreffend, **TaxUncommitted**. Während der Steuerbuchung wird **TaxTrans** erzeugt.


## <a name="add-breakpoints"></a>Haltepunkte hinzufügen
Um Haltepunkte hinzuzufügen, führen Sie die folgenden Schritte aus: 

1. Fügen Sie Erweiterungen und Haltepunkte in *insert()* und *update()* in den Erweiterungen wie unten gezeigt hinzu.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Alternativ können Sie Haltepunkte direkt hinzufügen, wenn **TaxUncommitted** nicht enthalten ist.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Reproduzieren und Debuggen

Nachdem die Haltepunkte festgelegt sind, ist jede Änderung der Datenpersistenz während des Debuggens sichtbar. Um die Ursache für eine fehlerhafte Spalte von **TaxTrans**, **TaxUncommitted** oder **TmpTaxWorkTrans** zu finden, prüfen und beachten Sie die folgenden Elemente:

- Der letzte Haltepunkt, an dem die Spalte korrekt ist.
- Der erste Haltepunkt, an dem die Spalte fehlerhaft ist.
- Was passiert zwischen diesen beiden Punkten.

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt
Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber das Problem nicht beheben konnten, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, wenden Sie sich an den Microsoft Support, um Hilfe zu erhalten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

