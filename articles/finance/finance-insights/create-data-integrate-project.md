---
title: Erstellen Sie ein Datenintegrationsprojekt
description: In diesem Thema wird erläutert, wie Sie ein Datenintegrationsprojekt erstellen.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4d69ffcb6ccfcc7bae2891f2539941f7b6bbf86e
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722882"
---
# <a name="create-a-data-integration-project"></a>Erstellen Sie ein Datenintegrationsprojekt

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie ein Datenintegrationsprojekt erstellen.

1. Melden Sie sich bei Microsoft Dynamics 365 Finance an.
2. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie **Datenentitäten**. Warten Sie, bis alle Datenentitäten aktualisiert wurden, bevor Sie mit dem nächsten Schritt fortfahren.
3. Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com/) und befolgen Sie diese Schritte:

    1. Wählen Sie die entsprechende Umgebung aus.
    2. Wählen Sie im linken Navigationsbereich **Dataverse \> Verbindungen** aus.
    3. Stellen Sie eine Verbindung zu geeigneten Instanzen der folgenden Elemente her:

        - Dynamics 365
        - Dynamics 365 for Finance and Operations

4. Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:

    1. Wählen Sie **Datenintegration**.
    2. Wählen Sie **Verbindungssätze**.
    3. Wählen Sie **Neuer Verbindungssatz**.
    4. Geben Sie einen Namens für die Verbindung ein.
    5. Wählen Sie die entsprechenden Verbindungen für die folgenden Elemente aus:

        - Dynamics 365
        - Dynamics 365 for Finance and Operations

    6. Wählen Sie die entsprechende Organisationszuordnung aus.
    7. Wählen Sie **Erstellen** aus.

5. Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:  

    1. Erstellen Sie ein einzelnes Datenintegrationsprojekt für jede der folgenden Vorlagen mit dem soeben erstellten Verbindungssatz:

        - Ergebnis der Debitorenzahlungserkenntnisse (CDS an Finance and Operations 10.0.17 oder höher)
        - Ergebnisse der Cashflow-Zeitreihen (CDS an Finance and Operations)
        - Ergebnisse der Budget-Zeitreihen (CDS an Finance and Operations)

      > [!NOTE]
      > Das Erstellen mehrerer Datenintegrationsprojekte für jede Vorlage kann Fehler verursachen, die die Aktualisierungen blockieren.

    2. Legen Sie für jedes Projekt die entsprechende Zeitplanung fest.

> [!NOTE]
> Wenn Sie die erforderlichen Entitäten in Dataverse sehen, gehen Sie bitte zu **Guthaben und Inkasso** > **Einrichtung** > **Finance Insights** > **Parameter für Finance Insights**, aktivieren Sie die Funktion **Debitorenzahlungsvorhersagen** und wählen Sie **Vorhersagemodell erstellen**. Wenn die Bereitstellung des KI-Modells abgeschlossen ist, werden die zum Erstellen der Integration erforderlichen Dataverse-Entitäten bereitgestellt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
