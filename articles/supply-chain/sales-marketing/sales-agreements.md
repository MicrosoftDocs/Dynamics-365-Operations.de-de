---
title: "Kaufverträge"
description: "Dieser Artikel gibt Informationen zu Kaufverträgen. Durch einen Kaufvertrag verpflichtet sich der Debitor, Produkte in einer bestimmten Menge oder für einen bestimmten Preis über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Sonderpreise und Rabatte zustehen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15e3f872e4ded027734ee73081ba7af68be5107d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="sales-agreements"></a>Kaufverträge

[!include[banner](../includes/banner.md)]


Dieser Artikel gibt Informationen zu Kaufverträgen. Durch einen Kaufvertrag verpflichtet sich der Debitor, Produkte in einer bestimmten Menge oder für einen bestimmten Preis über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Sonderpreise und Rabatte zustehen.

Ein Kaufvertrag ist ein Vertrag, der den Debitor verpflichtet, Produkte in einer bestimmten Menge oder einer bestimmten Menge über einen vorgegebenen Zeitraum, gegen die Gewährung von Sonderpreisen, Sonderrabatte und anderen speziellen Bedingungen, wie Zahlungs-und Lieferbedingungen, abzunehmen. Die Preise und Rabatte des Kaufvertrags überschreiben alle Preise und Rabatte, die in sämtlichen vorhandenen Handelsvereinbarungen angegeben sind.  

Die Gültigkeitsperiode der Kaufvertragsposition wird durch die Felder **Gültigkeitsdatum** und **Ablaufdatum** in der Kaufvertragsposition definiert. Der Auftrag eines Debitors ist für die Bedingungen der Vereinbarung qualifiziert, wenn das angeforderte Lieferdatum des Auftrags innerhalb der Gültigkeitsperiode ist. Alle Auftragspositionen, die mit einem Kaufvertrag verknüpft sind, tragen zur Erfüllung dieses Kaufvertrags bei.  

Sie können einen Auftrag direkt von einem Kaufvertrag erstellen, indem Sie die Aktivität **Freigabeauftrag** verwenden. Alternativ können Sie einen gültigen Kaufvertrag auswählen, wenn Sie Aufträge entgegennehmen (mehr unter "Kaufverträge im Bestellungsprozess übernehmen" in diesem Artikel).  

**Hinweis:** In früheren Versionen wurden Kaufverträge als Rahmenaufträge bezeichnet.

## <a name="commitment-types"></a>Zusagetypen
Jede Position in einem Kaufvertrag drückt eine Zusage für den Verkauf eines Artikels aus. Im Allgemeinen gibt es zwei Kategorien von Zusagen:

-   **Wertzusage** – Der Debitor erklärt sich damit einverstanden, Produkte für eine bestimmte Summe zu kaufen.
-   **Mengenzusage** – Der Debitor erklärt sich damit einverstanden, eine bestimmte Menge von Produkten zu kaufen.

Außerdem kann ein Vertrag den Debitor verpflichten, ein bestimmtes Produkt oder Produkte in einer Produktkategorie zu kaufen. Durch die Kombination dieser zwei Faktoren (Wert gegen Menge und bestimmte Produkte gegen Produktkategorien) erhalten wir vier Arten von Zusagen:

-   **Produktmengenzusage** – Der Debitor erklärt sich damit einverstanden, eine bestimmte Menge von Produkten zu kaufen. Positionen, für die dieser Zusagetyp verwendet wird, werden durch eine Artikelnummer und die Menge und Einheit definiert, die vereinbart wurden. Das **Betrag**-Feld ist nicht verfügbar.
-   **Produktwertzusage** – Der Debitor erklärt sich damit einverstanden, spezifische Produkte für eine bestimmte Summe zu kaufen. Positionen, für die der Zusagetyp verwendet wird, werden durch eine Artikelnummer und die vereinbarte Summe definiert. Das **Menge**- und **Einheit**-Feld ist nicht verfügbar.
-   **Produktkategorie-Wertzusage** – Der Debitor erklärt sich damit einverstanden, Produkte auf einer bestimmten Verkaufskategorie für eine bestimmte Summe zu kaufen. Positionen, für die der Zusagetyp verwendet wird, werden durch eine Verkaufskategorie in der Hierarchie der Verkaufskategorien und durch eine Summe definiert. Das **Menge**- und **Einheit**-Feld ist nicht verfügbar.
-   **Wertzusage** – Der Debitor erklärt sich damit einverstanden, ein beliebiges Produkte oder Produkte aus einer beliebigen Beschaffungskategorie für eine bestimmte Summe zu kaufen. Das **Menge**- und **Einheit**-Feld ist nicht verfügbar.

Positionen im gleichen Kaufvertrag können unterschiedliche Arten von Zusagen haben.

## <a name="pricing-terms-for-sales-agreements"></a>Preisgestaltungsbedingungen für Kaufverträge
Die Preisgestaltungsbedingungen können je nach Typ der Zusage variieren. Bei einem Auftrag, der mit einem Kaufvertrag verknüpft ist, überschreiben die Preisstellungen aus dem Kaufvertrag alle anderen Preisstellungen, die auf Grundlage von Handelsvereinbarungen gelten. In der folgenden Tabelle werden die preisbezogene Felder beschrieben, die von jedem Zusagetyp betroffen sind. "Ja" legt fest, dass das Feld in einer Auftragsposition aktualisiert werden kann.

| Zusagetyp                   | Preis je Einheit | Preiseinheit | Rabatt in Prozent | Skontobetrag |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produktmengenzusage       | Ja        | Ja        | Ja              | Ja                  |
| Produktwertzusage          |            |            | Ja              |                      |
| Produktkategorie-Wertzusage |            |            | Ja              |                      |
| Wertzusage                  |            |            | Ja              |                      |

## <a name="policies-for-sales-agreements"></a>Richtlinien für Kaufverträge
Die folgenden Richtlinien wirken sich auf die Verknüpfung zwischen einer Kaufvertragszusage und den entsprechenden Auftragspositionen aus:

-   **Maximum wird erzwungen**: Die Gesamtmenge oder der Betrag für alle Auftragspositionen darf die Menge oder Summe nicht überschreiten, der auf der zugehörigen Zusage angegeben ist.
-   **Festpreis und ‑rabatt** – Der Preis in einer Auftragsposition und der Preis auf der entsprechenden Zusage können nicht unterschiedlich sein. Wenn der Preis in der Auftragsposition geändert wird, ist die Verknüpfung mit der Zusage aufgehoben. Wenn die Verknüpfung aufgehoben ist, trägt die Auftragsposition nicht zur Erfüllung der Zusage bei.
-   **Mindestfreigabebetrag** und **Höchstfreigabebetrag** – Wenn ein Betrag angegeben ist, erhalten Sie eine Meldung, wenn Sie Änderungen an einer Auftragsposition vornehmen, die bewirken, dass sich die Auftragsposition von der zugehörigen Zusage unterscheidet.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Erfüllungsberechnungen für Kaufverträge
Die **Erfüllung**-Registerkarte auf dem **Positionsdetails**-Inforegister auf der **Kaufverträge**-Seite zeigt Erfüllungsmengen und Beträge an.  

Im Bereich **Erfüllung** können Sie die Gesamtmengen und Beträge für alle Auftragspositionen anzeigen, die mit dem angegebenen Kaufvertrag verknüpft sind. Sie können auch den Restbetrag oder die Menge anzeigen, die benötigt wird, um die Zusage zu erfüllen.  

Im Bereich **Vereinbarung** können Sie die Mengen und die Beträge aus dem angegebenen Kaufvertrag anzeigen. Diese Mengen und Beträgen sind die Gesamtmengen und die Beträge, die zugesagt wurden.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Bestätigungen sowie Versionshistorie für Kaufverträge
Wenn Sie einen Kaufvertrag bestätigen, wird die aktuelle Version des Kauftrags in einer Historientabelle gespeichert. Wenn Sie den Kaufvertrag ändern, können Sie ihn erneut bestätigen, um eine andere Version des Kaufvertrags in der Historie zu speichern.  

Wenn Sie einen Kaufvertrag nicht bestätigen, können Sie ihn trotzdem zum Erstellen von Bestellungen verwendet. Allerdings werden Informationen für den Kaufvertrag nicht gespeichert.  

Sie können alle Überarbeitungen der Bestätigungen in der Vorschau anzeigen oder drucken. Sie können die Überarbeitungen dann an den Debitor weitergeben, um sie genehmigen zu lassen.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Anwenden von Kaufverträgen während des Bestellungsprozesses
Wenn Sie keine Aufträge direkt für Kaufverträge freigeben, können Sie trotzdem während des Auftragserfassungsprozesses einen Kaufvertrag mit einem Auftrag verknüpfen. Wenn Sie einen neuen Auftrag erstellen und einen Kaufvertrag auswählen, werden die Bedingungen dieses Vertrags (z. B. die Zahlungsbedingungen, Lieferbedingungen und die Lieferadresse) für den Auftragskopf angewandt und die Verknüpfung zwischen der Vereinbarung und dem Auftrag wird erstellt. In den Auftragspositionen, in denen Sie Produkte und Kategorien auswählen können, die im Kaufvertrag angegeben sind, werden die Preise und Rabatte von dieser Vereinbarung kopiert. Der gleiche Auftrag kann sowohl Positionen enthalten, die mit keinem Kaufvertrag verknüpft sind, als auch Positionen, für die eine Zusage in einem Kaufvertrag besteht.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Aufträge ändern, die mit Kaufverträgen verknüpft sind
Wenn Sie einen Auftrag gegen einen Kaufvertrag erstellt haben (freigegeben), können einige Felder für die Auftragspositionen nur dann geändert werden, wenn Sie die Verknüpfung mit den zugeordneten Kaufvertragspositionen entfernen. In der folgenden Tabelle werden einige dieser Felder aufgeführt:

| Feld                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Angefordertes Lieferdatum                                               | Wenn Sie das angeforderte Lieferdatum auf ein Datum festlegen, das vor dem Wert für **Gültigkeitsdatum.** der Kaufvertragsposition liegt, müssen Sie die Verknüpfung mit der Kaufvertragsposition entfernen, um das geänderte Lieferdatum speichern zu können. Wenn Sie das angeforderte Lieferdatum auf ein Datum festlegen, das nach dem Wert für **Ablaufdatum:** der Kaufvertragsposition liegt, müssen Sie die Verknüpfung mit der Kaufvertragsposition entfernen, um das geänderte Lieferdatum speichern zu können. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet Betrag | Wenn Sie den Wert in einem dieser Felder ändern, während für eine zugeordnete Kaufvertragsposition das Kontrollkästchen **Festpreis und -rabatt** aktiviert ist, wird ein Dialogfeld zum Speichern der Änderung angezeigt: Klicken Sie auf **Ja**, um die Verknüpfung mit der Kaufvertragsposition zu entfernen und den Preis neu zu berechnen. Klicken Sie auf **Nein**, um die Verknüpfung mit der Kaufvertragsposition ohne erneute Berechnung des Preises zu entfernen.                                                                   |
| Nettobetrag                                                        | Wenn der von Ihnen angegebene Betrag den Betrag überschreitet, der in einer Kaufvertragsposition mit aktiviertem Kontrollkästchen **Max. Menge** angegeben ist, müssen Sie den Aufforderungen im Dialogfeld zum Speichern des geänderten Betrags folgen. Klicken Sie auf **Ja**, um die Verknüpfung mit der Kaufvertragsposition zu entfernen und den Preis neu zu berechnen. Klicken Sie auf **Nein**, um die Verknüpfung mit der Kaufvertragsposition ohne erneute Berechnung des Preises zu entfernen.                                                                 |
| Menge                                                          | Wenn die von Ihnen angegebene Menge die Menge überschreitet, die in einer Kaufvertragsposition mit aktiviertem Kontrollkästchen **Maximum wird erzwungen** angegeben ist, wird ein Dialogfeld zum Speichern der geänderten Menge angezeigt: Klicken Sie auf **Ja**, um die Verknüpfung mit der Kaufvertragsposition zu entfernen und den Preis neu zu berechnen. Klicken Sie auf **Nein**, um die Verknüpfung mit der Kaufvertragsposition ohne erneute Berechnung des Preises zu entfernen.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Rückgabe eines Artikels, der aus einem Kaufvertrag bestellt wurde
Wenn ein Kunde einen Produkt zurückgibt, das durch einen Kaufvertrag bestellt wurde, kann Microsoft Dynamics 365 for Finance and Operations die zugehörige Kaufvertragszusage suchen und automatisch aktualisieren, um die Änderung in der Menge oder im Betrag widerzuspiegeln. Wenn Sie eine Rücklieferung basierend auf dem Originalauftrag erstellen, die mit einem Kaufvertrag verknüpft ist, richten Sie eine Beziehung zwischen der Kaufvertragszusage, der Auftragsposition und der Rücklieferungsrechnung ein.  

Wenn Sie die Menge der zurückgegebenen Artikel nicht aus der Kaufvertragszusage abgezogen werden soll, können Sie das **Verknüpfung entfernen**-Steuerelements auf der Seite **Rücklieferung** verwenden, um die Verknüpfung zwischen der Rücklieferung und dem Kaufvertragszusage zu entfernen. Wenn Sie den Link später neu einrichten müssen, klicken Sie auf **Verknüpfung erstellen**.  

**Hinweis:** Eine Rücklieferung kann mit nur einem Kaufvertrag verknüpft werden. Wenn Ihre Debitoren mehr als ein Produkt retourniert, das von mehr als einem Kaufvertrag bestellt wurde, müssen Sie eine neue Rücklieferung für jedes Produkt erstellen und eine Verbindung zum entsprechenden Rahmenbestellung erstellen.

## <a name="automatic-search-for-sales-agreements"></a>Automatische Suche nach Kaufverträgen
In bestimmten Situationen, in den Aufträge indirekt erstellt werden (beispielsweise, wenn Sie eine Gutschrift oder Intercompany-Aufträge erstellen), können Sie steuern, ob Microsoft Dynamics 365 for Finance and Operations automatisch nach gültigen Kaufverträgen sucht.

## <a name="financial-dimensions-on-sales-agreements"></a>Finanzdimensionen in Kaufverträgen
Sie können Finanzdimensionen in Dokumentüberschriften oder einzelne Positionen eines Kaufvertrags kopieren. Sie können die Dimensionen bei einem Vereinbarungskopf oder -Vereinbarungsposition jederzeit ändern. In diesem Fall werden die Dimensionen automatisch auf den Freigabenkopf oder die Freigabenposition von Freigabeaufträgen kopiert.




