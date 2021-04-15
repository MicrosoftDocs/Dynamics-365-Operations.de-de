---
title: Integrieren von Dynamics 365 Supply Chain Management (Anlagenverwaltung) in Dynamics 365 Guides
description: In diesem Thema wird erläutert, wie Sie das Anlagenverwaltungsmodul in Microsoft Dynamics 365 Supply Chain Management in Dynamics 365 Guides integrieren, um die Mixed-Reality-Anleitungen in Ihren täglichen Service- und Wartungsworkflows zu nutzen.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 4af14a66c839ccee02008057ad1de8ef5b9d291b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813916"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Integrieren von Dynamics 365 Supply Chain Management (Anlagenverwaltung) in Dynamics 365 Guides

Sie können das Modul **Anlageverwaltung** in Microsoft Dynamics 365 Supply Chain Management in Dynamics 365 Guides integrieren, um die Mixed-Reality-Anleitungen in Ihren täglichen Service- und Wartungsworkflows zu nutzen. Wenn eine Anleitung einem Anlagenverwaltungs-Arbeitsauftrag zugeordnet ist, sieht ein Mitarbeiter, der die Wartungsprüfliste des Arbeitsauftrags in der mobilen Supply Chain Management (Dynamics 365)-App öffnet, dass eine Anleitung verfügbar ist. Die Arbeitskraft kann dann die Anleitung in der Dynamics 365 Guides HoloLens-App finden und öffnen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie Anleitungen an Anlagenverwaltungs-Arbeitsaufträge anhängen können, müssen Sie die folgenden Voraussetzungen erfüllen:

- [Einrichten von Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) Version 10.0.9 oder höher.
- [Aktivieren Sie duales Schreiben für Supply Chain Management-Apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Schalten Sie Flight ein](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) für die Funktion **MRGuidesFeature**. (Für Produktionsumgebungen müssen Sie zuerst ein Support-Ticket übermitteln, damit Ihr Mandant zur Flighting-Gruppe hinzugefügt wird.)
- [Aktivieren Sie die folgenden Konfigurationsschlüssel](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) auf der Seite **Lizenzkonfiguration**:

    - Anlagenverwaltung \> Anlagenverwaltung – Mixed Reality
    - Mixed Reality \> Mixed Reality-Anleitung

- [Einrichten von Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) Version 200.0.0.96 oder höher.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Verwenden von Dynamics 365 Guides mit Anlagenverwaltung

Um eine Anleitung zuzuordnen, verwenden Sie eine Wartungsprüflistenposition in der Anlagenverwaltung. Sie können die Zuordnung über eine Wartungsprüflistenvorlage, einen Wartungsauftragstyp oder einen Arbeitsauftrag erstellen, da alle drei Wartungsprüflistenpositionen enthalten. Sie können Zeit sparen, indem Sie eine Vorlage verwenden, da eine Vorlage allen Wartungsauftragstypen zugeordnet werden kann, die sie verwenden. Beispielsweise wird eine Anleitung, die einem Wartungsauftragstyp zugeordnet ist, automatisch allen Arbeitsaufträgen zugeordnet, die diesen Auftragstyp angeben. Andererseits existiert eine Anleitung, die direkt einem Arbeitsauftrag zugeordnet ist, nur für diesen Arbeitsauftrag.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Eine Anleitung einer Wartungsprüflistenvorlage zuordnen

Um eine Anleitung einer Wartungsprüflistenvorlage zuzuordnen, folgen Sie diesen Schritten.

1. Erstellen Sie eine Anleitung mit dem Dynamics 365 Guides-PC und HoloLens-Apps. Informationen darüber, wie eine Anleitung erstellt wird, finden Sie in den folgenden Themen:

    - [Verwenden der PC-App, um eine Anleitung zu erstellen](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Verwenden der HoloLens-App, um Ihre Hologramme zu platzieren](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. In Supply Chain Management [erstellen Sie eine Wartungsprüflistenvorlage](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Ordnen Sie die Anleitung zu, die Sie mit einer Wartungsprüflistenposition in der neuen Wartungsprüflistenvorlage erstellt haben:

    1. Im Inforegister **Wartungsprüflistenpositionen** wählen Sie die Position aus, der Sie die Anleitung zuordnen möchten.
    1. Wählen Sie im Inforegister **Zugeordnete Anleitungen** die Option **Anleitung hinzufügen** aus.

        ![Eine Anleitung einer Wartungsprüflistenposition zuordnen](media/am-guides-integration-add-guide.png "Eine Anleitung einer Wartungsprüflistenposition zuordnen")

    1. Wählen Sie im Feld **Name** eine Anleitung aus, und wählen Sie dann **Speichern** aus.

        ![Eine Anleitung im Feld „Name“ auswählen](media/am-guides-integration-select-guide.png "Eine Anleitung im Feld „Name“ auswählen")

1. Ordnen Sie die Wartungsprüflistenvorlage einem Auftragstyp zu:

    1. [Erstellen Sie einen Wartungsauftragstyp](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), oder wählen Sie einen vorhandenen Wartungsauftragstyp aus.
    1. Wählen Sie im Aktionsbereich **Standardeinstellungen für den Wartungsauftragstyp** aus.

        ![Schaltfläche für Wartungsauftragstyp-Standardwerte](media/am-guides-integration-job-defaults.png "Schaltfläche für Wartungsauftragstyp-Standardwerte")

    1. Erstellen Sie eine Position, und wählen Sie dann **Speichern** aus.

        ![Eine Position erstellen](media/am-guides-integration-add-line.png "Eine Position erstellen")

    1. Wählen Sie im Aktionsbereich **Wartungsprüfliste** aus.

        ![Schaltfläche „Wartungsprüfliste“](media/am-guides-integration-maintenance-checklist.png "Schaltfläche „Wartungsprüfliste“")

    1. In der Registerkarte **Wartungsprüflistenpositionen** fügen Sie eine Position hinzu, und ändern Sie dann den Wert des Felds **Typ** zu **Vorlage**.

        ![Den Wert „Typ“ ändern](media/am-guides-integration-checklist-lines.png "Den Wert „Typ“ ändern")

    1. In der Registerkarte **Positionsdetails** im Feld **Vorlage** wählen Sie die Vorlage aus, der Sie die Anleitung zugeordnet haben, und wählen Sie dann **Speichern** aus.

        ![Die Vorlage auswählen](media/am-guides-integration-checklist-line-details.png "Die Vorlage auswählen")

1. [Erstellen Sie einen Arbeitsauftrag](work-orders/manually-created-workorders.md#create-work-order), und wählen Sie dann den Wartungsauftragstyp aus, der die Wartungsprüflistenvorlage verwendet, der Sie die Anleitung zugeordnet haben. Die Anleitung wird automatisch dem Arbeitsauftrag zugeordnet.

    ![Einen Wartungsauftragstyp auswählen](media/am-guides-integration-create-work-order.png "Einen Wartungsauftragstyp auswählen")

1. Zeigen Sie die Anleitung an, die dem Arbeitsauftrag und den Arbeitskräften zugeordnet ist:

    1. Öffnen Sie den [mobilen Arbeitsbereich „Anlagenverwaltung“](asset-management-mobile-workspace.md), um auf den Arbeitsauftrag zuzugreifen.
    1. [Öffnen Sie die Wartungsprüfliste](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) für den Arbeitsauftrag.
    1. Wählen Sie eine Prüflistenposition aus, um die zugeordnete Anleitung anzuzeigen.

        ![Einer Prüflistenposition zugeordnete Anleitung](media/am-guides-integration-show-guide.png "Einer Prüflistenposition zugeordnete Anleitung")

    1. Öffnen Sie die Anleitung in HoloLens.

        ![Öffnen Sie die Anleitung in HoloLens](media/am-guides-integration-hololens-select.png "Die Anleitung in HoloLens öffnen")

> [!NOTE]
> Sie können einen Leitfaden auch direkt in der Wartungsprüfliste eines Arbeitsauftrags oder eines Auftragstyps zuordnen.

> [!IMPORTANT]
> Es gibt ein bekanntes Problem, bei dem, wenn Sie eine Wartungsprüflistenvorlage einem Standard-Wartungsauftragstyp zuordnen, die Anleitung, die mit der Vorlage verknüpft ist, nicht im Inforegister **Zugeordnete Anleitungen** der Seite **Wartungsauftragstyp-Standardwerte** angezeigt wird. Die Anleitung wird jedoch angezeigt, nachdem dieser Auftragstyp auf einen Arbeitsauftrag im Inforegister **Zugehörige Anleitungen** angewendet ist.

## <a name="see-also"></a>Siehe auch

- [Duales Schreiben – Übersicht](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Überblick über die Anlagenverwaltung](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]