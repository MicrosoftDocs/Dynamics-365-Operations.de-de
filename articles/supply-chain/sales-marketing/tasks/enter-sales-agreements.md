--- 
title: "Kaufverträge eingeben"
description: "Diese Prozedur zeigt wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: a0d49068d2c6a62bf7912c2fd7cccd53308bd196
ms.contentlocale: de-de
ms.lasthandoff: 02/13/2018

---
# <a name="enter-sales-agreements"></a>Kaufverträge eingeben

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="set-up-sales-agreement-header"></a>Kaufvertragskopfzeile einrichten
1. Wechseln Sie zu "Vertrieb und Marketing" > "Kaufverträge" > "Kaufverträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Erweitern Sie den Abschnitt "Allgemein".
9. Wählen Sie im Feld "Standardzusage" "Produktwertszusage" aus.
    * Ein Zusagetyp ist ein erforderliches Kriterium, das Sie Verträgen zuweisen müssen, um zu definieren, wie Vertrag erfüllt wird. Mit den vier vordefinierten Typen können Sie das Zusageziel des Debitors einrichten (als Menge bzw. Wert). Der Mengenzusagetyp kann nur auf ein bestimmtes Produkt angewendet werden. Die wertbasierten Typen sind auf den Verkauf bestimmter und unspezifischer Produkte anwendbar.  
10. Wählen Sie im Feld "Ablaufdatum" Datum auf das Datum fest, ab dem Sie die Vereinbarung abzulaufen soll.
11. Klicken Sie auf "OK".

## <a name="set-up-product-value-commitment-lines"></a>Produktwertzusagepositionen einrichten
1. Klicken Sie auf "Position hinzufügen".
2. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Der Typ der Zusage, den Sie für die Vereinbarung ausgewählt haben, betrifft die Art der Informationen, die Sie für die Vereinbarungspositionen eingeben können. Für eine wertbasierte Vereinbarung müssen Sie zum Beispiel den Gesamtnettobetrag (in der vereinbarten Währung) für den der Debitor den Kauf von Waren von Ihnen zusagt angeben. In diesem Beispiel sind die Felder "Menge" und "Einheit" in der Position nicht verfügbar, da Sie eine Vereinbarung für den Kunden zum Kauf eines bestimmten Wertes eines Produkts erstellten.   
5. Im Feld "Nettobetrag" geben Sie den Geldbetrag ein, den der Debitor für den Einkauf zugesagt hat.
6. Geben Sie im Feld "Rabattprozent" einen Prozentwert ein, der für die Auftragspositionen des Debitors gilt, der dieser Vereinbarung zugeordnet ist.
7. Erweitern Sie den Abschnitt "Positionsdetails".
8. Wählen Sie "Ja" im Feld "Maximum wird erzwungen".
    * Die Auswahl von "Maximum wird erzwungen" bedeutet, dass der Gesamtbetrag aller Auftragspositionen, die die Sonderpreise der Zusage verwenden und/oder der Zahlungsbedingungen den auf der Zusage angegeben Betrag nicht überschreiten darf.  
    * Die minimalen und maximalen Freigabemengen geben einen Wertebereich an, für bei jedem Auftrag verkauft werden muss, der die ausgewählte Vereinbarung verwendet.   
9. Erweitern Sie den Kopfbereich "Kaufvertrag".
    * Solange der Status der Vereinbarung nicht auf "Effektiv" festgelegt ist, können Aufträge nicht dem Vertrag zugeordneten werden. Sie können daher nicht zur Erfüllung dieser Vereinbarung beitragen. Der können den Status zu diesem Zeitpunkt manuell ändern. Allerdings wird der Status normalerweise geändert, wenn die Vereinbarung für den Debitor bestätigt wird.  
10. Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".
11. Klicken Sie auf Bestätigung.
    * Stellen Sie sicher, dass die Option "Vertrag als 'Effektiv' kennzeichnen" auf "Ja" festgelegt ist.  
12. Wählen Sie "Ja" im Feld "Bericht drucken" aus.
13. Klicken Sie auf "OK".
14. Schließen Sie die Seite.
    * Die Vereinbarung ist nun effektiv und Sie können Kundenaufträge mit der Vereinbarung verknüpfen, um diese dem Zusageziel zuzurechnen.  


