---
title: Pflegen Sie das Zertifikat des Kreditors
description: Dieser Artikel beschreibt die Schritte, mit denen Kreditoren ihre Zertifikate mit Hilfe des Arbeitsbereichs „Kreditorenzusammenarbeit“ pflegen können.
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583203"
---
# <a name="maintain-vendor-certification"></a>Pflegen Sie das Zertifikat des Kreditors

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Schritte, die Ihre Kreditoren verwenden können, um ihre Zertifikate unter Verwendung des **Arbeitsbereichs Kreditorenzusammenarbeit** zu pflegen. Beispiele für Zertifikate sind Woman Business Enterprise (WBE) oder eine Firma, die nach LEED (Leadership in Energy and Environment Design) zertifiziert ist. Kreditor müssen Zertifizierungsinformationen in den Arbeitsbereich **Lieferanteninformationen** eingeben. Von dort aus wählen die Kreditor **Mehr Details** und dann **Zertifikate** aus.

## <a name="turn-on-the-vendor-certification-feature"></a>Die Funktion zur Kreditorenzertifizierung aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul** - *Kreditorenkonten*
- **Funktionsname** - *Zertifizierungsverwaltung der Kreditoren-Kooperation aktivieren*

## <a name="add-a-new-certification"></a>Eine neue Zertifizierung hinzufügen

Um ein neues Zertifikat hinzuzufügen, wählen Sie die Schaltfläche **Hinzufügen**, die sich oberhalb des Rasters **Zertifizierung** im Arbeitsbereich **Lieferanteninformationen** befindet. Geben Sie die folgenden Informationen ein:

- Zertifizierungsnummer
- Zertifizierungstyp
- Zertifizierungsorganisation
- Zertifizierungsdatum
- Haftungsbetrag, falls zutreffend
- Gültigkeitsdatum
- Ablaufdatum
- Kommentare, optional

Wenn es Dokumente gibt, die sich auf das spezifische Zertifikat beziehen, können Sie diese anhängen, indem Sie die Schaltfläche **Dokument** wählen.

Zertifikate, die von Ihren Kreditoren auf dieser Seite eingegeben werden, erhalten die Quelle „Kreditor“. Sie können Informationen zu Zertifikaten im Namen Ihres Kreditors unter Kreditor-Bankkonten eingeben. Die Informationen werden hier angezeigt und die Quelle wird als **Kunde** angezeigt.

Kreditor kann seine Zertifikate nach Bedarf bearbeiten oder löschen.

## <a name="vendor-collaboration-generated-certification-records"></a>Durch die Zusammenarbeit mit Kreditoren wurden Zertifizierungsdatensätze erstellt

Nachdem Zertifizierungsinformationen von einem Kreditor hinzugefügt wurden, werden die Informationen auf der Seite **Durch Zusammenarbeit mit Kreditoren generierte Zertifikate** hinzugefügt. Um die Seite zu öffnen, gehen Sie zu **Kreditorenkonten > Anfragen> Kreditorenberichte > Durch Zusammenarbeit mit Kreditoren generierte Zertifizierungen**. Standardmäßig sind alle neuen oder geänderten Zertifizierungsdatensätze sichtbar. Ein Sachbearbeiter des Kreditorenkontos kann die Änderungen anzeigen und die Informationen zur Validierung durch den Bestätigungsprozess validieren. Wenn die Informationen bestätigt wurden, kann der auf der Seite aufgeführte Zertifizierungsdatensatz ausgewählt und als überprüft gekennzeichnet werden. Wenn Sie den Datensatz als überprüft kennzeichnen, wird er aus der Standardliste entfernt.

Alle Zertifizierungsänderungen sind auf der Seite **Durch Zusammenarbeit mit Kreditoren generierte Zertifikate** sichtbar. Wenn eine Änderung nicht auf der Seite angezeigt wird, können Sie sie anzeigen, indem Sie die Filter für das Kreditorenkontos oder den Gültigkeitszeitraum anpassen oder auswählen, ob Informationen für überprüfte Zertifizierungsänderungen enthalten sein sollen.

