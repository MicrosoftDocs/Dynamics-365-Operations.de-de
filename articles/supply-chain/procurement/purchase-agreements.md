---
title: Rahmenbestellungen
description: Dieser Artikel gibt Informationen zu Kaufverträge. Ein Kaufvertrag ist ein Vertrag, der eine Organisation bindet, eine angegebene Menge oder einen Betrag zu kaufen, indem sie mehrere Bestellungen tätigt. Für diese Zusage erhält der Käufer Sonderpreise und Rabatte.
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 188a71ec660787b0b942a3d3bf4967b747c4469f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335884"
---
# <a name="purchase-agreements"></a>Rahmenbestellungen

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt Informationen zu Kaufverträge. Ein Kaufvertrag ist ein Vertrag, der eine Organisation bindet, eine angegebene Menge oder einen Betrag zu kaufen, indem sie mehrere Bestellungen tätigt. Für diese Zusage erhält der Käufer Sonderpreise und Rabatte. 

Kaufverträge können für eine bestimmte Menge eines Produkts, einen bestimmten Währungsbetrag eines Produkts oder einen bestimmten Währungsbetrag der Produkte in einer Beschaffungskategorie gelten. Die Preise und Rabatte des Kaufvertrags setzen alle Preise und Rabatte außer Kraft, die in anderen ggf. vorhandenen Handelsvereinbarungen angegeben sind.  

Auf der Seite **Kaufverträge** können Sie Kaufverträge, die zwischen Ihrer Organisation und Kreditoren gelten, erstellen, anwenden und weiterverfolgen. Nach der Erstellung eines Kaufvertrags können Sie zum Beispiel damit direkt eine Bestellung in Auftrag geben. Jeder Kaufvertrag hat einen Gültigkeitszeitraum, der von der Person definiert wird, die den Kaufvertrag erstellt. Das Lieferdatum einer Bestellung muss innerhalb der Gültigkeitsdaten dieser Gültigkeitsperiode liegen.  

Nachdem Sie einen Kaufvertrag erstellen, müssen Sie diesen aktivieren, bevor er gültig ist. Um einen Kaufvertrag zu aktivieren, legen Sie die **Vertrag als 'Effektiv' kennzeichnen** Option auf **Ja** fest. 

Um zu verhindern, dass Ihr Kaufvertrag verwendet und bestätigt wird, markieren Sie den Vertragsstatus als **Geschlossen**. Sie können den Status jederzeit nach dieser Änderung wieder als **Gültig** aktualisieren.

## <a name="responsible-workers-on-purchase-agreements"></a>Verantwortliche Mitarbeiter bei Kaufverträgen

Sie können einen primären und einen sekundären verantwortlichen Mitarbeiter in der Klassifizierung des Kaufvertrags identifizieren. Diese Werte werden vom resultierenden Kaufvertrag übernommen. Sie müssen dem Kaufvertrag keine verantwortlichen Mitarbeiter hinzufügen, und diese können im Kaufvertrag selbst fallweise direkt geändert werden. Sie können keinen sekundärverantwortlichen Mitarbeiter ohne einen primärverantwortlichen Mitarbeiter angeben, obwohl Sie keinen sekundärverantwortlichen Mitarbeiter benötigen. Sie können nicht denselben Mitarbeiter als primären und sekundären verantwortlichen Mitarbeiter angeben.

> [!IMPORTANT]
> Um die Funktion „Zuständige Partei“ nutzen zu können, muss es für Ihr System aktiviert sein. Ab Supply Chain Management Version 10.0.25 ist die Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Zuständige Partei für Kaufvertrag* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="commitment-types"></a>Zusagetypen
Jede Position in einem Kaufvertrag drückt eine Zusage für den Kauf eines Artikels aus. Sie können Positionen aus mehreren Bestellungen (POs) verwenden, um die Zusage zu erfüllen. Es gibt vier Typen von Zusagen:

-   **Produktmengenzusage** – Sie kaufen eine bestimmte Produktmenge.
-   **Produktwertzusage** – Sie kaufen einen bestimmten Währungsbetrag eines Produkts.
-   **Produktkategorie-Wertzusage** – Sie kaufen einen bestimmten Währungsbetrag einer Beschaffungskategorie. Der Betrag kann für einen Katalogartikel oder einen nicht im Katalog enthaltenen Artikel sein.
-   **Wertzusage** - Sie kaufen eine einem bestimmten Währungsbetrag entsprechende Menge eines oder mehrerer Produkte in einer Beschaffungskategorie.

## <a name="pricing-terms-for-purchase-agreements"></a>Preisgestaltungsbedingungen für Kaufverträge
Die Preisgestaltungsbedingungen können je nach Typ der Zusage variieren. Die Preisgestaltungsbedingungen von Rahmenbestellungen überschreiben alle anderen Preisgestaltungsbedingungen, die für Handelsvereinbarungen festgelegt wurden. In der folgenden Tabelle werden die preisbezogene Felder beschrieben, die von jedem Zusagetyp betroffen sind. Felder, die **Ja** enthalten, können in einer Auftragsposition aktualisiert werden.

| Zusagetyp                   | Preis je Einheit | Preiseinheit | Rabatt in Prozent | Skontobetrag |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produktmengenzusage       | Ja        | Ja        | Ja              | Ja                  |
| Produktwertzusage          |            |            | Ja              |                      |
| Produktkategorie-Wertzusage |            |            | Ja              |                      |
| Wertzusage                  |            |            | Ja              |                      |

## <a name="policies-for-purchase-agreements"></a>Richtlinien für Kaufverträge
Die folgenden Richtlinien wirken sich auf die Verknüpfung zwischen einer Kaufvertragszusage und den entsprechenden Bestellposition aus:

-   **Maximum wird erzwungen**: Die Gesamtmenge oder der Betrag für alle Auftragspositionen darf die Menge oder Summe nicht überschreiten, der auf der zugehörigen Zusage angegeben ist.
-   **Festpreis und ‑rabatt** – Der Preis in einer Auftragsposition und der Preis auf der entsprechenden Zusage müssen gleich sein. Wenn der Preis in der Auftragsposition geändert wird, ist die Verknüpfung mit der Zusage aufgehoben. Wenn die Verknüpfung aufgehoben ist, trägt die Auftragsposition nicht zur Erfüllung der Zusage bei.
-   **Mindestfreigabebetrag und Höchstfreigabebetrag** – Wenn ein Betrag angegeben ist, erhalten Sie eine Meldung, wenn Sie Änderungen an einer Auftragsposition vornehmen, die bewirken, dass sich die Auftragsposition von der zugehörigen Zusage unterscheidet.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Erfüllungsberechnungen für Kaufverträge
Erfüllungsmengen und ‑beträge werden auf der Registerkarte **Erfüllung** auf dem Inforegister **Positionsdetails** der Seite **Kaufverträge** angezeigt.  

Der Bereich **Erfüllung** zeigt den Restbetrag oder die Menge an, die benötigt wird, um die Zusage zu erfüllen.  

Im **Vereinbarung** Bereich werden die Gesamtmenge oder den Gesamtbetrag angezeigt, für den die Kaufvertragsposition gültig ist.  

Sie können auf die Bestellpositionen und Rechnungspositionen zugreifen, die zur Erfüllungsberechnung beitragen, indem Sie die Aktivität in **Zugehörige Informationen** für die Positionen oder im Kopf eines Kaufvertrags auswählen.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Bestätigungen sowie Versionshistorie für Kaufverträge
Wenn Sie einen Kaufvertrag bestätigen, wird die aktuelle Version des Kauftrags in einer Historientabelle gespeichert. Wenn Sie den Kaufvertrag ändern, können Sie ihn erneut bestätigen, um eine andere Version des Kaufvertrags in der Historie zu speichern. Wenn Sie einen Verkaufvertrag nicht bestätigen, können Sie ihn trotzdem zum Erstellen von Aufträgen verwendet. Allerdings werden Informationen für den Kaufvertrag nicht gespeichert. Sie können alle Versionen der Vereinbarung in der Vorschau anzeigen oder drucken. Sie können die Überarbeitungen dann an den Kreditor weitergeben, um sie genehmigen zu lassen.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Anwenden on Kaufverträgen im Bestellungsprozess
Wenn Sie eine Bestellung erstellen, können Sie einen Kaufvertrag für sie übernehmen. Informationen aus den Bedingungen für die Vereinbarung, wie die Zahlungsbedingungen, Lieferbedingungen und Lieferadresse, werden dann in den Kopf der Bestellung kopiert. Wenn die Bestellung eine oder mehrere Auftragspositionen für Produkte und Kategorien enthält, die im Kaufvertrag angegeben sind, werden die Preise und Rabatte aus dem Kaufvertrag für diese Positionen verwendet. Der Betrag oder die Menge in der Auftragsposition trägt zur Erfüllung der Zusage im Kaufvertrag bei. Die gleiche Bestellung kann sowohl Positionen enthalten, die mit keinem Kaufvertrag verknüpft sind, als auch Positionen, für die eine Zusage in einem Kaufvertrag besteht.  

Sie können einen Kaufvertrag auswählen, wenn Sie eine Bestellung erstellen. Sie können einen Kaufvertrag nicht aktivieren, nachdem die Bestellung erstellt wurde.  
In einigen Fällen, in denen Kaufverträge indirekt erstellt werden, können Sie steuern, ob Supply Chain Management automatisch nach gültigen Kaufverträgen sucht. Dies kann beispielsweise ratsam sein, wenn Sie geplante Einkaufsbestellungen automatisch umwandeln oder Bestellungen erstellen, die auf Aufträgen basieren.

## <a name="matching-policy-on-purchase-agreements"></a>Zuordnungsrichtlinie zu Kaufverträgen
Sie können eine Zeilenabgleichsrichtlinie auf dem Kopf des Kaufvertrags definieren. Diese Zeilenabgleichsrichtlinie respektiert die Zeilenabgleichsrichtlinie für Kreditorenparameter, wenn das Feld **Überschreiben der Abgleichsrichtlinie zulassen** auf der Seite **Abgleich der Kreditorenparameter** (auf der Seite **Preis- und Mengenabgleich** Inforegister) auf **Höher als die Unternehmensrichtlinie** gesetzt ist. Belege, die sich auf den Kaufvertrag beziehen, verwenden die Zeilenabgleichsrichtlinie, die im Kopf des Kaufvertrags definiert ist, sofern in der entsprechenden Position, Position und Lieferant oder in der Einkaufsrichtlinie der Kategorie nichts anderes angegeben ist.

## <a name="purchase-agreements-and-intercompany-trade"></a>Kaufverträge und Intercompany-Handel
Intercompany-Handelsbeziehungen können zwischen Kreditorenkonten und Debitorenkonten erstellt werden, die zu verschiedenen juristischen Personen gehören. Wenn ein Auftrag oder eine Bestellung für eine der Parteien erstellt wird, wird eine Intercompany-Auftragskette erstellt. In der Auftragskette werden der Auftrag und die Bestellung in den entsprechenden juristischen Personen erstellt.  

Sie können einen Kaufvertrag für eine der Intercompany-Handelsparteien erstellen. Sie können den entsprechenden Kaufvertrag dann für den anderen Intercompany-Handelspartner in der anderen juristischen Person generieren.  

Wenn Sie eine Intercompany-Bestellung anlegen, die den Intercompany-Kaufvertrag in einer juristischen Person verwendet, wird für den entsprechenden Intercompany-Auftrag der entsprechende Intercompany-Kaufvertrag in der anderen juristischen Person verwendet. Die Erfüllung der Kaufvertragszusagen und die Erfüllung der Kaufverträge wird synchronisiert, genauso wie der Intercompany-Auftrag und die Intercompany-Bestellung synchronisiert werden.

## <a name="financial-dimensions-on-purchase-agreements"></a>Finanzdimensionen in Kaufverträgen
Sie können Finanzdimensionen in Dokumentüberschriften oder einzelne Positionen eines Kaufvertrags kopieren. Wenn Sie die Dimensionen im Vereinbarungskopf oder in der Kaufvertragsposition ändern, wirkt sich diese Änderung keine freigegebenen Aufträgen, es wird jedoch über alle neuen Aufträge angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Kaufvertrag erstellen](tasks/create-purchase-agreement.md)
- [Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag anwenden](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]