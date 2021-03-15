---
title: Erstellen Sie ein Originalbudget und machen Sie dann vorläufige Budgeteinträge im öffentlichen Sektor rückgängig
description: Dieses Thema enthält Informationen zum Erstellen und Stornieren eines ursprünglichen Budgeteintrags mithilfe von Budgetmodellen und Dimensionswerten mit vorläufigen Budgetbeträgen.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987953"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>Erstellen Sie ein Originalbudget und machen Sie dann vorläufige Budgeteinträge im öffentlichen Sektor rückgängig

[!include [banner](../../includes/banner.md)]

Wenn Sie einen Budgeteintrag erstellen und die Budgetmodell- und Dimensionswerte verwenden, die vorläufige Budgetbeträge enthalten, dann werden die vorläufigen Budgetbeträge rückgängig gemacht. Diese Prozedur wurde unter Verwendung der PSUS-Vorführungsunternehmensdaten in der Partition "Öffentlicher Sektor" erstellt.

1. Wechseln Sie zu "Budgetierung" > "Budgetregistereinträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Budgetmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie im Feld "Budgetcode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf "Ursprüngliches Budget".
7. Klicken Sie auf Speichern.
8. Klicken Sie auf "Position hinzufügen".
9. Optional: Wenn Sie das Datum im Kopfbereich ändern möchten, geben Sie ein neues Datum. Dieses Datum bestimmt den Finanzzeitraum, für den das Budget erfasst wird.
10. Klicken Sie im Feld "Kontenstruktur" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Geben Sie im Feld "Dimensionswerte" die gewünschten Werte an.
13. Geben Sie im Feld "Betrag" eine Zahl ein.
14. Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Klicken Sie auf "Speichern".
17. Klicken Sie auf "Budgetsalden aktualisieren".
    * Optional: Sie können die Option "Vorläufiges Budget rückgängig machen" auswählen. Beachten Sie, dass Sie alle vorläufigen Budgeteinträge rückgängig machen können, oder nur die vorläufigen Budgeteinträge, die den Budgetcode haben, den Sie angeben.  
    * Um eine optionale Auswahl zu treffen, klicken Sie auf das Entsperren-Symbol am oberen Seitenrand.  
18. Klicken Sie auf Aktualisieren.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]