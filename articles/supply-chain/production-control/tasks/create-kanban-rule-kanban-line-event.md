--- 
title: Eine Kanban-Regel mithilfe eines Kanban-Positionsereignisses erstellen
description: "Diese Prozedur erstellt eine Kanban-Regel mithilfe der Kanban-Positionsereigniseinstellung, um das Ausführen von Pull aus einer Prozessaktivität auszulösen."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Eine Kanban-Regel mithilfe eines Kanban-Positionsereignisses erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur erstellt eine Kanban-Regel mithilfe der Kanban-Positionsereigniseinstellung, um das Ausführen von Pull aus einer Prozessaktivität auszulösen. Die Kanban-Regel wird durch eine Kanban-Prozessaktivität jeweils mit einer Menge gleich oder größer als 25 ausgelöst. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.


## <a name="create-a-kanban-rule"></a>Erstellen einer Kanban-Regel
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.
    * Dadurch werden Kanbans direkt auf Grundlage des Bedarfs generiert. Dies wird verwendet, um Regeln einzurichten, die ein Auftragsfertigungszenario definieren.  
4. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie "SpeakerAssemblyAndPolish" ein oder wählen Sie es aus. Die erste Aktivität einer Kanban-Regel für die Fertigung ist eine Prozessaktivität im Produktionsfluss. Wenn Sie die Aktivität auswählen, werden die Gültigkeitsdaten der Aktivität in die Gültigkeitsdaten der Kanban-Regel kopiert.  
5. Erweitern Sie den Abschnitt "Details".
6. Geben Sie im Feld "Produkt" den Wert "L0001" ein.
7. Erweitern Sie den Abschnitt "Ereignis".
8. Wählen Sie im Feld "Kanban-Positionsereignis" die Option "Automatisch" aus.
    * Dadurch werden Ereignis-Kanbans bei Bedarf generiert.  Dieses Feld wird verwendet, um Kanban-Regeln zu konfigurieren, durch die für eine Downstream-Prozessaktivität erforderliches Material aufgefüllt wird. Wenn Sie "Automatisch" auswählen, werden die Ereignis-Kanbans mit dem Bedarf erstellt. Diese Einstellung wird empfohlen, wenn Sie erwarten, Produktion am gleichen Tag auszuführen.  
9. Legen Sie die "Mindestmenge für Ereignis" auf '25' fest.
    * Ereignis-Kanbans werden generiert, wenn die Bedarfsmenge gleich oder größer als dieses Feld ist. Dies ist nützlich, wenn Sie eine Auftragsmenge produzieren möchten, die geringer als dieses Feld auf einer Maschine und größer als dieses Feld auf einer anderen Maschine ist.  
10. Klicken Sie auf "Speichern".

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Aufträge erstellen und Kanban-Kette auslösen
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Kundenkonto "US-003, Forest Wholesales" aus.  
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0001" ein.
    * L0001 ist ein Artikel, für den Sie die Kanban-Regel erstellt haben.  
6. Legen Sie die Menge auf "27" fest.
    * Weil 27 höher als die Mindestmenge von 25 auf der Kanban-Regel ist, löst dies ein Ereignis-Kanban aus.  
7. Geben Sie im Feld 'Standort' den Wert '1' ein.
8. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Lagerort 13.  
9. Klicken Sie auf "Speichern".

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Die durch die Kanban-Regel generierte Kanban anzeigen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Erweitern Sie den Abschnitt "Kanbans".
    * Beachten Sie, dass ein Kanban für 27 erstellt wurde, um die Aktivität auf Grundlage der erstellten Kanban-Regel zu verarbeiten.  
    * Dies ist der letzte Schritt.  


