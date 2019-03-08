---
title: Ausleihartikel einrichten
description: Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e17005bda302c58f5a6560fe9c4eda04e918c92f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "341832"
---
# <a name="create-loan-items"></a>Ausleihartikel einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht. Jeder physische Artikel muss einen entsprechenden Ausleihartikel haben. Jeder Ausleihartikel-Datensatz beschreibt, was ausgeliehen wird, wer für das Ausleihen zuständig ist und die Anzahl von Tage, die der Artikel ausgeliehen werden kann. Sie können mehrere Ausleihartikel, wie Schlüssel, Zugangsberechtigungskarten oder Uniformen, gleichzeitig erstellen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-loan-types"></a>Ausleihtypen einrichten
1. Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihtypen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ausleihtypen" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie die Anzahl der Tage ein, die diesem Ausleihtyp zugeordnete Artikel überfällig sein können. 
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.
8. Aktualisieren Sie die Seite.

## <a name="create-loan-items"></a>Ausleihartikel erstellen
1. Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihartikel".
2. Klicken Sie auf "Ausleihartikel einrichten".
3. Im Feld "Mge." eine Zahl ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Ausleihtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Geben Sie hier die maximale Ausleihdauer in Tagen ein.
    * Der Standardwert im Feld "Geplante Rückgabe" auf der Seite "Ausgeliehene Ausrüstung" wird als aktuelles Datum zuzüglich der Nummer berechnet.  
9. Klicken Sie im Feld "Zuständige Person" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Klicken Sie auf Auswählen.
11. Geben Sie eine Zahl in das Feld "Anfangswert" ein.
12. Geben Sie im Feld "Intervall" eine Zahl ein.
13. Geben Sie im Feld "Format" einen Wert ein.
    * Wenn die Startnummer für einen Ausleihartikel beispielsweise 10 ist, geben Sie im Feld "Format" zwei Nummernzeichen ein.  
14. Klicken Sie auf "OK".
15. Aktualisieren Sie die Seite.

