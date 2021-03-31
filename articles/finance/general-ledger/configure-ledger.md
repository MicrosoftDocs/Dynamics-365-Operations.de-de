---
title: Sachkonten konfigurieren
description: Dieses Thema enthält Informationen zum Konfigurieren von Sachkonten für jede juristische Person. Es enthält Informationen zur Auswahl von Währungen, Steuerkalendern, dem Kontenplan und den Kontostrukturen, die für jede juristische Person verwendet werden sollten.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d2d0bebbdde96e6751f749dfbc0d4cdedd4036a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212324"
---
# <a name="configure-ledgers"></a>Sachkonten konfigurieren

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zum Konfigurieren von Sachkonten für jede juristische Person. Es enthält Informationen zur Auswahl von Währungen, Steuerkalendern, dem Kontenplan und den Kontostrukturen, die für jede juristische Person verwendet werden sollten.

## <a name="selecting-the-chart-of-accounts"></a>Den Kontenplan auswählen

Für jede juristische Person in Microsoft Dynamics 365 Finance müssen Details zum Sachkonto konfiguriert werden. Auf der Seite **Sachkonto** können Sie den Kontenplan und die Kontostrukturen auswählen, die für die ausgewählte juristische Person verwendet werden. Sie können Ihren Kontenplan und die Kontostrukturen freigeben, indem Sie die Seite **Sachkonto** in jeder juristischen Person konfigurieren, um den gleichen Kontenplan und die gleichen Kontostrukturen zu verwenden. Sie können auch einen Teil der Konfiguration in jeder juristischen Person freigeben und in jeder juristischen Person bestimmte Konfigurationen festlegen.

Wenn Ihre juristischen Personen unterschiedliche Kontenpläne oder unterschiedliche Kontostrukturen haben müssen, kann die Funktion zum Überschreiben von juristischen Personen hilfreich sein. Indem Sie denselben Kontenplan und dieselben Kontostrukturen für mehrere juristische Personen verwenden und dann alle Ausnahmen durch Überschreibungen von juristischen Personen verwalten, können Sie die Wartung im Laufe der Zeit vereinfachen.

Um den Kontenplan für eine juristische Person zu konfigurieren, gehen Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Sachkonto**. Auf der Seite **Sachkonto** wählen Sie **Kontenplan** und dann in der Liste den zu verwendenden Kontenplan aus. Beachten Sie, dass der Kontenplan nicht geändert werden kann, nachdem Sie einen Wert ausgewählt und Transaktionen in der juristischen Person gebucht haben.

Weitere Informationen zum Planen und Konfigurieren des Kontenplans und der Hauptkonten finden Sie unter [Planen des Kontenplans](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Kontostrukturen auswählen

Jede juristische Person in Dynamics 365 Finance kann so konfiguriert werden, dass eine oder mehrere Kontostrukturen verwendet werden. Jede Kontostruktur definiert die finanziellen Dimensionen und die Kombinationen von Hauptkonten und finanziellen Dimensionen, die bei der Buchung von Transaktionen zulässig sind. Sie können dieselben Kontostrukturen in mehr als einer juristischen Person verwenden.

Beachten Sie, dass Sie bei mehreren Kontostrukturen nur Kontostrukturen auswählen können, die keine überlappenden Kombinationen aus Hauptkonten und Finanzdimensionen aufweisen. Beispielsweise ist eine Ihrer Kontostrukturen so konfiguriert, dass zwischen 1000 und 1999 ein Geschäftsbereich für Hauptkonten hinzugefügt wird. In einer anderen Kontostruktur haben Sie eine Abteilungsfinanzdimension für Hauptkonten hinzugefügt, die mit 1 beginnen. In diesem Fall kann nur eine der Kontostrukturen in derselben juristischen Person hinzugefügt werden.

Um Kontostrukturen für Ihr Sachkonto zu konfigurieren, klicken Sie auf der **Sachkonto**-Seite, auf das **Kontostrukturen**-Inforegister, wählen Sie **Hinzufügen**, eine Kontostruktur in der Liste und dann **Auswählen** aus. Es kann einige Minuten dauern, bis die Kontostrukturen hinzugefügt und gespeichert werden. Beachten Sie, dass die von Ihnen ausgewählten Kontostrukturen aktiv sein müssen. Andernfalls werden die Details der Kontostrukturen in den juristischen Personen, mit denen sie verknüpft sind, nicht wirksam.

Um eine Kontostruktur zu entfernen, klicken Sie auf die **Sachkonto**-Seite, wählen Sie im **Kontostrukturen**-Inforregister **Entfernen** aus. Beachten Sie, dass Sie beim Entfernen einer Kontostruktur aus Ihrem Sachkonto keine Transaktionen entfernen, die mithilfe der Konfiguration dieser Kontostruktur gebucht wurden.

Weitere Informationen zum Einrichten Ihrer Kontostrukturen finden Sie unter [Konfigurieren von Kontostrukturen](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Kalender für das Sachkonto konfigurieren

Ein weiterer Bestandteil des Sachkontos ist der Finanzkalender. Für jede juristische Person muss ein Steuerkalender ausgewählt werden. Sie können dieselben Finanzkalender in mehr als einer juristischen Person verwenden. Wenn Sie einen Finanzkalender für das Sachkonto auswählen, wird eine Kopie erstellt. Diese Kopie wird als Sachkontokalender bezeichnet. Im Sachkontokalender können Sie den Status der Perioden und der Module in jeder Periode auswählen.

Um auf den Kalender für die ausgewählte juristische Person zuzugreifen und ihn zu aktualisieren, klicken Sie auf **Sachkonto**, im Aktionsbereich wählen Sie die Option **Sachkontokalender** aus.

Um den Kalender auszuwählen, wählen Sie **Finanzkalender** und dann den Kalender in der Liste aus. Wenn Sie den Finanzkalender ändern, nachdem Transaktionen in der juristischen Person gebucht wurden, müssen Sie **Sachkontoperioden neu berechnen** auswählen. Anschließend können Sie im angezeigten Dialogfeld die Sachkontosalden für die Perioden in Ihrem Kalender aktualisieren. Wir empfehlen Ihnen, die den Prozess **Sachkontoperioden neu berechnen** im **Batch**-Modus ausführen, wenn unkritische Prozesse in Ihrem System auftreten. Abhängig von der Anzahl der Transaktionen und den Kombinationen der Finanzdimensionen kann dieser Vorgang einige Zeit dauern.

Wenn für eine juristische Person kein Finanzkalender ausgewählt ist, wird eine Fehlermeldung angezeigt, wenn Sie versuchen, eine Transaktion in dieser juristischen Person zu buchen.

Weitere Informationen finden Sie unter [Steuerkalender, Geschäftsjahre und Perioden](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Verwenden einer ausgleichenden Finanzdimension

Nachdem Sie den Kontenplan ausgewählt und eine oder mehrere Kontostrukturen hinzugefügt haben, können Sie optional eine einzelne Finanzdimension auswählen, die als finanzielle Ausgleichsdimension verwendet werden soll. Die von Ihnen ausgewählte Dimension muss in allen Kontostrukturen vorhanden sein. Sie muss auch in allen Buchhaltungseinträgen ausgeglichen sein. Mit anderen Worten, die Soll und Haben müssen für das Hauptkonto und die finanzielle Ausgleichsdimension gleich sein. Das System erstellt automatisch Transaktionen, um die Einträge auszugleichen. Dies geschieht basierend auf den Hauptkonten, die in der **Einheitenbezogen Haben** und **Einheitenbezogen Soll**-Feldern auf der **Konten für automatische Transaktion**-Seite angegeben sind.

Weitere Informationen zum Ausgleichen von Einträgen finden Sie unter [Ausgeglichene Erfassungen für einheitenbezogene Buchhaltung](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Wähungen für das Sachkonto konfigurieren

Die **Sachkonto**-Seite wird auch verwendet, um die Währungen zu steuern und zu definieren, die verwendet werden, wenn Transaktionen in das Sachkonto gebucht werden. Sie müssen die Buchhaltungswährung angeben. Dies ist die Währung, die in der **-Buchhaltungswährung** -Spalte im Hauptbuch auf allen Belegen verwendet wird. Außerdem können Sie in der Spalte **Berichtswährung** optional eine zweite Währung auswählen. Wenn Sie eine Berichtswährung auswählen, werden alle Transaktionen in dieser Währung in der **Berichtswährung**-Spalte im Hauptbuch auf allen Belegen erfasst.

Wenn Transaktionen in einer anderen Währung gebucht werden, rechnet das System den Transaktionsbetrag automatisch von der Transaktionswährung in die Buchungswährung und die Berichtswährung auf dem Beleg um. Wählen Sie auf der **Sachkonto**-Seite, im Feld **Wechselkurstyp der Buchhaltungswährung** den Wechselkurstyp aus, der für die Wechselkurse konfiguriert ist, die zum Umrechnen von Werten von der Transaktionswährung in die Buchhaltungswährung auf einem Beleg verwendet werden sollen. Wenn Sie eine Berichtswährung ausgewählt haben, müssen Sie auch das Feld **Wechselkurstyp der Berichtswährung** festlegen, um den Wechselkurs anzugeben, der zum Umrechnen von Werten von der Transaktionswährung in die Berichtswährung auf einem Beleg verwendet werden soll.

Wenn Sie die Budgetierungsfunktion verwenden, können Sie auch das Feld **Budget -Wechselkurstyp** festlegen, um den Wechselkurs anzugeben, der zum Umrechnen von Budgettransaktionen von einer Währung in eine andere verwendet werden soll.

Wenn Sie zwei Währungen oder eine einzige Währung verwenden, Transaktionen jedoch in einer anderen Währung gebucht werden, müssen Sie das Inforegister **Konten für die Neubewertung von Währungen** auf der Seite **Sachkonto** konfigurieren. Auf diesem Inforegister definieren Sie die standardmäßig realisierten und nicht realisierten Gewinn- und Verlustkonten, die standardmäßig verwendet werden, wenn Transaktionen gebucht werden, sofern auf der Seite **Konten für die Neubewertung von Währungen** kein Konto angegeben ist. (Die Seite **Konten für die Neubewertung von Währungen** wird verwendet, um verschiedene Konten für realisierte und nicht realisierte Gewinne und Verluste für jede Währung zu konfigurieren.)

Realisierte Gewinne und Verluste sind Gewinne und Verluste aus abgeschlossenen Transaktionen. Sie werden in der Gewinn- und Verlustrechnung erfasst. Nicht realisierte Gewinne und Verluste sind Gewinne und Verluste, die eingetreten sind, aber die Transaktion ist noch nicht abgeschlossen. Mit anderen Worten, Sie haben beispielsweise eine Rechnung gebucht, aber die Rechnung ist noch nicht beglichen und bezahlt. Nicht realisierte Gewinne und Verluste werden in der Bilanz erfasst.

Weitere Informationen darüber, wie Sie zwei Währungen verwenden, finden Sie unter [Duale Währung](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]