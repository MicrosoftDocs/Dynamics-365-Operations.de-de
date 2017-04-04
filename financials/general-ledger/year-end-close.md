---
title: Jahresabschluss
description: "In diesem Thema wird beschrieben die erforderlichen Einstellungen und die Schritte für das Ausführen des Hauptbuchjahresende-Schließenprozesses."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Jahresabschluss

In diesem Thema wird beschrieben die erforderlichen Einstellungen und die Schritte für das Ausführen des Hauptbuchjahresende-Schließenprozesses. 

Am Ende eines Geschäftsjahres, müssen Sie den Schließenprozess ausführen, um am Jahresende Anfangssalden in das neue Jahr zu übertragen. Die meisten Organisationen führen den Jahresendeschließenprozess mehrmals aus. Beim erstmaligen sind, die Salden abzurufen, die im neuen Geschäftsjahr verschoben wurden. Schließen (kann erneut ausgeführt werden, so oft wie erforderlich, die Salden von den Regulierungseingaben vor im neuen Geschäftsjahr zu verschieben. 

Während des (Schließenprozesses sind zwei Aktivitätstypen die erstellte Buchungen. Eine Primobuchung wird immer generiert und wird verwendet, um die von Anfangssalden im neuen Geschäftsjahr zu erstellen. Die Primobuchung werden die Bilanzsachkontosalden im neuen Geschäftsjahr anzeigen und sich aus den Gewinn- und Verlustsachkontosalden im einbehaltenen Einnahmesachkonto im neuen Geschäftsjahr aus. Die Abschlussbuchung optional wird erstellt, um die Salden der Gewinn- und Verlustkonten Null das Geschäftsjahr schließend zu kalkulieren.

## <a name="prepare-to-run-the-year-end-close"></a>Bereiten Sie sich vor Schließen (auszuführen,
Bevor Sie den (Schließenprozess ausführen, prüfen die Einstellungen für Folgendes: 

Auf der Seite **Hauptkonto**:

-   Prüft ** Hauptkontotyp ** wird ordnungsgemäß definiert für jedes Hauptkonto. Die Hauptkontoart wird verwendet, um zu bestimmen, ob der Saldo des Hauptkontos (als Anfangssaldo in eingefügt oder thesaurierter Gewinn Primobuchung im Formular geschlossen wird.
-   Das Öffnungskonto ** ** Feld kann verwendet werden, um den Saldo des Hauptkontos auf ein neues Hauptkonto für Jahresabschluss- Schließens umzubuchen. Das neue Hauptkonto wird im Feld Öffnungskonto ** ** Feld eingegeben. In der Regel wird dieses Bilanzhauptkonten für verwendet, wenn das Hauptkonto wird deaktiviert und ein neues Hauptkonto für das neue Geschäftsjahr verwendet wird.

Auf der Hauptbuchparameter ** ** Seite unter ** Geschäftsjahresschluss **:

-   ** Die Löschung auf der Jahrbuchungen ** Option wird verwendet, anzugeben, ob die vom System generierte Primobuchung früherer Jahresendeschließen gelöscht werden soll, wenn Jahresendeschließen erneut ausgeführt wird. Ist die Option auf festgelegt wird ** Ja **, wird die vorherige Primobuchung gelöscht und eine Neueröffnungsbuchung wird auf Basis der aktuellen Salden erstellt. Wenn diese Option aktiviert ist ** no **, bleibt die vorhergehende Primobuchung und eine zusätzliche Primobuchung wird erstellt, damit der Saldenvortrag von der Lagerregulierung gebuchter Buchungen zu verschieben nach Abzug Jahresendeschließen.
-   ** Die Erstellen von Abschlussbuchungen bei der Umbuchung ** Option wird, schließend Abschlussbuchungen im Geschäftsjahr zu erstellen, um die Salden der Gewinn- und Verlustkonten zu null aufzufüllen verwendet. Ist die Option auf Ja ** **, festgelegt, wird die Primobuchung und die Abschlussbuchung erstellt. Wenn diese Option aktiviert ist ** no ** Primobuchung nur, die im folgenden Geschäftsjahr erstellt, um die Salden übertragen. Die GuV-Konto-Salden bleiben am Ende des Geschäftsjahrs.
-   ** Die auf "Abgeschlossen" zu Geschäftsjahrsstatus dauerhaft ** Option wird, das Geschäftsjahr im dauerhaft einen Status Geschlossen festgelegt verwendet. Verwenden Sie diese Einstellung mit besonderer Vorsicht der, da alle Perioden mit einem Status Geschlossen dauerhaft nicht erneut geöffnet werden können und Anpassungen vorgenommen werden dem Geschäftsjahr verhindern. Es ist eine bewährte, dieses festzulegen ** no **.
-   ** Die Belegnummer muss ausgefüllt werden ** Option wird definiert verwendet, um festzustellen, dass einer Belegnummer erforderlich ist, wenn sie den Schließenprozess am Jahresende ausgeführt wird. Es ist eine bewährte, eine Belegnummer zu benötigen, um dem Bedarf Primobuchung vereinfacht das Identifizieren.

Auf der Steuerkalender ** ** Seite:

-   Das nächste erstellte Geschäftsjahr muss vorhanden sein, bevor er ausgeführt wird (z Schließen. Das nächste erstellte Geschäftsjahr ist erforderlich, um die Anfangssalden in der Eröffnungsperiode zu erstellen.

Auf der ** Sachkontokalender ** Seite:

-   Optional: Jeder Finanzzeitraum für das Geschäftsjahr schließend kann auf festgelegt werden gesperrt ** ** um neue Buchungen angezeigt eingegeben werden zu verhindern. Wenn Regulierungseingaben vor identifiziert werden können, die gesperrt Perioden erneut geöffnet sein, um Regulierungseingaben vor vornehmen, wenn der Jahresendeschließenprozess bereits ausgeführt wurde.

## <a name="define-year-end-close-templates"></a>Definieren Sie Sie Vorlagen ab Jahresende
Nachdem das System entsprechend konfiguriert ist, kann der Schließenprozess am Jahresende ausgeführt werden. Auf der ** das Jahresabschluss ** Seite kann eine Vorlage für die Gruppe definiert werden mit juristischen Personen, für die der Jahresendeschließenprozess ausgeführt wird. Die Vorlage wird bei jedem Jahresabschluss- Führen wiederverwendet, kann jedoch geändert werden, wenn Ihre Organisation ändern. 

Zunächst werden ** Gruppenname ** für die Vorlage, und wählen Sie den Steuerkalender aus. Der Name sollte die Gruppe die von den juristischen Personen.  Beispielsweise werden die Vorlagen auf Grundlage geografischen eingerichtet werden, wenn die nordamerikanische separaten Gruppen für juristische Personen, EMEA-juristischePersonen und APAC-juristischePersonen erstellt wurden. 

Danach können die juristischen Personen zur Vorlage hinzugefügt werden. Juristische Personen können hinzugefügt werden, indem eine Organisationshierarchie auswählen oder indem die juristischen Personen auswählen. Wenn eine Organisationshierarchie aktiviert ist, werden nur juristische Personen in der Hierarchie, die den ausgewählten Steuerkalender verwenden, die Vorlage hinzugefügt werden. Wenn von juristischen Personen verwendet, der die Vorlage hinzugefügt werden soll, werden nur juristische Personen mit dem gleichen Steuerkalender hinzugefügt werden können. Der gleiche Steuerkalender ist erforderlich, da am Jahresende Abschluss ausgeführt wird, indem ein Geschäftsjahr auswählen, das von Kalender Kalender zu variieren kann. 

Nachdem die juristischen Personen hinzugefügt wurden, können Sie die nicht ausgeschütteten, die Hauptziele jede juristische Person angegeben. ** Das Datum von Endenschließen des letzten Jahres ** Feld wird aktualisiert, wenn Verbinden mit unterschiedlichen Geschäftsjahresenddaten für die juristische Person aus. 

** Die Finanzdimension ** Registerkarte wird verwendet, um festzulegen, welche Finanzdimensionen in der Primobuchung verwendet werden. Beachten Sie, dass die Einstellungen, die Sie definieren, auf die juristische Person nur relevant sind, die im aktiviert ** juristische Personen ** Raster. Sie prüfen die Einstellung für jede juristische Person im Raster. 

** Übergangsbilanzdimensionen ** wird verwendet, um festzulegen, ob die Finanzdimensionen in den Buchungen, die auf Bilanzkonten gebucht werden, der auf Primobuchung verwaltet werden sollen. Es ist eine bewährte, um diese Option auszuwählen ** Ja **. ** Übergangsgewinn- und verlustdimensionen ** wird verwendet, um festzulegen, Finanz- auf Buchungen auf Gewinn- und Verlustkonto gebucht, wird in den Einnahmehauptkonto einbehaltenen. Hiermit kennzeichnen Sie die Finanzdimensionen, die sich jeweils auf die ausgewählte juristische Person relevant sind. Hierzu zählen sämtliche Finanzdimensionen werden, die für während des Jahres vorgenommen wurden, wenn die Finanzdimension nicht zu einer aktiven Kontostruktur ist. Definieren Sie als Nächstes jede Dimension die entweder als nahes ** einzelnes ** oder ** Bezieht alle **.  Der Standard ist ** Bezieht alle **, die der ursprünglichen Finanzdimensionswerte gebuchter Posten werden und sie für das Erstellen von Anfangssalden für die einbehaltene Einnahmekonto verwendet. Separate Einnahmen bei, wurden die Anfangssalden für jede eindeutige Kombination von Finanzdimensionswerten erstellt werden. Wenn nahes ** einzelnes ** aktiviert ist, werden alle Buchungen, die mit dieser Finanzdimension gebucht werden, in einen einbehaltenen Einnahmeanfangssaldo für den Dimensionswert ein, der im Feld eingegeben wird nach nahes ** einzelnes **. Angenommen, dass alle Transaktionen während des Geschäftsjahrs mit der Kontostruktur - Abteilung des Hauptkontos gebucht wurden. Auf der Finanzdimension "Abteilung" in der Vorlage, nahes ** einzelnes ** wird und 100 liegt der eingegebene Wert ausgewählt. Wenn der gesamte Gesamteinkommen aller Buchungen in Abteilungen 200, 300 gebucht hat und 400 Euro ein Anfangssaldo erstellt werden, für Retained Einnahmen - 100. Wenn Sie auswählen nahes ** einzelnes ** und das Finanzdimensionswertleerzeichen lassen, buchen alle Buchungen zu nicht ausgeschütteten mit diesem Dimensionswert, der leer ist. 

Der am Jahresende Schließenprozess befolgt Kontostrukturen nicht. Dies ist erforderlich, weil Kontostrukturen für eines Geschäftsjahres ändern können und es nicht möglich ist, die betreffende Kontostruktur aufgrund dieser Änderungen zu ermitteln.  Wenn Primobuchungen erstellt, werden Salden mit Finanzdimensionen " Vorwärts gebracht, siehe Nahen mit unterschiedlichen Geschäftsjahresenddaten Vorlage definiert. Die Anfangssaldoeneinträge können Finanzdimensionen in den Struktur- und Segmentkombinationen des aktuellen Kontos nicht mehr enthalten, die nicht mehr in der Struktur des aktuellen Kontos gültig sind. Wenn Ihre Organisation eine Finanzdimension für den einbehaltenen erwerbenden Anfangssaldo ausschließen, möchte die Finanzdimension festlegen, so nahes ** einzelnes ** und den Dimensionswert leer lassen.

## <a name="run-the-year-end-close-process"></a>Führen Sie den aus (Schließenprozess
Nachdem die am Jahresende Nahen Vorlagen erstellt wurden, wird der Jahresendeschließenprozess eingeleitet wurde, indem Ausführungsgeschäftsjahr ** ** im Aktivitätsbereich auswählt. Entweder wählen Sie alle oder eine Teilmenge juristische Personen aus der Vorlage aus, für die Jahresendeschließen ausführt. Wenn Sie zum ersten Mal Schließen (in einem Geschäftsjahr ausführen, werden Sie vermutlich alle juristischen Personen, um Anfangssalden für alle juristischen Personen erstellen. Wenn Sie am Jahresende Abschluss erneut ausführen, werden Sie möglicherweise, um den Prozess nur für die juristischen Personen, für ausführen Regulierungseingaben vor die gebucht wurden. 

Wählen Sie das Geschäftsjahr aus, die Sie ausführen möchten mit unterschiedlichen Geschäftsjahresenddaten für den Schließenprozess. Wenn mehr als eine Abschlussperiode für die letzte Periode des Geschäftsjahres vorhanden ist, wird das Feld verfügbar ** Periodenname **, sodass Sie auswählen, welche die Abschlussperiode, um die Abschlussbuchung zu buchen, wenn Einstellungen definiert, um die Abschlussbuchung zu erstellen. 

Geben Sie die Belegnummer ein, die oder nicht, je nach Einstellungen im den Hauptbuchparametern erforderlich sein kann. Die Belegnummer wird für alle juristischen Personen verwendet, die für den Schließenprozess mit unterschiedlichen Geschäftsjahresenddaten ausgewählt werden. Die Belegnummer wird nicht mithilfe eines Nummernkreises generiert. Es ist eine bewährte, eine Belegnummer eingegeben werden, wenn es nicht erforderlich ist. Das Eingeben einer Belegnummer wird es einfacher Primobuchung, die im neuen Geschäftsjahr zu suchen. Wenn keine Belegnummer eingegeben ist, wurde der Beleg für die Primobuchung leer. 

Wenn Sie ein vorangegangene Jahresende stornieren möchten, das für das ausgewählte Geschäftsjahr Lagerabschluss, Satz ** Treffen Sie die vorangegangene Führen rückgängig ** ** Ja **. Führen am Jahresende wird storniert, aber der Prozess kann zu einem beliebigen Zeitpunkt geprüft werden. Wenn Sie am Jahresende Abschluss stornieren, der Endenschließen ** Datum des letzten Jahres ** be nicht verfügbar. 

Der am Jahresende Schließenprozess wird übernommen, um im Stapelverarbeitungsmodus ausgeführt werden. Es ist eine bewährte, den Vorgang im Stapelverarbeitungsmodus ausführen, um den Benutzern zur Rücklieferung auf andere Aktivitäten zu ermöglichen. Nachdem der Schließenprozess mit unterschiedlichen Geschäftsjahresenddaten abgeschlossen ist, von Endenschließen ** Datum des letzten Jahres ** wird dem Sitzungsdatum aktualisiert.

Weitere Informationen finden Sie [schließt das Hauptbuchs am Perioden ende] (close-general-ledger-at-period-end.md).


