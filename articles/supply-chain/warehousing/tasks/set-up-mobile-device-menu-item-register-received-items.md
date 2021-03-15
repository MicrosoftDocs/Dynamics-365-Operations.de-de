---
title: Eine Menüoption für das mobile Gerät einrichten, um die eingegangenen Artikel zu erfassen
description: In diesem Thema geht es um die Einrichtung eines Menüpunktes für mobile Geräte.
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6f9cf258a991b88faa0d2db90cd3c21f9703267
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976962"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Eine Menüoption für das mobile Gerät einrichten, um die eingegangenen Artikel zu erfassen

[!include [banner](../../includes/banner.md)]

In diesem Thema geht es um die Einrichtung eines Menüpunktes für mobile Geräte. Diese Menüoption wird für die Erfassung des Artikelzugangs verwendet, der über Bestellungen bestellt wurde. 

Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Diese Prozedur ist für die Lagerverwaltung vorgesehen.


## <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts
1. Gehen Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einrichtung > Mobiles Gerät > Menüpunkte Mobiles Gerät**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Menüoptionsname** einen Wert ein. Dies ist der eindeutige Kennung für diese Menüoption des mobilen Geräts. Sie können z.B. `My PO registration` eingeben.  
4. Geben Sie im Feld **Titel** einen Wert ein. Dies ist der Titel, der für den Benutzer im mobilen Gerät angezeigt wird. Sie können z.B. `PO registration` eingeben.  
5. Wählen Sie im Feld **Modus** **Arbeit**. Die Erfassung von den eingegangen verfügbaren Mengen für eine Bestellposition erstellt Arbeit für das Verschieben der Artikel aus dem Eingangsbereich in das Lager. Arbeit wird erst erstellt, nachdem die Artikel erfasst sind. Lassen Sie daher die Option **Bestehende Arbeit nutzen** auf **Nein** gesetzt.
6. Wählen Sie im Feld **Arbeitserstellungsprozess** des Abschnitts **Allgemein** **Bestellpositioneneingang**.
    - Eine Bestellposition muss eindeutig identifiziert werden können bevor ein offener Lagerbestand am Lagerort erfasst werden kann. In diesem Szenario erfasst das mobile Gerät die Bestellnummer und die Artikelnummer, und das System kann so die Bestellposition identifizieren. Einlagerungsarbeit wird erstellt und kann von einer anderen Arbeitskraft gewählt werden. Die von Ihnen gewählte Methode der Arbeitserstellung bestimmt, welche Felder auf der **Allgemein** FastTab verfügbar werden.  
    - Wenn Sie die Option **Standarddaten verwenden** auswählen, ist die Schaltfläche **Standarddaten** aktiviert. Hier können Sie Felder für die Anzeige der Daten wählen, die eine Arbeitskraft in der Regel in ihrer täglichen Arbeit benötigt, so das diese Werte auf dem mobilen Gerät angezeigt werden.  
    - Der Parameter **Ladungsträgerbeschriftungsgruppierung** arbeitet in Kombination mit der Einheitsfolgegruppe, die dem empfangenen Element zugeordnet ist. Sie können festlegen, ob Wareneingänge aus weniger oder mehr als einer Palette in einen Ladungsträger gruppiert werden oder in einen separaten Ladungsträger für jede Einheit aufgeteilt werden sollen.  
    - Wenn Sie die Option **Ladungsträgerbeschriftung generieren** auswählen, wird ein eindeutiges Kennzeichen basierend auf der Auswahl der Nummernfolge erzeugt.  
    - Sie können die Vorlage auswählen, die verwendet wird, wenn Arbeit erstellt wird. Wenn Sie zum Beispiel einen Artikel für eine Bestellung erfassen, wird die Entnahmearbeit auf Grundlage der Arbeitsvorlage generiert. Wenn Sie keine Arbeitsvorlage auswählen, weist das System eine Vorlage auf Grundlage der Abfragekriterien zu, die den Vorlagen zugeordnet sind.  
    - Wenn Dispositionscodes auf dem mobilen Gerät angezeigt werden, können Arbeitskräfte den Status oder die Menge der Artikel überprüfen und den entsprechenden Code auswählen. Die Regeln für den Dispositionscode bestimmen, ob die Artikel für andere Lagerortprozesse verfügbar ist. Die Regeln legen außerdem fest, welche Lagerplatzdirektive für die Arbeit verwendet wird, die erstellt wird.   
    - Wenn Sie die Option **Chargenverteilungscodes** auswählen, können die Mitarbeiter den Status oder die Qualität einer Charge bewerten und den entsprechenden Dispositionscode auswählen. Die Regeln für den Chargendispositionscode bestimmen, ob die Charge für andere Lagerortprozesse verfügbar ist.  
    - Wenn Sie die Option **Etiketten drucken** auswählen, wird beim Empfang von Artikeln automatisch ein Nummernschild gedruckt.  
7. Wählen Sie **Speichern**.
8. Schließen Sie die Seite.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Hinzufügen der Menüoption zu einem mobilen Gerät
1. Gehen Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einrichtung > Mobiles Gerät > Menü Mobiles Gerät**.
2. Verwenden Sie den **Schnellfilter**, um nach dem Feld **Name** mit dem Wert `inbound` zu filtern.
3. Wählen Sie **Bearbeiten** aus.
4. Wählen Sie im Baum Verfügbare Menüs und Elemente den Menüpunkt aus, den Sie zuvor erstellt haben.
5. Wählen Sie den Pfeil, der nach rechts zeigt.
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]