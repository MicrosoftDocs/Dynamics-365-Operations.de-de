---
title: Planzahlenmodelle für Projektbudgets erstellen
description: In diesem Thema wird beschrieben, wie ein Planzahlenmodell für verbleibende Budgets erstellt wird.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321778"
---
# <a name="create-forecast-models-for-project-budgets"></a>Planzahlenmodelle für Projektbudgets erstellen 

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Planzahlenmodell für verbleibende Budgets erstellt wird. Für Projekte, die der Budgetsteuerung unterliegen, werden zwei Arten von Budgets verwendet: ursprünglich und verbleibend. Beim Erstellen eines Projektbudgets müssen Sie die Planzahlenmodelle für das ursprüngliche Budget und das Restbudget angeben, die auf der Seite **Prognosemodelle** erstellt wurden. Projektbudgets basierend auf den angegebenen Modellen werden erstellt, wenn Sie das Projektbudget bestimmen.

> [!NOTE]
> Ein Planzahlenmodell, das für die Budgetsteuerung verwendet wird, kann kein Teilmodell enthalten oder kann nicht als Teilmodell verwendet werden.

1. Wählen Sie **Projektmanagement und Buchhaltung** > **Setup** > **Prognosen**  > **Planzahlenmodelle** aus.
2. Wählen Sie **Neu** aus, um ein neues Planzahlenmodell zu erstellen, und geben Sie dann die Modellkennungsnummer und einen Namen für das neue Modell ein. 
3. Legen Sie die Option **Beendet** auf **Ja** fest, um Änderungen an den Prognosepositionen für das Planzahlenmodell zu verhindern. 
4. Wenn die Prognosepositionen, denen das Modell zugeordnet ist, Cashflow-Prognosen im Hauptbuch erstellen sollen, legen Sie **In Cashflow-Prognosen einbeziehen** auf **Ja** fest. 
5. Um das Projektdatum als Rechnungsdatum zu verwenden, legen Sie **Prognose-Rechnungsdatum** auf **Ja** fest. 
6. Wählen Sie im Feld **Budgettyp** einen der folgenden Modelltypen aus:

   - **Ursprüngliches Budget**: Verwenden Sie die ursprünglichen Budgetbeträge, die zugesagt wurden, als das anfängliche Budget erstellt und genehmigt wurde.
   - **Restbudget**: Verwenden Sie die verbleibenden Budgetbeträge während des Verlaufs des Projekts. Die Salden im Planzahlenmodell werden durch die tatsächlichen Buchungen reduziert und durch Budgetüberarbeitungen erhöht oder verringert.
   - **Vortrag**: Verwenden Sie die Vortragsbudget-Beträge für das Projekt. Ein Vortrag ist ein optionaler Prozess, mit dem nicht verbrauchte Budgetbeträge auf ein anderes Geschäftsjahr übertragen werden können.

7. Legen Sie die folgenden Optionen nach Bedarf fest:

   - Aktivieren Sie **Prognose-Rechnungsdatum**, um das Projektdatum als Rechnungsdatum zu verwenden.
   - Aktivieren Sie **Prognose mit RIF**, um eine Prognose anhand der laufenden Arbeit (RIF) zu treffen, und wählen Sie dann den RIF-Typ aus. 
   - Sie können den standardmäßigen **Budgettyp** als **Keiner** beibehalten oder einen neuen Typ eingeben. Der Budgettyp kann nicht geändert werden, nachdem Sie einen Datensatz geändert haben.     
    > [!NOTE]
    > Wenn Sie den Standardbudgettyp ändern, stehen alle anderen Optionen nicht mehr für Updates zur Verfügung, und Sie können dieses Planzahlenmodell nicht wiederverwenden. 
   


 

