---
title: Definieren von Kreditorenzahlungsbedingungen
description: In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden.
author: abruer
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f47fc0cd67cddef3c73f9c4c6b8dd6f41bbe85ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838908"
---
# <a name="define-vendor-payment-terms"></a>Definieren von Kreditorenzahlungsbedingungen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Zahlungseinstellungen > Zahlungsbedingungen**.
2. Wählen Sie **Neu** aus. Die Seite "Zahlungsbedingungen" wird verwendet, um zu definieren, wie das Fälligkeitsdatum berechnet wird. Sie wird nicht verwendet, um zu definieren, wie das Skontodatum berechnet wird.  
3. Geben Sie im Feld **Zahlungsbedingungen** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Geben Sie im Feld **Tage** eine Zahl ein. Die Zahl, die hier eingegeben wird, wird verwendet, um sie dem Fälligkeitsdatum oder dem Ende der Periode, die in der Zahlungsmethode angegeben ist, hinzuzufügen. Wenn Sie zum Beispiel **Netto** auswählen, wird die Zahl zum Fälligkeitsdatum addiert. Wenn Sie **Aktueller Monat** auswählen, wird die Zahl dem letzten Tag des aktuellen Monats hinzugefügt, um das Fälligkeitsdatum zu berechnen.  
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.
8. Wechseln Sie zu **Kreditoren > Zahlungseinstellungen > Skonti**.
9. Wählen Sie **Neu** aus.
10. Geben Sie im Feld **Skonto** eine Kennung ein.
11. Geben Sie im Feld **Beschreibung** einen Wert ein.
12. Wenn der Kreditor einen gestaffelten Rabatt anbietet, wählen Sie das nächste Skonto aus, nachdem das aktuelle abgelaufen ist.
13. Schließen Sie die Seite.
14. Geben Sie im Feld **Tage** eine Zahl ein. Die Menge, die im Feld **Tage** eingegeben wird, wird verwendet, um das Skontodatum zu berechnen, basierend darauf, welche Option im Feld **Netto/Aktuell** ausgewählt wurde. Wenn **Netto** ausgewählt wurde, wird die Menge zum Rechnungsdatum hinzugefügt, um das Skontodatum zu bestimmen. Wenn **Aktueller Monat** ausgewählt wurde, wird die Menge zum Ende des Währungsmonats hinzugefügt, um das Skontodatum zu bestimmen.  
15. Geben Sie im Feld **Rabatt** den Prozentsatz des Skontos ein. 
16. Geben Sie das Hauptkonto ein, in das der Skonto für Debitorenrechnungen gebucht wird. Geben Sie dann das Hauptkonto ein, in das der Skonto für Kreditorenrechnungen gebucht wird. Wenn **Rabattgegenkonten** auf **Hauptkonto für Kreditorenrabatte verwenden** festgelegt wird, dann wird das „Hauptkonto“ verwendet. Wenn die Option auf **Konten in den Rechnungspositionen** festgelegt ist, wird der Skonto zu den Anlagen-/Ausgabenkonten auf den Rechnungspositionen gebucht.  
17. Wählen Sie **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]