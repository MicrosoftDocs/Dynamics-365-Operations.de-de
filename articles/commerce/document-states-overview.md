---
title: Dokumentstatus und -Lebenszyklus
description: In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c30932800beda13ac8fe6b0386fe29efe93f79c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982615"
---
# <a name="document-states-and-lifecycle"></a>Dokumentstatus und -Lebenszyklus

[!include [banner](includes/banner.md)]

In diesem Thema werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.

## <a name="document-state-descriptions"></a>Dokumentstatusbeschreibung

Die [Seitenelemente](page-elements-overview.md) der Themen führen verschiedene Dokumente im Content Management System (CMS) auf. Diese Dokumenttypen können mehrere Status im Erstellungstool haben. Die Dokumenttypen helfen, Datenkonflikte zu verhindern und Versionskontrollen zu erzwingen. Sie bestimmen, wer die Dokumente ändern kann, wenn die Dokumente geändert werden können und wenn Änderungen von anderen Personen angezeigt werden können.

Die folgende Tabelle enthält die möglichen Dokumentstatus von Seitenelementen in Commerce.

| Dokumentstatus      | Site Builder Aktivität        | Beschreibung                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Ausgecheckt         | Wählen Sie **Bearbeiten** aus.           | Das entsprechende Dokument wird Ihnen ausgecheckt. Während sich ein Dokument in diesem Status befindet, kann es von anderen authentifizierten Systembenutzern nicht geändert werden, und alle Änderungen, die Sie am Dokument vornehmen, sind nur für Sie sichtbar. |
| Gespeichert               | Wählen Sie **Speichern**.           | Änderungen, die an einem ausgecheckten Dokument vorgenommen wurden, werden in der Datenbank gespeichert, das Dokument ist jedoch noch nicht eingecheckt oder veröffentlicht. Die gespeicherten Änderungen sind nicht für andere authentifizierten Systembenutzer sichtbar, bis der Artikel **Bearbeitung beendet** gewählt wird. Sie sind nicht für externe Benutzer sichtbar, bis der Artikel veröffentlicht wird. |
| Auschecken verworfen | Wählen Sie **Änderungen verwerfen**.  | Alle Änderungen am ausgecheckten Dokument werden verworfen, und das Element wird auf die zuletzt eingecheckte Version zurückgesetzt. |
| Eingecheckt          | Wählen Sie **Beenden Sie die Bearbeitung**. | Das bearbeitete Dokument ist eingecheckt. Alle Änderungen sind für andere authentifizierte Systembenutzer sichtbar, und diese Benutzer können das Dokument dann bearbeiten. Jedes Einchecken erstellt einen Dokumentversionsdatensatz im Workflowverlauf des Artikels. |
| Publiziert           | Wählen Sie **Veröffentlichen** aus.        | Das Dokument wird veröffentlicht, und die Änderungen werden auf Ihre Live-Site übertragen und können von externen Benutzern erkannt werden. Artikel können nur veröffentlicht werden, wenn sie zuerst eingecheckt wurden durch Auswahl von **Bearbeitung beenden**. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Möglichkeiten zum Hinzufügen von Inhalten](add-manage-content.md)

[Seitenmodellglossar](page-elements-overview.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)

[Aktivieren und verwenden Sie die kanalübergreifende Freigabe](cross-channel-sharing.md)

[Arbeiten mit Modulen](work-with-modules.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Übersicht über Vorlagen und Layouts](templates-layouts-overview.md)

[Anpassen der Sitenavigation](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]