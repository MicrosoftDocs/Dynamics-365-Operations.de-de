--- 
title: " Zahlungskonfigurationen für Einzelhandelsauszüge"
description: "Diese Prozedur zeigt Konfigurationen für Einzelhandelsgeschäft-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 19f9c0b1c3a93ed9c84d66041814fd64951744b0
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---
# <a name="payment-configurations-for-retail-statements"></a> Zahlungskonfigurationen für Einzelhandelsauszüge

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur zeigt Konfigurationen für Einzelhandelsgeschäft-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.

Für diese Erfassung wird das Demo-Unternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Einrichten".
5. Klicken Sie auf "Zahlungsmethoden".
6. Erweitern oder reduzieren Sie den Abschnitt ''Buchung".
7. Klicken Sie auf "Bearbeiten".
    * Wählen Sie aus, ob die Beträge, die für diese Zahlungsmethode eingehen, auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.  
    * Wählen Sie das Konto aus, auf dem die Beträge, die für diese Zahlungsmethode eingehen, gebucht werden sollen.  
    * Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem Betrag, der für diese Zahlungsmethode berechnet wird, zu buchen.  
    * In diesem Feld können Sie einen Betrag eingeben, um zu steuern, wann der Differenzbetrag auf einem anderen Differenzkonto gebucht werden soll. Sie können dieses verwenden, um große Differenzen zu verfolgen.  
    * Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem gezählten Betrag zu buchen, wenn er den Wert überschreitet, der im Feld "Maximaler Differenzbetrag" definiert ist.  
    * Wählen Sie "Ja" aus, um Bankeinzahlungsbeträge auf einem separaten Konto zu buchen.  
    * In diesem Feld können Sie auswählen, ob Bankeinzahlungsbeträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.  
    * Wählen Sie das Konto zum Buchen von Bankeinzahlungsbeträgen aus.  
    * Wählen Sie die Bankbuchungsart aus, die zum Buchen von Bankeinzahlungsbeträgen auf das Bankkonto verwendet werden soll.  
    * Wählen Sie "Ja" aus, um Ablage im Tresor-Beträge auf einem separaten Konto zu buchen.  
    * Wählen Sie aus, ob Ablage im Tresor-Beträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.  
    * Wählen Sie das Konto zum Buchen von Ablage im Tresor-Beträgen aus.  
8. Klicken Sie auf "Speichern".


