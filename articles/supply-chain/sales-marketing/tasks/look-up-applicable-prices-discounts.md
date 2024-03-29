---
title: Anwendbare Preise und Rabatte nachschlagen
description: Im folgenden Verfahren, wie Preis und/oder den Rabatt für ein Produkt sucht, das für einen bestimmten Debitor derzeit gültig ist, ohne einen Auftrag zu erstellen.
author: Henrikan
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c80ae00e1bcbc4498ec4705195c3208170cee1b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578919"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Anwendbare Preise und Rabatte nachschlagen

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren, wie Preis und/oder den Rabatt für ein Produkt sucht, das für einen bestimmten Debitor derzeit gültig ist, ohne einen Auftrag zu erstellen. Die Prozedurgänge durch ein besonderes Beispiel und Sie müssen im Beispiel für die Verwendung des USMF-Vorführungsunternehmens folgt, um die erforderlichen Werte auszuwählen.


## <a name="find-the-applicable-price"></a>Suchen des gültigen Preis
1. Wechseln Sie zu Vertrieb und Marketing > Preise und Rabatte > Preise suchen.
2. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den Debitor US-001 und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "T0004" ein.
    * Stellen Sie sicher, dass das Feld Menge standardmäßig auf 1 festgelegt ist. Wenn Sie jedoch die Größe des Auftrags bekannt, den der Debitor bewirken, für das fragliche Produkt erteilen möchten, geben Sie diesen Wert stattdessen ein. Diese Informationen sind von Bedeutung, wenn die Handelsvereinbarungen mit dem Debitor Mengenpausen haben, d. h. der Preis des Produkts aus der eingekauften Menge abhängt.  
6. Im Datumsfeld geben Sie ein Datum für, wenn der Debitor erwartet, einen Auftrag zu erteilen. 
    * Das Datum kann heute oder ab einem beliebigen Datum in der Zukunft beginnen.  
    * Im System wird nun den Preis zurück, der für das ausgewählte Produkt gültig ist, wenn er durch den ausgewählten Debitor für das ausgewählte Datum mit einer angegebenen Menge eingekauft wird. In diesem Beispiel wenn der Debitor US-001 1 Einheit des Produkts T0004 heute erworben hat, werden  350 EUR pro Einheit berechnet. Dieser Preis stammt aus einer Fähigkeit oder Handelsvereinbarung mit dem Debitor.      Andere Felder auf der Seite finden Sie weitere Informationen zu den Produktpreis und die Produkt Kosten (wenn im Produktmaster eingerichtet werden) und berechnete Rentabilität.  
    * Wenn die Option "Ähnliche Produktvarianten anzeigen" aktiviert ist, bedeutet dies, dass es zusätzliche Handelsvereinbarungen für die Varianten des Produkts gibt.  
7. Klicken Sie auf das Kontrollkästchen "Ähnliche Produktvarianten anzeigen".
    * Eine Liste der Produktvarianten wird, mit Informationen zu ihrem Dimensionen angezeigt.  
8. Wählen Sie in der Liste markieren Sie die Position, die Farbe Weiß darstellt.
    * Hinweis, der Produktpreis ist jetzt zu dem unterscheiden, der zuvor angezeigt wird, als diese nicht pro Dimension angegeben wurde.  
9. Klicken Sie auf Verkaufspreise anzeigen.
    * Auf der Preis (Verkauf) aller Handelsvereinbarungen anwendbar dem Produkt, einschließlich der Varianten.  
10. Schließen Sie die Seite.

## <a name="find-the-applicable-discount"></a>Suchen des gültigen Rabatts
Stellen Sie sicher, dass das Feld "Debitorenkonto" Debitornummer US-001 enthält    
1. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "T0012" ein.
    * Stellen Sie sicher, dass das Feld Menge auf 1 festgelegt ist.  
    * Die folgenden Preiskalkulationsdetails, die für Produkt T0012 angezeigt werden, stammen aus einer oder mehreren Handelsvereinbarungen: Der Preis je Einheit beträgt 1,000 EUR sowie der Rabattprozentsatz ist 5.  
2. Legen Sie die Menge auf "20" fest.
    * Die erweiterte Bestellmenge verursacht den Positionsrabatt, der dem Debitor der Änderung von 5 bis 7 Prozent angeboten wird.  
    * Der Nettobetrag wird auf dem Stückpreis, dem Rabatt und dem Gesamtpreis berechnet.  
3. Klicken Sie auf Positionsrabatt anzeigen.
    * Es gibt zwei Positionsrabattvereinbarungen für Produkt T0012 und gibt einen 5-Prozent-Rabatt für eine Auftragspositionsmenge von 1 bis 10 und ein 7-Prozent-Rabatt für Bestellmengen zu 10. geliefert. Beachten Sie, dass die Rabatte zu einer Gruppe Produkten, in diesem Beispiel, Gruppencode 01 angewendet werden, des Produkts T0012 angehört.  
4. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]