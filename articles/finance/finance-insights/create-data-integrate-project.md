---
title: Erstellen Sie ein Datenintegratorprojekt (Vorschau)
description: In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009443"
---
# <a name="create-a-data-integrator-project-preview"></a>Erstellen Sie ein Datenintegratorprojekt (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie ein Datenintegratorprojekt erstellen.

1. Melden Sie sich bei Microsoft Dynamics 365 Finance an.
2. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung** und wählen Sie **Datenentitäten**. Warten Sie, bis alle Datenentitäten aktualisiert wurden, bevor Sie mit dem nächsten Schritt fortfahren.
3. Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com/) und befolgen Sie diese Schritte:

    1. Wählen Sie die entsprechende Umgebung aus.
    2. Wählen Sie im linken Navigationsbereich **Daten \> Verbindungen** aus.
    3. Stellen Sie eine Verbindung zu geeigneten Instanzen der folgenden Elemente her:

        - Dynamics 365
        - Dynamics 365 for Finance and Operations

4. Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:

    1. Wählen Sie **Datenintegrator**.
    2. Wählen Sie **Verbindungssätze**.
    3. Wählen Sie **Neuer Verbindungssatz**.
    4. Geben Sie einen Namens für die Verbindung ein.
    5. Wählen Sie die entsprechenden Verbindungen für die folgenden Elemente aus:

        - Dynamics 365
        - Dynamics 365 for Finance and Operations

    6. Wählen Sie die entsprechende Organisationszuordnung aus.
    7. Wählen Sie **Erstellen** aus.

5. Öffnen Sie die [Power Apps-Umgebungen](https://admin.powerapps.com/environments) und befolgen Sie diese Schritte:  

    1. Erstellen Sie Datenintegrationsprojekte für die folgenden Vorlagen mit dem soeben erstellten Verbindungssatz:

        - Ergebnisse der Debitorenzahlungserkenntnisse (CDS an Finance and Operations)
        - Ergebnisse der Cashflow-Zeitreihen (CDS an Finance and Operations)
        - Ergebnisse der Budget-Zeitreihen (CDS an Finance and Operations)

    2. Legen Sie für jedes Projekt die entsprechende Zeitplanung fest.

> [!NOTE]
> Wenn Sie die erforderlichen Entitäten in CDS nicht sehen, gehen Sie bitte zu **Guthaben und Inkasso > Einrichtung > Finance Insights > Parameter für Finance Insights**, aktivieren Sie die Funktion „Debitorenzahlungsvorhersagen“ und klicken Sie auf die Schaltfläche **Vorhersagemodell erstellen**. Wenn die Bereitstellung des KI-Modells abgeschlossen ist (erfolgreich oder fehlgeschlagen), werden die zum Erstellen der Integration erforderlichen CDS-Entitäten in CDS bereitgestellt.

## <a name="privacy-notice"></a>Datenschutzhinweis

Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]