---
title: Kaufvertrag erstellen
description: Diese Prozedur führt Sie durch die Erstellung eines Kaufvertrags.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "338612"
---
# <a name="create-a-purchase-agreement"></a>Kaufvertrag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch die Erstellung eines Kaufvertrags. Dadurch wird normalerweise von einem Einkaufsleiter bearbeitet. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden. Sie müssen Einstellungen Kaufvertragsklassifizierungen haben, bevor Sie beginnen. Sobald Sie eine Vereinbarung erstellt haben, können Sie diese verwenden, wenn Sie eine Bestellung erstellen, und dieses kopiert die Kaufvertragszustände in den Kopf und alle möglichen Positionen in der Reihenfolge angezeigt, die in der Vereinbarung betroffen sind.


## <a name="create-a-new-purchase-agreement"></a>Erstellen Sie eine neue Rahmenbestellung
1. Wechseln Sie zu "Beschaffung" > "Kaufverträge" > "Kaufverträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Erweitern Sie den Abschnitt "Allgemein".
10. Geben Sie im Feld "Ablaufdatum" ein Datum ein.
    * Dieses Ablaufdatum ist der Standardwert für alle Zusagepositionen und bestimmt, wie lange jede einzelne Zusage gültig ist.  
11. Geben Sie im Feld Dokumenttitel einen Namen für den neuen Kaufvertrag ein.
    * Überlassen Sie dem Standard Zusagefeldsatz Produktmengenzusage (oder ändern Sie sie, wenn keine Zuordnung zu diesem festgelegt ist).  
    * Der standardmäßige Zusagewert bestimmt Die verfügbaren Optionen in der Vertragspositionen. Wenn Sie einen neuen Zusagetyp erfordern, wenn Sie die Vereinbarungspositionen erstellen, müssen Sie die standardmäßige Zusage im Kopf ändern.  Es gibt 4 Typen von Zusagen: Produktmengenzusage - für eine bestimmte Menge eines Produkts; Produktwertszusage - für einen bestimmten Währungsbetrag eines Produkts; Produktkategoriewertszusage - für einen bestimmten Währungsbetrag in einer Beschaffungskategorie, in der der Betrag für einen Katalogartikel oder einen nicht im Katalog enthaltenen Artikel sein kann; Wertszusage - für einen bestimmten Währungsbetrag, der durch ein beliebiges Produkt oder von einer beliebigen Beschaffungskategorie gedeckt werden kann.  
12. Klicken Sie auf "OK".

## <a name="add-a-commitment"></a>Zusage hinzufügen
1. Klicken Sie auf "Position hinzufügen".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie das Produkt aus, das Sie eine Zusage für hinzufügen möchten.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Geben Sie im Feld "Menge" eine Zahl ein.
    * Dies ist die Gesamtmenge, die Sie Lieferscheinbuchung, von Ihrem Lieferanten kaufen.  
7. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
8. Erweitern Sie den Abschnitt "Positionsdetails".
9. Legen Sie die Option "Maximum wird erzwungen" auf "Ja" fest.
    * Die Höchstzahl ist erzwungene Optionsgrenzen der Verwendung der Zusage. Sie können auf die Menge nur kaufen, die im Feld für die Position angegeben wird.  
10. Reduzieren Sie den Abschnitt "Positionsdetails".

## <a name="add-header-conditions"></a>Kopfzeilenbedingungen hinzufügen
1. Klicken Sie im Aktivitätsbereich auf "Optionen".
2. Klicken Sie auf "Ansicht ändern".
3. Klicken Sie auf die Kopfzeilenansicht.
4. Erweitern Sie den Abschnitt "Bedingungen".
5. Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Zahlungsbedingungen vom Kreditorenkonto werden hier standardmäßig angezeigt.       
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Lieferart" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Klicken Sie im Feld "Lieferbedingungen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="confirm-and-activate-the-agreement"></a>Bestätigen und Aktivieren des Kaufvertrags
1. Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".
2. Klicken Sie auf Bestätigung.
    * Setzen Sie die Option "Vertrag als 'Effektiv' kennzeichnen" auf "Ja" fest.  
3. Klicken Sie auf "OK".
4. Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".
5. Klicken Sie auf Kaufvertragsbestätigungen.
    * Die Vorschau anzeigen/der Druckoption ermöglicht es Ihnen, ein Dokument für den Kaufvertrag zu generieren, den Sie oder Kreditor senden können dann drucken. Wenn Sie die Vereinbarung später aktualisieren und sie wieder-bestätigen, werden beide Versionen hier angezeigt.  
6. Schließen Sie die Seite.

