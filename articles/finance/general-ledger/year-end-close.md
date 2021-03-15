---
title: Jahresabschluss
description: In diesem Thema werden die erforderlichen Einstellungen und die Schritte für den Jahresabschlussprozess im Hauptbuch beschrieben.
author: kweekley
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed15659d156427d0f591a63df7ed0a1ecd4f23c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978410"
---
# <a name="year-end-close"></a>Jahresabschluss

[!include [banner](../includes/banner.md)]

In diesem Thema werden die erforderlichen Einstellungen und die Schritte für den Jahresabschlussprozess im Hauptbuch beschrieben. 

Am Ende eines Geschäftsjahrs müssen Sie den Jahresabschlussprozess ausführen, um Anfangssalden in das neue Jahr zu übertragen. Die meisten Organisationen führen den Jahresabschlussprozess mehrmals aus. Beim ersten Mal werden die Salden in das neue Geschäftsjahr verschoben. Der Jahresabschluss kann dann so oft wie nötig erneut ausgeführt werden, um die Salden aus den Regulierungseinträgen in das neue Geschäftsjahr zu verschieben. 

Während des Jahresabschlusses werden zwei Arten von möglichen Buchungen erstellt. Eine Primobuchung wird immer generiert und verwendet, um die Anfangssalden im neuen Geschäftsjahr zu erstellen. Die Primobuchung zeigt die Bilanzsachkontosalden im neuen Geschäftsjahr und die Salden der Gewinn- und Verlust-Sachkonten im Sachkonto für nicht ausgeschüttete Gewinne im neuen Geschäftsjahr. Die Abschlussbuchung wird optional erstellt, um die Salden der Gewinn- und Verlustkonten für das endende Geschäftsjahr auf Null zu bringen.

## <a name="prepare-to-run-the-year-end-close"></a>Vorbereitungen auf den Jahresabschluss
Validieren Sie die Einstellungen für folgende Elemente, ehe Sie den Jahresabschlussprozess durchführen: 

Auf der Seite **Hauptkonto**:

-   Stellen Sie sicher, das der **Hauptkontotyp** korrekt für alle Hauptkonten definiert ist. Der Hauptkontotyp wird verwendet, um zu bestimmen, ob der Saldo des Hauptkontos als Anfangssaldo oder Abschlusssaldo in die nicht ausgeschütteten Gewinne in der Primobuchung übernommen werden.
-   Das **Eröffnungskonto** kann für die Übertragung des Hauptkontosaldos in das neue Hauptkonto während des Jahresabschlusses verwendet werden. Das neue Hauptkonto wird in das Feld **Eröffnungskonto** eingegeben. In der Regel wird dies für Bilanzhauptkonten verwendet, wenn das Hauptkonto deaktiviert ist und ein neues Hauptkonto für das neue Geschäftsjahr verwendet wird.

Auf der Seite **Hauptbuchparameter** unter **Geschäftsjahresschluss**:

-   Die Option **Jahresabschlussbuchungen löschen** wird verwendet, um anzugeben, ob die von System generierte Primobuchung aus einem vorherigen Jahresabschluss gelöscht werden soll, wenn der Jahresabschluss erneut ausgeführt wird. Ist die Option auf **Ja** festgelegt, wird die vorherige Primobuchung gelöscht und eine neue Primobuchung basierend auf den aktuellen Salden erstellt. Ist die Option auf **Nein** festgelegt, bleibt die vorherige Primobuchung erhalten und es wird eine weitere Primobuchung erstellt, um die Salden aus angepassten Buchungen zu übertragen, die nach dem vorherigen Jahresabschluss gebucht wurden.
-   Die Option **Abschlussbuchungen bei Umbuchung erstellen** wird verwendet, um Abschlussbuchungen für das Geschäftsjahr zu erstellen, das abgeschlossen wird, um die Salden der Gewinn- und Verlustkonten auf Null zu bringen. Ist die Option auf **Ja** festgelegt, werden die Primobuchung und die Abschlussbuchung erstellt. Ist die Option auf **Nein** festgelegt, wird nur die Primobuchung für das nächste Geschäftsjahr erstellt, um die Salden zu übertragen. Die GuV-Konto-Salden verbleiben am Ende des Geschäftsjahrs.
-   Die Option **Geschäftsjahresstatus auf dauerhaft abgeschlossen festlegen** wird verwendet, um den Geschäftsjahresstatus dauerhaft auf abgeschlossen zu setzen. Verwenden Sie diese Einstellung mit Vorsicht, da alle Perioden mit einem Dauerhaft geschlossen-Status nicht erneut geöffnet werden können und keine Regulierungen im Geschäftsjahr gebucht werden können. Es ist eine bewährte Methode, diese Option auf **Nein** festzulegen.
-   Die Option **Belegnummer muss angegeben werden** wird verwendet, um festzulegen, ob eine Belegnummer erforderlich ist, wenn der Jahresabschlussprozess ausgeführt wird. Eine Belegnummer sollte erforderlich sein, um die Primobuchung einfach identifizieren zu können.

Auf der Seite **Steuerkalender**:

-   Das nächste Geschäftsjahr muss vorhanden sein, bevor der Jahresabschluss ausgeführt wird. Das nächste Geschäftsjahr ist erforderlich, um die Anfangssalden in der Eröffnungsperiode zu erstellen.

Auf der Seite **Sachkontokalender**:

-   Optional: Jeder Finanzzeitraum für das zu schließende Geschäftsjahr kann auf **Gesperrt** gesetzt werden, damit keine neuen Buchungen eingegeben werden können. Wenn Regulierungseingaben identifiziert werden, können die gesperrt Perioden erneut geöffnet werden, um neue Regulierungseinträge zu buchen, auch wenn der Jahresabschlussprozess bereits durchgeführt wurde.

## <a name="define-year-end-close-templates"></a>Definieren von Jahresabschlussvorlagen
Nachdem das System konfiguriert wurde, kann der Jahresabschlussprozess ausgeführt werden. Auf der Seite **Jahresabschluss** kann eine Vorlage für die Gruppe von juristischen Personen, für die der Jahresabschlussprozess durchgeführt wird, definiert werden. Die Vorlage wird bei jedem Jahresabschluss wiederverwendet, kann jedoch bei Änderungen in Ihrer Organisation geändert werden. 

Definieren Sie zunächst den **Gruppennamen**, und wählen Sie dann den Steuerkalender. Anhand des Gruppennamens sollte die enthaltene Gruppe von juristischen Personen identifiziert werden können.  Beispielsweise können die Vorlagen basierend auf der Geografie eingerichtet werden mit separaten Gruppen für juristische Personen aus Nordamerika, juristische EMEA-Personen und juristische APAC-Personen. 

Danach können die juristischen Personen zur Vorlage hinzugefügt werden. Juristische Personen können hinzugefügt werden, indem entweder eine Organisationshierarchie oder juristischen Personen ausgewählt werden. Wenn eine Organisationshierarchie ausgewählt ist, werden nur juristische Personen in der Hierarchie, die den ausgewählten Steuerkalender verwenden, zur Vorlage hinzugefügt. Wenn Sie die Option für das Hinzufügen von juristischen Personen zur Vorlage verwenden, können nur juristischen Personen mit dem gleichen Steuerkalender hinzugefügt werden. Der gleiche Steuerkalender ist erforderlich, da der Jahresabschluss über die Auswahl eines Geschäftsjahres ausgeführt wird. Dieses kann von Kalender zu Kalender unterschiedlich sein. 

Nachdem die juristischen Personen hinzugefügt wurden, definieren Sie die Hauptkonten für nicht ausgeschüttete Gewinne für die einzelnen juristischen Personen. Das Feld **Datum des letzten Jahresabschlusses** wird jedes Mal aktualisiert, wenn der Jahresabschluss für die juristische Person ausgeführt wird. 

Die Registerkarte **Finanzdimension** wird verwendet, um festzulegen, welche Finanzdimensionen für die Primobuchung verwendet werden. Beachten Sie, dass die Einstellungen, die Sie definieren, nur für die juristische Person relevant sind, die im Raster **Juristische Personen** auswählen. Sie wiederholen die Einrichtung für alle juristischen Personen im Raster. 

Die Option **Bilanzdimensionen übertragen** wird verwendet, um festzulegen, ob die Finanzdimensionen für die Buchungen, die auf den Bilanzkonten gebucht wurden, in der Primobuchung erhalten bleiben sollen. Es hat sich bewährt, diese Option auf **Ja** festzulegen. Die Option **Gewinn- und Verlustdimensionen übertragen** wird verwendet, um festzulegen, welche Finanzdimensionen in Buchungen, die auf dem Gewinn- und Verlustkonto gebucht wurden, auf das Hauptkonto für nicht ausgeschüttete Gewinne übertragen werden sollen. Identifizieren Sie hierfür zunächst die Finanzdimensionen, die für die ausgewählte juristische Person relevant sind. Hierzu zählen sämtliche Finanzdimensionen, die während des Jahres gebucht wurden, auch wenn die Finanzdimension nicht Teil einer aktiven Kontostruktur ist. Definieren Sie als Nächstes jede Dimension entweder als **Einzeln abschließen** oder **Alle abschließen**.  Der Standard ist **Alle abschließen**. Dabei bleiben die ursprünglichen Finanzdimsionswerte aus vorgenommenen Buchungen erhalten. Diese werden zum Erstellen von Anfangssalden für das Konto nicht ausgeschütteter Gewinne verwendet. Einzelne Anfangssalden für nicht ausgeschüttete Gewinnen werden für jede eindeutige Kombination von Finanzdimensionswerten erstellt. Wird **Einzeln abschließen** gewählt, werden alle mit der Finanzdimension vorgenommenen Buchungen zu einem Anfangssaldo nicht ausgeschütteter Gewinne für den Dimensionswert zusammengefasst, der im Feld nach **Einzeln abschließen** angegeben ist. Angenommen, alle Buchungen für das Geschäftsjahr wurden mit der Kontostruktur Hauptkonto - Abteilung vorgenommen. Für die Finanzdimension Abteilung auf der Vorlage ist **Einzeln abschließen** ausgewählt, und als Wert ist 100 eingegeben. Wenn das Gesamteinkommen aller Buchungen für die Abteilungen 200, 300 und 400 100.000 Euro ist, wird eine Primobuchung für nicht ausgeschüttete Gewinne - 100 erstellt. Wenn Sie **Einzeln abschließen** wählen und keinen Wert für die Finanzdimension angeben, werden alle Buchungen für die nicht ausgeschütteten Gewinne ohne diesen Wert vorgenommen. 

Der Jahresabschlussprozess muss sich nicht an Kontostrukturen orientieren. Dies liegt daran, dass sich die Kontostrukturen während des Geschäftsjahres ändern können und es aufgrund dieser Änderungen nicht immer möglich ist, die relevante Kontostruktur zu identifizieren.  Wenn Primobuchungen erstellt werden, werden die Salden mit Finanzdimensionen übertragen, wie in der Jahresabschlussvorlage definiert. Die Anfangssaldeneinträge können Finanzdimensionen enthalten, die nicht mehr in der aktuellen Kontostruktur enthalten sind, sowie Segmentkombinationen, die nicht mehr länger für die aktuelle Kontostruktur gelten. Wenn Ihre Organisation eine Finanzdimension für den Anfangssaldo nicht ausgeschütteter Gewinne ausschließen möchte, setzen Sie die Finanzdimension auf **Einzeln abschließen** und lassen den Dimensionswert leer.

## <a name="run-the-year-end-close-process"></a>Ausführen des Jahresabschlussprozesses
Nachdem die Jahresabschlussvorlagen erstellt wurden, wird der Jahresabschlussprozess initiiert, indem im Aktivitätsbereich die Option für **Jahresabschluss abschließen** gewählt wird. Wählen Sie entweder alle oder eine Untergruppe von juristischen Personen aus der Vorlage, für die der Jahresabschluss ausgeführt werden soll. Wenn Sie den Jahresabschluss das erste Mal in einem Geschäftsjahr ausführen, werden Sie vermutlich alle juristischen Personen auswählen, um Anfangssalden für alle juristischen Personen zu erstellen. Wenn Sie den Jahresabschluss erneut ausführen, können Sie diesen nur für die juristischen Personen durchführen, für die Regulierungseinträge gebucht wurden. 

Wählen Sie das Geschäftsjahr aus, für das Sie den Jahresabschlussprozess durchführen möchten. Wenn mehr als eine Abschlussperiode für die letzte Periode des Geschäftsjahres vorhanden ist, wird das Feld **Periodenname** verfügbar, sodass Sie auswählen können, für welche Abschlussperiode die Abschlussbuchung vorgenommen werden soll, wenn das Setup so definiert ist, dass eine Abschlussbuchung erstellt wird. 

Geben Sie eine Belegnummer ein, die je nach Einstellung der Hauptbuchparameter erforderlich ist oder nicht. Die Belegnummer wird für alle juristischen Personen verwendet, die für den Jahresabschlussprozess ausgewählt wurden. Die Belegnummer wird nicht mit einem Nummernkreis generiert. Es hat sich bewährt, eine Belegnummer auch dann einzugeben, wenn sie nicht erforderlich ist. Das Eingeben einer Belegnummer vereinfacht das Auffinden der Primobuchung im neuen Geschäftsjahr. Wenn keine Belegnummer eingegeben ist, ist der Beleg für die Primobuchung leer. 

Wenn Sie einen vorherigen Jahresabschluss für das ausgewählte Geschäftsjahr stornieren möchten, setzen Sie **Vorherigen Abschluss rückgängig machen** auf **Ja**. Der Jahresabschluss wird rückgängig gemacht, aber der Prozess kann jederzeit wieder ausgeführt werden. Wenn Sie einen Jahresabschluss rückgängig machen, ist **Datum des letzten Jahresabschlusses** nicht verfügbar. 

Der Jahresabschlussprozess wird standardmäßig im Stapelverarbeitungsmodus ausgeführt. Es hat sich bewährt, den Prozess im Stapelverarbeitungsmodus auszuführen, damit der Benutzer zu anderen Aktivitäten zurückkehren kann. Nach Abschluss des Jahresabschlussprozesses wird das Feld **Datum des letzten Jahresabschlusses** mit dem Sitzungsdatum aktualisiert.

Weitere Informationen erhalten Sie unter [Abschluss des Hauptbuchs am Ende der Periode.](close-general-ledger-at-period-end.md) und [Geschäftsjahr beenden](tasks/close-fiscal-year.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]