---
title: Stundungsbuchungen in der Abonnementabrechnung
description: In diesem Thema werden die verschiedenen Transaktionen beschrieben, die in Stundungsbuchungen als Teil von Umsatzerlös- und Ausgabenstundungen in der Abonnementabrechnung verwendet werden können.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2022
ms.locfileid: "8558106"
---
# <a name="deferral-default-transactions"></a>Stundungsstandardbuchungen

In diesem Thema werden die Buchungen beschrieben, die Umsatzerlös- und Ausgabenstundungen erlauben. Stundungszeitpläne basieren immer auf einem Ursprungsbeleg oder Abrechnungszeitplan und sind auch davon abhängig. Stundungszeitpläne werden basierend auf Standardwerten erstellt und können nicht separat eingegeben oder erstellt werden.

## <a name="sales-order-transaction-deferral"></a>Stundung einer Auftragstransaktion

Verwenden Sie die Seite **Stundungen** oder **Gutschrift erstellen**, um die Stundungsparameter für eine Auftragsposition einzugeben oder zu bearbeiten.

> [!NOTE]
> Wenn ein Auftrag aus einem Abrechnungszeitplan erstellt wird, sind alle Werte auf der Seite **Stundungen** oder **Gutschrift erstellen** schreibgeschützt und die Stundungsparameter können nicht bearbeitet werden. Um die Werte zu bearbeiten, verwenden Sie die Seite **Zeitplan ändern**.

### <a name="edit-deferral-options"></a>Stundungsoptionen bearbeiten

Gehen Sie wie folgt vor, um die Stundungsoptionen für eine Position zu bearbeiten.

1. Erstellen Sie eine Auftragsbuchung.
2. Wählen Sie die Position und dann **Stundungen** aus.
3. Auf der Seite **Transaktionsstundung** muss die Option **Verzögert** auf **Ja** festgelegt sein. Bearbeiten Sie die anderen Felder je nach Bedarf.
4. Wählen Sie **Vorschau** aus, um den Stundungszeitplan in der Vorschau anzuzeigen.
5. Wenn Sie Änderungen an der Transaktionsstundung vorgenommen haben, wählen Sie **OK** aus, und kehren Sie zur Transaktionsseite zurück.
6. Committen und buchen Sie die Transaktion.

Nachdem die Transaktion gebucht wurde, öffnen Sie die Seite **Alle Stundungszeitpläne**, um den Stundungszeitplan anzuzeigen.

### <a name="create-a-credit-note"></a>Erstellen einer Gutschrift

Gehen Sie folgendermaßen vor, um eine Gutschrift zu erstellen:

1. Erstellen Sie eine Auftragsbuchung.
2. Wählen Sie im Bereich **Auftragspositionen** den Artikel aus, für den Sie eine Gutschrift erstellen möchten.
3. Wählen Sie **Auftragsposition** \> **Neu** und dann **Gutschrift** aus.
4. Wählen Sie **Stundungen** aus.
5. Legen Sie auf der Seite **Stundung der Auftragstransaktion** die Option **Vorhandenen Zeitplan anpassen** für den Artikel auf **Ja** fest.
6. Wählen Sie im Feld **Angepasster Zeitplan** den Stundungszeitplan aus, auf den Sie die Gutschrift anwenden möchten.
7. Aktualisieren Sie die Felder **Datum neu berechnen** und **Endtermin** je nach Bedarf.
8. Wählen Sie **OK** aus.
9. Schließen Sie die Buchung der Auftragstransaktion ab.

### <a name="purchase-orders-and-purchase-invoices"></a>Bestellungen und Einkaufsrechnungen

Wenn Sie die Stundungsfunktion für eine Bestellung nutzen möchten, erstellen Sie zuerst die Rechnung. Verwenden Sie dann die Seite **Ausstehende Kreditorenrechnungen** zum Bearbeiten oder Hinzufügen von Stundungspositionen. Sie können Stundungen nicht direkt in einer Bestellung bearbeiten oder hinzufügen.

1. Verwenden Sie die Seite **Ausstehende Kreditorenrechnungen**, um eine Kreditorenrechnung einzugeben.

    Wenn Sie eine Position eingeben, wird die Stundung automatisch für den ausgewählten Artikel oder die ausgewählte Beschaffungskategorie eingerichtet. Diese Stundung basiert auf der Stundungseinrichtung auf der Seite **Standardstundungseinstellungen**. Die Stundungen können auf Verteilungsebene bearbeitet oder hinzugefügt werden.

3. Wählen Sie in der Einkaufszeile **Finanzdaten \> Beträge verteilen** aus.
4. Wählen Sie für jeden Verteilungsbetrag **Stundungen** aus. Beim Buchen der Rechnung wird für jede Verteilung, für die eine Stundung festgelegt wurde, ein Stundungszeitplan erstellt.

### <a name="tax"></a>Steuern

In einigen Fällen kann es sein, dass der Steuerbetrag ganz oder teilweise nicht erstattungsfähig sein. Wenn der Steuerbetrag einer stundbaren Position einen nicht erstattungsfähigen Betrag enthält, wird der nicht erstattungsfähige Steuerbetrag beim Buchen der Rechnung in den stundbaren Zeitplanbetrag aufgenommen.

### <a name="variance"></a>Abweichung

Wenn der Betrag in der Kreditorenrechnungsposition von dem Betrag der Bestellposition abweicht, werden Abweichungsverteilungen erstellt. Wenn die Position gestundet wird, wird das Sachkonto für diese Verteilungen auf das Stundungskonto festgelegt, und die Beträge werden beim Buchen der Rechnung in den stundbaren Zeitplanbetrag aufgenommen. Diese Verteilungen werden als **Preisabweichung** und **Kostenabweichung** bezeichnet.

### <a name="general-journals-and-invoice-journals"></a>Allgemeine Erfassungen und Rechnungserfassungen

Verwenden Sie die Seite **Stundungen** zur Eingabe der Stundungsparameter für eine Erfassungsbelegzeile. Sie können den Stundungszeitplan für lineare Stundungen in einer Vorschau anzeigen. Wenn Sie eine Position eingeben, wird die Stundung automatisch basierend auf der Einrichtung der Stundungskonten auf der Seite **Standardstundungseinstellungen** eingerichtet. Die Stundungsoptionen können für die einzelnen Positionen manuell geändert werden. Wenn der Erfassungsbeleg gebucht wird, wird der Stundungszeitplan erstellt.

#### <a name="post-and-transfer"></a>Buchen und übertragen

Um den Erfassungsbeleg zu buchen, verwenden Sie den Befehl **Buchen und übertragen**. Die Stundungsoptionen folgen der Position, für die der Beleg gilt. Für Belege ohne Fehler wird ein Stundungszeitplan erstellt, sofern er gestundet ist. Bei einem fehlerhaften und übertragenen Beleg werden auch alle Stundungsoptionen mit übertragen.

#### <a name="tax"></a>Steuern

In einigen Fällen kann es sein, dass der Steuerbetrag ganz oder teilweise nicht erstattungsfähig sein. Wenn der Steuerbetrag einer stundbaren Position einen nicht erstattungsfähigen Betrag enthält, wird der nicht erstattungsfähige Steuerbetrag beim Buchen der Rechnung in den stundbaren Zeitplanbetrag aufgenommen.

## <a name="free-text-invoice-transaction-deferral"></a>Stundung einer Freitextrechnungstransaktion

Verwenden Sie die Seite **Stundungen** zur Eingabe der Stundungsparameter für eine Positionsverteilung für Freitextrechnungen. Wenn Sie eine Verteilung eingeben, wird die Stundung automatisch basierend auf den Stundungseinstellungen auf der Seite **Standardstundungseinstellungen** eingerichtet.

## <a name="fields"></a>Felder

Die Seite **Transaktionsstundung** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------|
| Verzögert | <p>Geben Sie an, ob es sich bei der Position um eine Stundung handelt:</p><ul><li>**Ja** – Bei der Position handelt es sich um eine Stundung.</li><li>**Nein** – Bei der Position handelt es sich nicht um eine Stundung.</li></ul><p>Wenn diese Option auf **Ja** eingestellt ist, ist die Option **Vorhandenen Zeitplan anpassen** nicht verfügbar. Für Artikel und Belastungen, die bereits als gestundet eingerichtet wurden, ist diese Option auf **Ja** festgelegt. Für Artikel und Belastungen, die nicht standardmäßig als gestundet eingerichtet sind, legen Sie diese Option auf **Ja** fest.</p> |
| Vorhandenen Zeitplan anpassen | <p>Geben Sie an, ob es sich bei der Position um eine Anpassung für einen bestehenden Stundungszeitplan handelt:</p><ul><li>**Ja** – Die neue Verkaufsposition ist eine Anpassung eines bestehenden Stundungszeitplans. In diesem Fall können Sie im Feld **Angepasster Zeitplan** einen Stundungszeitplan auswählen.</li><li>**Nein** – Die neue Verkaufsposition ist keine Anpassung eines bestehenden Stundungszeitplans.</li></ul><p>Wenn diese Option auf **Ja** eingestellt ist, ist die Option **Verzögert** nicht verfügbar.</p> |
| Angepasster Zeitplan | <p>Wählen Sie den Stundungszeitplan aus, den die Position anpasst. Alle Werte auf der Seite werden dann mit den Werten aus dem ursprünglichen Stundungszeitplan aktualisiert. Diese Werte können nicht bearbeitet werden.</p><p>Dieses Feld ist nur verfügbar, wenn die Option **Vorhandenen Zeitplan anpassen** auf **Ja** festgelegt ist.</p> |
| Datum der Neuberechnung | <p>Geben Sie das Startdatum des Zeitraums an, ab dem Sie den Restbetrag neu berechnen möchten. Das Standarddatum ist das Datum des nächsten nicht erkannten Zeitraums.</p><p>Dieses Feld ist nur verfügbar, wenn die Option **Vorhandenen Zeitplan anpassen** auf **Ja** festgelegt ist.</p> |
| Enddatum | <p>Je nach Art der Stundung kann das Enddatum aktualisiert werden oder nicht:</p><ul><li>Geben Sie für eine lineare Stundung das neue Enddatum des Zeitplans an. Das vorhandene Enddatum des Stundungszeitplans ist der Standardwert.</li><li>Geben Sie für eine ereignisbasierte Stundung das Enddatum der Kreditereignisposition an. Dieses Datum kann leer sein.</li></ul><p>Dieses Feld ist nur verfügbar, wenn die Option **Vorhandenen Zeitplan anpassen** auf **Ja** festgelegt ist.</p> |
| Abrechnungszeitplannummer | <p>Die Abrechnungszeitplannummer.</p><p>Dieses Feld ist nur für wiederkehrende Vertragsabrechnungszeitpläne verfügbar.</p> |
| Stundungsregulierungsmethode | <p>Die gestundete Anpassungsmethode. Der Wert stimmt mit dem Wert auf der Seite **Massenkündigungsverarbeitung** für den wiederkehrenden Vertragsabrechnungszeitplan überein.</p><p>Dieses Feld ist nur für wiederkehrende Vertragsabrechnungszeitpläne verfügbar.</p> |
| **Konten – Umsatzerlös** | |
| Stundungskonto | <p>Das Stundungskonto, bei dem es sich um das Buchungskonto handelt, das auf der Seite **Auftrag** angezeigt wird.</p><p>Wenn die Position nicht gestundet ist, ist dieses Feld leer. In diesem Fall ist das Buchungskonto das Standardumsatzerlöskonto.</p> |
| Erkennungskonto | <p>Geben Sie das Konto an, das verwendet wird, wenn eine Stundung erkannt wird. Dieses Konto muss sich vom Stundungskonto unterscheiden.</p><p>Wenn die Option **Verzögert** anfänglich auf **Ja** festgelegt wurde, werden die im Stundungskonto verwendeten Dimensionswerte in das Erkennungskonto kopiert. Wenn die Dimension im Stundungskonto für das Erkennungskonto nicht vorhanden ist, wird sie ignoriert.</p> |
| Konto für anfängliche Erkennung | <p>Wählen Sie das Konto für die anfängliche Umsatzerlöserkennung. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist.</p> |
| Erkennungsgegenkonto | <p>Wählen Sie das Gegenkonto für die Umsatzerlöserkennung. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist.</p> |
| **Konten – Rabatt** | Dieser Abschnitt wird nur für gestundete Artikel angezeigt. Für gestundete Belastungen ist er ausgeblendet. |
| Stundungskonto | <p>Geben Sie die Stundungskontonummer für Rabatt an. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Stundungsoption für Rabatt** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Separater Zeitplan für Rabatt** festgelegt ist und ein Rabatt auf die Position angewendet wird.</p> |
| Erkennungskonto | <p>Geben Sie die Erkennungskontonummer für Rabatt an. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Stundungsoption für Rabatt** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Separater Zeitplan für Rabatt** festgelegt ist und ein Rabatt auf die Position angewendet wird.</p> |
| Konto für anfängliche Erkennung | <p>Wählen Sie das Konto für die anfängliche Rabatterkennung. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist und ein Rabatt auf die Position angewendet wird.</p> |
| Erkennungsgegenkonto | <p>Wählen Sie das Gegenkonto für die Umsatzerlöserkennung. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist und ein Rabatt auf die Position angewendet wird.</p> |
| **Konten – Verbrauch** | Dieser Abschnitt wird nur für gestundete Artikel angezeigt. Für gestundete Belastungen ist er ausgeblendet. |
| Stundungskonto | <p>Geben Sie die Stundungskontonummer für Verbrauch an.</p><p>Für Standardprodukte werden zwei Stundungszeitpläne erstellt:</p><ul><li>**Standardverkauf** – Ein Umsatzerlöszeitplan, der ein Guthaben hat. Wählen Sie in diesem Fall das Verbrauchsstundungskonto aus.</li><li>**Verbrauch** – Ein Ausgabenplan für Verbrauch (Wareneinsatz \[COGS\]), der ein Sollsaldo aufweist. Wählen Sie in diesem Fall das Verbrauchserkennungskonto aus.</li></ul><p>Beim Buchen der Rechnung wird der Verbrauchsbetrag auf das angegebene Verbrauchsstundungskonto gebucht. Diese Felder sind für Serviceelemente nicht verfügbar.</p> |
| Erkennungskonto | Geben Sie die Erkennungskontonummer für Verbrauch an. |
| Konto für anfängliche Erkennung | <p>Geben Sie das Konto für den anfänglichen Verbrauchserkennungsbetrag an. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist.</p> |
| Erkennungsgegenkonto | <p>Geben Sie das Gegenkonto für den Verbrauchserkennungsbetrag an. Der Standardwert stammt von der Seite **Standardstundungseinstellungen**.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Buchungsmethode für Stundung** auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** auf **Gewinn und Verlust** festgelegt ist.</p> |
| **Zeitplan** | |
| Zeitplantyp | <p>Wählen Sie den Typ des Stundungszeitplans aus: **Linear** (Standard) oder **Ereignisbasiert**.</p><p>Die auf der Seite angezeigten Optionen basieren auf dem von Ihnen ausgewählten Stundungszeitplantyp.</p><p>Wenn die Standardvorlage auf der Seite **Standardstundungseinstellungen** für die Buchungsposition eingestellt ist, basiert der Typ des Stundungszeitplans auf dem Typ der ausgewählten Vorlage.</p> |
| **Zeitplan – Linear** | |
| Vorangegangene Zeiträume konsolidieren | <p>Geben Sie an, ob Stundungszeitplanpositionen für Vorperioden konsolidiert werden sollen:</p><ul><li>**Ja** – Die Stundungszeitplanpositionen werden für frühere Perioden konsolidiert.</li><li>**Nein** – Die Stundungszeitplanpositionen für frühere Perioden werden nicht konsolidiert.</li></ul><p>Der Standardwert stammt von der Seite **Parameter für Umsatzerlös- und Ausgabenstundung**.</p> |
| Pro Zeitraum angleichen | <p>Geben Sie an, ob die Anzahl der Tage in jedem Zeitraum gleich ist oder je nach Zeitraum variiert:</p><ul><li>**Ja** – Jeder Zeitraum hat die gleiche Anzahl von Tagen.</li><li>**Nein** – Zeiträume haben nicht die gleiche Anzahl von Tagen.</li></ul><p>Wenn diese Option auf **Nein** eingestellt ist, wird bei der Berechnung des Betrag in jedem Zeitraum für einen Stornierungszeitplan die Anzahl der Tage in einem Zeitraum berücksichtigt.</p><p>Der Standardwert stammt von der Seite **Parameter für Umsatzerlös- und Ausgabenstundung**.</p> |
| Zeitplan aus Vorlage | <p>Geben Sie an, ob der Stundungszeitplan basierend auf einer Vorlage oder einem Enddatum erstellt werden soll:</p><ul><li>**Ja** – Der Stundungszeitplan wird anhand einer Vorlage erstellt.</li><li>**Nein** – Der Stundungszeitplan wird anhand eines Enddatums erstellt.</li></ul> |
| Vorlage | Wählen Sie die Stundungsvorlage aus. |
| Startdatum überschreiben | <p>Geben Sie an, ob Sie das Startdatum überschreiben möchten:</p><ul><li>**Ja** – Das Startdatum wird mit dem Datum, das Sie in das Feld **Startdatum** eingeben, überschrieben.</li><li>**Nein** – Das Startdatum entspricht der Regel **Startdatum der Standardstundung**, die auf das Rechnungsdatum angewendet wird, das auf der **Rechnung buchen** angegeben ist. Diese Regel kann auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** eingerichtet werden.</li></ul> |
| Startdatum der Stundung | Geben Sie das Startdatum der Stundung an. Der Standardwert ist das Transaktionsdatum. |
| Enddatum für Stundung | <p>Das Enddatum der Stundung.</p><p>Dieses Datum wird automatisch anhand der Stundungsvorlage berechnet. Wenn keine Vorlage ausgewählt ist, müssen Sie das Datum manuell eingeben.</p> |
| **Zeitplan – Ereignisbasiert** | |
| Vorlage | <p>Wählen Sie die ereignisbasierte Vorlage aus. Dieses Feld ist optional.</p><p>Wenn Sie eine Vorlage auswählen, überschreiben die Werte aus der Vorlage alle ereignisbasierten Daten und Ereignispositionen.</p> |
| Umlagetyp | <p>Wählen Sie den Umlagetyp für die Ereignispositionen aus:</p><ul><li>**Variable Beträge** – Für jede Position wird ein bestimmter Umlagebetrag eingegeben.</li><li>**Beträge angleichen** – Der Betrag wird gleichmäßig auf jede Zeile verteilt.</li><li>**Prozentsatz** – Es wird ein Betrag zugewiesen, der auf dem Prozentwert basiert, der für jede Position eingegeben wird.</li><li>**Vollendungsgrad in Prozent** – Für jede Zeile wird ein kumulativer Fertigstellungswert verwendet.</li><p>**Variable Menge** – Für jede Position wird eine bestimmte Umlagemenge eingegeben.</li></ul><p>**Hinweis:** Wenn Sie **Vollendungsgrad in Prozent** auswählen möchten, müssen die Daten in aufsteigender Reihenfolge sein.</p> |
| **Separate Ereignisse pro Einheit erstellen** | |
| Description | <p>Geben Sie an, ob Sie Ereignisse pro Einheit trennen möchten:</p><ul><li>**Ja** – Die Ereignispositionen werden getrennt, sodass pro Menge eine Position vorhanden ist.<p>Beispiel: Es gibt drei Ereignispositionen, und die Rechnung hat die Menge „4“. In diesem Fall hat der resultierende Stundungszeitplan 12 Positionen.</p></li><li>**Nein** – Die Ereignispositionen werden nicht getrennt.</li></ul> |
| Ablaufkonto | <p>Wählen Sie das Konto aus, das für erkannte abgelaufene Positionen verwendet wird. Sie können das Konto auswählen, nachdem der Stundungszeitplan erstellt wurde.</p><p>Wenn für ein Ereignis ein Ablaufdatum festgelegt ist, wird der Erkennungsbetrag während des Erkennungsprozesses auf das Ablaufkonto anstatt auf das Erkennungskonto übertragen.</p> |
| **Zeitplan – Ereignisbasierte Positionen** | |
| Description | Eine Beschreibung des Ereignisses. |
| Enddatum für Stundung | <p>Wählen Sie das Enddatum für das Ereignis aus.</p><p>**Hinweis:** Wenn Sie ein Enddatum auswählen, wird das Feld **Ablaufdatum** gelöscht. Sie können nicht sowohl ein Enddatum als auch ein Ablaufdatum verwenden.</p> |
| Ablaufdatum | <p>Wählen Sie das Ablaufdatum für das Ereignis aus.</p><p>**Hinweis:** Wenn Sie ein Enddatum auswählen, wird das Feld **Ablaufdatum** gelöscht. Sie können nicht sowohl ein Enddatum als auch ein Ablaufdatum verwenden.</p> |
| Menge | <p>Geben Sie die Umlagemenge an. Der Standardwert für alle Positionen ist **0** (null). Wenn Sie die Menge aktualisieren, muss die Gesamtmenge aller Positionen kleiner oder gleich der Menge sein, die für den Einzelposten im Auftrag angegeben ist.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Umlagetyp** auf **Variable Menge** festgelegt ist.</p><p>Wenn die Menge des Einzelpostens im Auftrag so geändert wird, dass sie kleiner als die ursprüngliche Menge ist, und die Rechnung erstellt wird, werden weniger ereignisbasierte Positionen erstellt. Die zugewiesene Gesamtmenge überschreitet nicht die Menge, die im ursprünglichen Auftrag oder Abrechnungszeitplan angegeben ist.</p> |
| Zuteilung in Prozent | <p>Geben Sie den Umlageprozentsatz an. Wenn das Feld **Umlagetyp** auf **Prozentsatz** oder **Vollendungsgrad in Prozent** festgelegt ist, können Sie manuell einen Prozentsatz eingeben. Andernfalls wird er automatisch berechnet.</p><p>Wenn das Feld **Umlagetyp** auf **Prozentsatz** festgelegt ist, muss der Prozentsatz insgesamt 100 ergeben.</p> |
| Betrag | <p>Geben Sie den Umlagebetrag ein. Wenn das Feld **Umlagetyp** auf **Variable Beträge** oder **Vollendungsgrad in Prozent** festgelegt ist, können Sie manuell einen Betrag eingeben.</p><p>Wenn das Feld **Umlagetyp** auf **Vollendungsgrad in Prozent** festgelegt ist und Sie hier einen Betrag eingeben, wird der Wert für **Vollendungsgrad in Prozent** automatisch berechnet.</p><p>Aufgrund von Rundungen stimmt der berechnete Betrag möglicherweise nicht genau mit dem manuell eingegebenen Betrag überein. Wenn Sie eine genaue Menge benötigen, legen Sie das Feld **Umlagetyp** auf **Variable Beträge** fest.</p> |
| Vollendungsgrad in Prozent | <p>Geben Sie den Vollendungsgrad in Prozent an. Der Wert muss zwischen 0 und 100 liegen.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Umlagetyp** auf **Vollendungsgrad in Prozent** festgelegt ist.</p> |
| Abschlussbetrag | <p>Die berechnete Summe für alle Positionen im Stundungszeitplan.</p><p>Wenn das Feld **Umlagetyp** auf **Vollendungsgrad in Prozent** festgelegt ist, können Sie manuell einen Betrag eingeben. In diesem Fall wird der Wert für **Vollendungsgrad in Prozent** basierend auf dem von Ihnen eingegebenen Betrag berechnet.</p><p>Aufgrund von Rundungen stimmt der berechnete Betrag möglicherweise nicht genau mit dem manuell eingegebenen Betrag überein.</p><p>Dieses Feld ist nur verfügbar, wenn das Feld **Umlagetyp** auf **Vollendungsgrad in Prozent** festgelegt ist.</p> |
| Beim Buchen erkennen | <p>Geben Sie an, ob die Position automatisch erkannt wird, sobald die Transaktion gebucht wird:</p><ul><li>**Aktiviert** – Die Position wird automatisch erkannt, sobald die Transaktion gebucht wird.</li><li>**Deaktiviert** – Die Position wird nicht erkannt, wenn die Transaktion gebucht wird.</li></ul> |
| Erkennungskonto | <p>Geben Sie das Erkennungskonto für das Ereignis an, falls das Konto von dem Konto abweicht, das für den gesamten Stundungszeitplan verwendet wird.</p><p>Sie können dieses Feld in Verbindung mit der Option **Beim Buchen erkennen** verwenden.</p> |
