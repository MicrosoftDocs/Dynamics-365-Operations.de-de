---
title: Leasingobjekte über das Framework für Mietvertragsimport verwalten
description: In diesem Thema wird erläutert, wie Sie mithilfe des Mietvertragsimport-Frameworks mehrere Mietverträge gleichzeitig anpassen.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 26fb195ff18dc0c86d3546b782265043c2c78bf4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819793"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Leasingobjekte über das Framework für Mietvertragsimport verwalten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie mithilfe des Mietvertragsimport-Frameworks mehrere Mietverträge in einem Schritt anpassen. Durch die Verwendung dieser Funktion können Sie Zeit sparen und genauere Anpassungen sicherstellen, indem Sie das Risiko menschlicher Fehler verringern. Darüber hinaus kann diese Funktion Microsoft Dynamics 365 Finance mit externen Dateneinheiten zum effizienten Hochladen von Daten verbinden.

Die folgenden Dateneinheiten können verwendet werden, um Anlagenleasing in externe Systeme zu integrieren:

- Mietvertrags-Staging
- Staging des Zahlungsvertrags
- Staging für Vertrag zu Nebenkosten beim Leasing

Mit dem Importvorgang können Sie einen Mietvertrag anpassen, nicht finanzielle Informationen aktualisieren oder neue Mietverträge hinzufügen. Sie können die Mietvertragsdaten anzeigen und bearbeiten, bevor Sie sie importieren.

Das System kann die folgenden drei Prozesse über die Mietvertragsimport-Suite ausführen.

| Prozesstyp  | Beschreibung |
|---------------|-------------|
| Datensatz hinzufügen    | Migrierte Mietverträge mit diesem Prozesstyp erstellen einen Mietvertrag im System. Der Zahlungsplan muss manuell bestätigt werden, und der Journaleintrag der erstmaligen Erfassung muss nach der Migration manuell gebucht werden. |
| Datensatz aktualisieren | Migrierte Mietverträge mit diesem Prozesstyp aktualisieren Feldwerte für einen Mietvertrag, der sich bereits im System befindet. Nur die Felder, die auf der **Feldauswahl aktualisieren**-Seite ausgewählt wurden, werden aktualisiert. Wir empfehlen Ihnen, nichtfinanzielle Felder auf der Seite **Feldauswahl aktualisieren** auszuwählen, da dieser Prozesstyp den Mietvertrag nicht anpasst. |
| Datensatz anpassen | Migrierte Mietverträge mit diesem Prozesstyp passen den Mietvertrag an. Diese Regulierung führt zu einer finanziellen Mietvertragsänderung des Mietvertrags. Nach der Verarbeitung des Mietvertrags erstellt das System einen neuen Zahlungsplan unter Verwendung der neuen Daten aus der Mietvertragsimport-Suite. Das System bestätigt den Zahlungsplan nicht und bucht den Regulierungsjournaleintrag nicht. |

Nachdem Informationen über die Arbeitsbereich **Datenverwaltung** hochgeladen wurden, öffnen Sie die Seite **Header importieren** (**Anlagenleasing \> Mietvertragsimport Framework \> Header importieren**). Diese Seite listet alle Importe der drei zuvor aufgelisteten Datenentitäten auf.

Um die Mietvertrags-Staging-Daten anzuzeigen, bevor die Verarbeitung ausgeführt wird, wählen Sie **Daten bereitstellen** aus.

Mit der Vergleichsfunktion können Sie einen Datensatz, den Sie importieren, mit dem entsprechenden Datensatz vergleichen, der sich bereits in Ihrem System befindet. Um einen einzelnen Mietvertragsdatensatz zu vergleichen, wählen Sie einen Mietvertrag aus und wählen Sie dann **Vergleichen** aus. Sie sollten diesen Schritt ausführen, um einen **Unterschiede**-Bericht zu generieren, bevor Sie die Mietvertragsdatensätze migrieren. Die Vergleichsfunktion vergleicht die Werte in den Staging-Daten mit den Werten für Mietverträge, die sich derzeit im System befinden.

> [!NOTE]
> Die Vergleichsfunktion funktioniert nicht für Mietverträge mit dem **Datensatz hinzufügen**-Prozesstyp, da mit diesem Mietvertrag nichts zu vergleichen ist.
>
> Um mehrere Mietverträge gleichzeitig zu vergleichen, gehen Sie zu **Anlagenleasing \> Mietvertragsimport-Framework \> Periodisch \> Vergleichen** und wählen Sie **Vergleichen** aus.

Für jede Entität können Sie die Unterschiede zwischen dem, was sich derzeit im System befindet, und dem, was sich in den Staging-Tabellen befindet, anzeigen. Wählen Sie für jede Entität in den Staging-Tabellen **Unterschiede anzeigen** aus. Das angezeigte Dialogfeld zeigt den aktuellen Wert und den vorgeschlagenen Staging-Wert an.

Sie können den Staging-Wert auch aktualisieren, indem Sie ihn in der **Neuer Wert**-Spalte ändern und dann **Staging aktualisieren** auswählen.

Sie können Mietverträge validieren, um sicherzustellen, dass die Datensätze ohne Fehler in das System übernommen werden können. Bevor ein Mietvertragsdatensatz migriert wird, führt das System mehrere Überprüfungen durch, um sicherzustellen, dass der Datensatz erfolgreich importiert wird. Wählen Sie **Validieren** aus, um einen einzelnen Mietvertrag zu validieren.

> [!NOTE]
> Um mehrere Mietverträge gleichzeitig zu validieren, gehen Sie zu **Anlagenleasing \> Mietvertragsimport-Framework \> Periodisch \> Validieren** und wählen Sie **Vergleichen** aus.

Um einen einzelnen Mietvertrag zu bearbeiten, wählen Sie **Mietvertragsdatensätze migrieren** auf der **Header importieren**-Seite. Wenn ein Mietvertrag migriert wird, führt das System die im **Prozesstyp**-Feld angegebenen Aktion aus.

> [!NOTE]
> Um mehrere Mietverträge gleichzeitig zu validieren, gehen Sie zu **Anlagenleasing \> Mietvertragsimport-Framework \> Periodisch \> Validieren** und wählen Sie **Vergleichen** aus.

Nach dem Vergleich der Mietverträge können Sie einen Bericht ausführen, um die Unterschiede für jeden Mietvertrag anzuzeigen, der in der Import-ID enthalten ist. Um den Bericht für einen Mietvertrag auszuführen, wählen Sie diese Mietverträge in den Staging-Daten aus und wählen Sie dann **Bericht vergleichen und anzeigen \> Differenzbericht** aus.

> [!NOTE]
> Um mehrere Mietverträge gleichzeitig zu validieren, gehen Sie zu **Anlagenleasing \>Anfragen und Berichte \> Differenzbericht** und wählen Sie **Validieren** aus.

## <a name="set-up-update-fields"></a>Einrichten von Aktualisierungsfeldern

Wenn Sie das Mietvertragsimport-Framework zum Aktualisieren von Mietverträgen verwenden und der Prozesstyp **Datensatz aktualisieren** lautet, können Sie bestimmte zu aktualisierende Felder auswählen.

1. Gehen Sie zu **Anlagenleasing \> Mietvertragsimport Framework \> Installieren \> Feldauswahl aktualisieren**.
2. Wählen Sie auf der angezeigten Seite die zu aktualisierenden Felder aus und klicken Sie dann auf den grünen Pfeil, um sie in die Liste **Ausgewählte Felder** zu verschieben. Nur Felder in der Liste **Ausgewählte Felder** können mithilfe der Mietvertragsimport-Suite aktualisiert werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]