--- 
title: "Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen"
description: Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cecda03dd4d224d4319f2b0b196560389bb54195
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen. Der Kaufvertrag muss angewendet werden, wenn Sie die Bestellung anlegen, da es allgemeine Begriffe gibt, die in den Bestellkopf kopiert werden sollen. In der Regel steht diese Aufgabe von einem Einkaufsvertreter ausgeführt. Als Komponente für dieses Manuell, müssen Sie einen gültigen Kaufvertrag mit einer Produktmengenzusage für einen Kreditor und Artikel verwenden. Die gleichen Verfahren kann verwendet werden, wenn Sie einen Kaufvertrag mit anderen Typen von Zusagen haben. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Wenn Sie USMF verwenden, können Sie Handbuch "Erstellen eines Kaufvertrags" zuerst ausführen, um die erforderlichen Vorbedingungen für dieses Handbuch einzurichten.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Bestellungsvorbereitungs des Arbeitsbereich anzeigen
2. Neue Bestellung
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.
7. Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Alle verfügbaren Vereinbarungen für den Kreditor werden hier aufgeführt. Finden Sie die gültige Vereinbarung, die Sie verwenden wollen.  
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "Ja".
10. Klicken Sie auf "OK".

## <a name="add-a-line"></a>Hinzufügen einer Line
1. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Sind bestimmte Lager- oder Lagerplatzdimensionen auf der Zusage besteht, müssen Sie die denselben Werten in der Bestellposition eingeben, um die Vereinbarung auszunutzen.  
2. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Der Standort bereits wird mit dem Standardwert aus dem Auftrag oder Kreditor ausgefüllt werden. Ist dies der Fall, fahren Sie diesen Schritt.  
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Menge" eine Zahl ein.
    * Überprüfen Sie, ob der Preis aus der Zusage kopiert wird.  

## <a name="look-up-the-commitment"></a>Hiermit wird die Zusage
1. Klicken Sie auf "Position aktualisieren".
2. Klicken Sie auf "Zugeordnet".
    * Hier können Sie Details für den Kaufvertrag abrufen. So können Sie den Preis finden und ob der Preis und Rabatt korrigiert werden, damit es, das heißt dass, wenn Sie Preis oder Rabatt auf die Bestellung zu einem anderen Wert als auf der Zusage ändern, das System den Link entfernt, sodass die Bestellposition nicht die Zusage erfüllt. Sie können außerdem feststellen, ob das Maximum erzwungene Option ist aktiviert ist, das heißt, dass die Menge in der Zusage nicht überschritten werden kann, indem Sie alle Einkäufe summiert, die die Zusage erfüllen.  
3. Schließen Sie die Seite.

## <a name="look-up-the-purchase-agreement"></a>Rahmenbestellung einrichten
1. Klicken Sie im Aktivitätsbereich auf "Allgemein".
2. Rahmenbestellungsrichtlinie
3. Schließen Sie die Seite.
4. Schließen Sie die Seite.


