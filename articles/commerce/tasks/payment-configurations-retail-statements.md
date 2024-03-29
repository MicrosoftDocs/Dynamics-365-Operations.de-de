---
title: " Zahlungskonfigurationen für Einzelhandelsauszüge"
description: Diese Prozedur zeigt Konfigurationen für Commerce-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3c8c7678d88b3c01138aa098b8830336885e6445fb41931b19bcda2b95b86b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712356"
---
# <a name="payment-configurations-for-retail-statements"></a> Zahlungskonfigurationen für Einzelhandelsauszüge

[!include [banner](../includes/banner.md)]

Diese Prozedur zeigt Konfigurationen für Commerce-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.

Für diese Erfassung wird das Demo-Unternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Geschäfte > Alle Einzelhandelsgeschäfte.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]