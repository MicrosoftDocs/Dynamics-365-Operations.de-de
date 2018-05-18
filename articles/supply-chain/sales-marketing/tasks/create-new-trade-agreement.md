--- 
title: Eine neue Handelsvereinbarung erstellen
description: Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a>Eine neue Handelsvereinbarung erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Wenn Sie eigene Daten verwenden, bevor Sie dieses Handbuch starten, müssen Sie prüfen, ob ein Handelsvereinbarungserfassungsname vorhanden ist, in die standardmäßige Beziehung festgelegt ist " Preis- (Verkauf )".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Erstellen und buchen einer neuen Handelsvereinbarungs-Erfassung.
1. Wechseln Sie zu Vertrieb und Marketing > Preise und Rabatte > Handelsvereinbarungserfassungen.
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf "Positionen".
7. Wählen Sie im Feld Kontocode die Option Tabelle aus.
    * In diesem Beispiel aktualisieren Sie den Preis für einen bestimmten Debitor, dem Durchschnitt Sie Tabelle auswählen muss. Wenn Sie den Listenpreis des Produkts aktualisierten, geben Sie alle aktivieren, damit der neue Preis für alle Debitoren gültig ist. Wenn Sie Preise unter verschiedenen Debitorensegmenten unterschieden, dann geben Sie Gruppe auswählen. Um Gruppe festzulegen, muss Debitorenpreisgruppen eingerichtet haben.  
8. Klicken Sie im Feld Konto-Auswahl auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Wählen Sie im Feld Artikelcode "Tabelle" aus.
    * Wenn Sie eine Handelsvereinbarung vom Typ "Preis (Verkauf)" eingegeben werden, müssen Sie "Tabelle" im Feld Artikelcode nur auswählen. Dies ist, da ein Preis ein absoluter Wert ist und nicht gleiche für alle oder eine Gruppe Produkte werden kann.  
11. Klicken Sie im Feld Artikelrelation auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
12. In der Liste wählen Sie das Produkt aus, das Sie in die Vereinbarung aufnehmen wollen.
    * Notieren Sie, an dem Produkt Sie ausgewählt haben.  
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Geben Sie in das Von-Feld eine Minimalmenge ein.
    * Wenn der Debitor eine Menge bestellen muss, bevor sie für den neuen Preis qualifiziert sind, dann können Sie Anforderung, diese Menge hier anzugeben.  
    * Geben Sie einen Wert im Feld, um die maximale Menge anzugeben, zu der der Preis der Vereinbarung nicht gültig ist. Wenn Sie Angebotspreise und Rabatte auf Grundlage mehrere Mengenpausen, dann jede Mengenklammer als Paar der minimalen und maximalen Menge in " " und"" zu aus den Feldern bzw. angeben.  
15. Geben Sie einen Preis in das Feld "Betrag in Währung" ein.
16. In das Feld Von Datum, geben Sie ein Datum ein, ab dem diese Vereinbarung gilt.
17. Klicken Sie auf "Speichern".
18. Klicken Sie auf "Überprüfen".
19. Klicken Sie auf Ausgewählte Positionen überprüfen.
20. Klicken Sie auf "OK".
21. Klicken Sie auf "Buchen".
22. Klicken Sie auf "OK".

## <a name="view-trade-agreements-for-a-product"></a>Handelsvereinbarungen für ein Produkt anzeigen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Wählen Sie in der Liste suchen Sie und wählen Sie das Produkt aus, dessen Preis Sie derzeit aktualisiert haben.
3. Klicken Sie im Aktivitätsbereich auf "Verkaufen".
4. Klicken Sie auf Handelsvereinbarungen anzeigen.
    * Prüfen Sie die Details der Preishandelsvereinbarung, soeben erstellt haben.    
5. Schließen Sie die Seite.


