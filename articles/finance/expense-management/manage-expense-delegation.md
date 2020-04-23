---
title: Ausgabendelegierung verwalten
description: Ein Benutzer, der die Kosten delegiert, kann im Auftrag eines anderen Mitarbeiters in der Organisation Spesenabrechnungen erstellen und verwalten.
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0871017ebe111464e79800ef83b90931afb50df0
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124115"
---
# <a name="manage-expense-delegation"></a>Ausgabendelegierung verwalten

[!include [banner](../includes/banner.md)]

Ein Benutzer, der die Kosten delegiert, kann im Auftrag eines anderen Mitarbeiters in der Organisation Spesenabrechnungen erstellen und verwalten.

## <a name="configuring-expense-delegation"></a>Ausgabendelegierung konfigurieren

Um einen Benutzer als Ausgabenvertreter einzurichten, gehen Sie zu **Ausgabenverwaltung> Einrichtung> Allgemein> Stellvertretungen** zum Öffnen der Seite **Delegierte**. Wählen Sie **Neu** und wählen Sie dann den Mitarbeiter aus, für den ein Delegierter definiert werden soll. Geben Sie den Alias des delegierten Benutzers sowie das Start- und Enddatum für den Delegierungszeitraum ein.

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a>Verwaltung der Kostendelegation für einen anderen Mitarbeiter

Wenn der Feature-Management-Schlüssel **Seite mit der Liste der Kostendelegierten aktivieren** aktiviert ist, wird die Listenseite **Ausgaben an mich delegiert** verfügbar, wenn Sie zu **Ausgabenverwaltung> Meine Ausgaben> An mich delegierte Ausgaben** navigieren.

Ein delegierter Benutzer kann vorhandene Ausgabenberichte, die an den Benutzer delegiert wurden, schnell filtern und durchsuchen. Der Benutzer kann auch schnell eine neue Spesenabrechnung für andere Benutzer erstellen, indem er auf **Neue Spesenabrechnung** klickt.

Stellvertretende Benutzer können auch Spesenabrechnungen für andere Mitarbeiter erstellen und verwalten, indem Sie zu **Ausgabenverwaltung> Meine Ausgaben> Ausgabenberichte** navigieren und auf die Schaltfläche **Öffnen Sie die Ausgaben anderer Benutzer** klicken.