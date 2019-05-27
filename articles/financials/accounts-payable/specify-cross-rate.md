---
title: Angeben des Kreuzkurses
description: Dieses Thema enthält allgemeine Informationen zu Kreuzkurse in Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546063"
---
# <a name="specify-the-cross-rate"></a>Angeben des Kreuzkurses

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Zweck eines Kreuzkurses erklärt, und wie der Kreuzkurs angegeben wird, wenn Sie eine Zahlung mit einer Rechnung ausgleichen. Verwenden Sie einen Kreuzkurs, wenn alle folgenden Kriterien zutreffen: 
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
