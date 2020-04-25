---
title: Anlagendokumente
description: In diesem Thema werden Anlagendokumente in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f994e519e354a766a2437f182d2ade39155749b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216550"
---
# <a name="asset-documents"></a>Anlagendokumente

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden Anlagendokumente in Asset Management erläutert.

In Asset Management können Sie Dokumente beispielsweise so einrichten, dass diese automatisch zu den Einzelvorgangstypen, den Anlagenherstellern, den Anlagentypen oder Anlagen zugeordnet werden. Diese Funktion ist hilfreich, wenn aktualisierte Dokumentversionen freigegeben werden. In diesem Fall müssen Sie einfach das aktualisierte Dokument im Standardspeicherort ablegen, den Sie für Supply Chain Management-Dokumente verwenden, und Sie müssen das Dokument dem Anlagendokumentdatensatz zuordnen, den Sie erstellt haben. Auf das aktualisierte Dokument kann dann über **Alle Anlagen**, **Aktive Anlagen**, **Meine aktiven Anlagen**, **Alle Arbeitsaufträge** und **Aktive Arbeitsauftragseinzelvorgänge** zugegriffen werden. Der Vorgang für das Zuordnen von Dokumenten zu einem Anlagendokumentdatensatz verwendet das Standardverfahren für die Dokumentverwaltung.

**Beispiel 1:** Ein Dokument, das einem Einzelvorgang zugeordnet ist, beschreibt möglicherweise eine Prozedur für diesen Einzelvorgangstyp.

**Beispiel 2:** Ein Dokument, das einer Kombination aus Anlagentyp, Hersteller und Modell zugeordnet ist, kann möglicherweise das Standardhandbuch für das ausgewählte Anlagenherstellermodell sein.

## <a name="create-asset-document-relation"></a>Anlagendokumentzuordnung erstellen

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagendokumente**.
2. Wählen Sie **Neu**, um einen Anlagendokumentdatensatz zu erstellen.
3. Je nachdem, wie spezifisch die Dokumentzuordnung sein soll, nehmen Sie die entsprechende Auswahl in den folgenden Feldern vor: **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Einzelvorgangstypkategorie**, **Einzelvorgangstyp**, **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung**. Die Optionen, die in den Feldern **Einzelvorgangstypvariante** und **Einzelvorgangsanforderung** verfügbar sind, hängen von der Auswahl im Feld **Einzelvorgangstyp** ab.

    > [!NOTE]
    > Wenn das System nach Dokumenten sucht, die einer Anlage oder einem Arbeitsauftrag zugeordnet sein sollten, durchläuft Asset Management alle Anlagendokumentdatensätze, um mögliche Übereinstimmungen zu finden. Die spezifischste Kombination wird immer zuerst geprüft. Das bedeutet, Asset Management sucht als Erstes nach einer Übereinstimmung für das Feld **Einzelvorgangsanforderung**. Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Einzelvorgangstypvariante**. Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Einzelvorgangstyp** usw. Wie Sie im Layout der Seite **Anlagendokumente** sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft. Es können mehrere Dokumente einer Anlage oder einem Arbeitsauftrag zugeordnet sein. Sie können den Servicelevel einer Wartungsanfrage oder eines Arbeitsauftrags bearbeiten, falls notwendig.

4. Wählen Sie **Anhänge** aus. Die Standardseite **Handhabung von Dokumenten** wird angezeigt.
5. Hier können Sie die Dokumente oder Hinweise einrichten, die dem Anlagendokumentdatensatz zugeordnet werden sollen. Nachdem Sie Dokumente zugeordnet haben, wird im Feld **Anhänge** die Anzahl der Dokumente angezeigt, die dem Datensatz zugeordnet sind.
