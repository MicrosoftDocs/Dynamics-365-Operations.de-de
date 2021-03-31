---
title: Anlage erstellen
description: In diesem Thema wird erläutert, wie Sie auf der Seite Liste der Anlagen einen neuen Anlagendatensatz erstellen.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227039"
---
# <a name="create-a-fixed-asset"></a>Anlage erstellen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie auf der Seite Liste der **Anlagen** einen neuen Anlagedatensatz erstellen.

Das System weist die Anlage-Nummer basierend auf der Nummernfolge zu, die der Anlagegruppe zugeordnet ist. Wenn Sie die Anlagevorlage verwenden, um Vermögenswerte über das Microsoft Excel Add-In zu importieren oder wenn Sie einen anderen Importjob verwenden, erstellt das System automatisch Anlagenbestandsdatensätze und erhöht die Bestandsnummer.

Führen Sie die folgenden Schritte aus, um einen Anlage-Datensatz manuell zu erstellen.

1. Wechseln Sie zu **Navigationsbereich \> Module \> Anlagen \> Anlagen \> Anlagen**.
2. Wählen Sie im **Aktivitätsbereich** **Neu** aus.
3. Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus. Das Feld **Nummer** wird als Standardwert angegeben, wenn Sie die Funktion **Anlagen automatisch nummerieren** in den **Anlagenparametern** und der **Anlagengruppe** aktiviert haben. Anderenfalls müssen Sie eine eindeutige Nummer zur Identifizierung der Anlage eingeben.
4. Geben Sie im Feld **Name** einen Wert ein. Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für diese Anlage benötigt.
5. Wählen Sie im **Aktivitätsbereich** **Bücher** aus.
6. Geben Sie im Feld **Anschaffungsdatum** ein Datum ein.
7. Geben Sie im Feld **Anschaffungspreis** eine Zahl ein.

    - Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für diese Buchung benötigt.
    - Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für verbleibenden Bücher benötigt.

8. Schließen Sie die Seite.

Sie können Anlagen auch mithilfe des Excel-Add-Ins oder durch Ausführen eines Importauftrags aus dem Arbeitsbereich **Datenmanagement** importieren. Geben Sie vor dem Ausführen des Imports die Werte für die erforderlichen Felder in die Vorlage ein.

Wenn Sie die Anlagennummer nicht in der Vorlage des Excel-Add-Ins oder in der Datenverwaltung definiert haben, erstellt das System für jede importierte Anlage eine Anlagennummer und erhöht automatisch die Nummernfolge für jede Anlage. Wenn Sie jedoch Anlagens importieren und Anlagen-Nummern in der Vorlage definieren, erhöht das System **nicht** automatisch die Nummernfolge. In diesem Fall muss ein Administrator möglicherweise die Nummernfolge manuell aktualisieren. Wenn Sie die Anlagenummer in der Vorlage des Excel-Add-Ins definiert haben, verwendet das System die definierte Anlagenummer und erhöht die Nummernfolge.

> [!NOTE]                                                                                                         
> Nach Buchung der Abschreibung werden die **Inbetriebnahme** und **Abschreibungslaufdatum**-Felder auf der **Buch** Seite gesperrt. Außerdem werden beide Felder von der Datenentität nicht aktualisiert.

> [!WARNING]
> Der Anlagebestand wird nicht gelöscht, wenn Transaktionen in das zugehörige Buch gebucht wurden oder wenn die neu erstellte Anlage in einer Erfassungszeile erfasst, aber nicht gebucht wurde. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]