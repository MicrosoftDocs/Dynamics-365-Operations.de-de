--- 
title: Freitextrechnungen erstellen
description: "In diesem Thema wird erläutert, wie Freitextrechnungen erstellt werden."
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: f64292a1b3726ea9b43f959a44c4ed2a1f392484
ms.openlocfilehash: f6ee6fda0b52b8af7c253b7d22e470345a8a421f
ms.contentlocale: de-de
ms.lasthandoff: 09/05/2018

---

# <a name="create-free-text-invoices"></a>Freitextrechnungen erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Freitextrechnungen erstellt werden. Für diese Prozedur wird das Demo-Unternehmen **USMF** verwendet.

## <a name="create-a-free-text-invoice"></a>Freitextrechnung erstellen

1. Wechseln Sie zu **Debitoren \> Rechnungen \> Alle Freitextrechnungen**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Debitorenkonto** einen Wert aus.

    * Das Rechnungskonto wird standardmäßig auf dasselbe Konto festgelegt, das für das Rechnungskonto verwendet wird.
    * Der Buchhaltungsstatus beginnt mit **In Bearbeitung**, wenn die Rechnung nicht gebucht wird.
    * Die Rechnungsnummer wird zugewiesen, wenn die Rechnung gebucht wird.
    * Wenn Sie einheitliche Euro-Zahlungsverkehrsraum-Vollmachten (SEPA) verwenden, wird das Direkteinzugsmandat automatisch mit einer Vollmacht aufgefüllt, wenn Sie das Debitorenkonto auswählen.

4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Hauptkonto** eine Kontonummer ohne Dimensionen an. Sie öffnen Finanzdimensionen weiter unten in diesem Handbuch.

    Sie können auch ein oder mehrere Zeichen für das Hauptkonto eingeben und die Suche verwenden, um Ihr Konto zu suchen.

6. Erweitern Sie das Inforegister **Positionsdetails**, sodass Sie Ihrem Hauptkonto Dimensionen hinzufügen können.
7. Klicken Sie auf die Registerkarte **Finanzdimensionsposition**.

    * Die Dimensionen sind nur für die ausgewählte Position.
    * Die Mehrwertsteuergruppe wird standardmäßig aus dem Debitorendatensatz übernommen. Wenn der Debitor keine Mehrwertsteuergruppe aufweist, wird die Mehrwertsteuergruppe aus dem Hauptkonto verwendet.
    * Die Artikel-Mehrwertsteuergruppe wird vom Hauptkonto aufgefüllt. Wenn das Hauptkonto keine Artikel-Mehrwertsteuergruppe aufweist, wird die Artikel-Mehrwertsteuergruppe in den Mehrwertsteuerparametern für das Hauptbuch verwendet.

8. Optional: Geben Sie im Feld **Menge** eine Zahl ein.
9. Optional: Geben Sie im Feld **Einheitspreis** eine Zahl ein.

    Der Betrag wird als Menge mal Preis je Einheit berechnet. Sie können diese Berechnung jedoch außer Kraft setzen und einen Betrag eingeben.

10. Klicken Sie auf **Mehrwertsteuer**, um die Mehrwertsteuer anzuzeigen, die für Ihre Rechnung berechnet wird.

    Zeigen Sie die Mehrwertsteuerbeträge auf dieser Seite an oder Sie können die Beträge auf der Registerkarte **Regulierung** überschreiben.

11. Wählen Sie **OK**.
12. Klicken Sie auf **Belastungen**, um der Rechnung eine Belastung hinzuzufügen.
13. Geben Sie im Feld **Belastungen** einen Wert ein.
14. Geben Sie im Feld **Wert der Belastungen** eine Zahl ein.
15. Schließen Sie die Seite.
16. Klicken Sie auf **Summen**, um die zusammengefassten Rechnungsdetails und Summen anzuzeigen.
17. Wählen Sie **Schließen** aus.
18. Wählen Sie **Buchen** aus, um die Rechnung zu buchen. Sie haben noch eine Verkaufschance zu stornieren, bevor Sie buchen.

    * Sie können die Zeit des Rechnungsdruckes zu ändern. Wählen sie **Aktuell** um jede Rechnung zu drucken, wenn diese aktualisiert wird Wählen Sie **Später**, um alle Rechnungen zu drucken, die aktualisiert wurden.
    * Um zu ändern wie die Kreditlimite geprüft wird, bevor die Rechnung gebucht wird, ändern Sie den Wert im Feld **Kreditlimit-Typ**.
    * Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu drucken.
    * Aktivieren Sie diese Option auf **Ja**, um die Rechnung zu buchen. Sie können die Rechnung ohne Buchen drucken.

19. Wählen Sie **OK**.

## <a name="copy-lines"></a>Positionen kopieren
Um die Positionen auf der Freitextrechnung zu kopieren, wählen Sie eine oder mehrere Positionen aus und gehen anschließend auf **ausgewählte Positionen kopieren**. Sie können die Anzahl von Kopien angeben, die Sie erstellen möchten, und Sie können Hinweise und Anhänge kopieren. Sie können die Verteilungen kopieren oder zulassen, dass sie neu erstellt werden, wenn Sie buchen.

Anschließend können Sie die Informationen nach Bedarf bearbeiten.

## <a name="create-a-free-text-invoice-from-a-template"></a>Erstellen einer Vorlage für Freitext-Serienrechnungen
Sie können eine Freitext-Rechnung von einer Vorlage erstellen. Wenn Sie **Neu von Vorlage** aus der **Rechnungs**registerkarte auswählen, können Sie einen Vorlagennamen gür die neue Freitextrechnung auswählen. Sie können die Standardwerte wie die Zahlungsbedingungen und die Zahlungsmethode der Zahlung auch auswählen oder die Werte verwenden, , die mit der Vorlage gespeichert wurden.

Eine neue Freitextrechnung wird erstellt und Sie können die Werte in dieser Rechnung bearbeiten.

