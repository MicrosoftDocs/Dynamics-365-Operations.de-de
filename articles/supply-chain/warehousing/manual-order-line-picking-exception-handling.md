---
title: Ausnahmen bei der Entnahme von Auftrags- und Umlagerungspositionen manuell handhaben
description: Dieser Artikel beschreibt, wie Administratoren Lagerbuchungen manuell entnehmen (oder die Entnahme rückgängig machen) können, um Probleme zu beheben, die durch beschädigte Auftrags- und Umlagerungsauftragsdaten verursacht werden.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403669"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Ausnahmen bei der Entnahme von Auftrags- und Umlagerungspositionen manuell handhaben

[!include [banner](../includes/banner.md)]

Durch die manuelle Handhabung von Ausnahmen bei der Entnahme von Auftrags- und Umlagerungspositionen können Administratoren Probleme beheben, die durch beschädigte Auftrags- und Umlagerungsauftragsdaten verursacht werden. Sie ermöglicht vertrauenswürdigen Benutzern, Lagerbuchungen, die sich auf Auftrags- und Umlagerungsauftragspositionen beziehen, manuell zu entnehmen (oder die Entnahme rückgängig zu machen), während Lagerortprozesse bereits laufen.

Die hier beschriebene Funktionalität sollte nur in Fällen verwendet werden, in denen das System die Verarbeitung des Lagerortprozessstapels nicht auf die übliche Weise beenden kann. Standardmäßig dürfen nur Benutzer mit einer Systemadministratorrolle diese verwenden. Sie können jedoch Zugriff auf die Funktionalität gewähren, indem Sie bei Bedarf anderen Rollen die Berechtigung *Auftragspositionen manuell entnehmen* zuweisen.

## <a name="turn-on-this-feature-for-your-system"></a>Schalten Sie diese Funktion für Ihr System ein

Bevor Sie die beschriebenen Features verwenden können, müssen Sie sie in Ihrem System aktivieren Administratoren können die [Featureverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status dieser Features zu überprüfen und sie zu aktivieren. Im Arbeitsbereich **Featureverwaltung** sind die Features mithilfe der folgenden Namen aufgeführt:

- *Kommissionierdienst für manuelle Verkaufsposition für Administrator oder ähnliche vertrauenswürdige Benutzer*<br>(Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden.)
- *Dienst zur manuellen Auswahl von Umlagerungszeilen für Admins oder ähnliche vertrauenswürdige Benutzer*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Buchungen im Zusammenhang mit Auftrags- oder Umlagerungsauftragspositionen korrigieren

Verwenden Sie das folgende Verfahren, um Buchungen zu korrigieren, die sich auf Auftrags- oder Umlagerungsauftragspositionen beziehen.

1. Folgen Sie einem dieser Schritte, je nachdem, welche Art von Auftrag Sie korrigieren müssen:

    - Um eine Transaktion zu korrigieren, die sich auf einen Auftrag bezieht, gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Bereinigen \> Auftragsposition manuell auswählen**.
    - Um eine Buchung zu korrigieren, die sich auf einen Umlagerungsauftrag bezieht, gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Bereinigen \> Umlagerungsauftragsposition manuell auswählen**.

1. Nutzen Sie auf der Seite **Auftragspositionen manuell auswählen** oder **Umlagerungsauftragspositionen manuell auswählen** die Filter oben im Raster, um die gesuchte Position zu finden, und wählen Sie dann die Zielauftragsposition im oberen Raster aus.
1. Verwenden Sie die Registerkarten **Lagerbuchungen**, **Ladepositionen**, **Arbeitspositionen** und **Containerpositionen** im unteren Bereich, um weitere Informationen zur ausgewählten Position anzuzeigen. Die Informationen auf diesen Registerkarten geben einen grundlegenden Überblick über die zugehörigen Lagerortprozesse und deren Status.
1. Wählen Sie im Aktivitätsbereich **Entnahme**, um die ausgewählte Auftragsposition auf der Seite **Entnahme** für Lagerbuchungen zu öffnen. Sie können diesen Schritt sogar für Auftragspositionen ausführen, die bereits an das Lager freigegeben wurden. (Normalerweise können Auftragspositionen, die an das Lager freigegeben wurden, nicht auf der Seite **Entnahme** geöffnet werden.)

    > [!NOTE]
    > Möglicherweise erhalten Sie verschiedene Warnungen, wenn Sie die Seite **Entnahme** öffnen. Ergreifen Sie alle Maßnahmen, die diese Warnungen empfehlen. Beispielsweise erhalten Sie möglicherweise eine Warnung zu Auftragspositionen, die mit Lagerarbeit verknüpft sind. In diesem Fall ist es sinnvoll, zu versuchen, die Arbeit mit der Standardfunktionalität [Arbeit abbrechen](cancel-warehouse-work.md) abzubrechen, bevor Sie eine manuelle Korrektur vornehmen.

1. Wählen Sie die Position im Raster **Buchungen** und wählen Sie dann **Entnahmeposition hinzufügen** auf der Symbolleiste **Buchungen** aus.
1. Die ausgewählte Position wird in das Raster **Entnahmepositionen** verschoben. Legen Sie geeignete Werte für alle Spalten fest, in denen erforderliche Informationen fehlen. (Geben Sie beispielsweise den Lagerplatz und den Ladungsträger an, von dem der Artikel entnommen bzw. nicht mehr entnommen werden sollte.)
1. Wählen Sie **Alle entnehmen bestätigen** auf der Symbolleiste **Entnahmepositionen**.

## <a name="correct-load-line-quantities"></a>Ladepositionsmengen korrigieren

Gehen Sie wie folgt vor, um die Ladepositionsmenge zu korrigieren.

1. Folgen Sie einem dieser Schritte, je nachdem, welche Art von Auftrag Sie korrigieren müssen:

    - Um eine Transaktion zu korrigieren, die sich auf einen Auftrag bezieht, gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Bereinigen \> Auftragsposition manuell auswählen**.
    - Um eine Buchung zu korrigieren, die sich auf einen Umlagerungsauftrag bezieht, gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Bereinigen \> Umlagerungsauftragsposition manuell auswählen**.

1. Nutzen Sie auf der Seite **Auftragspositionen manuell auswählen** oder **Umlagerungsauftragspositionen manuell auswählen** die Filter oben im Raster, um die gesuchte Position zu finden, und wählen Sie dann die Zielauftragsposition im oberen Raster aus.
1. Wählen Sie auf der Registerkarte **Ladepositionen** im unteren Bereich **Ladepositionen manuell korrigieren** auf der Symbolleiste aus.
1. Überprüfen Sie auf der Seite **Ladepositionen manuell korrigieren** im Raster **Lagerbuchungen** die Bestandsbuchungen, die sich auf die ausgewählte Ladeposition beziehen.
1. Korrigieren Sie im oberen Raster die Ladepositionenmengen in den folgenden Spalten nach Bedarf:

    - **Durch Arbeit erstellte Menge**
    - **Entnommene Menge**
    - **Geplante Crossdocking-Menge**

    Das System überprüft alle Änderungen, die Sie an diesen Spalten vornehmen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
