---
title: Abrechnungszeitplan – Übersicht
description: In diesem Thema wird erläutert, wie Sie Abrechnungszeitpläne erstellen, löschen und bearbeiten.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e42be3f359e96f0861354ebc8e1e9c87478a5d89
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182698"
---
# <a name="billing-schedule-overview"></a>Abrechnungszeitplan – Übersicht

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Auf der Seite **Abrechnungszeitplan** können Sie Abrechnungszeitpläne erstellen, löschen oder bearbeiten. Sie können auch die Liste der Abrechnungszeitpläne überprüfen. Wenn Sie einen Abrechnungszeitplan erstellen, hängen die Standardwerte dafür von der zugehörigen Abrechnungsgruppe ab. Weitere Informationen werden auf der Seite **Wiederkehrende Vertragsabrechnungsparameter** eingerichtet.

## <a name="create-a-billing-schedule"></a>Einen Abrechnungszeitplan erstellen

Gehen Sie folgendermaßen vor, um einen Abrechnungszeitplan zu erstellen.

1. Wählen Sie auf der Seite **Abrechnungszeitplan** die Option **Neu** aus.
2. Wählen Sie im Dialogfeld **Abrechnungszeitplan erstellen** im Feld **Abrechnungszeitplangruppe** eine Abrechnungszeitplangruppe aus.
3. Wählen Sie im Feld **Debitorenkonto** ein Debitorenkonto aus.
4. Wählen Sie im Feld **Startdatum** das Startdatum und dann im Feld **Anzahl der Zeiträume** Geben Sie im Feld die Anzahl der Zeiträume ein. Das Feld **Endtermin** wird basierend auf der Anzahl der Zeiträume aktualisiert, die Sie eingeben. Wenn Sie das Feld **Enddatum für Rechnungsstellung** aktualisieren, wird das Feld **Anzahl der Zeiträume** auf **0** (null) aktualisiert.
5. Wählen Sie **OK** aus.
6. Geben Sie auf der Seite **Abrechnungszeitplan** in der Registerkarte **Allgemein** im Feld **Beschreibung** eine Beschreibung des Abrechnungszeitplans ein.
7. Wählen Sie im Feld **Meilensteinvorlage** eine Meilensteinvorlage für die **Abrechnung nach Meilenstein** aus.

Felder wie **Rechnungskonto** und **Währungscode** werden mit Informationen des Debitoren aktualisiert.

Die Felder **Fakturierungsintervall** und **Abrechnungsintervall** werden basierend auf der ausgewählten Abrechnungszeitplangruppe automatisch festgelegt.

8. Um separate Rechnungen zu erstellen, setzen Sie die Option **Separat in Rechnung stellen** auf **Ja**.
9. Um einen Abrechnungszeitplan nach Ablauf des letzten Abrechnungszeitraums automatisch zu verlängern, legen Sie die Option **Automatisch verlängern** auf **Ja** und dann das Feld **Pro Verlängerung hinzuzufügende Zeilen** fest.

Die Felder **Parameter** werden je nach den Werten auf der Seite **Wiederkehrende Vertragsabrechnungsparameter** automatisch festgelegt.

10. Um den Betrag eines Abrechnungszeitplans aufzuteilen, legen Sie die Option **Anteilige Teilzeiträume** auf **Ja** fest.
11. Um die Detailpositionen des Abrechnungszeitplans am Monatsende auszurichten, legen Sie die Option **An Monat ausrichten** auf **Ja** fest.
12. Geben Sie in die Felder **Vertragsstartdatum** und **Vertragsenddatum** das Start- und Enddatum des Vertrags ein. Diese Daten dienen nur zur Information.

Das Feld **Zahlung** zeigt die Debitorenzahlungsinformationen des Kunden. Wenn eine Position ausgesetzt oder beendet wird, können die Zahlungsinformationen nicht geändert werden.

> [!NOTE]
> Wenn Sie Rechnungen nach Artikel konsolidieren, müssen die Werte der Felder **Zahlungsbedingungen**, **Methode** und **Abrechnungszeitplan** übereinstimmen. Sonst können die Rechnungen nicht konsolidiert werden.

13. Auf der Registerkarte **Adresse** können Sie die Felder **Lieferadresse** und **Rechnungsanschrift** überprüfen und aktualisieren.
14. Auf der Registerkarte **Kontaktinformationen** können Sie dem Abrechnungszeitplan ein Endbenutzerkonto zuordnen.
15. In den Feldern **Kontaktinformationen** können Sie einen Kontakt, eine E-Mail-Adresse und eine Internetadresse eingeben.
16. Um Partnerprovisionsinformationen nachzuverfolgen, legen Sie die Felder **Partnerkonto** und **Partnerprovisionssatz** fest. Diese Felder dienen nur zur Information.
17. Auf der Registerkarte **Gesamt** werden Sie die verschiedenen Summen angezeigt, die für den Abrechnungszeitplan berechnet wurden.
18. Auf der Registerkarte **Halten** können Sie Prüfinformationen darüber anzeigen, wann der Abrechnungszeitplan ausgesetzt wurde und wann die Sperre entfernt wurde.
19. Auf der Registerkarte **Beendigung** können Sie einen Verlauf der Beendigungen anzeigen, die auf den Abrechnungszeitplan angewendet oder daraus entfernt wurden.
20. Wählen Sie **Speichern** aus.
21. Wählen Sie im Inforegister **Abrechnungszeitplanpositionen** die Option **Position hinzufügen** aus.
22. Wählen Sie im Feld **Artikelnummer** die Artikelnummer ein. Wenn der hinzugefügte Artikel ein übergeordneter Artikel in einer Umsatzerlösaufteilung ist, werden die Zeilen automatisch mit den untergeordneten Artikeln aktualisiert. Sie können nur den übergeordneten Artikel in einer Umsatzerlösaufteilung bearbeiten. Alle untergeordneten Artikel werden dann entsprechend aktualisiert.
23. Wählen Sie im Feld **Artikeltyp** den Artikeltyp aus.
24. Aktualisieren Sie das Start- und das Enddatum.
25. Bevor die Rechnungen erstellt werden, können Sie das Fakturierungsintervall ändern, indem Sie das Feld **Fakturierungsintervall** aktualisieren. Nachdem die erste Rechnung für den Abrechnungszeitplan erstellt wurde, kann das Fakturierungsintervall nicht mehr geändert werden.
26. Wählen Sie im Feld **Einheit** die Maßeinheit für den Artikel aus.
27. Wählen Sie im Feld **Preisberechnungsmethode** die Preisberechnungsmethode für den Artikel aus.

Das Feld **Einzelpreis** wird automatisch dem Bestand entnommen. Sie können ihn jedoch aktualisieren, wenn Sie die Preisgestaltungsmethode auf **Pauschal** ändern.

## <a name="remove-a-line-item"></a>Eine Position entfernen

Gehen Sie folgendermaßen vor, um einen Artikel aus einem Abrechnungszeitplan zu entfernen.

1. Wählen Sie auf der Seite **Abrechnungszeitplan** im Feld **Zeitplannummer** die Nummer des zu bearbeitenden Abrechnungszeitplans aus.
2. Wählen Sie im Inforegister **Abrechnungszeitplanpositionen** die zu löschende Position aus, und wählen Sie dann **Entfernen** aus.
3. Wählen Sie **Speichern** aus.

Der Rest dieses Themas beschreibt die Aktionen und Details, die für Positionen im Inforegister **Abrechnungszeitplanpositionen** verfügbar sind.

## <a name="billing-schedule-line-actions"></a>Aktionen für Abrechnungszeitplanpositionen

Die Schaltflächen des Inforegisters **Abrechnungszeitplanpositionen** Sie Aktionen auf einzelne Positionen anwenden.

| Schaltfläche | Description |
|--------|-------------|
| Position hinzufügen | Fügt dem Abrechnungszeitplan eine neue Position hinzu. |
| Aus Artikelliste hinzufügen | Fügen Sie einem Abrechnungszeitplan mehrere Artikel hinzu, indem Sie sie in einer Liste auswählen. |
| Entfernen | <p>Entfernen Sie die ausgewählte Position aus dem Abrechnungszeitplan.</p><p>Bei Artikeln, die Teil einer Umsatzerlösaufteilung sind, können Sie nur den übergeordneten Artikel entfernen. Alle zugehörigen untergeordneten Artikel werden dann automatisch entfernt.</p> |
| Abrechnungsdetail anzeigen | Lassen Sie sich die Abrechnungsdetails anzeigen. |
| Kündigen | <p>Beenden Sie die ausgewählten Positionen. Diese Schaltfläche ist nur verfügbar, wenn die ausgewählten Positionen den Status **Aktiv** haben.</p><p>Bei Artikeln, die Teil einer Umsatzerlösaufteilung sind, können Sie nur den übergeordneten Artikel beenden.</p> |
| Kündigung entfernen | <p>Entfernen Sie Beendigung aus den ausgewählten Positionen. Diese Schaltfläche ist nur verfügbar, wenn die ausgewählten Positionen den Status **Beendet** haben.</p><p>Bei Artikeln, die Teil einer Umsatzerlösaufteilung sind, können Sie nur die Beendigung des übergeordneten Artikels entfernen.</p> |
| Sperre platzieren | <p>Wählen Sie die Details aus, um die ausgewählte Position zu sperren.</p><p>Bei Artikeln, die Teil einer Umsatzerlösaufteilung sind, können Sie nur den übergeordneten Artikel sperren.</p> |
| Sperre entfernen | <p>Entfernen Sie die Sperre der ausgewählten Position.</p><p>Bei Artikeln, die Teil einer Umsatzerlösaufteilung sind, können Sie nur die Sperre des übergeordneten Artikels entfernen.</p> |
| Eskalation und Rabatt | Diese Schaltfläche ist für Artikel, die Teil einer Umsatzerlösaufteilung sind, nicht verfügbar. Davon ausgenommen sind übergeordnete Artikel, bei denen die Umsatzerlösaufteilung die Zuweisungsmethode **Ohne Betrag** nutzt. |
| Stundungen | <p>Geben Sie Stundungsoptionen für die ausgewählte Position ein.</p><p>Diese Schaltfläche ist für übergeordnete Artikel in einer Umsatzerlösaufteilung nicht verfügbar.</p> |
| Meilensteinzuteilung | <p>Überprüfen und aktualisieren Sie die Informationen zur Meilensteinzuteilung für die ausgewählte Position.</p><p>Diese Schaltfläche ist nur verfügbar, wenn es sich bei der Position des Abrechnungszeitplans um eine Meilensteinposition handelt.</p> |
| Support und Verlängerung | <p>Überprüfen und aktualisieren Sie die Support- und Verlängerungsinformationen für die ausgewählte Position.</p><p>Diese Schaltfläche ist nur verfügbar, wenn es sich bei der Position des Abrechnungszeitplans um eine Support- oder Verlängerungsposition handelt.</p> |
| Dimensionen anzeigen | Blenden Sie die Dimensionsspalten ein oder aus, die im Raster **Abrechnungszeitplanpositionen** angezeigt werden sollen. |
| Einzelpreis berechnen | <p>Berechnen Sie den Stückpreis des Artikels, damit der Debitor die Vertragssumme in Raten zahlen kann (z. B. täglich, monatlich, vierteljährlich, halbjährlich oder jährlich). Sie können den Vertragspreis und die Preishäufigkeit auswählen.</p><p>Sie können einen Überwachungspfad für die Änderungen anzeigen lassen: Preis und Häufigkeit des alten Vertrags, Preis und Häufigkeit des neuen Vertrags, der Benutzer, der die Änderung vorgenommen hat, sowie Datum und Uhrzeit der Änderung.</p> |
| Ausrichtungsdatum | <p>Geben Sie das Ausrichtungsdatum für Verlängerungsartikel an.</p><p>Wenn Sie eine Artikelgruppe im Feld **Artikelgruppe** auswählen, verwenden alle Artikel das Ausrichtungsdatum des ersten Artikels in der Artikelgruppe im Abrechnungszeitplan. Wenn das Feld **Artikelgruppe** leer ist, können Sie ein Ausrichtungsdatum angeben, das für alle Artikel verwendet werden soll.</p><p>Diese Schaltfläche ist nur verfügbar, wenn das Feld **Fakturierungsintervall** auf **Jährlich** gesetzt wird.</p> |
| Nicht abgerechneter Umsatzerlös | <p>Richten Sie den Artikel so ein, dass er die Funktion für nicht abgerechnete Umsatzerlöse verwendet. Anschließend können Sie die Konten für nicht abgerechnete Umsatzerlöse und nicht abgerechnete Rabatte für den Artikel angeben.</p><p>Diese Schaltfläche ist nur für Artikel verfügbar, bei denen das Feld **Artikeltyp** auf **Standard** festgelegt ist. Sie steht nicht für vorhandene Abrechnungszeitpläne oder Abrechnungszeitplanpositionen zur Verfügung, für die die Rechnung bereits erstellt wurde.</p> |
| Untergeordnete Umsatzerlösaufteilung hinzufügen | <p>Wählen Sie den untergeordneten Artikel aus, der zum Verkaufsauftrag hinzugefügt wird.</p><p>Diese Schaltfläche ist nur für übergeordnete Artikel in einer Umsatzerlösaufteilung verfügbar.</p> |
| Optionen zur erweiterten Preisgestaltung | Bearbeiten Sie die Optionen zur Preisgestaltung für einen Artikel. |

## <a name="billing-schedule-line-details"></a>Details für Abrechnungszeitplanpositionen

Wenn Sie eine Position im Inforegister **Abrechnungszeitplanpositionen** auswählen, können Sie spezifische Details für diese Position anzeigen lassen. Diese Details sind auf verschiedene Registerkarten verteilt.

### <a name="general-tab"></a>Registerkarte „Allgemeines“

Die folgenden Informationen finden Sie auf der Registerkarte **Allgemein**.

| Feld oder Abschnitt | Description |
|------------------|-------------|
| Verwendung | <p>Dieser Abschnitt enthält Informationen über Verbrauchsartikel: Er enthält die folgenden Felder:</p><ul><li>**Verbrauchsbezeichner**: Der Bezeichner der Verbrauchseinheit oder des Verbrauchsartikels.</li><li>**Leseoption**: Die Nutzungsleseoption: **Lesen** oder **Verbrauch**.</li><li>**Geschätzter Verbrauch**: Geben Sie den geschätzten Verbrauch für einen Verbrauchsartikel mit Zeiträumen an, in denen die Rechnung nicht erstellt wurde. Auf der Seite **Rechnungsdetails** können Sie die Rechnungsdetailpositionen für den geschätzten Verbrauch überprüfen.</li></ul> |
| Externe Referenzen\* | Dieser Abschnitt enthält die Felder **Extern** und **Positionsnummer**, in denen Sie externe Referenzinformationen angeben können. |
| Meilenstein | <p>Dieser Abschnitt enthält Informationen über Meilensteinartikel: Er enthält die Feld **Voraussichtliches Abschlussdatum**, das das Fertigstellungsdatum des Artikels anzeigt.</li></ul> |
| Text | Ein Kommentar zur Position. Der Text wird in die Standardsprache des Kunden oder der juristischen Person übersetzt. |
| Artikelgruppe | Die Artikelgruppe der Position. |
| Ausrichtungsdatum | Das Ausrichtungsdatum für den Abrechnungszeitplan. |

\* Wenn Sie Rechnungen nach Artikel auf der Seite **Rechnung erstellen** konsolidieren, müssen die Felder **Externe Referenz** übereinstimmen. Wenn auch nur ein Zeichen anders ist, werden die Artikel nicht auf der Rechnung konsolidiert. Für keines der Felder im Abschnitt **Externe Referenz** werden Validierungsprüfungen durchgeführt und der Wert im Feld **Positionsnummer** muss ein positives Integer sein.

### <a name="address-tab"></a>Registerkarte „Adresse“

Die folgenden Informationen finden Sie auf der Registerkarte **Adresse**.

| Feld | Description |
|-------|-------------|
| Lieferadresse | <p>Wählen Sie die Lieferadresse für die Position aus. Die Standardlieferadresse ist die primäre Lieferadresse aus dem Inforegister **Adresse**.</p><p>Wenn Sie die Adresse ändern, können Sie die folgenden Adressoptionen auswählen:</p><ul><li>**Adressen**: Wählen Sie eine Adresse für den aktuellen Kunden aus.</li><li>**Verwendet**: Wählen Sie eine Adresse aus, die derzeit für den aktuellen Kunden verwendet wird.</li><li>**Andere Adresse**: Wählen Sie eine Adresse für einen beliebigen Kundendatensatz aus.</li></ul><p>Bei Artikeln mit Umsatzerlösaufteilung kann nur die Adresse des übergeordneten Artikels bearbeitet werden. Die Adresse für die untergeordneten Artikel stimmt mit der Adresse für den übergeordnete Artikel überein und kann nicht separat bearbeitet werden.</p> |
| Rechnungsadresse | <p>Wählen Sie die Rechnungsadresse für die Position aus. Die Standardlieferadresse ist die primäre Lieferadresse aus dem Inforegister **Adresse**. Sie können die Adresse je nach Verwendungszweck der verfügbaren Adressen beliebig ändern:</p><ul><li>Wenn keine der Adressen den Zweck **Rechnung** hat, ist die Standardrechnungsadresse unabhängig vom Verwendungszweck die primäre Adresse für den Kunden.</li><li>Wenn eine oder mehrere der Adressen den Zweck **Rechnung** haben, ist die Standardrechnungsadresse die zuletzt eingegebene Adresse.</li><li>Wenn eine oder mehrere der Adressen den Zweck **Rechnung** haben und eine der Rechnungsadressen als primäre Adresse festgelegt ist, ist die Standardrechnungsadresse die Adresse, die den Zweck **Rechnung** hat und wird als primäre Adresse festgelegt.</li><li>Bei Artikeln mit Umsatzerlösaufteilung kann nur die Adresse des übergeordneten Artikels bearbeitet werden. Die Adresse für die untergeordneten Artikel stimmt mit der Adresse für den übergeordnete Artikel überein und kann nicht separat bearbeitet werden.</li></ul> |

### <a name="product-tab"></a>Registerkarte „Produkt“

Die folgenden Informationen finden Sie auf der Registerkarte **Produkt**.

| Feld oder Abschnitt | Description |
|------------------|-------------|
| Lagerdimensionen | <p>Dieser Abschnitt zeigt die Speicherinformationen für den Artikel an. Er enthält das Feld **Seriennummer**, das die Seriennummer des Artikels anzeigt.</p><p>Die Seriennummer wird während des Support- und Verlängerungsprozesses aus dem ursprünglichen Verkaufsauftrag kopiert. Bei Artikeln mit Umsatzerlösaufteilung wird die Seriennummer des übergeordneten Artikels auf alle untergeordneten Artikel kopiert. Die Seriennummer wird kopiert, wenn die Option **Seriennummer kopieren** auf **Ja** auf der Seite **Wiederkehrende Vertragsabrechnungsparameter** eingestellt ist.</li></ul> |
| Produktdimensionen | Die Produktdetails für den Artikel und die Werte werden basierend auf dem Wert **Variantennummer** automatisch aktualisiert, der für die Abrechnungszeitplanposition ausgewählt wird. |

### <a name="account-tab"></a>Registerkarte Konto

Die folgenden Informationen finden Sie auf der Registerkarte **Konto**.

| Feld | Description |
|-------|-------------|
| Hauptkonto | Das Hauptkonto, das in der Verkaufsposition erstellt wird. Der Standardwert stammt aus dem Verkaufsauftrag. Dieses Feld kann leer sein. |
| Artikelfinanzdimensionen | <p>Die Werte der Standardfinanzdimensionen, basierend auf dem Kunden- und Artikeldatensatz.</p><p>Bei Artikeln mit Umsatzerlösaufteilung verwenden die untergeordneten Artikel die Finanzdimensionswerte der Kunden- und Artikeldatensätze, wie zuvor beschrieben. Wenn Sie die Finanzdimensionswerte von untergeordneten Artikeln aktualisieren müssen, können Sie die Datenentität importieren.</p> |

### <a name="renewals-tab"></a>Registerkarte „Verlängerungen“

Die folgenden Informationen finden Sie auf der Registerkarte **Verlängerungen**.

| Feld | Description |
|-------|-------------|
| Automatisch verlängern | <p>Ein Wert, der angibt, ob die Abrechnungszeitplanposition automatisch in den nächsten Abrechnungszeitraum verlängert wird:</p><ul><li>**Ja**: Die Abrechnungszeitplanposition wird automatisch in den nächsten Abrechnungszeitraum verlängert, wenn Sie eine Rechnung erstellen:</li><li>**Nein**: Die Abrechnungszeitplanposition wird nicht automatisch verlängert. Sie müssen den Abrechnungszeitplan manuell verlängern.</li></ul> |
| Pro Verlängerung hinzuzufügende Positionen | Die Anzahl der Positionen, die einer Verlängerung des Abrechnungszeitplans hinzugefügt werden sollen. |

Zusätzlich sind die folgenden Schaltflächen auf dem Inforegister **Verlängerungen** verfügbar.

| Schaltfläche | Description |
|--------|-------------|
| Prüfung von Erfassungseinträgen für nicht fakturierte Umsätze | Zeigen Sie alle Änderungen für Artikel an, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden. |
| Verlängerungszeitraum hinzufügen | Fügen Sie einen Verlängerungszeitraum für den Artikel hinzu. Das Startdatum des neuen Verlängerungszeitraums ist das nächste Datum nach dem Enddatum der vorherigen Laufzeit. Die Felder **Verlängerungsenddatum**, **Stundungsstartdatum**, **Stundungsenddatum**, **Artikelmenge** und **Preis je Einheit** können aktualisiert werden. |
| Verlängerungszeitraum ändern | <p>Ändern Sie einen Verlängerungszeitraum. Für den anfängliche Zeitraum können Sie das Stundungsstartdatum und -enddatum ändern, bevor der anfängliche Journaleintrag erstellt wird. Für nachfolgende Zeiträume kann das Startdatum nicht geändert werden. Es ist immer das nächste Datum nach dem Ende des vorangegangenen Zeitraums.</p><p>Wenn nach dem Zeitraum, den Sie ändern, ein Verlängerungszeitraum besteht, können die Daten des Zeitraums nicht geändert werden. In diesem Fall können die Felder **Menge** und **Preis je Einheit** für den Verlängerungsartikel aktualisiert werden.</p><p>Nehmen wir ein Beispiel mit drei Zeiträumen. <ul><li>Der erste Zeitraum kann nicht geändert werden, da er bereits begonnen hat.</li><li>Für den zweiten Zeitraum können nur die Menge und der Preis je Einheit geändert werden.</li><li>Beim dritten Zeitraum können alle Werte außer dem Startdatum geändert werden. Des Weiteren können Sie über die Option **Zeitplan aus Vorlage** einen Stundungszeitplan erstellen, der auf der Vorlage für den Artikel mit nicht abgerechnetem Umsatzerlös basiert. Wenn diese Option auf **Ja** eingestellt ist, wählen Sie die Stundungsvorlage im Feld **Vorlage** aus und ändern Sie das Stundungsstartdatum und -enddatum nach Bedarf. Nachfolgende Verlängerungszeiträume verwenden dieselbe Stundungsvorlage. Die Stundungsvorlage kann jedoch geändert werden.</p></li></ul> |

### <a name="termination-tab"></a>Registerkarte „Beendigung“

Die folgenden Informationen finden Sie auf der Registerkarte **Beendigung**.

| Feld | Description |
|-------|-------------|
| Kündigungsdatum | Das Datum, an dem die Abrechnungszeitplanposition beendet wird. Der Standardwert stammt aus dem Feld **Beendigungsdatum** in der Kopfzeile. Sie den Wert in diesem Feld nach Bedarf ändern. |
| Kündigungstyp | Der Typ der Beendigung. Der Standardwert stammt aus dem Feld **Beendigungstyp** in der Kopfzeile. |

### <a name="hold-tab"></a>Registerkarte „Sperre“

Wenn Umsatzerlös- und Ausgabenstundungen verwendet werden, zeigt die Registerkarte **Sperre** das Stundungsdatum.

### <a name="escalation-and-discount-tab"></a>Registerkarte „Eskalation und Rabatt“

Die folgenden Informationen finden Sie auf der Registerkarte **Eskalation und Rabatt**.

| Feld | Description |
|-------|-------------|
| Eskalation | <p>Wählen Sie aus, ob Eskalationen für die Abrechnungszeitplanposition zulässig sind. Jede beliebige Eskalationsposition aus der Kopfzeile wird angewendet, wenn die Abrechnungszeitplanposition erstellt wird.</p><ul><li>**Ja**: Eskalationen können auf die Position angewendet werden. Wenn diese Option ausgewählt ist, können Sie die Eskalationen für die Abrechnungszeitplanpositionen auf der Seite **Eskalation und Rabatt** einrichten.</li><li>**Nein**: Eskalationen können nicht auf die Position angewendet werden.</li></ul><p>Die Standardeinstellung basiert auf der ausgewählten **Abrechnungszeitplangruppe**.</p> |

### <a name="price-changes-tab"></a>Registerkarte „Preisänderungen“

Für Positionen, die von **Standardpreis** auf **Pauschalpreis** geändert werden, enthält das Raster in der Registerkarte **Preisänderungen** die folgenden Spalten:

- Änderungsdatum
- Vom Benutzer geändert
- Standardpreis
- Pauschalpreis
- Preis aktualisieren
