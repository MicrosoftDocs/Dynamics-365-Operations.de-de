---
title: Kreditorenzahlungen des Typs „Zahlung bei Zahlungsempfang“ einrichten und verwenden
description: In diesem Thema wird erläutert, wie Sie Bedingungen für Zahlungen bei Zahlungsempfang erstellen, damit Sie basierend auf Debitorenzahlungen Teilzahlungen für die Kreditoren freigeben können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284112"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Kreditorenzahlungen des Typs „Zahlung bei Zahlungsempfang“ einrichten und verwenden

[!include [banner](../includes/banner.md)]

Wenn Sie einen Kreditor als Zulieferer für ein Projekt genehmigen, möchten Sie möglicherweise die Zahlung an den Kreditor aussetzen, bis Sie von Ihrem Debitor für das Projekt bezahlt wurden. Um dieses Szenario zu unterstützen, richten Sie Bedingungen für Zahlungen bei Zahlungsempfang ein, wenn Sie die Bestellung mit dem Kreditor vereinbaren.

Wenn beispielsweise ein Debitor einen Betrag einer Projektrechnung bezahlt, können Sie einen Teilbetrag oder den gesamten Betrag der Kreditorenrechnung freigeben. Richten Sie einfach Bedingungen für Zahlungen bei Zahlungsempfang ein, um die Zahlung eines Kreditors festzulegen, nachdem Sie einen Prozentsatz der zugehörigen Zahlung vom Debitor erhalten haben. Wenn Sie Teilzahlungen von einem Debitor erhalten, können Sie einige der zugehörigen Kreditorenrechnungen manuell zur Zahlung freigeben.

Das folgende Beispiel beschreibt den Prozess bei Verwendung von Bedingungen für Zahlungen bei Zahlungsempfang.

## <a name="example"></a>Beispiel

Ihre Organisation erklärt sich damit einverstanden, einem Kunden 100 Computer mit installierter Software zum Preis von 150,00 US-Dollar (USD) pro Computer zu liefern. Anschließend beauftragen Sie einen Kreditor mit der Bereitstellung der Computer, auf denen Software installiert ist. Laut der Vereinbarung muss der Debitor die Qualität der Computer sicherstellen, bevor er an Ihre Organisation zahlt. Die Richtlinie Ihrer Organisation besagt, Zahlungen an Kreditoren zurückzuhalten, bis der Debitor Sie bezahlt hat. Daher richten Sie das Projekt so ein, dass es einen Prozentsatz von 100 Prozent für Zahlungen bei Zahlungsempfang aufweist.

Der Kreditor sendet Ihnen die 100 Computer mit der installierten Software zusammen mit einer Rechnung über 10.000,00 USD. Da für Ihr Projekt Bedingungen für Zahlungen bei Zahlungsempfang eingerichtet sind, zahlen Sie den Kreditor nicht nach Erhalt der Computer. Stattdessen senden Sie die Computer zusammen mit einer Rechnung über 15.000,00 USD an den Kunden. Der Debitor überprüft die Computer und genehmigt die Zahlung des vollständigen Rechnungsbetrags.

Nachdem Sie die vollständige Zahlung vom Debitor erhalten haben, bezahlen Sie dem Kreditor 10.000,00 USD, also den Gesamtbetrag der Kreditorenrechnung.

## <a name="set-up-pwp-terms-for-a-project"></a>Einrichten von Bedingungen für Zahlungen bei Zahlungsempfang für ein Projekt

Wenn Sie für ein Projekt Bedingungen für Zahlungen bei Zahlungsempfang einrichten, müssen Sie als Prozentsatz den Mindestbetrag angeben, den ein Debitor für das Projekt bezahlen muss, bevor Sie den Kreditor bezahlen. Der Schwellenbetrag wird automatisch auf den Debitorenrechnungen für das Projekt berechnet. Gehen Sie folgendermaßen vor, um den Schwellenwert in Prozent für Bedingungen für Zahlungen bei Zahlungsempfang einzurichten:

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projekte** \> **Alle Projekte**.
2. Suchen und öffnen Sie das Projekt, für das Sie Bedingungen für Zahlungen bei Zahlungsempfang einrichten möchten.
3. Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Position hinzufügen** aus.
3. Wählen Sie im Feld **Kontocode** eine der folgenden Optionen aus:

    - **Tabelle** - Die Bedingungen für Zahlungen bei Zahlungsempfang gelten für einen einzelnen Kreditor.
    - **Gruppe** – Die Bedingungen für Zahlungen bei Zahlungsempfang gelten für alle Kreditoren in einer Kreditorengruppe.
    - **Alle** – Die Bedingungen für Zahlungen bei Zahlungsempfang gelten für alle Kreditoren.

4. Wenn Sie im vorherigen Schritt **Tabelle** oder **Gruppe** ausgewählt haben, wählen Sie für das Feld **Kreditor/Kreditorengruppe** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für Zahlungen bei Zahlungsempfang gelten sollen. Wenn Sie im vorherigen Schritt **Alle** ausgewählt haben, kann das Feld **Kreditor/Kreditorengruppe** nicht bearbeitet werden.
5. Wenn für den Kreditor des Projekts Bedingungen für Kreditoreneinbehalte eingerichtet sind, wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Regelkennung für die Einbehaltungsbedingungen aus.
6. Geben Sie im Feld **Pay When Paid - Schwellenwertprozentsatz** den Schwellenwertprozentsatz für das Projekt ein. Der Prozentsatz, den Sie für das Projekt eingeben, definiert den Mindestbetrag, den Sie vom Debitor erhalten müssen, bevor Sie den Kreditor bezahlen.

## <a name="create-a-po-that-has-pwp-terms"></a>Erstellen einer Bestellung mit Bedingungen für Zahlungen bei Zahlungsempfang

Wenn Sie eine Kreditorenrechnung buchen und der Kreditor abhängig von Bedingungen für Zahlungen bei Zahlungsempfang ist, werden diese Bedingungen in den Bestellpositionen angezeigt. Gehen Sie folgendermaßen vor, um eine Bestellung mit Bedingungen für Zahlungen bei Zahlungsempfang zu erstellen.

1. Wechseln Sie zu **Beschaffung** \> **Bestellungen** \> **Alle Bestellungen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus. Geben Sie anschließend im Dialogfeld **Bestellung erstellen** die erforderlichen Informationen ein und wählen Sie **OK** aus.

    Alternativ können Sie eine vorhandene Bestellung auf der Listenseite **Alle Bestellungen** öffnen.

4. Überprüfen Sie auf der Seite **Bestellung** im Inforegister **Bestellpositionen** die Details der Bestellposition für den Kreditor. Die Option **Zahlung bei Zahlungsempfang** wird automatisch ausgewählt und der Wert im Feld **Pay When Paid – Schwellenwertprozentsatz** wird automatisch aus dem Feld **Pay When Paid - Schwellenwertprozentsatz** auf der Seite **Projekte** kopiert.
6. Wenn Sie keine Bedingungen für Zahlungen bei Zahlungsempfang für eine Bestellposition auf den Kreditor anwenden möchten, deaktivieren Sie die Option **Zahlung bei Zahlungsempfang**. In diesem Fall wird das Feld **Pay When Paid – Schwellenwertprozentsatz** für die Bestellposition auf 0 (null) zurückgesetzt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualisieren einer Debitorenzahlung und Bezahlen des Kreditors

Wenn ein Kreditor seine Arbeit am Projekt abschließt und eine Rechnung übermittelt, müssen Sie den Projektstatus und die Debitorenrechnungen überprüfen, um festzustellen, ob die Bedingungen für Zahlungen bei Zahlungsempfang für das Projekt erfüllt wurden. Wenn die PWP-Begriffe für den Kreditor erfüllt wurden, können Sie auf Basis der Debitorenzahlungen für das Projekt entscheiden, welche Positionen auf der Kreditorenrechnung sie bezahlen. Wenn Sie sich entscheiden, den Kreditor zu bezahlen, obwohl die Bedingungen für Zahlungen bei Zahlungsempfang nicht erfüllt sind, können Sie die Bedingungen auf der Seite **Kreditorenrechnung mit Zahlung bei Zahlungsempfang** überschreiben.

1. Wechseln Sie zu **Projektmanagement und Buchhaltung** \> **Anfragen und Berichte** \> **Einbehaltungsanfragen** \> **Kreditorenrechnung mit Zahlung bei Zahlungsempfang**.
2. Geben Sie auf der Seite **Kreditorenrechnung mit Zahlung bei Zahlungsempfang** in das Suchfeld Werte ein, um die Kreditorenrechnung zu finden, die Sie prüfen möchten, und wählen Sie anschließend **Suchen** aus.
3. Wählen Sie im Inforegister **Kreditorenrechnungspositionen** die Positionen aus, die Sie ändern möchten.
4. Wenn die Bedingungen für **Zahlung bei Zahlungsempfang** für die Rechnungsposition erfüllt sind, wählen Sie **Kreditorenzahlung freigeben** aus. Die Option **Zahlung bei Zahlungsempfang** wird deaktiviert und der Wert für das Feld **Bereit für Zahlung** ändert sich in **Ja**.
