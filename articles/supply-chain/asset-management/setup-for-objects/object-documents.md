---
title: Anlagendokumente
description: In diesem Artikel werden Anlagendokumente in Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2e8d72dc938c43e266c6b7c39329f827c56607a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899468"
---
# <a name="asset-documents"></a>Anlagendokumente

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel werden Anlagendokumente in Anlagenverwaltung erläutert.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]