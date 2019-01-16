--- 
title: Mahnschreiben verarbeiten
description: Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: 33d9fd62a780ab109474eefa9e322a9c529f9e72
ms.contentlocale: de-de
ms.lasthandoff: 12/06/2018

---
# <a name="process-collection-letters"></a>Mahnschreiben verarbeiten

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Richten Sie eine Mahnschreibensequenz zum Buchungsprofil ein.
1. **Wechseln Sie zu "Kredit und Inkasso > Einstellungen > Debitorenbuchungsprofile**.
2. Klicken Sie auf **Bearbeiten**.
3. Wählen Sie eine Mahnschreibensequenz aus der Dropdownliste aus. Wenn Sie kein Mahnschreiben für Buchungen dieses Buchungsprofils erstellen wollen, lassen Sie das Feld leer.  
4. Das Erweitern der Tabelleneinschränkungsregisterkarte ermöglicht Ihnen das Verfahren, mit dem Mahnschreiben verarbeitet werden, zu ändern. Wenn dieses Feld auf **Ja** festgelegt ist, werden Mahnschreiben für dieses Buchungsprofil erstellt.  

## <a name="create-collection-letters"></a>Mahnschreiben erstellen
1. Wechseln Sie zu **Kredit und Inkasso > Mahnschreiben > Erstellen von Mahnschreiben**.
2. Sie müssen die Buchungsarten auswählen, die Sie anmahnen wollen. Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.  
2. Wählen Sie im Feld **Mahnschreiben** eine Mahnschreibenoption aus.
3. Geben Sie das Datum des letzten Mahnschreibens an.
4. Wählen Sie ein Buchungsprofil aus, wenn Sie **Verwenden des Buchungsprofils aus** in **Auswählen** geändert haben. Es gibt zwei Arten von Buchungsoptionen:   
   - **Konto** – Dient zum Verwenden des Buchungsprofils, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.   
   - **Auswählen** – Dient zum Verwenden des im Feld **Buchungsprofil** ausgewählten Buchungsprofils.  
5. Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
6. Klicken Sie auf **Filter**.
7. Geben Sie im Feld **Kriterien** eine "Debitorenkennung" ein. Geben Sie beispielsweise "US-001" ein.
8. Klicken Sie auf **OK**.
9. Klicken Sie auf **OK**.

## <a name="print-collection-letters"></a>Mahnschreiben drucken
1. Wechseln Sie zu **Kredit und Inkasso > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten**.
2. Wählen Sie im Feld **Status** die Option **Erstellt** aus.
3. Wählen Sie im Feld **Gedruckt** die Option **Nicht gedruckt** aus.
4. Klicken Sie auf **Drucken**.
5. Klicken Sie **Mahnung**.
6. Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
7. Geben Sie das Abschnittsdatum für Buchungen ein.
8. Klicken Sie **OK**, um das Mahnschreiben zu drucken.
9. Mahnschreiben buchen.
   1. Klicken Sie auf **Buchen**.
   2. Geben Sie ein Buchungsdatum für die Mahnung ein.
   3. Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
   4. Klicken Sie auf **OK**.
   5. Wählen Sie im Feld **Status** die Option **Gebucht** aus.
   6. Wählen Sie im Feld **Gedruckt** eine Option aus.

## <a name="control-collection-letters-at-the-customer-level"></a>Steuermahnschreiben auf Debitorenebene
Sie können Mahnschreiben auf Debitorenebene auch einrichten, sodass der Mahnschreibencode für jede Buchung erfasst ist, aber das Mahnschreibenverarbeiten basiert auf einer einzelne Mahnschreibenebene, die für den Debitor gespeichert wird. Das jeweilige Mahnschreiben enthält alle Buchungen, die für den Debitor überfällig sind. Da die Schontage nun auf Debitorenebene nachverfolgt werden, wird das nächste Mahnschreiben nicht übermittelt, bis die Anzahl der Schontagen für das nächste Mahnschreiben im Nummernkreis abgelaufen ist, obwohl Buchungen überfällig werden, nachdem das letzte Mahnschreiben gesendet wurde. Diese Option verringert die Nummer des Mahnschreibens, die Sie pro Debitor übermitteln. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Kunden einrichten, um Steuermahnschreiben auf Debitorenebene zu steuern
1.  Gehen Sie zu **Kredit und Inkasso > einrichten > Debitorenparameter** und klicken Sie auf die Registerkarte **Inkassi**. 
2.  Ändern Sie den Wert von **Erstellen Sie Mahnschreiben pro** zu **Debitor**. 
3.  Wechseln Sie zu **Kredit und Inkasso > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten**. Es wird ein Mahnschreiben für einen Debitor mit allen überfälligen Buchungen generiert.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren
Wenn Sie Zahlungen und Gutschriften in den Buchungen erfassen, die im Mahnschreiben integriert werden, haben Sie möglicherweise Zahlungen oder Gutschriften, für die ein Mahnschreiben gestartet wird. Sie können auch steuern, wie Zahlungen und Gutschriften den Mahnschreibencode steuern, indem Sie den Wert des Parameters **Ignorieren Sie Zahlungen und Gutschriften, wenn Sie den Mahnschreibencode berechnen** ändern. 

Um Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes zu ignorieren, gehen Sie wie folgt vor.
1. Gehen Sie zu **Kredit und Inkasso > einrichten > Debitorenparameter** und klicken Sie auf die Registerkarte **Inkassi**. 
2. Ändern Sie den Wert von **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** ab.

