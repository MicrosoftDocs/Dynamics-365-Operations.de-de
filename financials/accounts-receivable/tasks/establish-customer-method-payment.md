--- 
title: Zahlungsmethode des Debitoren einrichten
description: "Erstellen Sie eine Zahlungsmethode für Debitorenzahlungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bfafcccb12112ca7cceefb65be3f942bfc307751
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-method-of-payment"></a>Zahlungsmethode des Debitoren einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Erstellen Sie eine Zahlungsmethode für Debitorenzahlungen. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zahlungsmethoden" eine Kennung für die Zahlungsmethode ein.
    * Die "Zahlungsmethodenkennung" wird auf Rechnungen und Zahlungen angezeigt, damit werden sie beschreibend genug, um zu verstehen, welche Art der Zahlung erfasst wird und für welches Bankkonto.  
4. Geben Sie im Feld "Beschreibung" eine Beschreibung ein.
5. Wählen Sie aus, welcher Zahlungsstatus erforderlich ist, damit Zahlungen gebucht werden.
    * Wird eine Debitorenzahlung erstellt, kann sie nur gebucht werden, wenn der Zahlungsstatus mit dem Zahlungsstatus übereinstimmt, den Sie hier definieren.  
6. Wählen Sie aus, wie Debitorenzahlungen für Rechnungen erstellt werden sollen.
    * Diese Option wird nur verwendet, wenn ein Zahlungsvorschlag ausgeführt wird. Ein Zahlungsvorschlag könnte für Debitorenzahlungen verwendet werden, wenn Direktbelastungen ausgeführt werden und die Mittel aus den Bankkonten der Debitoren eingezogen werden.  
7. Wählen Sie den Typ der Zahlung aus.
    * Mithilfe des Zahlungstyps können Sie feststellen, ob irgendeine Prüfung für die Zahlung erfolgt oder nicht.  
8. Wählen Sie aus, auf welchen Kontotyp Zahlungen gebucht werden.
    * Normalerweise wird Bank für diese Option aktiviert.  
9. Wählen Sie das Bankkonto aus, in dem diese Zahlung erfasst wird.
10. Geben Sie den Banktransaktionstyp ein, um den Typ der Zahlung zu identifizieren, der von Ihrer Bank verwendet wird.
    * Der Banktransaktionstyp wird während des Bankabstimmungsprozesses verwendet und kann die Abstimmung erleichtern.  
11. Wählen Sie aus, ob diese Zahlung vorübergehend auf ein Transferkonto gebucht werden soll.
    * Wenn Sie die Zeittoleranz ausprobieren möchten, mit der eine Zahlung bei der Bank verrechnet wird, verwenden Sie die Funktionen "Transfer". Die Zahlung wird vorübergehend zu einem "Sachkonto" gebucht, bis sie bei der Bank verrechnet wird. Zu diesem Zeitpunkt erreicht die Zahlung das Bankkonto, das Sie hier definiert haben.  
12. 'Geben Sie das Hauptkonto ein, das für die Transferbuchung verwendet wird.
    * Dies ist das Hauptkonto, auf das die Zahlung vorübergehend gebucht wird, wenn Sie den Transfer verwenden.  
13. Verwenden Sie die Registerkarte "Dateiformat", um Einstellungen für elektronische Zahlungen zu definieren.
14. Verwenden Sie die Registerkarte "Zahlungskontrolle", um Felder zu definieren, die erforderlich sind.
    * Wenn Sie beispielsweise verlangen, dass alle Zahlungen mit dieser Zahlungsmethode eingezahlt werden, können Sie diese Option auf dieser Registerkarte auswählen.  
15. Verwenden Sie die Registerkarte "Zahlungsattribute", um zu definieren, welche Zahlungsattribute Sie für diese Zahlungsmethode verwenden möchten.
16. Klicken Sie auf "Speichern".


