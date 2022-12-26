---
title: Häufig gestellte Fragen zu Aktivitäten am Jahresende
description: In diesem Artikel werden Fragen aufgelistet, die zum Jahresabschluss auftreten können, sowie die Antworten, die bei Aktivitäten zum Jahresabschluss hilfreich sein können.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853039"
---
# <a name="year-end-activities-faq"></a>Häufig gestellte Fragen zu Aktivitäten am Jahresende 

[!include [banner](../includes/banner.md)]

In diesem Artikel werden Fragen aufgelistet, die zum Jahresabschluss auftreten können, sowie die Antworten, die bei Aktivitäten zum Jahresabschluss hilfreich sein können. Es geht überwiegend um Fragen zum Jahresabschluss von Hauptbuch und Kreditorenkonten.

## <a name="general-ledger-year-end-enhancements"></a>Jahresendoptimierungen für Hauptbuch

In Version 10.0.20 von Microsoft Dynamics 365 Finance wurde eine Erweiterung zum Jahresabschluss eingeführt. Ab Version 10.0.25 ist diese Erweiterung standardmäßig aktiviert und ab Version 10.0.29 obligatorisch. Wenn Ihr Unternehmen eine frühere Version als 10.0.25 verwendet, empfehlen wir, diese Funktion zu aktivieren, bevor Sie mit dem Jahresabschlussprozess beginnen. Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit dem Arbeitsbereich **Funktionsverwaltung** den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Modul:** Hauptbuch
- **Funktionsname:** Erweiterung zum Jahresendabschluss des Hauptbuchs

Die Einrichtung der Jahresabschlussvorlagen wurde auf eine neue Einrichtungsseite verschoben, **Einrichtung der Vorlage für Jahresendabschluss**. Die vorhandene Jahresendabschlussseite wird auf ähnliche Weise geändert wie bei der Seite **Neubewertung der Fremdwährung im Hauptbuch**, sodass bei jeder Ausführung oder Stornierung des Jahresendabschlusses eine Liste angezeigt wird. Auf der Seite werden keine Verlaufsinformationen zu Jahresabschlüssen angezeigt, die vor der Aktivierung der Funktion vorgenommen wurden. Ein Buchhaltungsleiter kann den Jahresendabschluss von der neuen Seite aus einleiten.

Um den Jahresendabschluss rückgängig zu machen, wählen Sie das letzte Geschäftsjahr für die entsprechende juristische Person und dann **Jahresendabschluss rückgängig machen** aus. Durch die Stornierung werden die Buchungseinträge für den vorherigen Jahresendabschluss gelöscht und wird der Jahresendabschluss nicht automatisch erneut ausgeführt. Wenn Sie die Funktion **Jahresendoptimierungen für Hauptbuch** aktivieren, nachdem Sie einen Jahresabschluss vorgenommen haben, und Sie die historischen Jahresendergebnisse stornieren möchten, führen Sie die historischen Jahresabschluss erneut aus, nachdem Sie den Hauptbuch-Parameter **Vorhandene Jahresabschlusseinträge beim erneuten Jahresabschluss löschen** aktivieren.

Sie können den Jahresendabschluss wiederholen, indem Sie den Prozess für das Geschäftsjahr und die juristische Person erneut starten. Der Prozess verwendet weiterhin die Hauptbuch-Parametereinstellung, um zu bestimmen, ob die Wiederholung des Jahresendabschlusses nur die neuen oder geänderten Transaktionen berücksichtigt oder den Prozess für alle Transaktionen erneut ausführt und den vorherigen Abschluss vollständig rückgängig macht.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Hauptbuch: Die Funktion „Jahresendoptimierungen für Hauptbuch“ ist aktiviert. Warum kann ich meine vorherigen Jahresabschlüsse nicht im Abschnitt „Verlauf“ auf der Seite „Jahresabschluss“ sehen?

Vor der Aktivierung der Funktion **Jahresendoptimierungen für Hauptbuch** werden Datum und Uhrzeit der letzten Ausführung des Jahresabschlussprozesses nachverfolgt. Der Verlauf wurde nicht jedes Mal, wenn der Jahresabschluss durchgeführt wurde, aufgezeichnet. Aus diesem Grund können die Details der einzelnen Jahresabschlussläufe nicht angezeigt werden. Nach der Aktivierung der Funktion werden die nachfolgenden Jahresabschluss-Prozessinformationen beibehalten. Auf der Seite **Buchungen für Beleg** können Belege aus allen Jahresabschlussprozessen, auch denen, die vor der Funktionsaktivierung ausgeführt wurden, angezeigt werden. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Hauptbuch: Der Jahresabschlussprozess schlägt aufgrund des folgenden Fehlers fehl: „Der Jahresabschluss kann nicht ausgeführt werden, da eine oder mehrere Sachkontobuchungen, die in das Geschäftsjahr gebucht wurden, das Sie abschließen, für eine Sachkontobuchung in einem anderen Geschäftsjahr abgerechnet wurden.“ Was bedeutet dieser Fehler?

Da die Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** aktiviert ist, werden nur abgerechnete Hauptbuchtransaktionen aus dem Geschäftsjahr, das abgeschlossen wird, aus dem Anfangssaldo ausgeschlossen. Dies führt dazu, dass Soll und Haben nicht ausgeglichen sind. Weitere Informationen finden Sie unter [Unterschied zwischen Sachkontoausgleich und Jahresendabschluss](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Hauptbuch: Die Umkehrung des Jahresabschlussprozesses schlägt aufgrund des folgenden Fehlers fehl: „Der Jahresabschluss für den 1.1.2022 kann nicht storniert werden, da die Anfangssaldobuchungen im Geschäftsjahr 1/1/2023 im Hauptbuch ausgeglichen wurden.“ Was bedeutet dieser Fehler?

Da die Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** aktiviert ist, sind Stornierungen der Jahresendverarbeitung nicht zulässig, wenn die Eröffnungsbuchungen im neuen Geschäftsjahr abgerechnet wurden. Stornieren Sie den Sachkontoausgleich im neuen Geschäftsjahr 2023, bevor Sie den Jahresabschluss für den 1. Januar 2022 rückgängig machen. Alternativ können Sie das Jahr für den 1. Januar 2022 erneut abschließen, jedoch nur für neue Anpassungseinträge. Deaktivieren Sie den Hauptbuchparameter **Vorhandene Jahresendeinträge beim erneuten Jahresabschluss löschen**, um das Jahr nur für Anpassungen erneut zu schließen.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Hauptbuch: Warum verarbeitet der Prozess für die Sachkontoausgleichsautomatisierung die Sachkonto-Ausgleichsbuchungen für Dezember nicht?

Die Funktion **Automatischer Sachkontoausgleich** führt die Automatisierung für Transaktionen aus, die vom ersten Tag des Geschäftsjahres bis zum aktuellen Datum datiert sind, an dem das Ereignis ausgeführt wird. Für Geschäftsjahre, die am 31. Dezember enden, müssen Sie möglicherweise das Ausführungsdatum Ihres Ereignisses anpassen, um sicherzustellen, dass es im Dezember ausgeführt wird. Die Automatisierung ist zum Beispiel so eingerichtet, dass sie am ersten Tag jedes Monats ausgeführt wird. Diese Automatisierung wird am 1. Dezember 2022 ausgeführt und soll am 1. Januar 2023 ausgeführt werden. Wir empfehlen Ihnen, das Ereignis für den 1. Januar 2023 zu ändern, sodass es stattdessen am 31. Dezember 2022 ausgeführt wird. Durch diese Änderung wird sichergestellt, dass Transaktionen vom 2. bis 31. Dezember beim automatischen Ausgleich berücksichtigt werden.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Hauptbuch: Was ist der Unterschied zwischen der Aktion „Jahresabschluss rückgängig machen“ und dem Parameter „Vorhandene Jahresabschlusseinträge beim Wiederabschluss löschen“ für den Jahresabschluss?

Eventuell bestehen Unklarheiten bezüglich des Unterschieds zwischen der Aktion **Jahresabschluss rückgängig machen** und dem Parameter **Vorhandene Jahresabschlusseinträge beim erneuten Abschluss löschen** im Hauptbuch (**Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**).

Wählen Sie die Aktion **Jahresendabschluss rückgängig machen** aus, wenn Sie den Jahresabschluss erneut durchführen, damit alle Abschluss- und Anfangssalden gelöscht werden, so als ob der Jahresendabschluss nie erfolgt wäre. Die Belege werden in diesem Fall gelöscht. Der Jahresendabschluss wird nicht automatisch erneut ausgeführt. Wählen Sie die Aktion **Jahresabschluss ausführen** aus, um den Jahresabschluss auszuführen.

Der Parameter **Vorhandene Jahresendeinträge beim erneuten Jahresabschluss löschen** im Hauptbuch wird nur verwendet, wenn Sie den Jahresabschluss ausführen (nicht rückgängig machen). Ist dieser Parameter auf **Ja** eingestellt, werden alle Abschluss- und Anfangssalden gelöscht, und der Jahresendabschluss wird erneut ausgeführt. Diese Option wird verwendet, wenn das Unternehmen möchte, dass alle Transaktionen, einschließlich Anpassungen seit dem letzten Jahresendabschluss, für Abschluss- und Anfangssaldo in einer einzigen Buchung gebucht werden sollen. Ist dieser Parameter auf **Nein** gesetzt, bleiben alle Abschluss- und Anfangssalden bestehen. Sie werden nicht gelöscht. Stattdessen werden ein neuer Abschlusssaldo- und ein neuer Anfangssaldoeintrag nur für das Delta oder die neuen Transaktionen erstellt, die seit dem letzten Jahresendabschluss dieses Geschäftsjahres gebucht wurden.

> [!NOTE]
> Der Abschlusssaldo wird im abzuschließenden Jahr erstellt. Dies tritt nur auf, wenn der Hauptbuchparameter **Abschlussbuchungen bei Umbuchung erstellen** auf **Ja** eingestellt ist. Der Anfangssaldo wird immer erstellt, weil damit das nächste Jahr beginnt.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Hauptbuch: Was ist der Unterschied zwischen den Optionen „Alle schließen“ und „Einzeln schließen“ im Abschnitt „Gewinn- und Verlustdimension übertragen“ im Jahresabschlussprozess?

Bei **Alle schließen** bleiben die ursprünglichen Finanzdimsionswerte aus vorgenommenen Buchungen erhalten. Diese werden zum Erstellen von Anfangssalden für das Konto nicht ausgeschütteter Gewinne verwendet. Einzelne Anfangssalden für nicht ausgeschüttete Gewinnen werden für jede eindeutige Kombination von Finanzdimensionswerten erstellt. Wird **Einzeln abschließen** ausgewählt, werden alle mit der Finanzdimension vorgenommenen Transaktionen zu einem Anfangssaldo nicht ausgeschütteter Gewinne für den Dimensionswert zusammengefasst, der im Feld nach **Einzeln abschließen** angegeben ist. 

Angenommen, alle Buchungen für das Geschäftsjahr wurden mit der Kontostruktur Hauptkonto – Abteilung vorgenommen. Für die Finanzdimension Abteilung auf der Vorlage ist **Einzeln abschließen** ausgewählt, und als Wert ist 100 eingegeben. Wenn das Gesamteinkommen aller Buchungen für die Abteilungen 200, 300 und 400 100.000 Euro ist, wird eine Primobuchung für nicht ausgeschüttete Gewinne – 100 erstellt. Wenn Sie **Einzeln abschließen** auswählen aber keinen Wert für die Finanzdimension angeben, werden alle Buchungen für die nicht ausgeschütteten Gewinne ohne diesen Wert vorgenommen.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Hauptbuch: Gehen meine detaillierten Transaktionsinformationen verloren, wenn ich im Abschnitt „Gewinn‑ und Verlustdimension übertragen“ beim Jahresabschluss die Option „Einzeln schließen“ auswähle?

Die Optionen **Alle abschließen** und **Einzeln abschließen** werden verwendet, um anzugeben, welche Finanzdimensionen für Transaktionen für Gewinn‑ und Verlustkonten auf das Gewinnvortragshauptkonto übertragen. Die historische, detaillierte Buchung für die Gewinn‑ und Verlustrechnung ist davon nicht betroffen und bleibt detailliert. Die Option wirkt sich auf den Detaillierungsgrad aus, der im neuen Jahr als Anfangssaldo auf die Gewinnrücklagenkonten übertragen wird. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Hauptbuch: Der Jahresabschlussprozess schlägt fehl, da die Berichtswährung für das Jahr nicht ausgeglichen ist. Was bedeutet das?

Dieser Fehler kann auftreten, nachdem die Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (die Awareness-Funktion) aktiviert wurde. Wenn diese Funktion aktiviert ist, werden abgerechnete Hauptbuchtransaktionen nicht mehr in den Anfangssaldo des nächsten Geschäftsjahres aufgenommen, wenn der Jahresendabschluss des Hauptbuchs ausgeführt wird. Das Ausschließen von abgerechneten Sachkontobuchungen kann für Kunden am Jahresende eine Herausforderung darstellen, wenn das Sachkonto mit einer Berichtswährung definiert ist.   
Der Sachkontoausgleich wird nur für die Buchhaltungswährung ausgeführt.  Wenn die Sachkontobuchungen abgerechnet werden, stellt die Validierung nur sicher, dass die Belastungen in der Buchhaltungswährung den Gutschriften in der Buchhaltungswährung entsprechen. Die Berichtswährungsbeträge für diese Sachkontobuchungen werden nicht validiert und weisen möglicherweise nicht Belastungen = Gutschriften auf.  Zudem berechnet und verbucht der Sachkontoausgleich nicht automatisch einen Gewinn/Verlust in der Berichtswährung.  Aufgrund dieser Einschränkungen muss in der Berichtswährung eine Gewinn-/Verlust-Transaktion vorliegen, wenn ein Sachkontoausgleich durchgeführt wird.  Wenn der Gewinn/Verlust nicht im Sachkontoausgleich enthalten ist, führt der Jahresabschluss dazu, dass eine Saldenfehlernachricht angezeigt wird.  Weitere Informationen finden Sie unter [Unterschied zwischen der Funktion Sachkontoausgleich und Berichtswährung ist nicht ausgeglichen](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Hauptbuch: Durch welche Änderungen kann die Leistung bei der Verarbeitung des Jahresendabschlusses verbessert werden?

Die Leistung bei der Verarbeitung des Jahresendabschlusses kann durch eine Reihe von Änderungen verbessert werden. Überlegen Sie anhand der vorgeschlagenen Änderungen, ob diese für Ihr Unternehmen geeignet sind.

### <a name="optimize-year-end-close-service"></a>Service Jahresabschluss optimieren

Der Service **Jahresabschluss optimieren** ermöglicht Microsoft Dynamics 365 Finance-Kunden, ihren Jahresabschluss zu beschleunigen, indem sie die umfangreiche Jahresabschlussverarbeitung auf einen Microservice verlagern. Durch die Zeitersparnis eines effizienten Jahresabschlusses kann jedes Finanzteam rechtzeitig auf nötige Anpassungen reagieren, was in der Erstellung der Finanzberichte endet. Durch das Verarbeiten des Jahresabschlusses auf einem Microservice werden wertvolle Ressourcen frei. Die Verarbeitungserhöhung minimiert die Belastung des SQL Server und gibt Kunden die Möglichkeit, den Jahresabschluss zu beschleunigen.

Der Service **Jahresabschluss optimieren** ist in Version 10.0.31 verfügbar, sodass mehr Kunden den neuen Service für den Jahresabschluss 2022 nutzen können. Außerdem wurde der Service auf die Versionen 10.0.30 und 10.0.29 zurückportiert. Weitere Informationen finden Sie unter [Jahresabschluss optimieren](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensionssätze

Jeder Dimensionssatzsaldo wird neu erstellt, wenn Sie den Jahresabschluss ausführen. Dieses Verhalten hat direkte Auswirkungen auf die Leistung. Einige Unternehmen erstellen unnötigerweise Dimensionssätze, weil diese in der Vergangenheit verwendet wurden oder ggf. wieder verwendet werden könnten. Da diese unnötigen Dimensionssätze werden beim Jahresendabschluss neu erstellt werden, benötigt der Prozess mehr Zeit. Sehen Sie sich Ihre Dimensionssätze genau an, und löschen Sie nicht benötigte Sätze.

Unnötige Dimensionssätze wirken sich auch auf den Batchauftrag **BudgetDimensionFocusInitializeBalance** (**Hauptbuch \> Kontenplan \> Dimensionen \> Finanzdimensionssätze**) aus.

[![Finanzdimensionssätze.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration der Vorlage zum Jahresendabschluss

Mit der Vorlage zum Jahresendabschluss können Organisationen das Finanzdimensionsniveau auswählen, das bei der Übertragung von Gewinn- und Verlustsalden auf einbehaltene Gewinne beibehalten werden soll. Mit den Einstellungen können Unternehmen die genauen Finanzdimensionen (**Alle abschließen**) beibehalten, wenn die Salden in einbehaltene Gewinne verschoben oder die Beträge zu einem eindimensionalen Dimensionswert zusammengefasst werden (**Einzeln abschließen**). Dies kann für jede Finanzdimension festgelegt werden. Weitere Informationen zu diesen Einstellungen erhalten Sie im Artikel [Jahresendabschluss](year-end-close.md).

Wir empfehlen, dass Sie die Anforderungen Ihres Unternehmens genau betrachten und mit der Option **Einzeln abschließen** so viele Dimensionen wie möglich abschließen, um die Leistung zu verbessern. Durch den Abschluss auf einen einzelnen Dimensionswert (der auch leer sein kann) fällt die systeminterne Berechnung der Salden des Kontos für einbehaltene Gewinne weniger ausführlich aus.

### <a name="degenerate-dimensions"></a>Degenerierte Dimensionen

Eine degenerierte Dimension bietet allein und in Kombination mit anderen Dimensionen wenig bis keine Wiederverwendung. Es sind zwei Arten von degenerierten Dimensionen verfügbar. Der erste Typ ist eine Dimension, die individuell degeneriert ist. Normalerweise wird diese Art von degenerierter Dimension nur bei einer einzelnen Transaktion oder bei kleinen Transaktionsgruppen angezeigt. Der zweite Typ ist eine Dimension, die in Kombination mit einer oder mehreren zusätzlichen Dimensionen degeneriert wird, die basierend auf den generierbaren Permutationen das gleiche Potenzial aufweisen. Eine degenerierte Dimension kann einen erheblichen Einfluss auf die Leistung des Jahresendabschlussprozesses haben. Um Leistungsprobleme zu minimieren, definieren Sie alle degenerierten Dimensionen beim Einrichten des Jahresendabschlusses als **Einzeln abschließen**, wie im vorherigen Abschnitt beschrieben.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Kreditorenkonten: Welche Änderungen wurden zugunsten der Jahresendsteuererklärung (US 1099) für das Jahr 2022 vorgenommen?

#### <a name="update-to-all-1099-forms"></a>Alle Steuerformulare (US 1099) aktualisieren

Folgende Änderungen wurden an allen Steuerformularen (US 1099) für das Steuerjahr 2022 vorgenommen:

- 2021 wurde das Jahr in den 1099-Formularen fixiert. Ab 2022 wird das Jahr aus dem Bericht übernommen.

#### <a name="1099-misc"></a>1099-MISC

Folgende Aktualisierungen wurden an dem Formular 1099-MISC für das Steuerjahr 2022 vorgenommen:

- Feld 13: Zeigt jetzt die Anforderung zur Foreign Account Tax Compliance Act (FATCA)-Einreichung an.
- Feld 14: Wird jetzt für die Meldung von übermäßigen Golden-Parachute-Zahlungen verwendet.
- Feld 15: Wird jetzt zur Meldung der Zahlung im Rahmen von Plänen zur nicht qualifizierten Kompensation (NQDC) verwendet.
- Feld 16: Wird jetzt zur Meldung von Quellensteuern verwendet.
- Feld 17: Wird jetzt zur Meldung der Bundeslandnummer des Zahlers verwendet.
- Feld 18: Wird jetzt zur Meldung der Einkommenssteuer verwendet.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditorenkonten: 1099 – Wie ändere ich das Steuerformularfeld (US 1099) und die Werte bei einem Kreditor, der das ganze Jahr über keine Steuerdaten (US 1099) erfasst hat?

Verwenden Sie die Funktion **1099 aktualisieren**, um zuvor bezahlte Rechnungstransaktionen durchzugehen, und ordnen Sie die 1099-Daten gemäß den Einstellungen für die Registerkarte **1099** auf der Seite **Kreditor**. Wechseln Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren**, wählen Sie einen Kreditor aus, und klicken Sie dann im Aktionsbereich auf der Registerkarte **Kreditor** auf die Option **1099 aktualisieren**, um die Option **1099 aktualisieren** zu verwenden.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Kann die Funktion zum Aktualisieren von 1099 für alle meine Kreditoren gleichzeitig ausgeführt werden?

Sie können die Seite **1099-Informationen für mehrere Lieferanten aktualisieren** verwenden, um das Feld 1099 in einem Kreditorendatensatz zu aktualisieren und Transaktionen mit den Informationen aus dem Feld 1099 zu aktualisieren. Wechseln Sie zu **Kreditorenkonten \> Periodische Aufgabe \> Steuer 1099**, um diese Seite zu öffnen. Ihnen muss das Sicherheitsprivileg **1099-Feld und Transaktionen für mehrere Kreditoren aktualisieren** zugewiesen sein, damit Sie Zugriff auf diese Seite haben.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Kreditorenkonten: 1099 – „Bestehende 1099-Beträge neu berechnen“ im Vergleich zu „Alle aktualisieren“ aus dem Dienstprogramm zur Aktualisierung von 1099

Mit dem Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird der Steuerbetrag (US 1099) auf die insgesamt bezahlte Summe zurückgesetzt, wenn dies zusammen mit dem Kontrollkästchen **Alle aktualisieren** verwendet wird.

[![Steuerbuchungen (US 1099): Vor Ausführung der Aktualisierung.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Das Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird nur verwendet, wenn die Rechnung partielle 1099-Werte aufweist oder wenn die Rechnung im Formular zur Steuererklärung (US 1099) geändert wurde. Angenommen, Sie haben eine Rechnung im Wert von 1.000,00 US-Dollar, aber der Benutzer gibt auf der Rechnung manuell einen 1099-Betrag von 500,00 US-Dollar ein.

[![Steuerbuchungen (US 1099): Markierung von sowohl „Alle aktualisieren“ als auch „Bestehende 1099-Beträge neu berechnen“.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Bei Bezahlung der Rechnung entspricht der Betrag von 500,00 US-Dollar dem gezahlten Betrag im Formular 1099. Wird eine Neuberechnung durchgeführt, wird der 1099-Betrag in 1.000,00 US-Dollar geändert, was der insgesamt bezahlten Summe entspricht.

[![Steuerbuchungen (US 1099): Nach Ausführung des 1099-Vorgangs.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditorenkonten: 1099 – Buchungen (US 1099) manuell erstellen

Eventuell müssen in einem Unternehmen Buchungen (US 1099), die keiner Rechnung zugeordnet sind, manuell erstellt werden. Dies ist möglich unter **Kreditorenkonten \> Periodische Aufgaben \> Steuererklärung (US 1099) \> Kreditorenausgleich für Steuerformulare (US 1099)**. Wählen Sie die Schaltfläche **Manuelle US 1099-Buchungen** aus.

Manuell erstellte Buchungen (US 1099) werden nicht im Zuge von **Alle aktualisieren** oder **Bestehende 1099-Beträge neu berechnen** aus dem Dienstprogramm **1099 aktualisieren** aktualisiert.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditorenkonten: 1099 – Wird das 1096-Formular in Dynamics 365 Finance unterstützt?

Das Formular 1096 mit der jährliche Zusammenfassung und Übermittlung von US-Informationserklärungen kann in Dynamics 365 Finance nicht gedruckt werden.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditorenkonten: 1099 – Gibt es neue Funktionen, mit denen die Steuererklärung (US 1099) im öffentlichen Sektor getätigt werden kann?

Es wurde eine neue Funktion mit der Bezeichnung **1099-Informationen anhand von Hauptkonto aktualisieren** ergänzt, die Sie im Arbeitsbereich **Funktionsverwaltung** aktivieren können. Damit können die 1099-Werte zu einem Kreditor anhand des Hauptkontos in der Buchhaltungsverteilung und nicht anhand des Standardkontos im Kreditorendatensatz verknüpft werden.

Weitere Informationen finden Sie unter [Kreditoren für Steuererklärung (US 1099) einrichten](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
