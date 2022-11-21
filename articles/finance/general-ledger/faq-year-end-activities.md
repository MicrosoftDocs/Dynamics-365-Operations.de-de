---
title: Häufig gestellte Fragen zu Aktivitäten am Jahresende
description: In diesem Artikel werden Fragen aufgelistet, die zum Jahresabschluss auftreten können, sowie die Antworten, die bei Aktivitäten zum Jahresabschluss hilfreich sein können.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a25f20c320b905a2cdd3091e76e3c5e73f1a845a
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752747"
---
# <a name="year-end-activities-faq"></a>Häufig gestellte Fragen zu Aktivitäten am Jahresende 

[!include [banner](../includes/banner.md)]

In diesem Artikel werden Fragen aufgelistet, die zum Jahresabschluss auftreten können, sowie die Antworten, die bei Aktivitäten zum Jahresabschluss hilfreich sein können. Es geht überwiegend um Fragen zum Jahresabschluss von Hauptbuch und Kreditorenkonten.

## <a name="general-ledger-year-end-enhancements"></a>Jahresendoptimierungen für Hauptbuch 
In Version 10.0.20 wurde eine Erweiterung zum Jahresende eingeführt, die ab Version 10.0.25 standardmäßig aktiviert ist. Wenn Ihr Unternehmen eine frühere Version als 10.0.25 verwendet, empfehlen wir, diese Funktion zu aktivieren, bevor Sie mit dem Jahresabschlussprozess beginnen. Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit der Einstellung Funktionsverwaltung den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

 - Modul: Hauptbuch
 - Funktionsname: Erweiterung zum Jahresendabschluss des Hauptbuchs

Die Einrichtung der Jahresabschlussvorlagen wurde auf eine neue Einrichtungsseite verschoben, **Einrichtung der Vorlage für Jahresendabschluss**. Die vorhandene Jahresendabschlussseite wird auf ähnliche Weise geändert wie bei der Neubewertung der Fremdwährung im Hauptbuch, sodass bei jeder Ausführung oder Stornierung des Jahresendabschlusses eine Liste angezeigt wird. Ein Buchhaltungsleiter kann den Jahresendabschluss von der neuen Seite aus einleiten. 

Um den Jahresendabschluss rückgängig zu machen, wählen Sie das letzte Geschäftsjahr für die entsprechende juristische Person und dann die Schaltfläche **Jahresendabschluss rückgängig machen** aus. Durch die Stornierung werden die Buchungseinträge für den vorherigen Jahresendabschluss gelöscht und wird der Jahresendabschluss nicht automatisch erneut ausgeführt. 

Sie können den Jahresendabschluss wiederholen, indem Sie den Prozess für das Geschäftsjahr und die juristische Person erneut starten. Der Prozess verwendet weiterhin die Hauptbuch-Parametereinstellung, um zu bestimmen, ob die Wiederholung des Jahresendabschlusses nur die neuen oder geänderten Transaktionen berücksichtigt oder den vorherigen Abschluss vollständig rückgängig macht und den Prozess für alle Transaktionen erneut ausführt.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Hauptbuch: Woher weiß ich, dass wir den Jahresendabschluss durchführen und nicht rückgängig machen?
Wir wissen, das Unternehmen versucht haben, den Jahresendabschluss durchzuführen, ihn stattdessen aber rückgängig gemacht haben. Wenn der Jahresendabschluss sehr schnell endet oder keine Anfangssalden ergibt, überprüfen Sie unter **Jahresendabschluss** die Einstellung **Vorherigen Abschluss rückgängig machen** (**Hauptbuch > Periodenabschluss > Jahresendabschluss > Geschäftsjahresabschluss ausführen**). 

[![Durchführung des Jahresendabschlusses im Vergleich zum Rückgängigmachen des Jahresendabschlusses.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ist **Vorherigen Abschluss rückgängig machen** auf **Ja** eingestellt, wird der vorherige Abschluss rückgängig gemacht. Beim Rückgängigmachen werden alle Abschluss- und Anfangssalden gelöscht, als wäre der Jahresendabschluss nie erfolgt. Belege werden gelöscht. Der Jahresendabschluss wird nicht automatisch erneut ausgeführt. Vielmehr muss der Vorgang manuell erneut gestartet werden, indem **Vorherigen Abschluss rückgängig machen** auf **Nein** gesetzt wird. 

> [!NOTE]
> Der Abschlusssaldo wird optional im abzuschließenden Jahr erstellt. Dies tritt nur auf, wenn der Hauptbuchparameter **Abschlussbuchungen bei Umbuchung erstellen** auf **Ja** eingestellt ist. Der Anfangssaldo wird immer erstellt, weil damit das nächste Jahr beginnt.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Hauptbuch: Was ist der Unterschied zwischen dem Rückgängigmachen und dem Löschen des Hauptbuchparameters beim Jahresendabschluss?
Eventuell bestehen Unklarheiten bezüglich des Parameters **Vorherigen Abschluss rückgängig machen** aus dem Dialogfeld **Jahresendabschluss** und des Parameters **Jahresabschlussbuchungen bei Umbuchung löschen** aus dem Hauptbuch (**Hauptbuch > Periodenabschluss > Jahresendabschluss > Geschäftsjahresabschluss ausführen**).  

[![Unterschied zwischen dem Rückgängigmachen und Löschen des Hauptbuchparameters.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Sollen alle Abschluss- und Anfangssalden gelöscht werden, so als ob der Jahresendabschluss nie erfolgt wäre, wählen Sie bei Durchführung des Jahresendabschlusses im Dialogfeld im Dropdownmenü die Option **Vorherigen Abschluss rückgängig machen** aus. Die Belege werden gelöscht. Der Jahresendabschluss wird nicht automatisch erneut ausgeführt. Um den Jahresendabschluss durchzuführen, müssen Sie diesen Prozess erneut starten, wobei Sie die Option **Vorherigen Abschluss rückgängig machen** (**Hauptbuch > Einrichten des Hauptbuchs > Hauptbuchparameter**) auf **Nein** setzen. 

[![Einstellung des Hauptbuchparameters.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Der Parameter **Jahresabschlussbuchungen bei Umbuchung löschen** aus dem Hauptbuch wird nur verwendet, wenn der Jahresendabschluss ausgeführt wird (nicht, wenn er rückgängig gemacht wird. Die Option **Vorherigen Abschluss rückgängig machen** ist auf **Nein** eingestellt). Ist dieser Parameter auf **Ja** eingestellt, werden alle Abschluss- und Anfangssalden gelöscht, und der Jahresendabschluss wird erneut ausgeführt. Dieser Vorgang wird verwendet, wenn das Unternehmen möchte, dass alle Transaktionen, einschließlich Anpassungen seit dem letzten Jahresendabschluss, für Abschluss- und Anfangssaldo in einer einzigen Buchung gebucht werden sollen. 

Ist diese Option auf **Nein** gesetzt, bleiben alle Abschluss- und Anfangssalden bestehen. Sie werden nicht gelöscht. Stattdessen werden ein neuer Abschlusssaldo- und ein neuer Anfangssaldoeintrag nur für das Delta oder die neuen Transaktionen erstellt, die seit dem letzten Jahresendabschluss dieses Geschäftsjahres gebucht wurden.  

> [!NOTE]
> Der Abschlusssaldo wird im abzuschließenden Jahr erstellt. Dies tritt nur auf, wenn der Hauptbuchparameter **Abschlussbuchungen bei Umbuchung erstellen** auf **Ja** eingestellt ist. Der Anfangssaldo wird immer erstellt, weil damit das nächste Jahr beginnt. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Hauptbuch: Durch welche Änderungen kann die Leistung bei der Verarbeitung des Jahresendabschlusses verbessert werden? 
Die Leistung bei der Verarbeitung des Jahresendabschlusses kann durch eine Reihe von Änderungen verbessert werden. Überlegen Sie anhand der vorgeschlagenen Änderungen, ob diese für Ihr Unternehmen geeignet sind.  

### <a name="dimension-sets"></a>Dimensionssätze
Bei Durchführung des Jahresendabschlusses wird der Saldo jedes Dimensionssatzes neu erstellt, was sich direkt auf die Leistung auswirkt. Einige Unternehmen erstellen unnötigerweise Dimensionssätze, weil diese in der Vergangenheit verwendet wurden oder ggf. wieder verwendet werden könnten.  Diese unnötigen Dimensionssätze werden beim Jahresendabschluss neu erstellt, was Zeit in Anspruch nimmt. Sehen Sie sich Ihre Dimensionssätze genau an, und löschen Sie nicht benötigte Sätze.

Unnötige Dimensionssätze wirken sich auch auf den Batchauftrag **BudgetDimensionFocusInitializeBalance** (**Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionssätze**) aus.

[![Finanzdimensionssätze.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration der Vorlage zum Jahresendabschluss
Mit der Vorlage zum Jahresendabschluss können Organisationen das Finanzdimensionsniveau auswählen, das bei der Übertragung von Gewinn- und Verlustsalden auf einbehaltene Gewinne beibehalten werden soll. Mit den Einstellungen können Unternehmen die genauen Finanzdimensionen (**Alle abschließen**) beibehalten, wenn die Salden in einbehaltene Gewinne verschoben oder die Beträge zu einem eindimensionalen Dimensionswert zusammengefasst werden (**Einzeln abschließen**). Dies kann für jede Finanzdimension festgelegt werden. Weitere Informationen zu diesen Einstellungen erhalten Sie im Artikel [Jahresendabschluss](year-end-close.md).

Wir empfehlen, dass Sie die Anforderungen Ihres Unternehmens genau betrachten und mit der Option **Einzeln abschließen** so viele Dimensionen wie möglich abschließen, um die Leistung zu verbessern. Durch den Abschluss auf einen einzelnen Dimensionswert (der auch leer sein kann) fällt die systeminterne Berechnung der Salden des Kontos für einbehaltene Gewinne weniger ausführlich aus.

## <a name="degenerate-dimensions"></a>Degenerierte Dimensionen

Eine degenerierte Dimension bietet allein und in Kombination mit anderen Dimensionen wenig bis keine Wiederverwendung. Es sind zwei Arten von degenerierten Dimensionen verfügbar. Der erste Typ ist eine Dimension, die individuell degeneriert ist. Normalerweise wird diese Art von degenerierter Dimension nur bei einer einzelnen Transaktion oder bei kleinen Transaktionsgruppen angezeigt. Der zweite Typ ist eine Dimension, die in Kombination mit einer oder mehreren zusätzlichen Dimensionen degeneriert wird, die basierend auf den generierbaren Permutationen das gleiche Potenzial aufweisen. Eine degenerierte Dimension kann einen erheblichen Einfluss auf die Leistung des Jahresendabschlussprozesses haben. Um Leistungsprobleme zu minimieren, definieren Sie alle degenerierten Dimensionen beim Einrichten des Jahresendabschlusses als **Einzeln abschließen**, wie im vorherigen Abschnitt beschrieben.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Hauptbuch: Was geschieht beim Periodenabschluss und beim Jahresendabschluss?
 
[![Periodenabschluss, Jahresendabschluss](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Leistungsverbesserungen beim Neuerstellen von Finanzdimensionssätzen
Eine neue Funktion, die in Version 10.0.16 ergänzt wurde, verbessert die Leistung bei Jahresendabschluss und Konsolidierung. Bei dieser Funktion handelt es sich um Leistungsverbesserungen bei der Neuerstellung von Finanzdimensionssätzen. Im Zuge dieser Verbesserungen werden Dimensionssätze nur über einen relevanten Zeitraum neu erstellt. In den Vorgängerversionen wurden die Dimensionssätze zu sämtlichen Datumsangaben neu erstellt. Wenn Sie beispielsweise das Jahr 2020 abschließen, erstellt das System nur die Salden für Transaktionen im Geschäftsjahr 2020 neu. Erfolgt die Konsolidierung über den Zeitraum vom 1. November bis zum 30. November 2020, erstellt das System die Salden nur über diesen Zeitraum neu.

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit der Einstellung Funktionsverwaltung den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:
 
- Modul: Hauptbuch
- Funktionsname: Leistungsverbesserungen bei der Neuerstellung von Finanzdimensionssätzen

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

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Kreditorenkonten: Welche Änderungen wurden zugunsten der Jahresendsteuererklärung (US 1099) für das Jahr 2021 vorgenommen?

Im Jahr 2021 wurden die Formulare DIV, NEC und MISC leicht geändert und einige zusätzliche Felder hinzugefügt.

#### <a name="div-new-box2e-2f"></a>DIV: neues Feld 2e, 2f
 
- Feld 2e. Zeigt den Teil des Betrags in Feld 1a, der dem Abschnitt 897, Veräußerung von US-Immobilienbeteiligungen (USRPI) zuzuordnen ist.  
- Feld 2f. Zeigt den Teil des Betrags in Feld 2a, der dem Abschnitt 897, Veräußerung von US-Immobilienbeteiligungen (USRPI) zuzuordnen ist. Beachten Sie, dass die Felder 2e und 2f nur für ausländische Personen und Organisationen gelten, deren Einkünfte ihren Charakter behalten, wenn sie an ihre direkten oder indirekten ausländischen Eigentümer oder Begünstigten weitergegeben oder an diese ausgeschüttet werden. Es wird im Allgemeinen als effektiv mit einem Handels- oder Geschäftsvorgang in den USA verbunden behandelt. Beachten Sie die Hinweise zu Ihrer Steuererklärung. 
 
#### <a name="nec-new-box-2"></a>NEC: neues Feld 2 
 
Wenn Feld 2 aktiviert ist, melden Sie Konsumgüter im Gesamtwert von 5.000 USD oder mehr, die Ihnen zum Wiederverkauf, auf einer Kauf-Verkaufs-Basis, einer Einzahlungsprovision oder auf andere Weise verkauft wurden. Im Allgemeinen geben Sie alle Einnahmen aus Ihrem Verkauf dieser Produkte in Anhang C (Formular 1040) an. 
 
Im gleichen Zug wird die Formulargröße von NEC geändert. Beim Drucken gibt es drei Formulare pro Seite. 
 
#### <a name="misc-new-box-11"></a>MISC: neues Feld 11 
 
Feld 11 zeigt den Betrag, der für den Kauf von Fisch zum Weiterverkauf einer Person gezahlt wird, die im Fischfanghandel tätig ist. Informationen zur Berichterstattung dieses Einkommens finden Sie in der Anleitung zu Ihrer Steuererklärung. 
 
#### <a name="electronic-filing"></a>Elektronische Übermittlung 
Informationen zur elektronischen Übermittlung finden Sie unter [Anforderungen bei der Veröffentlichung elektronischer Übermittlung](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Formatspezifikationen und Datensatzlayouts für elektronische Berichte 2021 aktualisieren 
- Sek. 2 Aussteller „A“-Datensatz. 
- Betragscodes – Feldposition 28-45 erhöht, Länge auf 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Sek. 2 Aussteller „A“-Datensatz für die Meldung von Zahlungen im Formular 1099-DIV: 
- Betragsart – Abschnitt 897 – Ordentliche Dividenden hinzugefügt und Betragscode H hinzugefügt. 
- Betragsart – Abschnitt 897 – Kapitalgewinne hinzugefügt und Betragscode J hinzugefügt. 
 
#### <a name="sec-3-payee-b-record"></a>Sek. 3 Zahlungsempfänger „B“-Datensatz 
- Allgemeine Informationsdatensätze – Dritter Aufzählungspunkt von 16 auf 18 Zahlungsbetragsfelder aktualisiert. 
- Feldtitel Zahlung H – Aktualisierte Feldposition 247-258, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Feldtitel Zahlung J – Aktualisierte Feldposition 259-270, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Leeres Feld auf Feldposition 271-286 aktualisiert. 
- Auslandskennzeichnung auf Feldposition 287 aktualisiert. 
- Das Feld „Name des ersten Zahlungsempfängers“ wurde auf Feldposition 288-327 aktualisiert. 
- Das Feld „Name des zweiten Zahlungsempfängers“ wurde auf Feldposition 328-367 aktualisiert. 
- Datensatz-Layoutpositionen, Formular 1099-MISC – Gelöschte Feldposition 548 und Feldtitel FATCA-Übermittlungsanforderungsanzeige. 
- Datensatz-Layoutpositionen, Formular 1099-NEC – 545-546 auf leer aktualisiert, Feld 547 auf Direktverkaufskennzeichen aktualisiert, Länge und Beschreibung und Bemerkungen 548-722-Feld auf leer aktualisiert. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Sek. 4 Ausstellerende „C“-Datensatz 
- Feldtitel Zahlung H – Aktualisierte Feldposition 304-321, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Feldtitel Zahlung J – Aktualisierte Feldposition 322-339, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Feldtitel 340-499 – Länge auf 160 aktualisiert. 
 
#### <a name="sec-5-state-totals-k-record"></a>Sek. 5 Statusgesamtbetrag „K“-Datensatz 
- Feldtitel Zahlung H – Aktualisierte Feldposition 304-321, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Feldtitel Zahlung J – Aktualisierte Feldposition 322-339, Feldtitel, Länge und allgemeine Feldbeschreibung. 
- Feldtitel 340-499 – Länge auf 160 aktualisiert.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditorenkonten: 1099 – Wie ändere ich das Steuerformularfeld (US 1099) und die Werte bei einem Kreditor, der das ganze Jahr über keine Steuerdaten (US 1099) erfasst hat?
Verwenden Sie die Funktionen zum Aktualisieren von 1099 (**Kreditorenkonten > Kreditoren > Alle Kreditoren > Kreditor auswählen > Registerkarte zum Kreditor im Menüband > 1099 aktualisieren**), um die Transaktionen zu den zuvor bezahlten Rechnungen durchzusehen und die Daten aus 1099 entsprechend den Einstellungen auf der Registerkarte **Steuererklärung (US 1099)** auf der Seite **Kreditor** neu zuzuweisen.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kann die Funktion zum Aktualisieren von 1099 für alle meine Kreditoren gleichzeitig ausgeführt werden?
Nein. Die Funktion zum Aktualisieren von 1099 muss für jeden Kreditor einzeln ausgeführt werden. Wenn eine massenweise Aktualisierung in Ihrem Unternehmen erforderlich sein sollte, stimmen Sie bitte für die Idee [Batchverarbeitung zur Aktualisierung der Steuerdaten (US 1099) von Kreditoren](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Kreditorenkonten: 1099 – „Bestehende 1099-Beträge neu berechnen“ im Vergleich zu „Alle aktualisieren“ aus dem Dienstprogramm zur Aktualisierung von 1099.
Mit dem Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird der Steuerbetrag (US 1099) auf die insgesamt bezahlte Summe zurückgesetzt, wenn dies zusammen mit dem Kontrollkästchen **Alle aktualisieren** verwendet wird. 

[![Steuerbuchungen (US 1099): Vor Ausführung der Aktualisierung.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Das Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird nur verwendet, wenn die Rechnung partielle 1099-Werte aufweist oder wenn Sie im Formular zur Steuererklärung (US 1099) geändert wurde. Angenommen, Sie haben eine Rechnung im Wert von 1.000,00 US-Dollar, aber der Benutzer gibt auf der Rechnung manuell einen 1099-Betrag von 500,00 US-Dollar ein.

[![Steuerbuchungen (US 1099): Markierung von sowohl „Alle aktualisieren“ als auch „Bestehende 1099-Beträge neu berechnen“.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Bei Bezahlung entspricht der Betrag von 500,00 US-Dollar dem gezahlten Betrag im Formular 1099. Wird eine Neuberechnung durchgeführt, ändert das System den 1099-Betrag in 1.000,00 US-Dollar, was der insgesamt bezahlten Summe entspricht.

[![Steuerbuchungen (US 1099): Nach Ausführung des 1099-Vorgangs.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditorenkonten: 1099 – Buchungen (US 1099) manuell erstellen
Eventuell müssen in einem Unternehmen Buchungen (US 1099), die keiner Rechnung zugeordnet sind, manuell erstellt werden. Dies ist möglich unter **Kreditorenkonten > Periodische Aufgaben > Steuererklärung (US 1099) > Kreditorenausgleich für Steuerformulare (US 1099)**. Wählen Sie die Schaltfläche **Manuelle US 1099-Buchungen** aus. 

Manuell erstellte Buchungen (US 1099) werden nicht im Zuge von **Alle aktualisieren** oder **Bestehende 1099-Beträge neu berechnen** aus dem Dienstprogramm **1099 aktualisieren** aktualisiert.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditorenkonten: 1099 – Wird das 1096-Formular in Dynamics 365 Finance unterstützt? 

Das Formular 1096 mit der jährliche Zusammenfassung und Übermittlung von US-Informationserklärungen kann in Dynamics 365 Finance nicht gedruckt werden.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditorenkonten: 1099 – Gibt es neue Funktionen, mit denen die Steuererklärung (US 1099) im öffentlichen Sektor getätigt werden kann? 
Es wurde eine neue Funktion mit der Bezeichnung **1099-Informationen anhand von Hauptkonto aktualisieren** ergänzt, die Sie im Arbeitsbereich **Funktionsverwaltung** aktivieren können. Damit können die 1099-Werte zu einem Kreditor anhand des Hauptkontos in der Buchhaltungsverteilung und nicht anhand des Standardkontos im Kreditorendatensatz verknüpft werden.

Weitere Informationen finden Sie unter [Kreditoren für Steuererklärung (US 1099) einrichten](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
