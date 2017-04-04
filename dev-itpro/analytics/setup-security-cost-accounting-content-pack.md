---
title: "Dient zum Einrichten der Sicherheit für den Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt"
description: "In diesem Thema wird erläutert, wie die ZugriffEbenensicherheit in der Kostenrechnung auf Positionsebene der Sicherheit in BI ausgebreitet werden Microsoft-Energie können. Diese Funktion wird sichergestellt, dass Benutzer nur BIdaten Energie anzeigen, für die Ihnen Zugriff erteilt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Dient zum Einrichten der Sicherheit für den Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt

In diesem Thema wird erläutert, wie die ZugriffEbenensicherheit in der Kostenrechnung auf Positionsebene der Sicherheit in BI ausgebreitet werden Microsoft-Energie können. Diese Funktion wird sichergestellt, dass Benutzer nur BIdaten Energie anzeigen, für die Ihnen Zugriff erteilt werden.

<a name="overview"></a>Überblick
--------

** Der Kostenrechnungsanalyse ** Microsoft-Energie Sicherheit verwendet BIinhalt Leistungsfähigkeit BI auf Positionsebene, um die Zugriffsrechte eines Benutzers zu beschränken. Sicherheit basiert auf den ZugriffEbenenorganisationshierarchie, die in den Kostenrechnungsparametern eingerichtet wird. Weitere Informationen zum Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt, finden Sie Kostenrechnungsanalyse Leistungsfähigkeit BIinhalt [] (Kostenrechnung - analysis-content-pack.md ).

## <a name="setup"></a>Einstellung
Um ZugriffEbenensicherheit Leistungsfähigkeit zu BI weitergegeben werden kann, muss der Eigentümer der Leistungsfähigkeit BIinhalts die folgenden Schritte ausführen. ** Hinweis: ** Der Benutzer, der den Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt automatisch, der Eigentümer veröffentlicht wird. Nur ein Eigentümer kann die Sicherheit in BI Energie einrichten. Darüber hinaus bis ein Eigentümer andere Benutzer auf sie nicht hinzugefügt, PowerBI.com, außer der Besitzer alle Daten im Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt anzeigen kann.

1.  Veröffentlicht Sie die Definitionsdatei in BI Leistung.
2.  Melden Sie sich bei PowerBI.com.
3.  Suchen Sie das für den Kostenrechnungsanalyse Dataset ** ** Leistungsfähigkeit BIinhalt.
4.  Öffnen Sie die Sicherheitsseite. 

    [![an![die Sicherheitsseite öffnet]( https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)( https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png) ]

5.  ** Die Kostenträgercontroller ** Rolle ist bereits erstellt. Fügen Sie andere Mitglieder hinzufügen, die Teil der Kostenrechnungszugriffebenenorganisationshierarchie sind. 

    [![Mitglieder hinzufügt] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png) (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)]

Benutzer, die zu hinzugefügt werden Kostenträgercontroller ** ** Rolle, finden nur die Daten, um die ihnen zulässig sind, um festzustellen, entsprechend der Definition im Formular Kostenrechnungszugriffebenenorganisationshierarchie. ** Hinweis: ** Sicherheit auf Positionsebene gilt für Kacheln zu und von Berichten in Microsoft Dynamics 365 für Arbeitsgänge, die Leistung von BI eingebettet werden.

## <a name="updating-security"></a>Aktualisieren von Sicherheit
Wenn Aktualisierungen der ZugriffEbenensicherheit in der Kostenrechnung erstellt werden und Sie BI Energie diese Aktualisierungen) möchten, müssen Sie den Entitätsshop für den Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalt aktualisieren. Nachdem Sie die Entitätsshopaktualisierung von Microsoft Dynamics 365 für Arbeitsgänge ausführen, müssen Sie die PowerBI.com Artefakte auf aktualisieren. Weitere Informationen dazu, wie eine Entitätsshopaktualisierung, finden Sie hierzu Aktualisierungsentitätsshop [](power-bi-integration-entity-store.md#update-entity-store). Der Eigentümer des Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalts muss eine Entitätsshopaktualisierung auch erforderlich, wenn neue Benutzer Zugriff der Organisationshierarchie gewährt werden. Zudem muss der Eigentümer die neuen Benutzer der Kostenträgercontroller ** ** Rolle für PowerBI.com hinzufügen, um Sicherheit auf Positionsebene für sie angewendet wird.

## <a name="disabling-security"></a>Deaktivieren von Sicherheit
Es wird davon ausgegangen, dass Ihre Organisation möchte den Datenzugriff einschränken. Wenn aus einem bestimmten Grund Sicherheitsparameter deaktiviert werden, die bei der Kostenrechnung ausführen, Eigentümer muss der Benutzer der Buchhalter ** Kosten ** Rolle in BI Energie stattdessen hinzufügen. Wenn die Sicherheit eines aktivierten Bundesland einem deaktivierten Zustand ändern, wird empfohlen, Benutzer von der Kostenträgercontroller ** ** Rolle entfernen. Und umgekehrt, falls Sicherheit erneut aktivieren. Benutzer können Rollen beiden gehören. Gemeinsamer Zugriff ist die Gewerkschaft beider Rollen. Im Fall eines Kostenrechnungsanalyse ** ** Leistungsfähigkeit BIinhalts Benutzer, die gemeinsamen Zugriff erhalten, Zugriff die kostenlose Daten vorhanden sind. Wenn Sie möchten, Zugriff Einschränkungen anzuwenden ist, müssen Benutzer nur der Kostenträgercontroller ** ** Rolle zugewiesen sind. Diese Sicherheitsupdates auf Positionsebene sind sofort wirksam. Betroffene Benutzer können ihre Browser aktualisieren.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Weitere Informationen über Sicherheit BI Leistungsfähigkeit zu ermitteln auf Positionsebene, finden Sie [Verwalten von Sicherheit auf dem Modell in BI Energie] (https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


