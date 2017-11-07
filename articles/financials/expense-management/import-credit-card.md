---
title: Kreditkartenbuchungen importieren und verwalten
description: "In diesem Thema wird erläutert, wie ausgabenbezogenen Kreditkartenbuchungen importiert und verwaltet werden. Diese Transaktionen können so eingerichtet werden, dass Sie automatische nach einem sich wiederholenden Zeitplan importiert werden sollen, oder Sie können die Buchungen nach Bedarf manuell importieren."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 3379e2f850653cb99231d4ab030b64beb72b626a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Kreditkartenbuchungen importieren und verwalten

[!include[banner](../includes/banner.md)]

Ausgabenbezogenen Kreditkartenbuchungen können eingerichtet werden, damit sie automatisch auf wiederkehrender Basis die Daten importieren. Alternativ können die Buchungen manuell importiert werden, wenn diese benötigt werden. Die Kreditkartentransaktionen werden über Kreditkartenbuchungs-Entität importiert.

Weitere Informationen zu den Daten-Entitäten finden Sie unter [Daten-Entitäten](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Kreditkartenbuchungen importieren

1. Wählen Sie auf der Seite **Kreditkartenbuchungen** **Buchungen importieren** aus. Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie den Vorgang fortsetzen können.
2. Geben Sie im Feld **Name** ggf. eine kurze Beschreibung des Import-Vorgangs ein.
3. Im Feld **Quelldatenformat** wählen Sie das Format der Datei aus, die die zu importierende Kreditkartentranskation enthält.
4. Wählen Sie **Hochladen** aus und anschließend "Suchen" und wählen die Datei aus, die importiert werden sollen.
5. Nachdem die Datei hochgeladen wurde, überprüfen Sie die Zuordnung der Kreditkartenbuchungsdatei und die Spalten der Kreditkartenbuchungsdatenentität, indem Sie den Link auswählen **Zuordnung anzeigen** auf der Kachel. Beim Auftreten von Zuordnungsfehlern oder wenn Sie die Verteilung ändern möchten, nehmen Sie die Registerkarte **Zuordnungsvisualisierung** oder **Zuordnungsdetails**.
6. Um die Kreditkartenbuchungen zu automatisieren, wählen Sie **Erstellen von sich wiederholenden Dateneneinzelvorgängen** aus. Sie können anschließend die Wiederholung festlegen, um festzulegen, wie oft Kreditkartenbuchungen importiert werden sollen. Klicken Sie abschließend auf **OK**.
7. Um die ausgewählte Datei nun zu importieren, wählen Sie **Importieren** aus.
8. Wenn Fehler beim Import auftreten, können Sie das Ausführungsprotokoll oder die Bereitstellungsdaten anzeigen, um die Fehler anzuzeigen, die Sie korrigieren möchten, um einen erfolgreichen Import sicherzustellen.

> [!NOTE]
> Wenn Sie mehr als ein Dateiformat importieren möchten, müssen Sie separate Importeinzelvorgänge für jeden Formattyp erstellen.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Kreditkartenbuchungen für ausgeschiedenen Mitarbeiter neu zuweisen.

Nachdem ein Mitarbeiterdatensatz beendet ist, wird das Konto Active Directory-Domain Services (AD DS) des Mitarbeiters deaktiviert. Allerdings gibt es möglicherweise aktive Kreditkartenbuchungen, die noch bezahlt und erstattet werden müssen. Sie können nun die Seite **Kreditkartenbuchungen** verwenden, um den Mitarbeiter für eine Kreditkartenbuchung neu zuzuweisen, wo der zugeordnete Mitarbeiter ausgeschieden ist.

Wählen Sie mindestens eine Kreditkartenbuchung aus, und wählen Sie dann **Weisen Sie Buchungen neu zu** aus. Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartenbuchungen zugewiesen werden sollen. Nachdem die Kreditkartenbuchung neu zugewiesen wurde, kann die Buchung für eine Spesenabrechnung ausgewählt werden und über den regulären Prozess für Spesenabrechnungsrückerstattung bezahlt werden.

