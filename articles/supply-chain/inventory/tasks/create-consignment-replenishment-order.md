---
title: Unterlieferungs-Wiederbeschaffungsauftrag erstellen
description: Dieses Thema erklärt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f426dbf00eace23da2f26eb50dd9675fe22ed445
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914772"
---
# <a name="create-a-consignment-replenishment-order"></a>Unterlieferungs-Wiederbeschaffungsauftrag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Thema erklärt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können. Es zeigt auch, wie einen Produktempfang erfassen, damit der Lieferungsbestand als verfügbarer Lagerbestand im Besitz des Kreditors erfasst wird. Diese Prozedur würde normalerweise durch einen Beschaffungsspezialist durchgeführt. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

## <a name="create-a-consignment-replenishment-order"></a>Unterlieferungs-Wiederbeschaffungsauftrag erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Lieferung > Unterlieferungs-Wiederbeschaffungsaufträge**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Kreditorenkonto** **US-104** aus (Sie müssen einen Kreditor auswählen, der als Besitzer auf der Seite **Bestandseigentümer** erfasst ist). 
4. Wählen Sie **OK**.
5. Wählen Sie **Position hinzufügen** aus.
6. Wählen Sie im Feld **Artikelnummer** `M9211CI` aus (Sie müssen einen Artikel auswählen, der für Lieferbestand eingerichtet wurde).
7. Geben Sie im Feld **Menge** eine Zahl ein.
8. Geben Sie im Feld **Angefordertes Lieferdatum** ein Datum ein. Die Angefordert und Bestätigt-Daten werden im MRP-Modul für den Wareneingang der erwarteten Waren verwendet.  
9. Geben Sie im Feld **Bestätigtes Lieferdatum** ein Datum ein.
10. Erweitern Sie den Abschnitt **Positionsdetails**.
11. Wählen Sie die Registerkarte **Lagerungsdimensionen** aus.
12. Um den Eigentümer im Feld **Lagerungsdimensionseigentümer** anzuzeigen, aktualisieren Sie die Seite. Kreditor US-104 wird jetzt als Besitzer aufgeführt.  

## <a name="check-the-inventory-transaction-status"></a>Prüfen des Lagerbuchungstatus
1. Wählen Sie **Bestand** aus.
2. Wählen Sie **Buchungen** aus.
3. Beachten Sie in der gewünschten Zeile, dass das Feld **Zugang** auf **Bestellt** festgelegt ist.  
4. Schließen Sie die Seite.

## <a name="receive-items"></a>Artikel empfangen
1. Wählen Sie **Produktzugang** aus.
2. Geben Sie im Feld **Externer Produktzugang** einen Wert ein.
3. Geben Sie im Feld **Menge** eine Zahl ein, die geringer ist als die Zahl, die dort angezeigt wird. 
4. Wählen Sie **OK**.

## <a name="check-the-on-hand-inventory"></a>Prüfen des verfügbaren Lagerbestands
1. Wählen Sie **Bestand** aus.
2. Wählen Sie **Verfügbar** aus.
3. Wählen Sie **Überblick** aus. Die Artikel, die als verfügbarer Lieferungsbestand eingegangen sind, der dem Kreditor gehört, sind der verfügbare Bestand. Die Restmenge für den Unterlieferungs-Wiederbeschaffungsauftrag wird im Feld **Insgesamt bestellt** angezeigt.  
4. Schließen Sie die Seite.

