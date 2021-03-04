---
title: Lohnprozess für Zeit und Anwesenheit aktivieren
description: Diese Prozedur zeigt, wie der Lohnprozess für Zeit und Anwesenheit aktiviert wird.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5805cc31bf9c7c2231defab63dc9a1e67f82622a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428669"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Lohnprozess für Zeit und Anwesenheit aktivieren

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie der Lohnprozess für Zeit und Anwesenheit aktiviert wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Lohnart mit einem zugehörigen Lohnsatz erstellen
1. "Zeit und Anwesenheit" > "Einstellungen" > "Lohn" > "Lohnarten"
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lohnart" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf "Sätze".
    * Sätze für Lohnarten werden für bestimmte Zeitintervalle eingerichtet, wobei für Arbeitskräfte individuelle Sätze erstellt werden können. Es ist nicht immer erforderlich, Sätze unter "Zeit und Anwesenheit" zu erstellen. Diese Informationen wurden möglicherweise bereits in dem Lohnabrechnungssystem angelegt, das zum Generieren von Löhnen und Gehältern verwendet wird.  
7. Klicken Sie auf "Neu".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld "Satz" eine Zahl ein.
10. Klicken Sie auf "Speichern".

## <a name="create-a-pay-agreement"></a>Erstellen einer Lohnvereinbarung
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu "Lohnvereinbarungen".
    * "Zeit und Anwesenheit" > "Einstellungen" > "Lohnvereinbarungen"  
4. Klicken Sie auf "Neu".
5. Geben Sie im Feld "Lohnvereinbarung" einen Wert ein.
6. Geben Sie im Feld "Beschreibung" einen Wert ein.
7. Klicken Sie auf "Speichern".
8. Klicken Sie auf "Vereinbarungspositionen".
9. Klicken Sie auf "Neu".
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Geben Sie im Feld "Profiltyp" einen Wert ein, oder wählen Sie einen Wert aus.
12. Geben Sie im Feld "Lohnart" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Lohnvereinbarung für Zeit- und Erfassungsarbeitskraft einrichten
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu "Zeiterfassung für Arbeitskräfte".
    * "Zeit und Anwesenheit" > "Einstellungen" > "Zeiterfassung für Arbeitskräfte"  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf die Registerkarte "Anstellung".
6. Erweitern Sie den Abschnitt "Zeiterfassung".
7. Klicken Sie auf "Bearbeiten".
8. Geben Sie im Feld "Lohnvereinbarung" einen Wert ein, oder wählen Sie einen Wert aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]