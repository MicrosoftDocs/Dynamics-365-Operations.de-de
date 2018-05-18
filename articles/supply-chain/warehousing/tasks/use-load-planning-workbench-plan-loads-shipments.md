--- 
title: Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen
description: "Im folgenden Verfahren wird gezeigt, wie der Auslastungsplanungswerktisch verwendet wird, um eine Auslastung für einen Auftrag zu erstellen."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren wird gezeigt, wie der Auslastungsplanungswerktisch verwendet wird, um eine Auslastung für einen Auftrag zu erstellen. Im Voraus erstellen wir zuerst den Auftrag. Dieses Verfahren ist Teil der täglichen Arbeit für den Transportkoordinator. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-sales-order"></a>Auftrag erstellen
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie das Konto US-004 aus.
5. Klicken Sie auf "OK".
6. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Artikel A0001 auswählen.
    * A0001 ist für die Verwaltung von Transports aktiviert.  
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie im Feld "Menge" eine Zahl ein.
10. Geben Sie im Feld Lagerort "24" ein.
    * In diesem Beispiel wählen Sie Lagerort 24 aus. Dieser Lagerort wird für Transportverwaltung und von erweiterten Lagerortverwaltung aktiviert.  
11. Klicken Sie auf "Speichern".
12. Schließen Sie die Seite.

## <a name="create-a-new-load"></a>Erstellen Sie eine neue Auslastung
1. Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.
2. Klicken Sie auf die Registerkarte Verkaufszeilen.
    * Nun erstellen Sie die Auslastung für den Auftrag, den Sie soeben erstellt haben. Auslastung des Systems während können auf Grundlage Angebot und Nachfrage aus Bestellungen, von den Umlagerungsaufträge und die Aufträge erstellt werden.  
3. Klicken Sie im Aktivitätsbereich auf "Angebot und Nachfrage".
4. Klicken um in neue Ladung verschieben.
5. Klicken Sie im Feld "Ladungsvorlagen-ID" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Auslastungsvorlage definiert maximale Messung für Gewicht und Volumen der gesamten Auslastung. Beispielsweise könnte die Auslastungsvorlage die Größe eines Containers oder des LKWs darstellen.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf "OK".

## <a name="rate-and-route-the-load"></a>Auslastung bewerten und umleiten
1. Klicken Sie auf Bewertung und Weiterleitung.
2. Klicken Sie auf Routen-Workbench-Satz.
3. Klicken Sie auf Shopsatz.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie auf Zuweisen.
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.


