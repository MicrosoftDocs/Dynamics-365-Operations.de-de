---
title: Status des Lagerplatzes an einem Lagerort
description: Dieser Artikel bietet einen Überblick über die Statusfunktion für den Lagerplatz an einem Lagerort.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d2632ed1f5c733e45f5d927643bdaef430bc4009
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850408"
---
# <a name="warehouse-location-status"></a>Status des Lagerplatzes an einem Lagerort

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management enthält mehrere Lagerplatzfelder, die Ihnen Flexibilität bei der Arbeit mit und Wartung von Lagerplätzen bieten. Sie können Lagerplatzstatus in die Lagerplatzrichtlinienabfrage aufnehmen, um eine bessere Kontrolle über den Lagerfluss zu ermöglichen.

Die folgenden vier Felder auf der Seite **Lagerplätze** bieten Informationen zur Nachverfolgung des aktuellen Status eines Lagerplatzes. In diesen Feldern erhalten Lagerverwalter einen Überblick über den Status der Lagerplätze an einem Lagerort. Sie ermöglichen auch erweiterte Berichterstellung und Filterung.

- **Artikelnummer** – Der Artikel, der sich derzeit am Lagerplatz befindet. Wenn der Lagerplatz mehrere Artikel enthält, ist dieses Feld leer.
- **Datum und Uhrzeit der letzten Aktivität** – Der Zeitstempel der letzten Lagertransaktion, die für den Lagerplatz ausgeführt wurde.
- **Fälligkeitsdatum** – Das Datum, an dem der Bestand am Lagerplatz in den Lagerort gebracht wurde. Dieser Wert wird anhand des Fälligkeitsdatums des Kennzeichens berechnet. Er ist genau für Lagerplätze, die mit einem Kennzeichen versehen sind, aber möglicherweise nicht für Lagerplätze, die nicht mit einem Kennzeichen versehen sind.
- **Lagerplatzstatus** – Der Status des Lagerplatzes. Es gibt vier mögliche Werte:

    - **Unbestimmt** – Das Lagerplatzprofil kann den Status nicht nachverfolgen. Daher ist der aktuelle Status unbekannt.
    - **Leer** – Derzeit befindet sich kein Bestand am Lagerplatz.
    - **Kommissionierung** – Ausgehende Transaktionen wurden für den Lagerplatz ausgeführt, da er zuletzt leer war.
    - **Lager** – Nur eingehende Transaktionen wurden für den Lagerplatz ausgeführt, da der Lagerplatz zuletzt leer war.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Statusfunktion für den Lagerplatz an einem Lagerort aktivieren

Bevor Sie die Funktion für *Status für den Lagerplatz an einem Lagerort* verwenden können, muss sie in Ihrem System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Status für den Lagerplatz an einem Lagerort*

## <a name="set-up-warehouse-location-status"></a>Status für den Lagerplatz an einem Lagerort einrichten

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Beispieldaten vorbereiten, die für das Beispielszenario erforderlich sind

Bevor Sie mit der Bearbeitung des Szenarios beginnen, müssen Sie Beispieldaten aktivieren und die Funktion wie in diesem Abschnitt beschrieben einrichten. Um das Beispielszenario abzuschließen, müssen Sie entweder die Warehouse Management Mobile App oder den browserbasierten Emulator verwenden. Die hier bereitgestellten Schritte verwenden die Warehouse Management Mobile App. Die Schritte für den browserbasierten Emulator sind ähnlich.

#### <a name="use-the-usmf-legal-entity"></a>USMF juristische Person verwenden

Um das Beispielszenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

#### <a name="set-up-location-profiles"></a>Lagerplatzprofile einrichten

Für das Beispielszenario müssen Sie zwei Lagerplatzprofile vorbereiten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Klicken Sie auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Wählen Sie das Profil **BULK-06** aus.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Artikel an Lagerplatz aktivieren:** Legen Sie diese Option auf _Ja_ fest.
    - **Lagerplatzaktivitätsdatum und -uhrzeit aktivieren:** Legen Sie diese Option auf _Ja_ fest.
    - **Lagerplatzstatus aktivieren:** Legen Sie diese Option auf _Ja_ fest.

    Diese Optionen steuern, ob die Referenzfelder am Lagerplatz aktiv sind.

1. Wiederholen Sie die Schritte 3 bis 4 für das Profil **PICK-06**.

> [!NOTE]
> Wenn die Parameter auf dem Standortprofil (**Element vor Ort aktivieren**, **Standortaktivität aktivieren**, **Standortstatus aktivieren**) auf *Ja* eingestellt sind, aktualisiert das System sofort die relevanten Positionen, indem es die *Konsistenzprüfung des Lagerstandortstatus*-Aufgabe ausführt.

### <a name="scenario"></a>Szenario

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Bestellung erstellen** im Inforegister **Kreditor** im Feld **Kreditorenkonto** die Option *104* aus.
1. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Lagerort** die Option *61* aus.
1. Wählen Sie **OK**.
1. Ihre neue Bestellung (PO) wird geöffnet. Sie enthält eine leere Position im Raster **Bestellpositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** _A0002_
    - **Menge** _5_

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kauf** in der Gruppe **Aktivitäten** auf **Bestätigen**, um die Bestellung zu bestätigen.
1. Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufempfang**.
1. Wählen Sie das Feld **PONUM**, geben Sie die Bestellnummer ein, und bestätigen Sie.
1. Wählen Sie das Feld **ARTIKEL**, geben Sie *A0002* als Artikelnummer ein, und bestätigen Sie.
1. Geben Sie auf der Seite **MENGE** *5* als Menge ein, und bestätigen Sie.

    Sie können die Menge auf eine der folgenden Arten eingeben:

    - Wählen Sie das Pluszeichen (**+**) oder Minuszeichen (**–**) aus, um einen numerischen Wert zu addieren oder zu subtrahieren.
    - Wählen Sie das leere Feld zwischen dem Pluszeichen (**+**) und Minuszeichen (**–**) aus, um das Nummernpad zu öffnen.

1. Bestätigen Sie Ihre Auswahl der Artikelnummer *A0002* und eine Menge von *5*. Am unteren Rand der Seite wird die Meldung „Arbeit erledigt“ angezeigt.
1. Wählen Sie in der rechten oberen Ecke die Menüschaltfläche (manchmal auch als Hamburger oder Hamburgerschaltfläche bezeichnet) und dann **Abbrechen** aus, um **Kaufempfang** zu beenden und zurück zum Menü **Eingehend** zu gelangen.
1. Wählen Sie auf der Bestellseite die Option **Arbeitsdetails** über dem Raster **Bestellpositionen** aus.
1. Beachten Sie auf der Registerkarte **Allgemein** die Werte **Arbeits-ID** und **Zielkennzeichen-ID**, die erstellt wurden.
1. Beachten Sie im Abschnitt **Positionen** die Werte **Lagerplatz** für die Arbeitstypen *Entnahme* und *Einlagerung*.
1. Gehen Sie auf dem mobilen Gerät zu **Eingehend \> Kaufeinlagerung**.
1. Wählen Sie das Feld **ID**, geben Sie die Arbeits-ID ein, und bestätigen Sie.
1. Bestätigen Sie noch einmal, um den Eintrag *Entnahme* abzuschließen.
1. Wählen Sie die Menüschaltfläche in der rechten oberen Ecke und dann **Fertig** aus, um die Arbeit *Entnahme* abzuschließen.
1. Notieren Sie sich den Einlagerungslagerplatz, und bestätigen Sie. Am unteren Rand der Seite wird die Meldung „Arbeit erledigt“ angezeigt.
1. Wählen Sie die Menüschaltfläche in der rechten oberen Ecke und dann **Abbrechen** aus, um **Kaufeinlagerung** zu beenden und zurück zum Menü **Eingehend** zu gelangen.
1. Wählen Sie **Zurück**, um zum Hauptmenü zurückzukehren.
1. Wechseln Sie in Dynamics 365 Supply Chain Management zur **Lagerortverwaltung \> Setup \> Lagerort \> Lagerplätze**.
1. Filtern Sie in **Lagerplatz**, und geben Sie den Einlagerungslagerplatz aus der Bestellarbeit ein. Sie sollten die folgenden Ergebnisse sehen:

    - Die Spalte **Lagerplatzstatus** zeigt einen Wert von *Lager*, weil die letzte Transaktion gegen diesen Lagerplatz eine Einlagerung war.
    - Die Spalte **Artikelnummer** zeigt einen Wert von *A0002*, weil dieser Artikel empfangen und am Lagerplatz eingelagert wurde.
    - In der Spalte **Datum und Uhrzeit der letzten Aktivität** wird der Zeitstempel für das Datum und die Uhrzeit angezeigt, zu der die Arbeit am Lagerplatz abgeschlossen wurde.

1. Gehen Sie auf dem mobilen Gerät zu **Qualität \> Bewegung**.
1. Wählen Sie das Feld **LOC/LP** aus, und geben Sie den Lagerplatz ein, den Sie in den vorherigen Schritten notiert haben.
1. Bestätigen Sie die angezeigten Informationen. Notieren Sie sich die generierte Kennzeichennummer.
1. Wählen Sie auf dem Bildschirm **Zu Informationen** das Feld **LOC/LP** aus, und geben Sie *06A07R2S1B* als Lagerplatz ein, an dem der Artikel verschoben werden soll.
1. Bestätigen Sie auf dem Bildschirm **Zu Informationen** den Wert **LP** (die Zielkennzeichen-ID), der automatisch generiert wird. Am unteren Rand der Seite wird die Meldung „Arbeit erledigt“ angezeigt.
1. Wählen Sie die Menüschaltfläche in der rechten oberen Ecke und dann **Abbrechen** aus, um **Bewegung** zu beenden und zurück zum Menü **Qualitätsmanagement** zu gelangen.
1. Wählen Sie **Zurück**, um zum Hauptmenü zurückzukehren.
1. Wechseln Sie in Dynamics 365 Supply Chain Management zur **Lagerortverwaltung \> Setup \> Lagerort \> Lagerplätze**.
1. Aktualisieren Sie die Seite **Lagerplätze**, und zeigen Sie den ursprünglichen Einlagerungslagerplatz erneut an. Beachten Sie, dass das Feld **Lagerplatzstatus** jetzt auf *Leer* festgelegt ist, und die Spalte **Artikelnummer** ist leer.
1. Zeigen Sie den Datensatz für den Lagerplatz *06A07R2S1B* an, und beachten Sie, dass sich der Wert **Status** zu *Lager* geändert hat und die Felder **Artikelnummer** und **Datum und Uhrzeit der letzten Aktivität** aktualisiert wurden.
1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** *US-002* aus.
1. Im Feld **Lagerort** wählen Sie *61* aus.
1. Wählen Sie **OK**.
1. Ihr neuer Auftrag wird geöffnet. Er enthält eine leere Position im Raster **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** _A0002_
    - **Menge** _1_

1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Bestand** die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die Auftragsposition zu reservieren. Wählen Sie dann die Schaltfläche **Schließen** (**X**) in der rechten oberen Ecke aus, um die Seite zu schließen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Wählen Sie im Abschnitt **Auftragspositionen** im Menü **Lagerort** die Option **Arbeitsdetails** aus.
1. Kopieren Sie den Wert **Arbeits-ID**, der erstellt wurde.
1. Gehen Sie auf dem mobilen Gerät zu **Ausgehend \> Verkaufsauswahl**.
1. Wählen Sie das Feld **ID**, geben Sie die Arbeits-ID ein, die Sie zuvor kopiert haben, und bestätigen Sie.
1. Auf der Seite **Aufträge: Entnahme** schlägt das Feld **LOC** den Kommissionierort als den zuvor erstellten Einlagerungslagerplatz vor. Notieren Sie den Lagerplatz.
1. Wählen Sie das Feld **LOC**, geben Sie den Lagerplatz ein, und bestätigen Sie.
1. Wählen Sie das Feld **LP**, geben Sie in das Feld die Kennzeichennummer ein, die Sie während der Bewegungsaktivität notiert haben, und bestätigen Sie.
1. Wählen Sie das Feld **Artikel**, geben Sie *A0002* als Artikelnummer ein, und bestätigen Sie.
1. Geben Sie auf der Seite **MENGE** *1* als Menge ein, und bestätigen Sie.

    Sie können die Menge auf eine der folgenden Arten eingeben:

    - Wählen Sie das Pluszeichen (**+**) oder Minuszeichen (**–**) aus, um einen numerischen Wert zu addieren oder zu subtrahieren.
    - Wählen Sie das leere Feld zwischen dem Pluszeichen (**+**) und Minuszeichen (**–**) aus, um das Nummernpad zu öffnen.

1. Wählen Sie das Feld **ZIEL-LP**, geben Sie in das Feld eine benutzerdefinierte Zielkennzeichen-ID ein, und bestätigen Sie.
1. Bestätigen Sie noch einmal, um die Kommissionierarbeit abzuschließen. Am unteren Rand der Seite wird die Meldung „Arbeit erledigt“ angezeigt.
1. Wählen Sie die Menüschaltfläche in der rechten oberen Ecke und dann **Abbrechen** aus, um die Kommissionieraktivität abzuschließen und zurück zum Menü **Ausgehend** zu gelangen.
1. Wechseln Sie in Dynamics 365 Supply Chain Management zur **Lagerortverwaltung \> Setup \> Lagerort \> Lagerplätze**.
1. Filtern Sie in **Lagerplatz**, und geben Sie den Entnahmelagerplatz aus der Auftragsarbeit ein.
1. Beachten Sie, dass das Feld **Lagerplatzstatus** für den Lagerplatz, von dem die Auftragsarbeit entnommen wurde, jetzt auf *Entnahme* festgelegt ist und das Feld **Datum und Uhrzeit der letzten Aktivität** aktualisiert wurde.

> [!NOTE]
> Die Lagerplatzfelder werden nur durch Lagertransaktionen aktualisiert. Wenn Sie Bestand mithilfe einer Erfassung oder anderer Nicht-WHS-Prozesse verschieben, werden die Felder nicht aktualisiert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]