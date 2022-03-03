---
title: Definieren von Kreditorenzahlungsbedingungen
description: In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2199c12e92d631d3eb058637c48b53335d779f2d
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109806"
---
# <a name="define-vendor-payment-terms"></a>Definieren von Kreditorenzahlungsbedingungen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Zahlungseinstellungen > Zahlungsbedingungen**.
2. Wählen Sie **Neu** aus. Die Seite **Zahlungsbedingungen** wird verwendet, um zu definieren, wie das Fälligkeitsdatum berechnet wird. Sie wird nicht verwendet, um zu definieren, wie das Skontodatum berechnet wird.  
3. Geben Sie im Feld **Zahlungsbedingungen** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Geben Sie im Feld **Tage** eine Zahl ein. Die Zahl, die hier eingegeben wird, wird verwendet, um sie dem Fälligkeitsdatum oder dem Ende des Zeitraums, der in der **Zahlungsmethode** angegeben ist, hinzuzufügen. Wenn Sie zum Beispiel **Netto** auswählen, wird die Zahl zum Fälligkeitsdatum addiert. Wenn Sie **Aktueller Monat** auswählen, wird die Zahl dem letzten Tag des aktuellen Monats hinzugefügt, um das Fälligkeitsdatum zu berechnen.  
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.
8. Wechseln Sie zu **Kreditoren > Zahlungseinstellungen > Skonti**.
9. Wählen Sie **Neu** aus.
10. Geben Sie im Feld **Skonto** eine Kennung ein.
11. Geben Sie im Feld **Beschreibung** einen Wert ein.
12. Wenn der Kreditor einen gestaffelten Rabatt anbietet, wählen Sie das nächste Skonto aus, nachdem das aktuelle abgelaufen ist.
13. Schließen Sie die Seite.
14. Geben Sie im Feld **Tage** eine Zahl ein. Die Menge, die im Feld **Tage** eingegeben wird, wird verwendet, um das **Skontodatum** zu berechnen, basierend darauf, welche Option im Feld **Netto/Aktuell** ausgewählt wurde. Wenn **Netto** ausgewählt wurde, wird die Menge zum Rechnungsdatum hinzugefügt, um das Skontodatum zu bestimmen. Wenn **Aktueller Monat** ausgewählt wurde, wird die Menge zum Ende des Währungsmonats hinzugefügt, um das Skontodatum zu bestimmen.  
15. Geben Sie im Feld **Rabatt** den Prozentsatz des Skontos ein. 
16. Geben Sie das Hauptkonto ein, in das der Skonto für Debitorenrechnungen gebucht wird. Geben Sie dann das Hauptkonto ein, in das der Skonto für Kreditorenrechnungen gebucht wird. Wenn **Rabattgegenkonten** auf **Hauptkonto für Kreditorenrabatte verwenden** festgelegt wird, dann wird das „Hauptkonto“ verwendet. Wenn die Option auf **Konten in den Rechnungspositionen** festgelegt ist, wird der Skonto zu den Anlagen-/Ausgabenkonten auf den Rechnungspositionen gebucht.  
17. Wählen Sie **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
