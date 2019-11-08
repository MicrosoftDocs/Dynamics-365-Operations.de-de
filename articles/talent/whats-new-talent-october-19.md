---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (16. Oktober 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551702"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (16. Oktober 2018)

[!include[banner](includes/banner.md)]

**Build 8.1.1067**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="allow-managers-to-update-time-off-requests"></a>Managern erlauben, Freizeitanforderungen zu aktualisieren.

Freizeitanforderungen von Mitarbeitern müssen möglicherweise aktualisiert werden, nachdem sie über den Workflow genehmigt sind. In vielen Fällen kann der Manager diese Aktualisierungen im Auftrag des Mitarbeiters machen. Diese neue Funktion bietet Managern die Möglichkeit, Freizeitanforderungen im Auftrag der Mitarbeiter zu aktualisieren oder zu stornieren. Diese Funktion wird vom Parameter **Arbeit im Auftrag** gesteuert, der auf der Seite **Personalverwaltungs-Parameter** aktiviert werden kann. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>HR erlauben, Freizeitanforderungen zu aktualisieren

Ähnlich der Funktion zuvor, müssen möglicherweise Mitarbeiterfreizeitanforderungen von HR aktualisiert werden, nachdem sie bereits über den Workflow genehmigt wurden. Diese Funktion bietet die Möglichkeit für HR-Nutzer, Freizeitanforderungen zu aktualisieren. Die Funktion ist im Arbeitsbereich **Personen** auf der Seite **Arbeitskraft** aktiviert, und zwar mithilfe eine neue Option **Ansichtsfreizeit**. Auf diesen Seiten können Personalverwaltungsbenutzer Freizeitanforderungstransaktionen anzeigen und aktualisieren, ähnlich wie Manager diese Aktivitäten ausführen können.

Die Sicherheitsberechtigung, die Zugriff auf diese Funktionen steuert, ist:
- Auftrag: Arbeitskraftspezifische Urlaubs- und Abwesenheitsprozesse verwalten.
- Recht: Urlaubs- und Abwesenheitsanforderungen für alle Arbeitskräfte.

## <a name="other-changes"></a>Andere Änderungen
Folgende Aktualisierungen sind in dieser Version erfolgt:
- Änderungen an Arbeitseinstellungsaktivitäten, sodass sie nicht mehr im Status **Workflow abgeschlossen** sind.
- Beschäftigungszahl kann nun ohne Beschäftigung erstellt werden.
- Das Registrierungsdatum für Dynamics 365 Talent für einen Kurs, der im Mitarbeiter-Self-Service angezeigt wird, wendet nun den Zeitzonenunterschied im Datum an.
- Excel-Dateien können mehrmals ohne gefundene Fehler mithilfe von  **Mitarbeiter-Entität** importiert werden.

## <a name="known-issue"></a>Bekannte Probleme

- **Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut. 
- **Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
