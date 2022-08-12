---
title: Den „Es wurde nicht genug Kapazität gefunden“Planungsmodulfehler und endliche Kapazität beheben
description: In diesem Artikel finden Sie Informationen zu den Gründen und Lösungen für „Produktionsauftrag %1 konnte nicht eingeplant werden“. Planungsmodulfehler über unzureichende Kapazität.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135598"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>„Planungsmodulfehler über unzureichende Kapazität“ beheben

[!include [banner](../includes/banner.md)]

Wenn Sie die Planung ausführen, wird möglicherweise die folgende Fehlermeldung angezeigt.

> Der Produktionsauftrag '%1' konnte nicht geplant werden. Es wurde keine ausreichende Kapazität gefunden.

Es gibt mehrere Gründe, warum das Planungsmodul fehlschlagen und diese Fehlermeldung ausgeben kann. Dieser Artikel enthält Richtlinien, die Ihnen helfen, die Ursache des Fehlers zu finden und ihn dann zu beheben.

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

Der Fehler kann auftreten, wenn Sie eine endliche Terminierung durchführen, aber keine freie Kapazität vorhanden ist.

Gehen Sie wie folgt vor, um eine Terminierung mit unbegrenzter Kapazität durchzuführen.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, und wählen Sie den Produktionsauftrag, der nicht geplant werden kann aus, oder öffnen Sie ihn.
1. Wählen Sie im Aktivitätsbereich, auf der **Planung**-Registerkarte, in der **Produktionsauftrag**-Gruppe, **Operationen planen** oder **Jobs planen** aus.
1. Stellen Sie im **Betriebsplanung**- oder **Jobplanung**-Dialogfeld, die **Endliche Kapazität**-Option auf *Nein*.
1. Wählen Sie **OK** aus, um den Auftrag zu planen.

Gehen Sie folgendermaßen vor, um die verfügbare Kapazität der Ressource zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcen**, und wählen Sie eine Ressource aus, die für den Auftrag gilt, der nicht geplant werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Ressourcen** in der Gruppe **Ansicht** die Option **Kapazität laden** oder **Kapazität laden, grafisch** und vergewissern Sie sich, dass die Kapazität verfügbar ist.

Gehen Sie folgendermaßen vor, um die verfügbare Kapazität der Ressourcengruppe zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcengruppen**, und wählen Sie eine Ressourcengruppe aus, die für den Auftrag gilt, der nicht geplant werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Ressourcengruppe** in der Gruppe **Ansicht** die Option **Kapazitätsladung** oder **Kapazitätsladung, grafisch** und vergewissern Sie sich, dass die Kapazität verfügbar ist.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Die Hauptplanung bucht eine Ressource, wenn der Ressourcenkalender geschlossen ist

Bei Verwendung der Betriebsterminierung plant die Produktprogrammplanung die Kapazität gemäß dem Kalender der primären Ressourcengruppe. Es bucht den sekundären Arbeitsgang gleichzeitig mit dem primären Arbeitsgang und berücksichtigt weder die Kalender noch die Kapazität des sekundären Arbeitsgangs. Dies kann dazu führen, dass der Produktionsauftrag in einem geschlossenen Kalender oder zu einem Zeitpunkt geplant wird, an dem der sekundäre Arbeitsgang nicht verfügbar ist (Kalender geschlossen, keine Kapazität).

Bei Verwendung der Auftragsterminierung berücksichtigt die Produktprogrammplanung die Kapazität und den Kalender sowohl des primären als auch des sekundären Arbeitsgangs, wenn der Auftrag terminiert wird. Damit der Auftrag terminiert werden kann, müssen Kalender für die Ressourcen beider Vorgänge geöffnet sein und verfügbare Kapazitäten haben.

## <a name="maximum-job-lead-time-is-too-short"></a>Maximale Vorlaufzeit für Aufträge ist zu kurz

Die Planungsmaschine kann einen Auftrag nicht einplanen, wenn die auf Ihrer Seite festgelegte **Maximale Vorlaufzeit** kleiner ist als die Vorlaufzeit, die für einen Artikel in den Standardauftragseinstellungen oder den Deckungseinstellungen festgelegt ist.

Um die Einstellung **Maximale Vorlaufzeit** für Ihren Standort anzuzeigen oder zu bearbeiten, gehen Sie auf **Produktionssteuerung \> Einrichtung \> Parameter der Produktionssteuerung** und öffnen Sie die Registerkarte **Allgemein**.

Um die Standardauftragseinstellungen für einen Artikel anzuzeigen oder zu bearbeiten, gehen Sie wie folgt vor:

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen Sie das betreffende Produkt und wählen Sie es in der Liste aus.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Lagerbestand verwalten** und wählen Sie **Standardauftragseinstellungen**.
1. Erweitern Sie das Inforegister **Bestand** und sehen Sie sich die Einstellung **Vorlaufzeit des Bestands** an oder bearbeiten Sie sie nach Bedarf.

Um die Reichweiteneinstellungen für einen Artikel anzuzeigen oder zu bearbeiten, gehen Sie wie folgt vor:

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen Sie das betreffende Produkt und wählen Sie es in der Liste aus.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Plan** und wählen Sie **Artikelabdeckung**.
1. Öffnen Sie die Registerkarte **Vorlaufzeit** und sehen Sie sich den Wert **Produktionszeit** an oder bearbeiten Sie ihn nach Bedarf.

## <a name="excessive-quantity-of-required-resources"></a>Überschüssige Menge an benötigten Ressourcen

Während der Terminierung versucht die Engine, die für einen Vorgang auf der Route festgelegte erforderliche Ressourcenmenge mit den anwendbaren Ressourcen gemäß dem Ressourcenbedarf des Vorgangs abzugleichen. Wenn Sie die Ressourcenmenge zu hoch festlegen, kann dies dazu führen, dass eine Route nicht durchführbar ist, was einen Planungsfehler zur Folge hat.

Verwenden Sie das folgende Verfahren, um sowohl die angegebene Menge als auch die anwendbaren Ressourcen für ein ausgewähltes Produkt, eine Route und einen Routenvorgang zu überprüfen:

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen Sie das entsprechende Produkt im Raster und wählen Sie es aus.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Engineer** und wählen Sie **Route**.
1. Suchen Sie die entsprechende Route im Raster und wählen Sie sie aus.
1. Öffnen Sie die Registerkarte **Übersicht** unten auf der Seite.
1. Wählen Sie einen Vorgang aus der Liste der ausgewählten Routenvorgänge.
1. Wählen Sie **Anwendbare Ressourcen**, um einen Dialog zu öffnen, in dem Sie die anwendbaren Ressourcen für den ausgewählten Vorgang der Route anzeigen können.
1. Öffnen Sie die Registerkarte **Ressourcen-Ladung**. Das Feld **Menge** zeigt die Ressourcenmenge an, die für den ausgewählten Vorgang der Route benötigt wird. Sehen Sie ihn an und/oder bearbeiten Sie ihn nach Bedarf.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
