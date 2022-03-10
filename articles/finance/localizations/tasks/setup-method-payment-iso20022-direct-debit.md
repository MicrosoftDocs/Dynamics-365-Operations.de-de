---
title: Zahlungsmethode für ISO20022-Direktbelastungen einrichten
description: Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127d5402abfedcce124b39b76a6c1036a6c818a7c1318aaeabdb0688b50f738e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779760"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Zahlungsmethode für ISO20022-Direktbelastungen einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird. 



Bevor Sie diese Aufgabe abschließen, müssen Sie Exportformatkonfigurations- und Zahlungskonteneinstellung eingerichtet haben.



Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.



Dies ist die dritte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.

1. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Zahlungsmethode" mit dem Wert "ELEKTRONISCH".
3. Klicken Sie auf Bearbeiten.
4. Geben Sie im Feld "Zahlungskonto" die Werte "DEMF OPER" an.
5. Erweitern Sie den Abschnitt 'Dateiformate'.
6. Wählen Sie „Ja“ im Feld "Generische elektronische Berichterstellung" aus.
7. Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.
    * Wählen Sie in der Liste "ISO20022 Direktbelastung (DE)" aus.  Wenn die Liste leer ist, bedeutet dies, dass es keine importierte und aktive Debitorenzahlungs-Exportformatkonfiguration gibt.  
8. Wählen Sie „Ja“ im Feld "Mandat anfordern" aus.
    * Wählen Sie den Parameter "Mandat anfordern" für Debitorenzahlungsformate, die Vollmachtsinformationen in der Zahlungsnachricht benötigen, wie SEPA-Direktbelastung.  
9. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]