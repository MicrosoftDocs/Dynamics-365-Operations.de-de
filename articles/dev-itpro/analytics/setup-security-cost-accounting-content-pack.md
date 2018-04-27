---
title: "Aufstellungssicherheit für Kostenrechnungsinhalt für Power BI Inhalt"
description: "In diesem Thema wird erläutert, wie Sie Zugriffebenensicherheit in der Kostenrechnung auf Positionsebene in Microsoft-Power BI umsetzen können. Diese Funktion stellt sicher, dass Benutzer nur Power BI-Daten sehen, für die Ihnen Zugriff erteilt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Aufstellungssicherheit für Kostenrechnungsinhalt für Power BI Inhalt

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Zugriffebenensicherheit in der Kostenrechnung auf Positionsebene in Microsoft-Power BI umsetzen können. Diese Funktion stellt sicher, dass Benutzer nur Power BI-Daten sehen, für die Ihnen Zugriff erteilt werden.

<a name="overview"></a>Überblick
--------

Der **Kostenrechnungsanalyse** Microsoft-Power BI-Inhalt verwendet die Power BI-Sicherheit auf Positionsebene, um die Zugriffsrechte eines Benutzers zu beschränken. Sicherheit basiert auf der Zugriffebenenorganisationshierarchie, die in den Kostenrechnungsparametern eingerichtet wird. Weitere Informationen zum **Kostenrechnungsanalyse** Power BI-Inhalt finden Sie in [Kostenrechnungsanalyse für Power BI-Inhalt](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Einstellung
Um die Zugriffebenensicherheit für Power BI zu nutzen, muss der Eigentümer der Power BI-Inhalte die folgenden Schritte ausführen. **Hinweis:** Der Benutzer, der den **Kostenrechnungsanalyse** Power BI-Inhalt veröffentlich, wird automatisch der Eigentümer. Nur ein Eigentümer kann die Sicherheit in Power BI einrichten. Darüber hinaus bis ein Eigentümer andere Benutzer auf PowerBI.com hinzufügt, außer dem Besitzer kann niemand Daten in **Kostenrechnungsanalyse** Power BI-Inhalten anzeigen.

1.  Veröffentlicht der Definitionsdatei in Power BI.
2.  Melden Sie sich bei PowerBI.com an.
3.  Suchen Sie das Dataset für den **Kostenrechnungsanalyse** Power BI-Inhalt
4.  Öffnet Sie die Sicherheitsseite. 

    ![Sicherheitsseite öffnen](./media/CA-picture-1.png)

5.  Die **Kostenträgercontroller** Rolle ist bereits erstellt. Fügen Sie andere Mitglieder hinzufügen, die Teil der Kostenrechnungs-Zugriffebenenorganisationshierarchie sind. 

    ![Mitglieder hinzufügen](./media/CA-picture-2.png)

Benutzer, die zur Rolle **Kostenträgercontroller** hinzugefügt werden, finden nur die Daten, um die ihnen zulässig sind, um festzustellen, entsprechend der Definition im Formular Kostenrechnungs-Zugriffebenenorganisationshierarchie. **Hinweis:** Sicherheit auf Positionsebene gilt für Kacheln zu und von Berichten in Microsoft Dynamics 365 for Finance and Operations, die Power BI eingebettet werden.

## <a name="updating-security"></a>Sicherheit aktualisieren
Wenn Aktualisierungen der Zugriffebenensicherheit in der Kostenrechnung erstellt werden und Sie Power BI diese Aktualisierungen anzeigen lassen möchten, müssen Sie den Entitätsspeicher für den **Kostenrechnungsanalyse** Power BI-Inhalte aktualisieren. Nachdem Sie die Entitätsshopaktualisierung von Finance and Operations abschließen, müssen Sie die Artefakte in PowerBI.com aktualisieren. Weitere Informationen darüber, wie ein Entitätsshopaktualisierung vorgenommen wird, finden Sie unter [Entitätsshop aktualisieren](power-bi-integration-entity-store.md#update-entity-store). Der Eigentümer des **Kostenrechnungsanalyse** Power Bi-Inhalts muss eine Entitätsspeicheraktualisierung auch erforderlich, wenn neue Benutzer Zugriff der Organisationshierarchie gewährt werden. Zudem muss der Eigentümer die neuen Benutzer der **Kostenträgercontroller** für PowerBI.com hinzufügen, um Sicherheit auf Positionsebene für sie angewendet wird.

## <a name="disabling-security"></a>Deaktivieren von Sicherheit
Es wird davon ausgegangen, dass Ihre Organisation möchte den Datenzugriff einschränken. Wenn aus einem bestimmten Grund Sicherheitsparameter deaktiviert werden, die bei der Kostenrechnung ausführen, Eigentümer muss der Benutzer der **Kostenbuchhalter** Rolle in Power BI stattdessen hinzufügen. Wenn Sie die Sicherheit von einem aktivierten Status zu einem deaktivierten Zustand ändern, wird empfohlen, Benutzer von der **Kostenträgercontroller** Rolle zu entfernen. Und umgekehrt, falls Sie die Sicherheit erneut aktivieren. Benutzer können Rollen beiden gehören. Gemeinsamer Zugriff ist beider Rollen gemeinsam. Im Fall eines **Kostenrechnungsanalyse** Power BI-Inhalts, Benutzer, die gemeinsamen Zugriff erhalten, haben Zugriff die uneingeschränkte Daten. Wenn Sie möchten, das der Zugriff eingeschränkt ist, müssen Benutzer nur der **Kostenträgercontroller** Rolle zugewiesen werden. Diese Sicherheitsupdates auf Positionsebene sind sofort wirksam. Betroffene Benutzer können ihre Browser aktualisieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Weitere Informationen über die Sicherheit auf Positionsebene in Power BI finden Sie unter [Sicherheit für Ihr Modell in Power BI verwalten](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




