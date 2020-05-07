---
title: Erweiterte Verträge für Abrechnung nach Arbeitsstatus erstellen
description: In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Debitoren basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282827"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Erweiterte Verträge für Abrechnung nach Arbeitsstatus erstellen
[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie für Debitoren Rechnungen basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können. Rechnungsbeträge für die Arbeitsbudgetkategorien, die Sie für das Projekt eingerichtet haben, werden automatisch berechnet. Der Zeitpunkt für die Rechnung wird bei der Vertragsverhandlung mit dem Debitor festgelegt.

Richten Sie mithilfe der Prozeduren in diesem Thema einen Vertrag, ein zugehöriges Projekt und die Fakturierungsregeln ein, mit denen die Rechnungsbeträge für die eingerichteten Arbeitsbudgetkategorien des Projekts berechnet werden.

Nachdem Sie den Vertrag und das Projekt erstellt haben, können Sie die Details des Projekts einrichten. Sie können beispielsweise Aktivitäten definieren und dem Projekt Arbeitskräfte zuweisen.

## <a name="example"></a>Beispiel

Ihre Organisation ist eine Softwareentwicklungsfirma. Sie vereinbaren, für eine Gesamtgebühr von 20.000 Euro ein Lohnbuchhaltungspaket für einen Debitor zu entwickeln. Ihre Organisation sagt zu, dem Debitor eine Rechnung auszustellen, sobald bestimmte Prozentsätze des Projekts abgeschlossen sind. Sie richten die folgenden Projektkategorien für die Arbeit ein, damit Sie sie im Abrechnungsprozess verwenden können:

- Beratung
- Entwurf
- Installation

Sie richten außerdem Fakturierungsregeln ein, durch die die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit in jeder Kategorie automatisch berechnet werden.

Der Budget-Manager erstellt ein Budget für die Projektkategorien. Der Betrag der abgeschlossenen Arbeit wird automatisch als Prozentsatz der tatsächlichen Arbeit im Vergleich zu den budgetierten Beträgen berechnet.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Projekt erstellen, das Fakturierungsregeln verwendet, müssen Sie die Nummernkreise für Fakturierungsregeln sowie eine Gebührenerfassung einrichten, mit der Abrechnungen nach Arbeitsstatus gebucht werden.

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Einrichtung** \> **Projektverwaltungs- und Buchhaltungsparameter**.
2. Richten Sie auf der Seite **Projektverwaltungs- und Buchhaltungsparameter** auf der Registerkarte **Nummernkreise** den Nummernkreis ein, den Sie beim Erstellen von Fakturierungsregeln verwenden möchten.
3. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Erfassungen** \> **Gebühr**.
4. Wählen Sie auf der Seite **Gebührenerfassung** die Option **Neu** aus und geben Sie den Erfassungsnamen ein.

## <a name="create-a-contract-for-progress-billings"></a>Erstellen eines Vertrags für die Abrechnung nach Arbeitsstatus

Gehen Sie folgendermaßen vor, um einen Projektvertrag für ein Festpreisprojekt zu erstellen. Sie erstellen eine Projektrechnung, wenn die Arbeit, die für das Projekt abgeschlossen ist, einen angegebenen Prozentsatz erreicht.

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Projekte** \> **Projektverträge**.
2. Wählen Sie auf der Seite **Projektverträge** die Option **Neu** aus.
3. Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Felder fest:

    - **Name**
    - **Finanzierungstyp**
    - **Finanzierungsquelle**
    - **Verkaufswährung** – Standardmäßig wird diese Währung für Debitorenrechnungen verwendet, die dem Projektvertrag zugeordnet sind. Sie können die Verkaufswährung auf einer bestimmten Debitorenrechnung jedoch ändern.

4. Wählen Sie **OK**. Die Informationen werden in den Kopf der Seite **Projektverträge** kopiert.
5. Geben Sie auf der Seite **Projektverträge** den Rest der erforderlichen Informationen für das Projekt ein.

## <a name="create-a-project-for-progress-billings"></a>Erstellen eines Projekts für die Abrechnung nach Arbeitsstatus

Gehen Sie folgendermaßen vor, um ein Projekt und alle Unterprojekte zu erstellen, die einem Projektvertrag zugeordnet sind.

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projekte** \> **Alle Projekte**.
2. Wählen Sie auf der Seite **Alle Projekte** die Option **Neu** aus.
3. Wählen Sie im Dialogfeld **Neues Projekt** im Feld **Projekttyp** die Option **Nach Aufwand** aus.
4. Wählen Sie eine Projektgruppe aus. Eine Projektgruppe definiert die Buchungsinformationen für die Projekte, die der Gruppe zugewiesen sind.
5. Wählen Sie **Projekt erstellen** aus.
6. Legen Sie nach dem Erstellen des Projekts die Projektphase auf **In Bearbeitung** fest.

## <a name="create-a-budget-for-a-project"></a>Erstellen eines Budgets für ein Projekt

Budgetkategorien werden verwendet, um die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit für jede Kategorie automatisch zu berechnen. Gehen Sie folgendermaßen vor, um Budgetkategorien für die vorkalkulierten Kosten zu erstellen.

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projekte** \> **Alle Projekte**.
2. Wählen Sie auf der Seite **Alle Projekte** das gewünschte Projekt aus und öffnen Sie es.
3. Wählen Sie auf der Seite**Projekte** im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Budget** die Option **Projektbudget** aus.
4. Geben Sie auf der Seite **Projektbudget** vorkalkulierte Kosten für jede Kategorie im Projekt ein.

## <a name="create-billing-rules-for-progress-billings"></a>Erstellen der Fakturierungsregeln für die Abrechnung nach Arbeitsstatus

1. Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Projekte** \> **Projektverträge**.
2. Wählen Sie auf der Seite **Projektverträge** einen Projektvertrag aus und öffnen Sie ihn.
3. Wählen Sie auf der Seite des Projektvertrags im Inforegister **Frakturierungsregeln** die Option **Hinzufügen** aus.
4. Wählen Sie auf der Seite **Fakturierungsregel** im Feld **Positionstyp** die Option **Status** aus.
5. Geben Sie im Inforegister **Details der Fakturierungsregelpositionen** in das Feld **Vertragswert** den Gesamtwert des Vertrags ein.
6. Wählen Sie im Feld **Kategorie** die Kategorie aus, in die die Gebührenbuchung gebucht werden soll.
7. Wählen Sie im Feld **Projekt** das Projekt aus, für das diese Fakturierungsregel verwendet wird.
8. Optional: Weisen Sie die Fakturierungsregel zusätzlichen Projekten zu. Wählen Sie im Inforegister **Projekt** im Bereich **Verfügbare Projekte** ein Projekt aus und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts, um das Projekt zum Abschnitt **Ausgewählte Projekte** hinzuzufügen.
9. Optional: Berechnen Sie den Prozentsatzbetrag, den der Debitor für die Zahlungen für eine Rechnung einbehält. Wählen Sie im Inforegister **Bedingungen für Einbehaltung der Zahlung** die Finanzierungsquelle aus. Wählen Sie anschließend im Feld **Prozentsatz der Einbehaltung** den Einbehaltungsprozentsatz aus.
10. Wiederholen Sie diese Schritte, um weitere Fakturierungsregeln für den Projektvertrag zu erstellen.
