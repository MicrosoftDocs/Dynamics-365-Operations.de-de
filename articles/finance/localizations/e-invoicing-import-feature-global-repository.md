---
title: Importieren Sie Funktionen aus dem Global Repository
description: In diesem Artikel wird erklärt, wie Sie Funktionen zur Globalisierung aus dem Global Repository importieren.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc8f346cdef4aa0b909d75b016b37cbbe3248ebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865554"
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
