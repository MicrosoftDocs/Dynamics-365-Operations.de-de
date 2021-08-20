---
title: Arbeitspositionsdetails
description: Dieses Thema enthält Informationen zur Seite „Arbeitspositionsdetails“, auf der eine umfassende, sortierbare und filterbare Liste der einzelnen Arbeitspositionen in Ihrem System angezeigt wird.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 34325d2a2d87a4bb84acae53211db36468b7432a016eb24c0473358a40415426
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753770"
---
# <a name="work-line-details"></a>Arbeitspositionsdetails

[!include [banner](../includes/banner.md)]

Die Seite **Arbeitspositionsdetails** zeigt eine umfassende, sortierbare und filterbare Liste der einzelnen Arbeitspositionen in Ihrem System an. Sie bietet einen vollständigen Überblick über die Arbeiten, die im Lagerort geplant und ausgeführt werden. Sie können problemlos zwischen der Anzeige aller Arbeitspositionen und der Anzeige nur offener Arbeitspositionen wechseln. Zu den Details, die für jede Position angegeben werden, gehören der Arbeitsstatus, die Artikelnummer, der Lagerplatz, die Arbeitsmenge, die Ladungs-ID und die Lieferungs-ID.

## <a name="turn-on-the-work-line-details-feature"></a>Funktion für Arbeitspositionsdetails aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Arbeitspositionsdetails*

## <a name="open-and-use-the-work-line-details-page"></a>Seite „Arbeitspositionsdetails“ öffnen und verwenden

Um die Liste der Arbeitspositionsdetails anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitspositionsdetails**. Von hier aus können Sie folgende Aktivitäten ausführen:

- Verwenden Sie das Feld **Filter**, um nach Positionen zu suchen, die einen bestimmten Wert für einen verfügbaren Parameter haben. (Zu den verfügbaren Parametern gehören viele Parameter, die nicht als Spalten im Raster angezeigt werden.)
- Verwenden Sie das Kontrollkästchen **Geschlossene anzeigen** zum Ein- oder Ausblenden geschlossener Positionen.
- Wählen Sie **Dimensionen anzeigen** aus, um das Dialogfeld **Dimensionsanzeige** zu öffnen, in dem Sie verschiedene Dimensionsspalten im Raster ein- oder ausblenden können.
- Wählen Sie eine beliebige Spaltenüberschrift aus, um ein Menü zu öffnen, in dem Sie die Liste nach Werten in dieser Spalte sortieren oder filtern können.
- Wählen Sie eine Arbeitsposition und dann **Lagerplatz wechseln** aus, um ein Dialogfeld zu öffnen, in dem Sie den Lagerplatz für diese Arbeitsposition ändern können. Der von Ihnen angegebene Lagerplatz überschreibt das Setup der Lagerplatzrichtlinie.
- Wählen Sie eine Arbeitsposition und dann **Arbeitsposition stornieren** aus, um ein Dialogfeld zu öffnen, in dem Sie die Menge dieser Arbeitsposition teilweise oder vollständig reduzieren können.
- Passen Sie die Mengen an.
- Zeigen Sie die Transaktionen hinter einer Arbeitsposition an.

## <a name="try-out-the-feature"></a>Funktion ausprobieren

Dieser Abschnitt enthält eine dreiteilige Demo, die zeigt, wie Sie mit Arbeitspositionsdetails arbeiten.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um diese Demo mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können diese Demo auch als Anleitung nutzen, wenn Sie an einem Produktionssystem arbeiten. Sie müssen jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Überprüfen, ob Szenario-Setup genügend verfügbaren Bestand umfasst

Wenn Sie mit den **USMF**-Demodaten arbeiten, sollten Sie zunächst sicherstellen, dass Ihr System so eingerichtet ist, dass an jedem relevanten Entnahmeplatz genügend Bestand verfügbar ist. Für diese Demo wird erwartet, dass folgender Bestand verfügbar ist:

- **Artikel M9200:** 45 EA. (oder mehr)
- **Artikel M9202:** 10 EA. (oder mehr)

Befolgen Sie diese Schritte, um sicherzustellen, dass genügend Bestand verfügbar ist, und um die erforderlichen Anpassungen vorzunehmen.

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Lagerplatzrichtlinien**, und bestimmen Sie, welche Kommissionierorte für die Auftragskommissionierarbeit im Lagerort 51 verwendet werden. (Weitere Informationen finden Sie unter [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](control-warehouse-location-directives.md).)
1. Überprüfen Sie die Lagerbestände an den entsprechenden Lagerplätzen.
1. Passen Sie den Bestand nach Bedarf an. Die können manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow anwenden, um den Bestand anzupassen.

### <a name="part-1-create-picking-work"></a>Teil 1: Entnahmearbeit erstellen

Stellen Sie vor dem Erstellen von Arbeiten sicher, dass Ihr Lagerort so eingerichtet ist, dass es auf Arbeitsanforderungen in der erwarteten Weise reagiert.

Befolgen Sie diese Schritte, um einige Kommissionierarbeiten zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um das Dialogfeld **Auftrag erstellen** zu öffnen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf _US-001_ fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf _51_ fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Ihr neuer Auftrag wird geöffnet. Er enthält eine neue leere Zeile im Raster **Auftragspositionen**. Stellen Sie die folgenden Werte für diese Bestellposition ein:

    - **Artikelnummer:** _M9200_
    - **Menge** _20_
    - **Einheit:** _ea_

1. Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** auf **Reservierung**, um die Seite **Reservierung** zu öffnen.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**. Das System erstellt eine Sendung, fügt sie einer neuen Ladung hinzu und erstellt die erforderliche Arbeit.
1. Erstellen Sie einen zweiten Auftrag für dasselbe Kundenkonto und den Lagerort, die Sie für den ersten Auftrag verwendet haben. Fügen Sie dieser Bestellung die folgenden zwei Bestellpositionen hinzu:

    - **Position 1:** Legen Sie das Feld **Artikelnummer** auf _M9200_, das Feld **Menge** auf _25_ und das Feld **Einheit** auf _EA_ fest.
    - **Position 2:** Legen Sie das Feld **Artikelnummer** auf _M9202_, das Feld **Menge** auf _10_ und das Feld **Einheit** auf _EA_ fest.

1. Wiederholen Sie die Schritte 6 bis 8, um den Bestand für jede Bestellposition (einzeln) zu reservieren, und wiederholen Sie dann Schritt 9, um die Bestellung für den Lagerort freizugeben.

### <a name="part-2-change-the-location-for-a-work-line"></a>Teil 2: Lagerplatz für eine Arbeitsposition ändern

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitspositionsdetails**.
1. Suchen Sie eine der Arbeitspositionen, die Sie für diese Demo erstellt haben, und wählen Sie sie aus.
1. Wählen Sie **Lagerplatz ändern** aus, um das Dialogfeld **Neuen Lagerplatz auswählen** zu öffnen.
1. Wählen Sie im Dialogfeld **Neuen Lagerplatz auswählen** im Feld **Lagerplatz** einen neuen Lagerplatz für die Arbeitsposition aus.
1. Wählen Sie **OK** aus, um Ihre Änderung zu übernehmen und das Dialogfeld zu schließen.

> [!IMPORTANT]
> Sie können Lagerplatzänderungen nur einreichen, wenn für den neuen Lagerplatz genügend Bestand verfügbar ist (für eine Entnahme) oder wenn die Lagerplatztypüberprüfung (für eine Einlagerung) bestanden wurde.

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Teil 3: Menge der Arbeitsposition ändern oder eine Arbeitsposition stornieren

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitspositionsdetails**.
1. Suchen Sie eine der Arbeitspositionen, die Sie für diese Demo erstellt haben, und wählen Sie sie aus. Beachten Sie, dass Sie Mengen nur für Arbeitspositionen stornieren oder ändern können, in denen der Arbeitstyp _Entnahme_ ist.
1. Wählen Sie **Arbeitsposition stornieren** aus, um das Dialogfeld **Zu stornierende Menge** zu öffnen.
1. Ändern Sie im Dialogfeld **Zu stornierende Menge** den Wert im Feld **Menge**, um die Menge anzugeben, die von der Menge *subtrahiert* werden soll, die aktuell für die Position angegeben ist. Standardmäßig wird im Feld **Menge** die vollständige Menge angezeigt.

    - Wenn Sie die vollständige Menge stornieren, wird der Wert **Arbeitsstatus** zu _Storniert_ geändert, aber das Feld **Arbeitsmenge** zeigt weiterhin den ursprünglichen Wert.
    - Wenn Sie nur einen Teil der Menge stornieren, wird das Feld **Arbeitsmenge** aktualisiert, um den neuen Wert anzuzeigen, aber der Wert **Arbeitsstatus** wird nicht geändert.

1. Wählen Sie **OK** aus, um Ihre Änderung zu übernehmen und das Dialogfeld zu schließen.

> [!IMPORTANT]
> Wenn Sie nur einen Teil der Menge für eine Arbeitsposition stornieren, müssen Sie auch die veraltete Menge aus der Ladungsposition entfernen. Andernfalls kann die Ladungsposition nicht per Schiff bestätigt werden, es sei denn, die Unterlieferung ist korrekt eingerichtet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]