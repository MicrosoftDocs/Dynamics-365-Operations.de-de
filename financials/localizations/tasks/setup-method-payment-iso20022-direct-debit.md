--- 
title: "Zahlungsmethode für ISO20022-Direktbelastung einrichten"
description: "Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Zahlungsmethode für ISO20022-Direktbelastung einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird. 



Bevor Sie diese Aufgabe abschließen, müssen Sie Exportformatkonfigurations- und Zahlungskonteneinstellung eingerichtet haben.



Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.



Dies ist die dritte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.

1. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Zahlungsmethode" mit dem Wert "ELEKTRONISCH".
3. Klicken Sie auf Bearbeiten.
4. Geben Sie im Feld "Zahlungskonto" die Werte "DEMF OPER" an.
5. Erweitern Sie den Abschnitt 'Dateiformate'.
6. Wählen Sie "Ja" im Feld "Generische elektronische Berichterstellung" aus.
7. Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.
    * Wählen Sie in der Liste "ISO20022 Direktbelastung (DE)" aus.  Wenn die Liste leer ist, bedeutet dies, dass es keine importierte und aktive Debitorenzahlungs-Exportformatkonfiguration gibt.  
8. Wählen Sie "Ja" im Feld "Mandat anfordern" aus.
    * Wählen Sie den Parameter "Mandat anfordern" für Debitorenzahlungsformate, die Vollmachtsinformationen in der Zahlungsnachricht benötigen, wie SEPA-Direktbelastung.  
9. Klicken Sie auf "Speichern".


