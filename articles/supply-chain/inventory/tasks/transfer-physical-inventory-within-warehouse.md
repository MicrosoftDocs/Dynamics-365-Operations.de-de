---
title: Physischen Bestand im Lagerort übertragen
description: Diese Prozedur führt Sie durch den Prozess der Erstellung und des Buchens einer Umlagerungserfassung, um Artikelbewegungen von einem Lagerplatz eines Lagerorts an einen anderen zu erfassen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b3e91be8aeab10188b6d3925d44a9ec1106406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554183"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Physischen Bestand im Lagerort übertragen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch den Prozess der Erstellung und des Buchens einer Umlagerungserfassung, um Artikelbewegungen von einem Lagerplatz eines Lagerorts an einen anderen zu erfassen. Sie müssen einen Namen der Lagererfassungen für die Umlagerungen haben, bevor Sie diese starten. Sie können diese Prozedur im Demodatunternehmen USMF mithilfe der angezeigten Beispielswerte ausführen, oder eigene Daten verwenden, wenn Sie bereits Produkte und Lagerplätze eingerichtet haben. Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt.


## <a name="create-an-inventory-transfer-journal"></a>Lagerumlagerungserfassung erstellen
1. Wechseln Sie zu "Umlagerung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".
    * Es gibt die Option, "Von"- und "Bis"-Dimensionen für jede Erfassungsposition anzugeben. Dies ist für diesen Erfassungstyp wesentlich. Sie können Artikel unter Verwendung der verschiedenen Regeln an andere Lagerplätze umlagern. In diesem Beispiel lagern Sie einen Artikel innerhalb des gleichen Lagerorts von einem Ladungsträger gesteuerten Lagerplatz zu einem Lagerplatz, der nicht von einem Ladungsträger gesteuert wird, um.   

## <a name="create-journal-lines"></a>Erfassungspositionen erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie A0001 auswählen.  
3. Geben Sie im Feld "Von Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "2" auswählen.  
4. Geben Sie im Feld "Nach Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "2" auswählen.  
5. Geben Sie im Feld "Von Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "24" auswählen.  
6. Geben Sie im Feld "Nach Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "24" auswählen.  
7. Geben Sie im Feld "Von Lagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "FL-001" auswählen.  
8. Geben Sie im Feld "Nach Lagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "BULK-001" auswählen.  
9. Geben Sie im Feld "Menge" eine Zahl ein.
10. Klicken Sie auf die Registerkarte "Lagerungsdimension".
11. Geben Sie im Feld "Ladungsträger" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "24" auswählen.  
12. Klicken Sie auf "Speichern".

## <a name="post-the-inventory-transfer-journal"></a>Umlagerungserfassung buchen
1. Klicken Sie auf "Buchen".
2. Klicken Sie auf "OK".

## <a name="view-inventory-transactions"></a>Lagerbuchungen anzeigen
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Transaktionen".
    * Hier können Sie die Transaktionen anzeigen, die erstellt wurden, als Sie Ihre Erfassung gebucht haben.  

