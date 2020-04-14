---
title: Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen
description: In diesem Thema wird gezeigt, wie die Ladungsplanungsworkbench verwendet wird, um eine Auslastung für einen Auftrag zu erstellen.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145880"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Auslastungen und Lieferungen mithilfe der Ladungsplanungsworkbench planen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird gezeigt, wie die Ladungsplanungsworkbench verwendet wird, um eine Auslastung für einen Auftrag zu erstellen. Im Voraus erstellen wir zuerst den Auftrag. Dieses Verfahren ist Teil der täglichen Arbeit für den Transportkoordinator. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-sales-order"></a>Auftrag erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Debitorenkonto** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
4. Wählen Sie das Konto **US-004** aus.
5. Wählen Sie **OK**.
6. Wählen Sie im Feld **Artikelnummer** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
7. Wählen Sie den Artikel **A0001** aus. **A0001** ist für die Transportverwaltung aktiviert.  
8. Wählen Sie im Feld **Standort** die Dropdown-Schaltfläche, um die Suche zu öffnen, und wählen Sie dann einen Artikel aus.
9. Geben Sie im Feld **Menge** eine Zahl ein.
10. Geben Sie im Feld **Lagerort** „24“ für dieses Beispiel ein. Dieser Lagerort wird für Transportverwaltung und von erweiterten Lagerortverwaltung aktiviert.  
11. Wählen Sie **Speichern**.
12. Schließen Sie die Seite.

## <a name="create-a-new-load"></a>Erstellen Sie eine neue Auslastung
1. Wechseln Sie zu **Navigationsbereich > Module > Transportverwaltung > Planung > Ladungsplanungsworkbench**.
2. Wählen Sie die Registerkarte **Verkaufspositionen** aus. Nun erstellen Sie die Auslastung für den Auftrag, den Sie soeben erstellt haben. Auslastung des Systems während können auf Grundlage Angebot und Nachfrage aus Bestellungen, von den Umlagerungsaufträge und die Aufträge erstellt werden.  
3. Wählen Sie im Aktivitätsbereich **Beschaffung und Bedarf** aus.
4. Wählen Sie **An neue Ladung** aus.
5. Wählen Sie im Feld **Ladungsvorlagenkennung** die Dropdown-Schaltfläche aus, um die Suche zu öffnen. Die Auslastungsvorlage definiert maximale Messung für Gewicht und Volumen der gesamten Auslastung. Beispielsweise könnte die Auslastungsvorlage die Größe eines Containers oder des LKWs darstellen. Wählen Sie einen Artikel aus.
6. Wählen Sie **OK**.

## <a name="rate-and-route-the-load"></a>Auslastung bewerten und umleiten
1. Wählen Sie **Bewertung und Weiterleitung** aus.
2. Wählen Sie **Routen-Workbench-Satz** aus.
3. Wählen Sie **Shopsatz** aus.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Wählen Sie **Zuweisen** aus.
6. Schließen Sie die Seite.

