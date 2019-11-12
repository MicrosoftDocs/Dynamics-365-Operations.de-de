---
title: Quellen für Kandidatenprofile und Anwendungen nachverfolgen
description: Dieses Thema enthält Informationen zum Verfolgen der Quelle für Kandidatenprofile und Bewerbungen bereit.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551886"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Quellen für Kandidatenprofile und Anwendungen nachverfolgen

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Die in diesem Abschnitt genannte Funktion steht im Rahmen einer Vorschauversion zur Verfügung. Inhalt und Funktionsweise unterliegen Änderungen. Um diese Funktion zu verwenden, bitten Sie einen Administrator um die Aktivierung mithilfe der **Administratoreinstellungen** in Attract. Eine zukünftige Version enthält Quellnachverfolgungsberichte. Weitere Informationen finden Sie unter [Zugriff auf Vorschaufunktionen im Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Wenn Kandidaten sich für eine Stelle bewerben, wird Attract automatisch die Quelle der Bewerbung nachverfolgen und Sie mit wertvollen Informationen versorgen, damit Sie die Rekrutierungsanstrengungen konkret angehen können. Personalbeschaffungsmanager und zukünftige Vorgesetzte können eine Bewerbungsquelle wählen, während manuell ein Kandidat einem Stelen- oder Kandidatenpool hinzugefügt wird.

Sie können die Bewerbungsquelle in den Bewerbungsaktivitätdetails auf der Registerkarte **Aktivität** sowie in der Bewerbungshistorie anzeigen, die unter **Profil** in den Talentpools bereitstehen. Sie können eine Kandidaten-Profilquelle in den Kandidatendetails in der Registerkarte **Profil** in der Bewerbung und in den Talentpools anzeigen.

> [!NOTE] 
> Sie finden Prozessvorlagen unter [Verständliches Add-On für Neueinstellungen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Quellen vorkonfigurieren

Die Standardquellliste enthält allgemeine Bewerbungsquellen. Einige Quelltypen wie **Stellenbörse** und **Soziales Netzwerk** haben zusätzliche Quelldetails. Beispielsweise enthält **Soziales Netzwerk** Facebook Twitter. Der **Bezug** Quelltyp ermöglicht es Ihnen, einen interne Mitarbeiter als Antragssteller anzugeben. Die Standardquellliste enthält die folgenden vorkonfigurierten Ressourcen:

-   Attract Website mit Stellenangeboten

-   Behörde

-   Karriere-Messe

-   Unternehmens-Marketing

-   Konferenzen und Messen

-   Berufsverbände

-   Stellenbörse

    -   Indeed

    -   Suche

    -   CareerBuilder

    -   Google-Stellen

    -   Xing

    -   Glassdoor

    -   Monster-Stellen

-   Zeitschriften und Magazine

-   Soziales Netzwerk

    -   Facebook

    -   Twitter

-   Hochschulrekrutierung

-   LinkedIn

-   Klassifiziert

-   Bezug

-   Hinzugefügt vom Personalbeschaffungsmitarbeiter

-   Sonstige

## <a name="customize-the-source-list"></a>Passen Sie die Quellliste an 

Sie können die Quellliste erweitern, um zusätzliche Bewerbungsquellen einzubeziehen. Um diese Liste anzupassen, folgen Sie den Anweisungen in [Optionsätze in Attract erweitern](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Bearbeiten Sie die Entität **TalentSource**, um zusätzliche Quellen einzubeziehen. 

Um negative Auswirkungen auf die Benutzeroberfläche (UI) zu vermeiden, bearbeiten oder löschen Sie nicht die  **TalentCategory** Aufzählungswerte (enum) (nicht Namen) aus folgenden Gründen:

- **Bezug**
- **LinkedIn**
- **Sonstige**

Stattdessen können Sie die Option **TalentSource** Aufzählungswerte erweitern, um andere Quelltypen hinzuzufügen.
