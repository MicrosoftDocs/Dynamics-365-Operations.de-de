--- 
title: "Eine Menüoption für das mobile Gerät einrichten, um die eingegangenen Artikel zu erfassen"
description: "Ziel dieser Aufgabe ist es, ein Menüelement für ein mobiles Gerät einzustellen."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7b5d757361c1163bbd0300abd3da4e0a2dd6b0e0
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Eine Menüoption für das mobile Gerät einrichten, um die eingegangenen Artikel zu erfassen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ziel dieser Aufgabe ist es, ein Menüelement für ein mobiles Gerät einzustellen. Diese Menüoption wird für die Erfassung des Artikelzugangs verwendet, der über Bestellungen bestellt wurde. 

Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Diese Prozedur ist für die Lagerverwaltung vorgesehen.


## <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menüoptionen für mobiles Gerät".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Menüoptionsname" einen Wert ein.
    * Dies ist der eindeutige Kennung für diese Menüoption des mobilen Geräts. So können beispielsweise "Meine Bestellungsregistrierung" eingeben.  
4. Geben Sie im Feld "Titel" einen Wert ein.
    * Dies ist der Titel, der für den Benutzer im mobilen Gerät angezeigt wird. So können beispielsweise "Bestellungsregistrierung" eingeben.  
5. Wählen Sie im Feld "Modus" "Arbeit"aus.
    * Die Erfassung von den eingegangen verfügbaren Mengen für eine Bestellposition erstellt Arbeit für das Verschieben der Artikel aus dem Eingangsbereich in das Lager. Arbeit wird erst erstellt, nachdem die Artikel erfasst sind.  Daher lassen Sie die Option "Vorhandene Arbeit verwenden" auf "Nein".  
6. Erweitern oder reduzieren Sie den Abschnitt "Allgemein".
7. Wählen Sie im Feld "Arbeitserstellungsprozess" "Bestellungsartikel – Empfang" aus.
    * Eine Bestellposition muss eindeutig identifiziert werden können bevor ein offener Lagerbestand am Lagerort erfasst werden kann. In diesem Szenario erfasst das mobile Gerät die Bestellnummer und die Artikelnummer, und das System kann so die Bestellposition identifizieren. Einlagerungsarbeit wird erstellt und kann von einer anderen Arbeitskraft gewählt werden.    Die Arbeitserstellungsmethode, die Sie auswählen, bestimmt, welche Felder auf dem Inforegister "Allgemein" verfügbar sind.  
    * Wenn Sie die Option "Standarddaten verwenden" auswählen, wird die Schaltfläche "Standarddaten" aktiviert. Hier können Sie Felder für die Anzeige der Daten wählen, die eine Arbeitskraft in der Regel in ihrer täglichen Arbeit benötigt, so das diese Werte auf dem mobilen Gerät angezeigt werden.  
    * Die Parameter "Ladungsträgergruppierung" arbeitet in Kombination mit der Einheit Nummernkreisgruppe die dem eingegangen Artikel zugewiesen ist. Sie können festlegen, ob Wareneingänge aus weniger oder mehr als einer Palette in einen Ladungsträger gruppiert werden oder in einen separaten Ladungsträger für jede Einheit aufgeteilt werden sollen.  
    * Wenn Sie die Option "Ladungsträger generieren" auswählen, generiert dies einen eindeutigen Ladungsträger aus Basis der Nummernkreis-Auswahl.   
    * Sie können die Vorlage auswählen, die verwendet wird, wenn Arbeit erstellt wird. Wenn Sie zum Beispiel einen Artikel für eine Bestellung erfassen, wird die Entnahmearbeit auf Grundlage der Arbeitsvorlage generiert. Wenn Sie keine Arbeitsvorlage auswählen, weist das System eine Vorlage auf Grundlage der Abfragekriterien zu, die den Vorlagen zugeordnet sind.  
    * Wenn Dispositionscodes auf dem mobilen Gerät angezeigt werden, können Arbeitskräfte den Status oder die Menge der Artikel überprüfen und den entsprechenden Code auswählen. Die Regeln für den Dispositionscode bestimmen, ob die Artikel für andere Lagerortprozesse verfügbar ist. Die Regeln legen außerdem fest, welche Lagerplatzdirektive für die Arbeit verwendet wird, die erstellt wird.   
    * Wenn Sie die Option "Chargendispositionscodes" verwenden, können Arbeitskräfte den Status oder die Menge einer Charge überprüfen und den entsprechenden Code auswählen.  Die Regeln für den Chargendispositionscode bestimmen, ob die Charge für andere Lagerortprozesse verfügbar ist.  
    * Wenn Sie die Option "Beschriftungen drucken" auswählen, wird eine Ladungsträgerbeschriftung beim Eingang der Artikel automatisch gedruckt.  
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Hinzufügen der Menüoption zu einem mobilen Gerät
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menü für mobiles Gerät".
2. Verwenden Sie den Schnellfilter, um im Feld "Name" nach dem Wert 'Eingehend' zu filtern.
3. Klicken Sie auf Bearbeiten.
4. Wählen Sie in der Struktur "Wählen Sie in der Struktur die Menüoption aus, die Sie zuvor erstellt haben." aus.
    * Wählen Sie das Menüelement aus, das Sie erstellt haben.  
5. Klicken Sie auf den Pfeil nach rechts.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.


