---
title: Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich
description: In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 457c547947ce6182d03e7a8276b380bc08535bca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985111"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können. Der CFO-Arbeitsbereich hat eine Registerkarte **Überblick** und eine **Finanzen** Registerkarte. Die Berichte zu diesen zwei Registerkarten werden mit zwei Kennzahlen unterstützt: LedgerActivityMeasure und BudgetActivityMeasure. Es gibt eine Beziehung zwischen diesen zwei Kennzahlen und der DimensionCombinationEntity-Entität. Andernfalls können Sie Dimensionen auswählen.

1. In Finance auf der Seite **Entitäts-Shop** aktualisieren Sie **LedgerActivityMeasure** und die Kennzahlen **BudgetActivityMeasure**.
2. Öffnen Sie in Microsoft Visual Studio den Anwendungs-Explorer und suchen Sie **LedgerCFO**.
3. Unter **Ressourcen** öffnen Sie **LedgerCFOWorkspacePBIX**.
4. Wenn die Ressource im Microsoft Power BI Desktop geöffnet wird, wählen Sie **Daten abrufen**, **SQL Server-Datenbank**, und dann **Verbinden** aus.
5. Geben Sie den Server mit der Berichtsdatenbank **AxDW** als Datenbank ein. Wählen Sie zunächst **Direct Query** und dann **OK** aus.
6. Suchen und wählen Sie **LedgerActivityMeasure \_DimensionCombination** aus und anschließend **Laden** aus.

    > [!TIP]
    > In der Liste **Felder** benennen Sie die Tabelle **Finanzdimensionen** um, sodass sie einfach zu u identifizieren ist.

7. Wählen Sie **Verwalten Sie Beziehungen** und **Neu** aus.
8. Wählen Sie im ersten Feld **Hauptbuch-Aktivitäten** und **LedgerDimension** aus.
9. Im zweiten Feld geben Sie **LedgerActivityMeasure\_DimensionCombination** (oder **Financial dimensions** wenn Sie die Tabelle umbenannt haben). Wählen Sie die Überschrift **DimensionCombinationRECID** aus.
10. Wählen Sie im Feld **Kardinalität** **Viele bis ein** aus.
11. Ändern Sie den Wert **Filterrichtung kreuzen** auf  **Einzeln**.
12. Wählen Sie **Führen Sie diese Beziehung aktiv** und **Nehmen Sie referenzielle Integrität an** aus, wählen Sie **OK** und **Schließen** aus.

    [![Eine Beziehung erstellen](./media/Create-relationship.png)](./media/Create-relationship.png)

13. In der Liste **Felder** können Sie die Tabelle sowie die verfügbaren Finanzdimensionen finden. Ziehen Sie die gewünschten Finanzdimensionen in die Berichtsebenenfilter.
14. Speichern Sie die Änderungen.
15. In der Entwicklungsumgebung (AOT), klicken Sie auf das Projekt mit der rechten Maustaste, und wählen Sie dann **Synchronisieren** aus.
16. Stellen Sie das Projekt zusammen und öffnen Sie dann die Anwendung, um die Ergebnisse anzeigen.

    [![Arbeitsabereich abgeschlossen](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]