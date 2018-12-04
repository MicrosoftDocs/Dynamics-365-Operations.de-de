--- 
title: Auftragssperren verwalten
description: "In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3edb8d2fe0fda6634bc2edb8e3bafc5a60344b7a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="manage-order-holds"></a>Auftragssperren verwalten

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden. Ein Auftrag kann aus unterschiedlichen Gründen gesperrt werden. Sie können beispielsweise einen Auftrag sperren, bis eine Debitorenadresse oder eine Zahlungsmethode überprüft werden können, oder bis ein Manager das Kreditlimit des Debitors prüfen kann. Während der Auftrag gesperrt ist, kann er vom Lager nicht für den Versand bearbeitet werden. 

Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="set-up-order-holds"></a>Auftragssperren einrichten
1. Wechseln Sie zu „Vertrieb und Marketing” > „Setup” > „Verkaufsaufträge” > „Auftragssperrcodes”.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld „Sperrcode” einen Wert ein.
    * Geben Sie beispielsweise „Rückruf” ein.  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Beispielsweise „Auftrag gesperrt bis Kundenrückruf”.  
    * Aktivieren Sie optional das Kontrollkästchen „Erfassungen entfernen”, um sämtliche physischen Erfassungen aus dem Auftrag zu entfernen, wenn dieser Sperrcode hinzugefügt wird.  
5. Klicken Sie auf "Speichern".

## <a name="place-order-on-hold"></a>Auftrag sperren
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Menge" eine Zahl ein.
7. Klicken Sie im Aktivitätsbereich auf "Auftrag".
8. Klicken Sie auf „Auftragssperren”.
9. Klicken Sie auf "Neu".
10. Wählen Sie im Feld „Sperrcode” einen Code aus, den Sie in der vorherigen Teilaufgabe erstellt haben.
11. Klicken Sie auf "Speichern".
12. Schließen Sie die Seite.
13. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
14. Markieren Sie in der Liste die ausgewählte Zeile.
    * Bei Aufträge, der derzeit gespert sind, sind die Felder „Nicht verarbeiten” und „Sperren” markiert.    
15. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".

## <a name="manage-order-holds"></a>Auftragssperren verwalten
1. Wechseln Sie zu „Vertrieb und Marketing”  „Aufträge” > „Offene Bestellungen” > „Auftragsssperren”.
    * Auftrag sperrt Seitenfunktionen als Workbench, wo Sie einen Überblick über alle aktuellen und verarbeiteten Sperren abrufen können sowie zugeordnete Verkaufsaufträge bearbeiten können.      
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Klicken Sie im Aktivitätsbereich auf „Sperre ausschecken”.
4. Klicken Sie auf „Auschecken”.
5. Heben Sie in der Liste die Markierung der ausgewählten Zeile auf.
    * Das „Auschecken nach Feld” zeigt jetzt Ihre Benutzer-ID.   
6. Klicken Sie auf „Auschchecken löschen”.
7. Klicken Sie im Aktivitätsbereich auf „Sperre aufheben”.
    * Wenn Sie bereit sind, die Sperre aufzuheben und die Verarbeitung des Auftrags bis zum nächsten Erfüllungsschritt zulassen, müssen Sie die Sperre aufheben. Wenn der Auftrag keine Änderungen erfordert, können Sie die Aktion „Sperren aufheben” ausführen. Allerdings können Sie die Aktion „Deaktivieren und ändern” verwenden, wenn bei der Aufhebung der Sperre der Auftrag aktualisiert werden muss.      
    * Die Aktion „Deaktivieren und übermitteln” kann nur verwendet werden, wenn Sie Callsenterfunktionen verwenden.  
8. Klicken Sie auf „Sperren aufhaben”.
    * Die Sperre ist nun aus dem Auftrag deaktiviert worden und aus der Liste von aktiver Sperren entfernt worden. Um alle Sperren oder ihre Teilmengen nach einem spezifischen Status anzuzeigen, ändern Sie den Wert im Feld „Anzeigen”.     


