---
title: Einrichten von Kreditorenkonten
description: "In diesem Thema werden die Typen von Informationen beschrieben, die Sie angeben müssen, wenn Sie ein neues Kreditorenkonto erstellen."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4a20fca7420e7bd546e29278b40046d69a81aac6
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-vendor-accounts"></a>Einrichten von Kreditorenkonten

[!include[banner](../includes/banner.md)]


In diesem Thema werden die Typen von Informationen beschrieben, die Sie angeben müssen, wenn Sie ein neues Kreditorenkonto erstellen.

Wenn Sie ein Kreditorenkonto erstellen, geben Sie Informationen zum Kreditor ein. Diese Informationen werden verwendet, um Daten automatisch in Dokumente einzugeben und Aktivitäten nachzuverfolgen, die den Kreditor betreffen. Angenommen, Sie haben folgende Informationen zu einem Kreditor konfiguriert:

-   Zuweisen einer Kreditorengruppe Jedem Kreditor muss eine Kreditorengruppe zugewiesen werden. Die Kreditoren in einer Kreditorengruppe verfügen über gemeinsame Parameter. Beispielsweise gelten für sie möglicherweise die gleichen Zahlungsbedingungen.
-   Konfigurieren Sie den Lieferanten für den Katalogimport. Kreditoren können eine Datei angeben, die den Katalog ihrer Artikel und Dienstleistungen enthält. Diese Datei kann hochgeladen werden, damit die Arbeitskräfte vom Kreditor bestellen können.
-   Dient zum Zuweisen des Kreditors zu Beschaffungskategorien.
-   Dies ermöglicht es einem vorhandenen Kreditor, in Geschäftsbeziehungen mit einer anderen juristischen Person Ihrer Organisation zu stehen.
-   Sie können einen Kreditor für bestimmte Buchungsarten sperren.
-   Richten Sie Bankdaten für den Kreditor, damit Sie Zahlungen elektronisch senden können.
-   Richten Sie Informationen zu Gebühren, Steuern, Zahlung und Lieferung für den Kreditor ein. Standardmäßig werden diese Einstellungen in neue Dokumente kopiert, die für den Kreditor erstellt werden.
-   Richten Sie standardmäßige Finanzdimensionen ein, die verwendet werden, um Buchungen mit dem Kreditor automatisch auf Finanzkonten zu buchen.

Um den Prozess der Erstellung von Kreditorenkonten zu beschleunigen, können Sie Vorlagen erstellen. Um eine Vorlage zu erstellen, klicken Sie auf der Seite **Kreditor** im Aktivitätsbereich auf **Optionen** &gt; **Datensatzinformationen.** Klicken Sie dann auf **Unternehmenskontovorlage**. Unternehmenskontovorlagen werden auch von anderen Benutzer verwendet.  

Sie können auch eine Benutzervorlage für den Eigengebrauch erstellen. Sie können einen Kreditor nicht löschen, wenn dieser anderen Datensätzen zugeordnet ist, z. B. Kontakten und Produkten.

## <a name="vendor-account-numbers"></a>Kreditorenkontonummern
Die Kontonummer ist eine eindeutige Kennung für einen Kreditor. Sie können Kontonummern einrichten, die automatisch beim Erstellen eines Kreditors generiert werden. Sie können außerdem den Nummernkreis konfigurieren, sodass Kontonummern manuell eingegeben werden. Beispielsweise möchten Sie die Telefonnummer des Kreditors als Kennung verwenden.

## <a name="vendor-organizations-and-individual-vendors"></a>Kreditorenorganisationen und einzelne Kreditoren
Wenn Sie ein neues Kreditorenkonto erstellen, müssen Sie festlegen, ob der Kreditor eine Person oder eine Organisation ist. Ihre Auswahl beeinflusst die Informationen, den Sie für den Kreditor angeben müssen. Bei einer Person enthalten diese Informationen den Vornamen, Nachnamen und den Titel. Bei einer Organisation enthalten diese Informationen die Unternehmensnummer und die Anzahl von Mitarbeitern.

## <a name="addresses"></a>Adressen
Für jeden Kreditor können mehrere Adressen definiert werden, von denen jede für einen anderen Zweck verwendet wird. So können Sie beispielsweise eine Adresse erstellen, deren Zweck **Rechnung** ist. Oder können Sie eine Adresse mit dem Zweck **Zahlungsempfänger** einrichten, wenn Sie die Kreditorenrechnung per Scheck begleichen. Wenn Sie eine Adresse für Überweisungen an ausländische Banken angeben müssen, ist der Verwendungszweck **SWIFT**.

## <a name="vendor-contacts"></a>Kreditorenkontakte
Können Sie Kontakte für einen Kreditoren speichern. Diese Kontakte können dann für Dokumente wie Bestellungen oder Angebotsanforderungen (RFQs) verwendet werden.  

Um Kontakte für einen Kreditor hinzuzufügen, klicken Sie auf der Seite **Alle Kreditoren** auf der Registerkarte **Kreditor** in der Gruppe **Einstellungen** auf **Kontakte** &gt; **Kontakte hinzufügen**.  

Sie können Kreditorenkontakte von Grund auf neu erstellen. Alternativ können Sie auch Details einer anderen Person kopieren, die bereits in Microsoft Dynamics 365 for Finance and Operations registriert ist und die Informationen nach Bedarf bearbeiten.  

**Hinweis:** Einen Kontakt für einen Kreditor hinzuzufügen ist nicht das Gleiche, wie das Hinzufügen von Kontaktinformationen für diesen Kreditor . Obwohl Sie allgemeine Kontaktinformationen für einen Kreditor hinzugefügt haben, möchten Sie vielleicht auch bestimmte Personen, die Kontakte dieses Unternehmens sind und die ihre eigenen Kontaktinformationen haben, hinzufügen.  

Sie können keinen Kontaktpersondatensatz löschen, wenn der Kontakt auf ein Dokument verweist. Stattdessen können Sie den Kontakt deaktivieren.  

Sie können Kreditorenkontakte Ihren persönlichen Kontakten in Microsoft Office 365 hinzufügen. Allerdings müssen Sie zuerst die Synchronisierung zwischen Finance and Operations und Office 365 sowohl in der Microsoft Exchange Server-Synchronisierung als auch im Microsoft Outlook-Setup-Assistenten einrichten.

## <a name="vendors-in-different-legal-entities"></a>Kreditoren in verschiedenen juristischen Personen
Wenn ein Kreditor für eine juristische Person in der Organisation erfasst ist und andere juristische Personen den gleichen Kreditor erfassen müssen, können Sie die Seite **Kreditor zu anderer juristischer Person hinzufügen** verwenden, um den Kreditor zu so konfigurieren, dass er Geschäfte mit einer anderen juristischen Person tätigen kann. Wählen Sie für den Kreditor in der ausgewählten juristischen Person eine Kreditorengruppe, eine Währung und einen Sperrstatus aus.  

Unterhalten innerhalb Ihrer Organisation mehrere juristische Personen eine Geschäftsbeziehung mit dem gleichen Kreditor, und wird in jeder juristischen Person ein eigenes Konto für diesen Kreditor verwaltet, können Sie die Parteikennungen der Kreditorenkonten zusammenführen. Auf diese Weise können Informationen wie die Adresse und Mitarbeiteranzahl freigegeben werden, sodass Sie sie nur an einer Stelle aktualisieren müssen.  

Zum Zusammenführen von Parteikennungen, führen Sie die folgenden Schritte aus.

1.  Wählen Sie auf der Seite **Globales Adressbuch** die Adressbuchdatensätze aus, die den Kreditor in den einzelnen juristischen Personen darstellen, der in die Zuordnung einbezogen werden soll.
2.  Klicken Sie im Aktivitätsbereich auf **Datensätze zusammenführen**.

## <a name="agreements"></a>Vereinbarungen
Wenn Sie ein Kreditorenkonto einrichten, sollten Sie auch die Vereinbarungen erfassen, die Sie mit dem Kreditor getroffen haben. Sie können Preis- und Rabattvereinbarungen einrichten, indem die Sie Aktionen im Kreditorendatensatz verwenden. Sie können auch eine Rahmenbestellung auf der Seite **Rahmenbestellungen** einrichten.

## <a name="putting-a-vendor-on-hold"></a>Sperren eines Kreditors
Sie können einen Kreditor für verschiedene Buchungsarten sperren. Die folgenden Optionen sind verfügbar:

-   **Nein** – Für den Kreditor gelten keine Sperren.
-   **Rechnung** – Für den Kreditor können keine Rechnungen erstellt oder gebucht werden.
-   **Alle** – Für den Kreditor sind alle Buchungsarten gesperrt. Diese Buchungsarten umfassen Bestellanforderungen, Rechnungen und Zahlungen.
-   **Zahlung** – Für den Kreditor können keine Zahlungen generiert werden.
-   **Anforderung** – Es können nur Bestellanforderungen erstellt werden. Es können keine anderen Buchungen erstellt werden.
-   **Nie** – Der Kreditor wird niemals für Inaktivität gesperrt.

Wenn Sie einen Kreditor sperren, können Sie auch einen Grund und ein Datum angeben, wann die Sperrung aufgehoben wird. Wenn Sie kein Enddatum eingeben, bleibt die Sperre des Kreditors auf unbestimmte Zeit bestehen.

Sie können eine Massenaktualisierung des Sperrstatus auf **Alle** für Kreditoren durchführen, basierend auf den ausgewählten Kriterien auf der Seite **Kreditorendeaktivierung**, und einen Grund zuweisen, warum der Kreditor gesperrt ist.

Die folgenden Kriterien werden verwendet, um Kreditoren einzuschließen, die in einer Periode inaktiv gewesen sind, um Kreditoren einzuschließen oder auszuschließen, die Mitarbeiter sind, und um Kreditoren auszuschließen, die sich in einer Karenzzeit bis zur nächsten Sperrung befinden.

- Basierend auf der Zahl der Tage, die Sie im Feld **In Aktivitätsperiode** auf der Seite **Kreditorendeaktivierung** eingeben, berechnet die Anwendung das letzte Datum, an dem der Kreditor eine beliebige Aktivität haben kann, die als inaktiv zu betrachten ist. Das bedeutet das aktuelle Datum minus der Anzahl der Tage, die Sie eingeben. Wenn mindestens eine Rechnung für den Kreditor vorhanden ist, auf der das Datum nach dem errechneten spätesten Datum liegt, wird der Kreditor von der Deaktivierung ausgeschlossen. Dies wird auch überprüft, wenn der Kreditor Zahlungen nach dem Datum, offene Bestellanforderungen, offene Bestellungen, Angebotsanforderungen oder Antworten hat.
- Die Anzahl von Tagen im Feld **Karenzzeit bis zur nächsten Sperrung** wird verwendet, um das späteste Karenzdatum zu berechnen. Das bedeutet das aktuelle Datum minus der Tage, die Sie eingeben. Dies gilt nur für Kreditoren, die zuvor deaktiviert wurden. Im Falle einer vorherigen Deaktivieren verifiziert die Anwendung die Historie anderer Deaktivierungen für den Kreditor und überprüft, ob die letzte Deaktivierung vor dem jüngsten Karenzdatum erfolgte. Ist dies der Fall, wird der Kreditor in den Deaktivierungsprozess einbezogen.
- Der Parameter **Mitarbeiter einbeziehen** bezieht sich auf Kreditoren, die mit einem Mitarbeiter verknüpft sind. Sie können festlegen, ob Sie diese Mitarbeiter einbeziehen möchten.

Bei diesem Prozess werden immer Kreditoren ausgeschlossen, bei denen das Feld **Kreditorensperre** den Wert **Nie** hat.

Kreditoren, die die Überprüfungen bestehen, werden gesperrt, wodurch der Feldwert **Kreditorensperre** auf **Alle** festgelegt wird und der **Grund** auf die getroffene Auswahl. Ein Datensatz in der Sperrungshistorie wird für den Kreditor erstellt.

## <a name="vendor-invoice-account"></a>Kreditorenrechnungskonto
Wenn mehrere Ihrer Kreditoren dieselbe Rechnungsadresse haben, oder wenn Rechnungen an den Kreditor über Dritte abgewickelt werden, können Sie ein Rechnungskonto im Kreditorendatensatz erstellen. Das Rechnungskonto ist das Konto, auf dem der Rechnungsbetrag gutgeschrieben wird, wenn Sie eine Kreditorenrechnung für eine Bestellung erstellen. Wenn Sie kein Rechnungskonto im Kreditorendatensatz angeben, wird das Kreditorenkonto als Rechnungskonto verwendet.

## <a name="vendor-bank-accounts"></a>Kreditoren-Bankkonten
Wenn Sie Zahlungen an ein Kreditorenbankkonto veranlassen müssen, können Sie Informationen über die Bank des Kreditors und Bankkonten auf der Seite **Kreditorenbankkonten** eingeben. Sie können auch Informationen zu Prüfungen und Zahlungen für das ausgewählte Bankkonto eingeben. Beispielsweise können Sie Testtransaktionen zu Kreditoren-Bankkonten hinzufügen. Diese Testtransaktionen können verwendet werden, um die Genauigkeit von Kontodaten zu überprüfen, zum Beispiel Bankleitzahlen und Kontonummern. Sie müssen ein Standardkonto für Zahlungen an den Kreditor angeben. Wenn Sie allerdings eine tatsächliche Zahlung leisten, können Sie dieses Konto auf eines der anderen Konten des Kreditors ändern.

## <a name="ledger-accounts"></a>Sachkonten
Sie können Standardkonten angeben, die in Kreditorenrechnungserfassungen automatisch für den angegebenen Kreditor angezeigt werden. Verwenden Sie diese Funktion, wenn Sie normaler Weise im Laufe der Zeit für dieselbe Art von Produkten oder Dienstleistungen derselben Kreditoren bezahlen. Wenn Sie ein Standardkonto angeben, können Sie Erfassungseinträge in der Rechnungserfassung schnell und effizient eingeben. Die in diesem Formular angegebenen Standardkonten werden nicht für Bestellungen oder Kreditorenrechnungen verwendet, die auf der Seite **Kreditorenrechnung** eingegeben wurden.  

Wählen Sie Standardkonten auf der Seite **Standardkontoeinstellungen** aus, die Sie auf der Registerkarte **Rechnung** im Kreditorendatensatz öffnen können. Die Konten, die Sie hier auswählen, werden in der gefilterten Liste der Konten für das Kreditorenkonto angezeigt, wenn Sie einen Erfassungseintrag eingeben. Sie können eines der Konten als Standardkonto festgelegt.




