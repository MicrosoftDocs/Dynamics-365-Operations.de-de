---
title: Einzelhandelskanäle definieren und verwalten
description: Dieses Thema bietet einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Dynamics 365 Commerce als Geschäfte bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Geschäft einrichten.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51524ad6918d962d70a8a700f135f96e236f7d34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000874"
---
# <a name="define-and-maintain-retail-channels"></a>Definieren und Verwalten von Retail-Kanälen

[!include [banner](includes/banner.md)]

Dieses Thema bietet einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Dynamics 365 Commerce als Geschäfte bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Geschäft einrichten.

Commerce unterstützt mehrere Einzelhandelskanäle wie Onlineshops, Callcenter und physische Shops. Ein physischer Laden wird Geschäft genannt. Jeder Shop kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten. Sie müssen alle Elemente für ein Geschäft einrichten, bevor Sie ihn erstellen. Nachdem Sie ein Geschäft erstellt haben, weisen Sie die Produkte zu, die der Shop umfassen soll. Sie ordnen außerdem Mitarbeiter, Register und Debitoren der Filiale zu. Fügen Sie den neuen Shop schließlich zu einer Organisationshierarchie hinzu.

## <a name="setting-up-stores"></a>Einrichten von Shops

Bevor Sie einen Einzelhandelsshop in Commerce einrichten können, müssen Sie mehrere erforderliche Aufgaben ausführen. Sie können dann das Geschäft erstellen und Details hinzufügen.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Geschäft einrichten können, müssen Sie die folgenden erforderlichen Aufgaben ausführen:

1. Konfigurieren Sie Ihre Organisationsstruktur und Einstellungsorganisationshierarchien für Einzelhandelssortimente, Auffüllung und Berichterstellung.
2. Einrichten eines Lagerorts, der das Geschäft abbildet.
3. Richten Sie Nummernkreise für Geschäfte, Lageraufstellungen und Auszugsbelege ein.
4. Parameter für Commerce konfigurieren.
5. Richten Sie die Zahlungsmethoden ein, die im Shop akzeptiert werden.
6. Für die Verarbeitung von Kreditkartentransaktionen an POS-Kassen können Sie auch Zahlungsdienste einrichten.
7. Mehrwertsteuergruppen einrichten.
8. Produkte einrichten. Als Teil dieser Aufgabe richten Sie auch Produkthierarchien, Produktvarianten und Sortimente ein.
9. Einrichten von Produktpreisgruppen.
10. Produktpreise einrichten. Als Teil dieser Aufgabe richten Sie auch Preisregulierungen, Rabatte und Rabattzeiträume ein.
11. Einrichten von Mitarbeitern.

    > [!NOTE]
    > Sie müssen die entsprechenden Berechtigungen den Arbeitskräften zuweisen, sodass diese sich anmelden und Aufgaben mit dem POS-System ausführen können.

12. Konfigurieren der POS-Profile, um sie dem Geschäft zuzuweisen. Diese Aufgabe beinhaltet zahlreiche weitere Aufgaben, wie das Einrichten von Registern, Einrichten von Offlineprofilen, und das Einrichten von Bonformaten und Profilen.

Prüfen Sie alle Aufgaben, die Voraussetzung sind, und führen Sie nur die Aufgaben aus, die für Sie gelten.

### <a name="set-up-a-store"></a>Ein Geschäft einrichten

Nach Abschluss der erforderlichen Aufgaben, führen Sie diese Aufgaben aus, um die Details für das Geschäft einzurichten:

1. Erstellen Sie einen Shop.
2. Eine Mehrwertsteuergruppe dem Shop zuweisen.
3. Die angenommenen Zahlungsmethoden dem Shop zuweisen.
4. Fügen Sie Details zu den Produktbeschreibungen für Produkte hinzu, die Sie in den Geschäften anbieten. Sie können beispielsweise Rich-Text und Bilder hinzufügen. Diese Produktdetails werden in verschiedenen Kontexten, wie auf der POS-Kasse oder auf gedruckten Beschriftungen angezeigt.
5. Fügen Sie den Shop zu einer Organisationshierarchie hinzu, die für ein **Sales-Sortiment**, eine **Sales-Auffüllung** oder die **Berichterstellung in Sales** zugewiesen ist.

### <a name="after-you-set-up-a-store"></a>Nachdem Sie ein Geschäft einrichten

Nachdem Sie die Details für das Geschäft eingeben, schließen Sie diese Aufgaben ab, um die neuen Geschäftdaten an POS zu senden.

1. Konfigurieren der POS-Kassen für den Shop.
2. Weisen Sie dem Shop Produktsortimente zu.
3. Sortimente verarbeiten, um die Liste der Produkte zu generieren, die im Sortiment berücksichtigt werden, und um die Produkte im Geschäft verfügbar zu machen.
4. Senden Sie Daten wie Nummernkreise, Hardwareprofile, POS-Bildschirmlayouts, usw. zu den POS-Kassen.
5. Veröffentlichen Sie das Geschäft, um Ladendaten an POS zu senden.
6. Führen Sie die Jobs aus, um die Speicherdaten an POS zu senden.

## <a name="organization-hierarchies"></a>Organisationshierarchien

Commerce verwendet Organisationshierarchien, um Kanäle zu strukturieren. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht. Wenn Sie Filialen einrichten, können Sie diese einer Organisationshierarchie hinzufügen. Die Filialen teilen dann Daten, die für Sortimente, Auffüllung und Berichterstellung verwendet werden.

> [!NOTE]
> Um die Commerce-Verkaufsfunktionalität zu nutzen, muss der Konfigurationsschlüssel für **Mehrfache Wareneingänge** aktiviert werden. Diesen Konfigurationsschlüssel finden Sie in den Konfigurationsschlüsseln **Handel** unter **Systemverwaltung**\> **Einstellungen** \> **Lizenzkonfiguration**. Dies ist aufgrund verschiedener Validierungen auf der Grundlage der auf der Ebene der Kundenauftragszeile konfigurierten Lieferadresse erforderlich.

