---
title: "Einzelhandelskanäle definieren und verwalten"
description: "Dieser Artikel gibt einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Microsoft Dynamics 365 for Retail als Einzelhandelsshops bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Einzelhandelsgeschäft einrichten."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: b6dd6d929d771e0b1fc2604b90a2a1522447e168
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---

# <a name="define-and-maintain-retail-channels"></a>Einzelhandelskanäle definieren und verwalten

[!include[banner](includes/banner.md)]


Dieser Artikel gibt einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Microsoft Dynamics 365 for Retail als Einzelhandelsshops bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Einzelhandelsgeschäft einrichten.

Dynamics 365 for Retail unterstützt mehrere Einzelhandelskanäle, wie Onlineshops, Call-Center und physische Läden. Ein physischer Laden wird Einzelhandelsshop genannt. Jeder Einzelhandelsshop kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten. Sie müssen alle Elemente für einen Shop einrichten, bevor Sie ihn erstellen. Nachdem Sie einen Einzelhandelsshop erstellt haben, weisen Sie die Produkte zu, die der Shop umfassen soll. Sie ordnen außerdem Mitarbeiter, Register und Debitoren der Filiale zu. Fügen Sie den neuen Shop schließlich zu einer Organisationshierarchie hinzu.

## <a name="setting-up-retail-stores"></a>Einrichten von Einzelhandelsgeschäften
Bevor Sie einen Einzelhandelsshop in Microsoft Dynamics 365 for Retail einrichten können, müssen Sie mehrere erforderliche Aufgaben ausführen. Sie können dann den Shop erstellen und Details hinzufügen.

### <a name="prerequisites"></a>Erforderliche Komponenten

Bevor Sie einen Einzelhandelsshop einrichten können, müssen Sie die folgenden erforderlichen Aufgaben ausführen:

1.  Konfigurieren Sie Ihre Organisationsstruktur und Einstellungsorganisationshierarchien für Einzelhandelssortimente, Auffüllung und Berichterstellung.
2.  Einrichten eines Lagerorts, der den Einzelhandelsshop abbildet.
3.  Richten Sie Nummernkreise für Einzelhandelsshops, Lageraufstellungen und Auszugsbelege ein.
4.  Parameter für Einzelhandel konfigurieren.
5.  Richten Sie die Zahlungsmethoden ein, die im Shop akzeptiert werden.
6.  Um Kreditkartenbuchungen an POS-Kassen zu verarbeiten, können Sie Zahlungsdienste einrichten.
7.  Mehrwertsteuergruppen einrichten.
8.  Einrichten von Einzelhandelsprodukten. Als Teil dieser Aufgabe richten Sie auch Produkthierarchien, Produktvarianten und Sortimente ein.
9.  Einrichten von Produktpreisgruppen.
10. Einrichten von Einzelhandelsproduktpreiskalkulation. Als Teil dieser Aufgabe richten Sie auch Preisregulierungen, Rabatte und Rabattzeiträume ein.
11. Einrichten von Mitarbeitern. **Hinweis:** Sie müssen den Arbeitskräften die entsprechenden Berechtigungen zuweisen, sodass diese sich anmelden und Aufgaben mit dem Microsoft Dynamics 365 for Retail für Retail POS-System ausführen können.
12. Konfigurieren der Retail POS-Profile, um sie dem Shop zuzuweisen. Diese Aufgabe beinhaltet zahlreiche weitere Aufgaben, wie das Einrichten von Registern, Einrichten von Offlineprofilen, und das Einrichten von Bonformaten und Profilen.

Prüfen Sie alle Aufgaben, die Voraussetzung sind, und führen Sie nur die Aufgaben aus, die für Sie gelten.

### <a name="set-up-a-retail-store"></a>Einrichten eines Einzelhandelsgeschäfts

Nach Abschluss der erforderlichen Aufgaben, führen Sie diese Aufgaben aus, um die Details für den Einzelhandelsshop einzurichten:

1.  Erstellt einen Einzelhandelsshop.
2.  Eine Mehrwertsteuergruppe dem Shop zuweisen.
3.  Die angenommenen Zahlungsmethoden dem Shop zuweisen.
4.  Fügen Sie Details zu den Produktbeschreibungen für Produkte hinzu, die Sie in den Einzelhandelsgeschäften anbieten. Sie können beispielsweise Rich-Text und Bilder hinzufügen. Diese Produktdetails werden in verschiedenen Kontexten, wie auf der POS-Kasse oder auf gedruckten Beschriftungen angezeigt.
5.  Fügen Sie den Shop zu einer Organisationshierarchie hinzu, die für ein **Sales-Sortiment**, eine **Sales-Auffüllung** oder die **Berichterstellung in Sales** zugewiesen ist.

### <a name="after-you-set-up-a-retail-store"></a>Nachdem Sie einen Einzelhandelsshop einrichten

Nachdem Sie die Details für den Einzelhandelsshop eingeben, schließen Sie diese Aufgaben ab, um die neuen Einzelhandelshopdaten an Retail-POS zu senden.

1.  Konfigurieren der POS-Kassen für den Shop.
2.  Weisen Sie dem Shop Produktsortimente zu.
3.  Sortimente verarbeiten, um die Liste der Produkte zu generieren, die im Sortiment berücksichtigt werden, und um die Produkte im Einzelhandelsshop verfügbar zu machen.
4.  Senden Sie Daten wie Nummernkreise, Hardwareprofile, POS-Bildschirmlayouts, usw. zu den Retail POS-Kassen.
5.  Veröffentlichen Sie das Einzelhandelsgeschäft, um Ladendaten an Retail POS zu senden.
6.  Führen Sie die Einzelvorgänge aus, um die Speicherdaten zu Retail POS zu senden.

## <a name="organization-hierarchies"></a>Organisationshierarchien
Retail verwendet Organisationshierarchien, um Einzelhandelskanäle zu strukturieren. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht. Wenn Sie Filialen einrichten, können Sie diese einer Organisationshierarchie hinzufügen. Die Filialen teilen dann Daten, die für Sortimente, Auffüllung und Berichterstellung verwendet werden.




