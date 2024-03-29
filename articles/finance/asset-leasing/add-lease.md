---
title: Mietverträge hinzufügen oder kopieren (Vorschau)
description: In diesem Artikel wird beschrieben, wie Sie einen neuen Mietvertrag erstellen, indem Sie Informationen dazu im Anlagenleasing eingeben oder Informationen aus einem vorhandenen Mietvertrag kopieren.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880931"
---
# <a name="add-or-copy-leases-preview"></a>Mietverträge hinzufügen oder kopieren (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie im Anlagenleasing einen Mietvertrag von Grund auf neu erstellen und wie Sie einen Mietvertrag durch Kopieren eines vorhandenen Mietvertrags erstellen. Der Prozess zum Erstellen eines Mietvertrags von Grund auf umfasst das Eingeben von Informationen für den neuen Mietvertrag und das anschließende Erstellen eines Mietplans. Nachdem mindestens ein Mietvertrag eingerichtet wurde, ist es möglicherweise einfacher, die Informationen aus einem vorhandenen Mietvertrag zu kopieren und diese Informationen dann zu bearbeiten, wenn Sie einen neuen Mietvertrag erstellen möchten.

## <a name="create-a-lease"></a>Einen Mietvertrag erstellen

Gehen Sie folgendermaßen vor, um einen Mietvertrag im Analgenleasing zu erstellen.

1. Wählen Sie auf der Seite **Mietvertragsübersicht** im Aktivitätsbereich **Neu** aus.
2. Geben Sie die Informationen zum Mietvertrag ein. Erforderliche Felder haben rote Ränder.

Das Startdatum für die Mietzahlung darf nicht vor dem Mietstartdatum liegen. Wenn Sie ein Startdatum für die Mietzahlung eingeben, das vor dem Startdatum für die Miete liegt, erhalten Sie eine Fehlermeldung.

Standardmäßig ist die **Aufschlüsselungszahlungsbetrag**-Option im Inforegister **Allgemein** der **Mietdetails**-Seite auf **Nein** eingestellt ist, wenn die **Zahlungsaufschlüsselung zulassen**-Option auf der **Parameter des Anlagenleasing**-Seite auf **Ja** eingestellt ist. 

Wenn die **Aufschlüsselungszahlungsbetrag**-Option auf **Ja** eingestellt ist, ist das **Zahlungsbetrag**-Feld auf dem Inforegister **Zahlungsplanpositionen** gesperrt. Er wird auf die Summe der Zahlungsbeträge gesetzt, die später im **Aufschlüsselung des Zahlungsbetrags**-Katalog eingegeben werden.

Wählen Sie **Aufschlüsselung des Zahlungsbetrags**, um eine Seite zu öffnen, auf der Sie die einzelnen Zahlungstypen hinzufügen können. Die **Summen zum Zahlungsbetrag addieren**-Schaltfläche verschiebt die Summen in das **Zahlungsbetrag**-Feld.

> [!NOTE]
> Wenn Sie einen aufgeschlüsselten Zahlungsbetrag hinzufügen und dann die **Esc**-Taste auswählen, werden die eingegebenen Beträge nicht zum **Zahlungsbetrag**-Feld auf dem **Zahlungsplanpositionen**-Inforegister hinzugefügt. Stattdessen werden sie im **Aufschlüsselung des Zahlungsbetrags**-Dialogfeld gespeichert. Wenn Sie möchten, dass das Dialogfeld den Gesamtbetrag anzeigt, wählen Sie die **Höhe**-Spalte aus, wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) und wählen Sie dann **Diese Spalte summieren**. 

Die **Zeile kopieren**-Schalfläche kopiert die aufgeschlüsselte Zahlungsaufschlüsselung.

## <a name="create-a-lease-schedule"></a>Einen Mietplan erstellen

Führen Sie die folgenden Schritte aus, um einen Mietplan zu erstellen, nachdem Sie die Informationen für den Mietvertrag eingegeben haben.

> [!NOTE]
> Die Finanzdimensionen können sich basierend auf benutzerdefinierten Finanzdimensionen ändern.

1. Wählen Sie **Zeitpläne erstellen** aus, um die Leasingbücher zu generieren. Die Leasingbücher enthalten die Zahlungs-, Amortisations-, Abschreibungs- und Ausgabenpläne.
2. Wählen Sie die Registerkarte **Bücher** aus, um auf die Leasingbücher zuzugreifen und die neu erstellten Zeitpläne anzuzeigen.

    Die Seite **Buchdetails** zeigt, wie der Mietvertrag durch die ihm zugewiesenen Bücher bilanziert wird. Von hier aus können Sie die Mietpläne anzeigen.

    Der Zahlungsplan enthält die Eingaben aus der **Zahlungsplanezeilen**-Registerkarte auf der **Mietvertrag hinzufügen**-Seite. Sie können weiterhin jeden Zahlungsbetrag und jede variable Zahlung ändern. Die Leasingverbindlichkeit wird anhand des geänderten Zahlungsplans berechnet.

    > [!NOTE]
    > Das Startdatum für die Mietzahlung muss mit dem Mietbeginn gleich oder nach dem Mietbeginn liegen. Wenn Sie ein Startdatum für die Zahlung eingeben, das vor dem Startdatum für die Miete liegt, erhalten Sie eine Fehlermeldung. 

4. Nachdem Sie den Zahlungsplan überprüft haben, wählen Sie **Zeitplan bestätigen**. Nachdem der Zeitplan bestätigt wurde, kann der Mietvertrag nicht mehr bearbeitet werden.

    > [!NOTE]
    > Das System berechnet die Mietdauer automatisch aus den Zahlungsplänen auf der **Mietvertrag hinzufügen**-Seite.
    >
    > Um die Mietdauer in Monaten zu berechnen, ermittelt das System die Differenz zwischen dem Startdatum und dem Enddatum für eine bestimmte Zahlungsplanzeile. Es wechselt dann zur nächsten Zahlungsplanzeile und ermittelt die Differenz erneut. Schließlich summiert das System alle Beträge, um die Mietdauer in Monaten zu bestimmen.

5. Öffnen Sie die Seite **Zeitplan zur Amortisierung von Leasingverbindlichkeiten**, um die berechneten Zinsaufwendungen für den Zeitraum anzuzeigen. Um die berechnete lineare Abschreibung anzuzeigen, öffnen Sie die Seite **Abschreibungsplan für Anlagen**.
6. Nachdem Sie den berechneten Betrag überprüft haben, können Sie den ersten Journaleintrag der erstmaligen Erfassung auf der Seite **Erstmalige Erfassung**. Sie erhalten eine Nachricht, dass die Erfassung erstellt wurde.

    > [!NOTE]
    > Der Journaleintrag wird erst in das Hauptbuch gebucht, wenn Sie den Eintrag manuell buchen.

7. Um den vorgeschlagenen Eintrag für die erstmalige Erfassung zu überprüfen, bevor Sie ihn buchen, wählen Sie **Erfassung für das Anlagenleasing**.

    > [!NOTE]
    > Die Erfassung für das Anlagenleasing kann nicht manuell erstellt werden. Es wird automatisch erstellt, wenn Mietpläne erstellt werden.

8. Wenn Sie den Journaleintrag für die erstmalige Erfassung überprüft haben und bereit sind, ihn zu buchen, wählen Sie **Buchen** aus, um das Nutzungsrecht am Leasingobjekt und die Leasingverbindlichkeit im Hauptbuch zu erfassen.

## <a name="copy-a-lease"></a>Einen Mietvertrag kopieren

Mit Anlagenleasing können Sie die Details eines Mietvertrags kopieren, um einen neuen Mietvertrag mit denselben Informationen zu erstellen. Sie können dann die Mietvertragsfelder ändern, bevor Sie die Zeitpläne für den kopierten Mietvertrag erstellen.

1. Wählen Sie auf der Seite **Mietvertragsübersicht** den zu kopierenden Mietvertrag und dann im Aktionsbereich die Option **Mietvertrag kopieren** aus.

    > [!NOTE]
    > Wenn der **Manuell**-Parameter für die Nummernfolge für Mietvertrags-IDs deaktiviert ist, wird die nächste Nummer in der Sequenz automatisch als Mietvertrags-ID des kopierten Mietvertrags generiert. Wenn der **Manuell**-Parameter aktiviert ist, erhalten Sie eine Nachricht, in der Sie aufgefordert werden, die Mietvertrags-ID einzugeben, bevor Sie mit dem Kopieren des Mietvertrags fortfahren.

2. Wählen Sie **Kopieren**. Die Mietvertragsdetails aus dem ausgewählten Mietvertrag werden in einen neuen Mietvertrag kopiert. Sie können dann die Details des neuen Mietvertrags bearbeiten, bevor Sie ihn speichern und die Mietpläne erstellen.

## <a name="asset-leasing-journal"></a>Erfassung für Anlagenleasing

Alle Journaleinträge, die im Anlagenleasing erstellt werden, sind in der Erfassung für Anlagenleasing enthalten. Auf der **Erfassung für Anlagenleasing**-Seite (**Anlagenleasing \> Journaleinträge \> Erfassung für Anlagenleasing**) können Sie nach Buchungsstatus filtern, bestimmte Journaleinträge und Belege anzeigen und nicht gebuchte Journaleinträge buchen.

> [!NOTE]
> Die Erfassung für das Anlagenleasing kann nicht manuell erstellt werden. Es wird automatisch erstellt, wenn Mietpläne erstellt werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
