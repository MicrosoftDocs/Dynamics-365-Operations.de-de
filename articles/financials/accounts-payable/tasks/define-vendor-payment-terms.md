---
title: Kreditorenzahlungsbedingungen definieren
description: Zahlungsbedingungen für Kreditorenrechnungen einrichten
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569031"
---
# <a name="define-vendor-payment-terms"></a>Kreditorenzahlungsbedingungen definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Zahlungsbedingungen für Kreditorenrechnungen einrichten Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu Kreditoren > Zahlungseinstellungen > Zahlungsbedingungen.
2. Klicken Sie auf "Neu".
    * Die Seite "Zahlungsbedingungen" wird verwendet, um zu definieren, wie das Fälligkeitsdatum berechnet wird. Sie wird nicht verwendet, um zu definieren, wie das Skontodatum berechnet wird.  
3. Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Tage" eine Zahl ein.
    * Die Zahl, die hier eingegeben wird, wird verwendet, um sie dem Fälligkeitsdatum oder dem Ende der Periode, die in der Zahlungsmethode angegeben ist, hinzuzufügen. Wenn Sie zum Beispiel "Netto" auswählen, wird die Zahl zum Fälligkeitsdatum addiert. Wenn Sie "Aktueller Monat" auswählen, wird die Zahl dem letzten Tag des aktuellen Monats hinzugefügt, um das Fälligkeitsdatum zu berechnen.  
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.
8. Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Skonti".
9. Klicken Sie auf "Neu".
10. Geben Sie im Feld "Skonto" eine Kennung ein.
11. Geben Sie im Feld "Beschreibung" einen Wert ein.
12. Wenn der Kreditor einen gestaffelten Rabatt anbietet, wählen Sie das nächste Skonto aus, nachdem das aktuelle abgelaufen ist.
13. Schließen Sie die Seite.
14. Geben Sie im Feld "Tage" eine Zahl ein.
    * Die Menge, die im Feld "Tag" eingegeben wird, wird verwendet, um das "Skontodatum" zu berechnen, basierend darauf, welche Option im Feld "Netto/Aktuell" ausgewählt wurde. Wenn "Netto" ausgewählt wurde, wird die Menge zum Rechnungsdatum hinzugefügt, um das Skontodatum zu bestimmen. Wenn "Aktueller Monat" ausgewählt wurde, wird die Menge zum Ende des Währungsmonats hinzugefügt, um das Skontodatum zu bestimmen.  
15. Geben Sie im Feld "Rabatt" den Prozentsatz des Skontos ein. 
16. Geben Sie das Hauptkonto ein, zu dem der Skonto für Debitorenrechnungen gebucht wird.
17. Geben Sie das Hauptkonto ein, zu dem der Skonto für Kreditorenrechnungen gebucht wird.
    * Wenn "Rabattgegenkonten" auf "Hauptkonto für Kreditorenrabatt verwenden" festgelegt wird, dann wird das "Hauptkonto" verwendet.  Wenn die Option auf "Konten zu den Rechnungspositionen" festgelegt ist, wird der Skonto zu den Anlagen-/Ausgabenkonten auf den Rechnungspositionen gebucht.  
18. Klicken Sie auf "Speichern".

