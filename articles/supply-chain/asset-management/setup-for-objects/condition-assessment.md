---
title: Bedingungsbewertung
description: In diesem Thema wird erläutert, wie Sie eine Bedingungsbewertungsvorlage und -erfassung für eine Anlage in der Anlagenverwaltung erstellen.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5294325f67f0484b39194b5bd9784a2e612001a4
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783284"
---
# <a name="condition-assessment"></a>Bedingungsbewertung

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie eine Bedingungsbewertungsvorlage und -erfassung für eine Anlage in der Anlagenverwaltung erstellen. Eine Bedingungsbewertung wird in regelmäßigen Intervallen durchgeführt. Das vorrangige Ziel einer solchen Bewertung ist, Zustandsdaten für Anlagen zu erstellen und zu verwalten. Gesehen aus einer Perspektive der vorbeugenden Wartung ist es wichtig, zentrale Informationen zu überwachen, wie z. B. den aktuellen Zustand und die verbleibende Nutzungsdauer. Wenn Sie außerdem eine Bedingungsbewertung in regelmäßigen Intervallen ausführen, sind Sie in der Lage, die Bedingungen des Maschinenparks in Ihrer Fabrik zu überwachen und zu vergleichen.

Die Bedingungsbewertung kann verwendet werden, um mehrere Bedingungen Ihrer Ausrüstung zu messen und zu überwachen. Beispiel: Sie können Erschütterungen auf Maschinen messen. Nachdem Sie Erschütterungsmessungen in der Anlagenverwaltung für verschiedene Arten von Ausrüstung erfasst haben, können Sie nach den aktuellen Bewertungen suchen und die Erschütterungsmessungen anzeigen.

Die Bedingungsbewertung wird für Anlagen erstellt. Sie richten eine Bedingungsbewertungsvorlage für einen Anlagentyp ein, bevor Sie die Bedingungsbewertung durchführen. Der Grund für die Verwendung von Vorlagen für die Bedingungsbewertung ist, Abweichungen bei den Bedingungsdaten auf ähnlichen Anlagen zu vermeiden. Die Reihenfolge für das Einrichten und Verwenden der Bedingungsbewertung in der Anlagenverwaltung ist folgende: Zuerst richten Sie die erforderlichen Bedingungsbewertungsvorlagen ein. Dann ordnen Sie Vorlagen den Anlagentypen im Formular **Anlagentypen** zu. Schließlich können Sie Bedingungsbewertungserfassungen für eine Anlage im Formular **Anlagen** erstellen.

## <a name="create-a-condition-assessment-template"></a>Bedingungsbewertungsvorlage erstellen

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Anlagentypen** > **Bedingungsbewertung** aus.
2. Wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
3. Geben Sie eine ID für die Vorlage im Feld **Vorlage** ein.
4. Geben Sie im Feld **Name** einen Namen für die Vorlage ein.
5. Fügen Sie auf dem Inforegister **Bedingungsbewertungspositionen** die für die Bedingungsbewertung benötigten Positionen hinzu. Hierbei wählen Sie auch den relevanten Bedingungstyp und die Maßeinheit aus.
6. Fügen Sie auf dem Inforegister **Anlagentypen** die Anlagentypen hinzu, die die Bedingungsbewertungsvorlage verwenden sollen.
7. In den Feldern **Positionen** und **Anlagentypen** in der Gruppe **Details** am oberen Rand des Bildschirms sehen Sie die Anzahl der Bewertungspositionen und Anlagentypen zur ausgewählten Bedingungsbewertungsvorlage.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Bedingungsbewertungserfassung für eine Anlage erstellen

1. Wählen Sie **Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen**.
2. Wählen Sie in der Liste eine Anlage aus, für die Sie eine Bedingungsbewertungserfassung erstellen möchten.
3. Klicken Sie auf der Registerkarte **Allgemein** auf **Bedingungsbewertung**.
4. Klicken Sie auf **Neu**, um eine neue Erfassung zu tätigen.
5. Wählen Sie das Datum für die Bedingungsbewertung im Feld **Datum** aus.
6. Wählen Sie im Feld **Arbeitskraft** den Namen der Arbeitskraft aus, die die Bewertungserfassung durchgeführt hat.
7. Im Feld **Positionen** sehen Sie die Anzahl der Bewertungspositionen, die in der Bedingungsbewertung eingerichtet sind.
8. Wählen eine Vorlage für die Bedingungsbewertung im Feld **Vorlage** aus. Der Name der Vorlage wird automatisch im Feld **Name** eingefügt, und die zugehörigen Erfassungspositionen werden auf dem Inforegister **Bedingungsbewertungspositionen** eingefügt.
9. Sie können Notizen in Bezug auf die ausgewählte Bedingungsbewertung auf dem Inforegister **Hinweise** einfügen.
10. Geben Sie für jede Bedingungsbewertungsposition Messungsdaten im Feld **Wert** ein.
11. Sie können einen Kommentar zur ausgewählten Erfassungsposition auf dem Inforegister **Bedingungsbewertungspositionen** im Feld **Kommentare** eingeben. Wenn Sie einen Kommentar für eine Position hinzufügen, wird das Kontrollkästchen **Kommentar** automatisch aktiviert.

Nachdem Sie eine Bedingungsbewertungserfassung für eine Anlage vorgenommen haben, können Sie einen Bedingungsbewertungsbericht drucken.

>[!NOTE]
>Sie können Bedingungsbewertungen auch in einem Arbeitsauftrag erfassen (**Anlagenverwaltung** > **Allgemeines** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** > **Bedingungsbewertung**).
