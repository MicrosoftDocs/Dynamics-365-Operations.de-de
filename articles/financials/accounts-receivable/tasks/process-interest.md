---
title: Prozesszinsen
description: Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "359151"
---
# <a name="process-interest"></a>Prozesszinsen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-interest-on-the-posting-profile"></a>Zinsen für das Buchungsprofil einrichten
1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenbuchungsprofile".
2. Klicken Sie auf "Bearbeiten".
    * Wählen Sie einen Zinscode aus der Dropdownliste aus. Wenn Sie nicht möchten, dass Zinsen für Transaktionen mithilfe dieses Buchungsprofils berechnet werden, lassen Sie das Feld leer.  
    * Die Registerkarte "Tabelleneinschränkung" ermöglicht Ihnen, das Verfahren zu ändern, mit dem Zinsen verarbeitet werden. Wenn dieses Feld auf "Ja" festgelegt ist, werden Zinsen für dieses Buchungsprofil berechnet.  

## <a name="calculate-interest"></a>Zinsen berechnen
1. Wechseln Sie zu "Kredit und Inkasso" > "Zinsen" > "Zinsrechnungen erstellen".
    * Sie müssen die Transaktionstypen auswählen, für die Sie Zinsen berechnen. Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.  
    * Wenn Sie Zinsen auswählen, berechnen Sie die Zinsen auf die Zinsen. Sie sollten die Gesetze prüfen, die für die Berechnung von Zinsen auf Zinsen gelten, bevor Sie diese Transaktionen einbeziehen.  
    * Zinsen werden ab diesem Datum bis zu "Bis Datum" berechnet. Wenn Sie kein "Von Datum" angeben, dann werden alle nicht gebuchten Zinsrechnungen storniert und Zinsen werden ab dem Transaktionsdatum neu berechnet.  
2. Geben Sie das Datum der Zinsrechnung ein.
    * Es gibt drei Buchungsprofiloptionen: Konto - Verwenden Sie das Buchungsprofil, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.   Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.   Transaktion – Dient zum Verwenden des jeweiligen Buchungsprofils von Transaktionen, für die Zinsen für die einzelnen Zinsrechnungen berechnet werden. Für Transaktionen ohne zugewiesenes Buchungsprofil wird das Buchungsprofil verwendet, das im Bereich "Sachkonto und Mehrwertsteuer" des Formulars "Debitorenparameter" angegeben ist.  
    * Wählen Sie hier ein Buchungsprofil aus, wenn Sie "Verwenden des Buchungsprofils aus" in" Auswählen" geändert haben.  
3. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
4. Klicken Sie auf "Filter".
5. Geben Sie im Feld "Kriterien" eine "Debitorenkennung" ein. Geben Sie beispielsweise "US-001" ein.
6. Klicken Sie auf "OK".
7. Klicken Sie auf "OK".

## <a name="print-interest-notes"></a>Zinsrechnungen drucken
1. Wechseln Sie zu "Kredit und Inkasso" > "Zinsen" > "Zinsrechnungen prüfen und verarbeiten".
2. Wählen Sie im Feld "Status" die Option "Erstellt" aus.
3. Wählen Sie im Feld "Gedruckt" die Option "Nicht gedruckt" aus.
4. Klicken Sie auf Drucken.
5. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
6. Klicken Sie auf "OK".
7. Schließen Sie die Seite.

## <a name="post-the-interest-note"></a>Die Zinsrechnung buchen
1. Wählen Sie eine Zinsrechnung aus, die zum Buchen bereit ist (Status wird erstellt).
2. Klicken Sie auf "Buchen".
3. Geben Sie das Buchungsdatum für die Zinsrechnung ein.
    * Wählen Sie "Ja" aus, um eine Hauptbuchtransaktion für jede Zinsrechnung zu erstellen.     Wenn Sie nicht "Ja" auswählen, werden die Zinsen für alle Zinsrechnungen für den Debitor kumuliert und in einer einzigen Transaktion im Hauptbuch gebucht.  
4. Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.
5. Klicken Sie auf "OK".
6. Wählen Sie im Feld "Status" die Option "Gebucht" aus.

