---
title: Prozesszinsen
description: Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916275"
---
# <a name="process-interest"></a>Prozesszinsen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-interest-on-the-posting-profile"></a>Zinsen für das Buchungsprofil einrichten
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Einzüge > Einrichtung > Kundenbuchungsprofile**.
2. Klicken Sie auf **Bearbeiten**.
3. Wählen Sie im Feld **Einrichtung-FastTab**, im Feld **Zinscode**, einen Zinscode aus der Dropdown-Liste aus. Wenn Sie nicht möchten, dass Zinsen für Transaktionen mithilfe dieses Buchungsprofils berechnet werden, lassen Sie das Feld leer. Die **Tabellenbeschränkung** fastTab ermöglicht es Ihnen, die Art und Weise, wie Zinsen verarbeitet werden, zu ändern. Wenn dieses Feld auf "Ja" festgelegt ist, werden Zinsen für dieses Buchungsprofil berechnet.  

## <a name="calculate-interest"></a>Zinsen berechnen
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Einzüge > Zinsen > Zinsen > Zinsnoten erstellen**.
2. Sie müssen die Transaktionstypen auswählen, für die Sie Zinsen berechnen. Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.  
3. Wenn Sie **Zinsen** auf'Ja' setzen, berechnen Sie die Zinsen. Sie sollten die Gesetze prüfen, die für die Berechnung von Zinsen auf Zinsen gelten, bevor Sie diese Transaktionen einbeziehen.  
4. Geben Sie im Feld **Ab Datum** ein Datum ein, ab dem die Zinsen berechnet werden sollen. Wenn Sie kein **Ab-Datum** angeben, werden alle nicht gebuchten Zinsnoten storniert und die Zinsen ab dem Transaktionsdatum neu berechnet.
5. Geben Sie im Feld **Bis Datum** ein Datum ein, bis zu dem die Zinsen berechnet werden sollen.
6. Wählen Sie im Feld **Buchungsprofil verwenden aus** eine Option aus. Es gibt drei Möglichkeiten des Buchungsprofils:
    - Konto – Dient zum Verwenden des Buchungsprofils, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist. 
    - Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.
    - Transaktion – Dient zum Verwenden des jeweiligen Buchungsprofils von Transaktionen, für die Zinsen für die einzelnen Zinsrechnungen berechnet werden. Für Transaktionen ohne zugewiesenes Buchungsprofil wird das Buchungsprofil verwendet, das im Bereich "Sachkonto und Mehrwertsteuer" des Formulars "Debitorenparameter" angegeben ist.  
7. Erweitern Sie die **Datensätze um** fastTab.
8. Klicken Sie auf **Filter**.
9. Geben Sie im Feld **Kriterien** eine "Debitorenkennung" ein. Geben Sie beispielsweise "US-001" ein.
6. Klicken Sie auf **OK**.
7. Klicken Sie auf **OK**.

## <a name="print-interest-notes"></a>Zinsrechnungen drucken
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Sammlungen > Zinsen > Zinsen > Zinsnotizen überprüfen und bearbeiten**.
2. Wählen Sie im Feld **Status** die Option 'Erstellt'.
3. Wählen Sie im Feld **Drucken** die Option 'Nicht gedruckt'.
4. Klicken Sie auf **Drucken**.
5. Erweitern Sie die **Datensätze um** fastTab.
6. Klicken Sie auf **OK**.
7. Schließen Sie die Seite.

## <a name="post-the-interest-note"></a>Die Zinsrechnung buchen
1. Wählen Sie eine Zinsrechnung aus, die zum Buchen bereit ist (Status wird erstellt).
2. Klicken Sie auf **Buchen**.
3. Geben Sie das Buchungsdatum für die Zinsrechnung ein. Wählen Sie "Ja" aus, um eine Hauptbuchtransaktion für jede Zinsrechnung zu erstellen. Wenn Sie nicht "Ja" auswählen, werden die Zinsen für alle Zinsrechnungen für den Debitor kumuliert und in einer einzigen Transaktion im Hauptbuch gebucht.  
4. Erweitern Sie die **Datensätze um** fastTab.
5. Klicken Sie auf **OK**.
6. Wählen Sie im Feld **Status** die Option 'Gebucht'.

