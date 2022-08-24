---
title: Importieren Sie Funktionen aus dem Global Repository
description: In diesem Artikel wird erklärt, wie Sie Funktionen zur Globalisierung aus dem Global Repository importieren.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278310"
---
# <a name="import-features-from-the-global-repository"></a>Importieren Sie Funktionen aus dem Global Repository

[!include [banner](../includes/banner.md)]

Das Global Repository enthält Funktionen für die Elektronische Rechnungsstellung, die mit Ihrem Konfigurationsanbieter gemeinsam genutzt werden. Alle Funktionen der Elektronischen Rechnungsstellung, die von Microsoft bereitgestellt werden, werden von allen Firmen gemeinsam genutzt. Sie haben automatisch Zugriff auf alle Funktionen für die Elektronische Rechnungsstellung, die Microsoft freigibt und im Global Repository veröffentlicht.

Um mit Funktionen für die Elektronische Rechnungsstellung zu arbeiten, die mit Ihrem Konfigurationsanbieter gemeinsam genutzt werden, importieren Sie sie in Ihre Instanz von Regulatory Configuration Service (RCS) aus dem Global Repository. Überprüfen Sie dann die Details der Funktionen, wie z.B. die Konfigurationen für die elektronische Berichterstattung (ER) und die Pipelines für die Verarbeitung.

## <a name="import-a-feature-from-the-global-repository"></a>Importieren Sie eine Funktion aus dem Global Repository

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie **Importieren**, um das Suchfeld **Funktion aus globalem Repository importieren** zu öffnen.
4. Um die Funktionen für die Elektronische Rechnungsstellung im Global Repository zu durchsuchen, die für einen bestimmten Konfigurationsanbieter verfügbar sind, synchronisieren Sie die RCS-Instanz Ihres Unternehmens, indem Sie **Synchronisieren** wählen. Nach Abschluss der Synchronisierung wird die Liste der verfügbaren Funktionen für die Elektronische Rechnungsstellung aus dem Global Repository aktualisiert. Diese Aktualisierung kann ein paar Minuten dauern.
5. Wählen Sie die Funktion aus, die Sie importieren möchten, und wählen Sie dann **Importieren**.

Um die importierte Funktion Elektronische Rechnungsstellung anzuzeigen, stellen Sie sicher, dass der richtige Konfigurationsanbieter ausgewählt ist. Standardmäßig werden Funktionen, die von dem aktiven Konfigurationsanbieter erstellt wurden, automatisch herausgefiltert. Sie können den Filter anpassen, um Funktionen anzuzeigen, die von anderen Anbietern erstellt wurden, z.B. dem Microsoft Konfigurationsanbieter.

Sie können jetzt mit der Funktion „Importieren“ arbeiten. Sie können seine Details überprüfen und eine neue Funktion erstellen, indem Sie die importierte Funktion als Vorlage verwenden.

> [!NOTE]
> Sie können eine Funktion nur ändern, wenn sie von dem derzeit aktiven Konfigurationsanbieter erstellt wurde. Sie können eine neue Funktion erstellen, indem Sie die ursprüngliche Funktion als Basis verwenden. Sie können dann die gewünschten Änderungen vornehmen oder die Parameter festlegen.

Wenn Microsoft oder eine andere Firma, die Globalisierungsfunktionen mit Ihrer Firma teilt, Funktionen aktualisiert, die Sie importiert haben, können Sie nach aktualisierten Versionen suchen, indem Sie **Nach Funktionsaktualisierungen suchen** im Abschnitt **Bezogene Einstellungen** des Arbeitsbereichs **Globalisierungsfunktionen** auswählen.

Wenn Sie sehen, dass es Aktualisierungen für eine Funktion gibt, die Sie als Vorlage verwenden, können Sie eine neue Version importieren, nachdem Sie die Liste der veröffentlichten Funktionen im globalen Repository synchronisiert haben.
