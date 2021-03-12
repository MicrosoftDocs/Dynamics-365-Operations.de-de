---
title: Mahnschreiben verarbeiten
description: In diesem Thema erfahren Sie, wie Sie Abholbriefe erstellen, drucken und versenden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a189bbdd360d07b2b5198fa357380fd9a89ac167
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992963"
---
# <a name="process-collection-letters"></a>Mahnschreiben verarbeiten

[!include [banner](../../includes/banner.md)]

In diesem Thema erfahren Sie, wie Sie Abholbriefe erstellen, drucken und versenden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Richten Sie eine Mahnschreibensequenz zum Buchungsprofil ein.
1. Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Einrichtung > Kundenbuchungsprofile**.
2. Klicken Sie auf **Bearbeiten**.
3. Wählen Sie eine Mahnschreibensequenz aus der Dropdownliste aus. Wenn Sie kein Mahnschreiben für Buchungen dieses Buchungsprofils erstellen wollen, lassen Sie das Feld leer.  
4. Erweitern Sie die Registerkarte **Tabellenbeschränkungen**, um die Verarbeitung von Sammelbriefen zu ändern. Wenn dieses Feld auf **Ja** festgelegt ist, werden Mahnschreiben für dieses Buchungsprofil erstellt.  

## <a name="create-collection-letters"></a>Mahnschreiben erstellen
1. Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Inkassoschreiben > Inkassoschreiben erstellen**.
2. Sie müssen die Buchungsarten auswählen, die Sie anmahnen wollen. Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.  
3. Wählen Sie im Feld **Mahnschreiben** eine Mahnschreibenoption aus.
4. Geben Sie im Feld **Inkassoschreiben Datum** das Datum des Inkassoschreibens ein.
5. Wählen Sie ein Buchungsprofil aus, wenn Sie **Verwenden des Buchungsprofils aus** in **Auswählen** geändert haben. Es gibt zwei Arten von Buchungsoptionen:   

   - **Konto** – Dient zum Verwenden des Buchungsprofils, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.   
   - **Auswählen** – Dient zum Verwenden des im Feld **Buchungsprofil** ausgewählten Buchungsprofils.  

6. Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
7. Wählen Sie **Filter** aus.
8. Geben Sie im Feld **Kriterien** eine "Debitorenkennung" ein. Geben Sie beispielsweise "US-001" ein.
9. Wählen Sie **OK**.
10. Wählen Sie **OK**.

## <a name="print-collection-letters"></a>Mahnschreiben drucken
1. Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Inkassoschreiben > Review und Bearbeitung von Inkassoschreiben**.
2. Wählen Sie im Feld **Status** die Option **Erstellt** aus.
3. Wählen Sie im Feld **Gedruckt** die Option **Nicht gedruckt** aus.
4. Wählen Sie **Drucken**.
5. Wählen Sie **Abholbrief Notiz**.
6. Geben Sie im Abschnitt **Parameter** das Stichtagsdatum für Buchungen ein.
7. Erweitern Sie den Abschnitt **Sätze um den Abschnitt** und geben Sie die Details des Inkassoschreibens ein.
8. Wählen Sie **OK**, um den Inkassoschreiben zu drucken.
9. Mahnschreiben buchen.

    1. Wählen Sie **Buchen** aus.
    1. Geben Sie ein Buchungsdatum für die Mahnung ein.
    1. Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
    1. Wählen Sie **OK**.
    1. Wählen Sie im Feld **Status** die Option **Gebucht** aus.
    1. Wählen Sie im Feld **Gedruckt** eine Option aus.

## <a name="control-collection-letters-at-the-customer-level"></a>Steuermahnschreiben auf Debitorenebene
Wenn Abholbriefe auf Transaktionsebene eingerichtet werden, werden möglicherweise mehrere Briefe für einen Kunden generiert, basierend auf der Fälligkeit der Transaktionen. Wenn Transaktionen in unterschiedlichen Buchstabenfolgen angezeigt werden, werden für jede Gruppe überfälliger Transaktionen für den Kunden separate Inkassobriefe generiert. Daher kann ein einzelner Kunde beispielsweise einen Inkassobrief für Transaktionen erhalten, die 60 Tage überfällig sind, und einen weiteren Inkassobrief für Transaktionen, die 90 Tage überfällig sind. 

Jeder Sammelbrief ist auch einem Sammelbriefcode zugeordnet. Der Abholbriefcode ist einzelnen Transaktionen zugeordnet und wird verwendet, um zu bestimmen, wann der nächste Abholbrief für jede Transaktion generiert werden soll. Wenn eine Transaktion beispielsweise mehr als 30 Tage überfällig ist, bestimmt der Abholbriefcode, dass der nächste Abholbrief gesendet wird, wenn die Transaktion 60 Tage überfällig ist, wenn sie nicht vorher bezahlt wurde. 

Abholbriefe können auch auf Kundenebene eingerichtet werden. In diesem Fall wird der Mahnschreibencode für jede Buchung erfasst ist, aber das Mahnschreibenverarbeiten basiert auf einer einzelne Mahnschreibenebene, die für den Debitor gespeichert wird. Das jeweilige Mahnschreiben enthält sämtliche Buchungen, die für den Debitor überfällig sind. Da die Schontage nun auf der Debitorenebene nachverfolgt werden, wird das nächste Mahnschreiben nicht übermittelt, bis die Anzahl der Schontagen für das nächste Mahnschreiben im Nummernkreis abgelaufen ist, obwohl Buchungen überfällig werden, nachdem das letzte Mahnschreiben gesendet wurde. Diese Option hilft, die Anzahl der Mahnschreiben zu reduzieren, die Sie pro Debitor übermitteln müssen.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Kunden einrichten, um Steuermahnschreiben auf Debitorenebene zu steuern
1.  Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Einrichtung > Debitorenparameter** und wählen Sie die Registerkarte **Inkasso**. 
2.  Ändern Sie den Wert von **Erstellen Sie Mahnschreiben pro** zu **Debitor**. 
3.  Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Inkassoschreiben > Review und Bearbeitung von Inkassoschreiben**. Es wird ein Mahnschreiben für einen Debitor mit allen überfälligen Buchungen generiert.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren
Wenn Sie Zahlungen und Gutschriften in den Buchungen erfassen, die im Mahnschreiben integriert werden, haben Sie möglicherweise Zahlungen oder Gutschriften, für die ein Mahnschreiben gestartet wird. Sie können auch steuern, wie Zahlungen und Gutschriften den Mahnschreibencode steuern, indem Sie den Wert des Parameters **Ignorieren Sie Zahlungen und Gutschriften, wenn Sie den Mahnschreibencode berechnen** ändern. 

Um Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes zu ignorieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Einrichtung > Debitorenparameter** und klicken Sie auf die Registerkarte **Inkasso**. 
2. Ändern Sie den Wert von **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** ab.
