---
title: Dokumentstatus und -lebenszyklus
description: In diesem Artikel werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269915"
---
# <a name="document-states-and-lifecycle"></a>Dokumentstatus und -lebenszyklus

[!include [banner](includes/banner.md)]

In diesem Artikel werden die verschiedenen Dokumentstatus von Seitenelementen in Microsoft Dynamics 365 Commerce behandelt.

## <a name="document-state-descriptions"></a>Dokumentstatusbeschreibung

Die [Seitenelemente](page-elements-overview.md) der Artikel führen verschiedene Dokumente im Content Management System (CMS) auf. Diese Dokumenttypen können mehrere Status im Erstellungstool haben. Die Dokumenttypen helfen, Datenkonflikte zu verhindern und Versionskontrollen zu erzwingen. Sie bestimmen, wer die Dokumente ändern kann, wenn die Dokumente geändert werden können und wenn Änderungen von anderen Personen angezeigt werden können.

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
