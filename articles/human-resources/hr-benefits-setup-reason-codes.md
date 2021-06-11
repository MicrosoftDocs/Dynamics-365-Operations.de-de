---
title: Ursachencodes einrichten
description: Dynamics 365 Human Resources erläutert anhand von Ursachencodes, warum sich die Vorteile eines Mitarbeiters ändern.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056347"
---
# <a name="set-up-reason-codes"></a>Ursachencodes einrichten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources erläutert anhand von Ursachencodes, warum sich die Vorteile eines Mitarbeiters ändern.

> [!NOTE]
> Ab Januar 2021 werden Ursachencodes zum **Personalverwaltung**-Arbeitsbereich statt zum **Vorteilsverwaltung**-Arbeitsbereich migriert. Weitere Informationen finden Sie unter [Ursachencodes manuell in die Personalverwaltung migrieren](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Erstellen von Ursachencodes

1. In dem **Personalverwaltung**-Arbeitsbereich (oder, wenn Ihre Ursachencodes noch nicht migriert wurden, im **Vorteilsverwaltung**-Arbeitsbereich) wählen Sie **Links** und dann **Ursachencodes** aus.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Ursachencode** | Ein eindeutiger Name, der den Grund angibt, aus dem ein Mitarbeiter die Registrierung eines Vergütungsplans ändern würde. |
   | **Beschreibung** | Eine Beschreibung des Ursachencodes. |

4. Legen Sie unter **Zutreffende Szenarios** die Option **Vorteilsverwaltung** auf **Ja** fest. (Gilt nicht, wenn Ihre Ursachencodes noch nicht auf den **Personalverwaltung**-Arbeitsbereich migriert wurden.)

5. Wählen Sie **Speichern** aus.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Ursachencodes manuell in die Personalverwaltung migrieren

Im Januar 2021 werden Ursachencodes zum **Personalverwaltung**-Arbeitsbereich statt zum **Vorteilsverwaltung**-Arbeitsbereich migriert. Die meisten Ursachencodedaten werden automatisch in Ihre Umgebung migriert. Einige Ursachencodedaten werden möglicherweise nicht migriert. Beispielsweise haben Ursachencodes jetzt ein Maximum von 15 Zeichen, sodass Ursachencodes, die länger als 15 Zeichen sind, nicht automatisch migriert werden.

Sie sehen ein Banner auf der **Links**-Seite des **Vorteilsverwaltung**-Arbeitsbereichs, das Sie über die Migration informiert und darüber, ob Ursachencodes nicht migriert wurden.

1. Wählen Sie **Ursachencodes** aus, um Einzelheiten zum Migrationsstatus zu erhalten.

   [![Ursachencodes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Wählen Sie einen Ursachencode aus, der nicht migriert werden konnte.

   [![Migrationsstatus des Ursachencodes](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Wählen Sie **Ursachencode migrieren**.

   [![Ursachencode für Migration](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. In dem **Migration von Vorteilsursachencodes**-Bereich haben Sie zwei Optionen für die Zuordnung zu einem Ursachencode der Personalverwaltung:

   - Um einen vorhandenen Ursachencode in der Personalverwaltung zu verwenden, wählen Sie einen aus der **Vorhandenen Ursachencode verwenden**-Dropdown-Liste.
     > [!NOTE]
     > Sie können nur dann einen vorhandenen Ursachencode in der Personalverwaltung verwenden, wenn noch kein anderer Ursachencode für die Vorteilsverwaltung dorthin migriert wurde.
   - Geben Sie einen neuen Ursachencode in **Neuer Ursachencode** ein, und geben Sie dann eine Beschreibung in ein **Neue Beschreibung** ein, um einen neuen Ursachencode in der Personalverwaltung zu erstellen.

   [![Zuordnung zu einem Ursachencode für die Personalverwaltung](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Nachdem Ursachencodes in die Personalverwaltung migriert wurden, wird die Option für deren Verwendung in der Vorteilsverwaltung automatisch auf **Ja** festgelegt.

[![Ursachencodes in der Vorteilsverwaltung verwenden](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]