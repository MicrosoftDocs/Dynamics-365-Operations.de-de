---
title: Den „Es wurde nicht genug Kapazität gefunden“Planungsmodulfehler und endliche Kapazität beheben
description: In diesem Thema finden Sie Informationen zu den Gründen und Lösungen für „Produktionsauftrag %1 konnte nicht eingeplant werden“. Planungsmodulfehler über unzureichende Kapazität.
author: ChristianRytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: becd537d37a8ba8931f2598dccbae8554a4d168e
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985029"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>„Planungsmodulfehler über unzureichende Kapazität“ beheben

[!include [banner](../includes/banner.md)]

Wenn Sie die Planung ausführen, wird möglicherweise die folgende Fehlermeldung angezeigt.

> Der Produktionsauftrag '%1' konnte nicht geplant werden. Es wurde keine ausreichende Kapazität gefunden.

Es gibt mehrere Gründe, warum das Planungsmodul fehlschlagen und diese Fehlermeldung ausgeben kann. Dieses Thema enthält Richtlinien, die Ihnen helfen, die Ursache des Fehlers zu finden und ihn dann zu beheben.

## <a name="review-the-applicable-resources"></a>Überprüfen der entsprechenden Ressourcen

Der Fehler kann auftreten, wenn keine anwendbaren Ressourcen die Vorgangsanforderungen am Produktionsauftragsstandort erfüllen.

Führen Sie die folgenden Schritte aus, um die anwendbaren Ressourcen zu überprüfen.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, und öffnen Sie den Fertigungsauftrag, der nicht geplant werden kann, oder wählen Sie ihn aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Produktionsdetails** auf **Route**.
1. Wählen Sie auf der **Produktionsroute**-Seite, den Vorgang aus, und wählen Sie dann im Aktivitätsbereich **Anwendbare Ressourcen**.
1. Legen Sie im **Anwendbare Ressourcen**-Dialogfeld das **Nutzungsanforderungen für**-Feld auf *Betriebsplanung* oder *Arbeit planen* fest, abhängig von der Art der Planung, die Sie verwenden.
1. Stellen Sie sicher, dass am Produktionsauftragsstandort geeignete Ressourcen vorhanden sind.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Überprüfen Sie die der Ressource zugeordneten Kalender

Der Fehler kann auftreten, wenn der Ressource oder Ressourcengruppe kein Kalender zugeordnet ist oder der zugeordnete Kalender nicht richtig eingerichtet ist (z.B. keine Arbeitszeiten oder die Effizienz als Prozentsatz ist 0 \[Null\]).

Gehen Sie folgendermaßen vor, um zu überprüfen, ob der Ressource oder Ressourcengruppe ein Kalender zugeordnet ist.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, und öffnen Sie den Fertigungsauftrag, der nicht geplant werden kann, oder wählen Sie ihn aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Produktionsdetails** auf **Route**.
1. Wählen Sie auf der **Produktionsroute**-Seite, den Vorgang aus, und wählen Sie dann im Aktivitätsbereich **Anwendbare Ressourcen**.
1. Wählen Sie im Dialogfeld **Anwendbare Ressourcen** die Ressource aus, und wählen Sie dann **Ressource anzeigen**. Alternativ können Sie das Feld **Ressourcengruppe** auswählen und halten (oder mit der rechten Maustaste darauf klicken) und dann **Details anzeigen** wählen.
1. Legen Sie auf der **Ressourcen**-Seite oder der **Ressourcengruppen**-Seite, auf dem **Kalender**-Inforegister sicher, dass der Ressource oder Ressourcengruppe ein Kalender zugeordnet ist.

> [!NOTE]
> Wenn der Fehler während der Betriebsplanung auftritt, müssen Sie sicherstellen, dass allen zutreffenden Ressourcengruppen ein Kalender zugeordnet ist.

Gehen Sie folgendermaßen vor, um die Einrichtung des Kalenders zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Einrichtung \> Kalender \> Kalender**, und wählen Sie den Kalender aus, der der Ressource oder Ressourcengruppe zugeordnet ist.
1. Wählen Sie im Aktivitätsbereich **Arbeitszeiten**.
1. Stellen Sie auf der **Arbeitszeiten**-Seite sicher, dass die Seite nicht leer ist. Stellen Sie außerdem für die Tage, an denen Sie interessiert sind, sicher, dass das **Steuerung**-Feld nicht auf *Geschlossen* eingestellt ist, dass Arbeitszeiten existieren, und das **Effizienz ist Prozentsatz**-Feld nicht auf *0* (Null) eingestellt ist.

Wenn der Kalender mit dem Basiskalender verknüpft ist, müssen Sie auch die Einrichtung des Basiskalenders überprüfen.

> [!NOTE]
> Bei der Grobterminierung wird der Kalender der Ressourcengruppe verwendet, um die Start- und Endzeiten und entsprechende Datumsangaben für jeden Arbeitsgang zu bestimmen. Außerdem wird die Zeit begrenzt, die das System für einen bestimmten Vorgang an einem bestimmten Tag in einer bestimmten Ressourcengruppe einplanen kann. Wenn beispielsweise die Arbeitszeiten für eine Ressourcengruppe an einem bestimmten Tag zwischen 8:00 und 16:00 Uhr liegen, darf die Last, die ein Vorgang auf die Ressourcengruppe ausübt, die Last nicht überschreiten, die in acht Stunden passt, unabhängig von der verfügbaren Kapazität der Ressourcengruppe an diesem Tag. Allerdings kann die verfügbare Kapazität die Last weiter begrenzen.

## <a name="review-the-scheduling-parameters"></a>Überprüfen der Planungsparameter

Um eine gute Leistung zu gewährleisten, sucht das Planungsmodul nur für eine bestimmte Zeitdauer und eine bestimmte Anzahl von Planungskonflikten nach einer Ressource.

Gehen Sie folgendermaßen vor, um die Einrichtung der Planungsparameter zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Einstellungen \> Planungsparameter**.
1. Führen Sie einen dieser Schritte aus:

    - Wenn die **Planungs-Timeout aktiviert**-Option auf *Nein* eingestellt ist, fahren Sie mit Schritt 3 fort.
    - Wenn die **Planungs-Timeout aktiviert**-Option auf *Ja* eingestellt ist, erhöhen Sie den Wert des Felds **Maximale Planungszeit pro Sequenz**, um der Verarbeitung mehr Zeit zum Abschluss zu geben.

1. Führen Sie einen dieser Schritte aus:

    - Wenn die **Planungsoptimierung aktiviert**-Option auf *Nein* eingestellt ist, fahren Sie mit Schritt 4 fort.
    - Wenn die **Planungsoptimierung aktiviert**-Option auf *Ja* eingestellt ist, erhöhen Sie den Wert des Felds **Timeout der Optimierungsversuche**, um der Verarbeitung mehr Zeit zum Abschluss zu geben.

1. Wenn Sie eine der Einstellungen auf der Seite geändert haben, planen Sie die Bestellung neu, um es erneut zu versuchen.

## <a name="review-capacity"></a>Kapazität überprüfen

Der Fehler kann auftreten, wenn Sie eine finite Terminierung durchführen, aber keine freie Kapazität vorhanden ist.

Gehen Sie wie folgt vor, um eine Terminierung mit unbegrenzter Kapazität durchzuführen.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, und wählen Sie den Produktionsauftrag, der nicht geplant werden kann aus, oder öffnen Sie ihn.
1. Wählen Sie im Aktivitätsbereich, auf der **Planung**-Registerkarte, in der **Produktionsauftrag**-Gruppe, **Operationen planen** oder **Jobs planen** aus.
1. Stellen Sie im **Betriebsplanung**- oder **Jobplanung**-Dialogfeld, die **Endliche Kapazität**-Option auf *Nein*.
1. Wählen Sie **OK** aus, um den Auftrag zu planen.

Gehen Sie folgendermaßen vor, um die verfügbare Kapazität der Ressource zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcen**, und wählen Sie eine Ressource aus, die für den Auftrag gilt, der nicht geplant werden kann.
1. Wählen Sie im Aktivitätsbereich, auf der **Ressource**-Registerkarte, in der **Ansicht**-Gruppe **Kapazitätsbelastung** oder **Kapazitätsbelastung, grafisch** aus, und stellen Sie sicher, dass freie Kapazitäten vorhanden sind.

Gehen Sie folgendermaßen vor, um die verfügbare Kapazität der Ressourcengruppe zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcengruppen**, und wählen Sie eine Ressourcengruppe aus, die für den Auftrag gilt, der nicht geplant werden kann.
1. Wählen Sie im Aktivitätsbereich, auf der **Ressourcengruppe**-Registerkarte, in der **Ansicht**-Gruppe **Kapazitätsbelastung** oder **Kapazitätsbelastung, grafisch** aus, und stellen Sie sicher, dass freie Kapazitäten vorhanden sind.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Die Hauptplanung bucht eine Ressource, wenn der Ressourcenkalender geschlossen ist

Bei Verwendung der Betriebsterminierung plant die Produktprogrammplanung die Kapazität gemäß dem Kalender der primären Ressourcengruppe. Es bucht den sekundären Arbeitsgang gleichzeitig mit dem primären Arbeitsgang und berücksichtigt weder die Kalender noch die Kapazität des sekundären Arbeitsgangs. Dies kann dazu führen, dass der Produktionsauftrag in einem geschlossenen Kalender oder zu einem Zeitpunkt geplant wird, an dem der sekundäre Arbeitsgang nicht verfügbar ist (Kalender geschlossen, keine Kapazität).

Bei Verwendung der Auftragsterminierung berücksichtigt die Produktprogrammplanung die Kapazität und den Kalender sowohl des primären als auch des sekundären Arbeitsgangs, wenn der Auftrag terminiert wird. Damit der Auftrag terminiert werden kann, müssen Kalender für die Ressourcen beider Vorgänge geöffnet sein und verfügbare Kapazitäten haben.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
