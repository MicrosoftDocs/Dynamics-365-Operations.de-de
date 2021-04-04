---
title: Zahlungsmethode für ISO20022-Kreditübertragung einrichten
description: Dieses Verfahren zeigt, wie ISO20022 für die Kreditorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung zur Generierung einer Datei verwendet wird.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ae91ce361ab3e4e799ec82ca9e05c9e11d81ed1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256569"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Zahlungsmethode für ISO20022-Kreditübertragung einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ISO20022 für die Kreditorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung zur Generierung einer Datei verwendet wird. 

Bevor Sie diese Aufgabe abschließen, müssen Sie Exportformatkonfigurations- und Zahlungskonteneinstellung eingerichtet haben.

Diese Aufgabe wurde mit dem Demodatenunternehmen DEMF erstellt.

Dies ist der dritte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

1. Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Zahlungsmethoden" mit dem Wert "SEPA CT".
3. Klicken Sie auf Bearbeiten.
4. Wählen Sie im Feld "Zeitraum" die Option "Summe".
5. Wählen Sie im Feld "Zahlungstyp" "Elektronischer Zahlungsverkehr" aus.
6. Erweitern Sie den Abschnitt 'Dateiformate'.
7. Wählen Sie „Ja“ im Feld "Generische elektronische Berichterstellung" aus.
8. Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.
    * Wählen Sie in der Liste den Wert ISO20022 Banküberweisung (DE) aus. Wenn die Liste leer ist, bedeutet dies, dass es keine importierte und aktive Kreditorenzahlungs-Exportformatkonfiguration gibt.  
9. Wählen Sie im Feld "Kontotyp" "Bank" aus.
10. Geben Sie im Feld "Zahlungskonto" die Werte "DEMF OPER" an.
11. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]