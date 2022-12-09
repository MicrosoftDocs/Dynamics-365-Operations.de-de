---
title: Eine unbefristete Beurlaubung erstellen
description: Dieser Artikel erklärt, wie Sie in Microsoft Dynamics 365 Human Resources eine unbefristete Beurlaubung erstellen.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805340"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Eine unbefristete Beurlaubung erstellen

> [!IMPORTANT]
> Die in diesem Artikel beschriebene Funktion wird in einem zukünftigen Release der Finance-Infrastruktur nach Microsoft Dynamics 365 Finance Version 10.0.31 verfügbar.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Anträge auf unbefristeten Urlaub stellen und den Status Ihrer Urlaubsanträge anzeigen in Dynamics 365 Human Resources anzeigen lassen.

## <a name="prerequisites"></a>Erforderliche Komponenten

1. Stellen Sie unter **Funktionsverwaltung** sicher, dass die Funktion **Unbefristeter Urlaub** aktiviert ist.

    > [!IMPORTANT]
    > Nachdem diese Funktion aktiviert wurde, kann sie nicht wieder deaktiviert werden.

2. Erstellen Sie einen Urlaubstyp für die Beurlaubung aus.
3. Geben Sie die Details wie Urlaubstyp, Beschreibung und Workflow-ID ein.
4. Wählen Sie im Feld **Antragsart** **Beurlaubung** aus.
5. Setzen Sie im Detailbereich für unbefristete Urlaube die Option **Unbefristet** auf **Ja**.
6. Setzen Sie die Option **Meldung zur Wiederaufnahme der Arbeit** auf **Ja** oder **Nein**.
7. Bei unbefristeten Urlaubsanträgen kann optional eine Meldung zur Wiederaufnahme der Arbeit verlangt werden.

> [!NOTE]
> Nachdem diese Funktion aktiviert wurde, wird die Funktion **Anhang erforderlich** deaktiviert.

## <a name="request-an-open-ended-leave-of-absence"></a>Eine unbefristete Beurlaubung beantragen

1. Wählen Sie im Arbeitsbereich **Mitarbeiter-Self-Service** auf der Kachel **Saldo der arbeitsfreien Zeit** **Mehr (...)** aus.
2. Um einen Antrag auf Beurlaubung einzureichen wählen Sie **Beurlaubung beantragen**.
3. Geben Sie Informationen in den Feldern **Beurlaubstyp** und **Anfangsdatum** ein. Geben Sie im Feld **Enddatum** ein voraussichtliches Enddatum ein.
4. Wenn Sie unterstützende Unterlagen einreichen müssen, wählen Sie **Anhänge** unter **Hochladen**.
5. Wenn Ihr Antrag zum Hochladen bereit ist, wählen Sie **Senden**. Andernfalls wählen Sie **Entwurf speichern**.
6. Wählen Sie, um einen Antrag auf unbefristete Beurlaubung zu aktualisieren, wählen Sie den Antrag aus, geben Sie ein Enddatum in das Feld **Enddatum** ein, legen Sie die Option **Enddatum bestätigen** auf **Ja** fest und laden Sie die Dokumentation hoch.
7. Wenn die Option **Meldung zur Wiederaufnahme der Arbeit** auf **Ja** eingestellt ist, wählen Sie **Hochladen** und aktivieren Sie dann das Kontrollkästchen, um zu bestätigen, dass eine gültige Mitteilung zur Wiederaufnahme der Arbeit hochgeladen wurde.
8. Wenn alle Details eingegeben wurden, wählen Sie **Senden**.
