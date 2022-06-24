---
title: Kreuzkurs angeben
description: Dieser Artikel enthält allgemeine Informationen zu Kreuzkursen in Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889960"
---
# <a name="specify-the-cross-rate"></a>Kreuzkurs angeben

[!include [banner](../includes/banner.md)]

In diesem Artikel wird der Zweck eines Kreuzkurses erklärt, und wie der Kreuzkurs angegeben wird, wenn Sie eine Zahlung mit einer Rechnung ausgleichen. Verwenden Sie einen Kreuzkurs, wenn die folgenden Kriterien zutreffen: 
-   Sie gleichen eine Zahlung mit einer Rechnung aus. 
-   Die Zahlungsposition und die Rechnungsposition verwenden verschiedene Währungen. 
-   Keine dieser Währungen ist die Buchhaltungswährung. 

Der Kreuzkurs wird nicht verwendet, um die Zahlungsbuchungswährungsübersetzung der Buchhaltungswährung für die Zahlung zu berechnen. Stattdessen werden die Wechselkurse aus den Wechselkurstabellen abgerufen, um den Wert des Zahlungsbuchungswährungsbetrags und des Zahlungsbuchhaltungswährungsbetrags zu berechnen. 

Beispielsweise ist die Buchhaltungswährung USD, die Rechnungswährung ist CAD, und die Zahlungswährung ist EUR. Mit dem Kreuzkurs können Sie einen Wechselkurs eingeben, um direkt zwischen CAD und EUR zu übersetzen, ohne in EUR zu übersetzen. Beim Auswählen einer Rechnung und einer Primärzahlung besteht die Möglichkeit zum Eingeben eines Kreuzkurses für die Rechungsposition. Bei diesem Kreuzkurs handelt es sich um den Wechselkurs zwischen den Währungen zum Ausgleichsdatum.

1.  Gehen Sie zu den folgenden Seiten:
- **Klicken Sie auf Debitoren  Allgemein  Kunden  Alle Kunden** 
- **Gehen Sie zu "Kreditorenkonten" > "Allgemein" > "Händler" > alle Händler** 
- **Klicken Sie auf Beschaffung > Gemeinsam > Kreditoren > Alle Kreditoren**
2.  Wählen Sie den Debitor oder Kreditor aus, dessen offene Posten ausgeglichen werden sollen. 
3.  Für einen Debitor auf der Listenseite **Alle Debitoren** gehen Sie zu **Sammeln > Offene Buchungen ausgleichen**. Für einen Debitor auf der Listenseite **Alle Debitoren** gehen Sie zu **Sammeln > Offene Buchungen ausgleichen**. 
4.  Wählen Sie die Buchung aus, bei der es sich um die primäre Zahlung handelt, und klicken Sie auf die Schaltfläche **Zahlung markieren** . Das Kontrollkästchen in der Spalte **Markieren** wird aktiviert, und in der Spalte **Primäre Zahlung** wird ein Informationssymbol angezeigt. 
5.  Geben Sie im Feld **Kreuzkurs** den Wechselkurs zwischen der Rechnungs- und der Zahlungswährung zum Ausgleichsdatum ein. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
