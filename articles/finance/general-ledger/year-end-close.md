---
title: Jahresabschluss
description: In diesem Thema werden die erforderlichen Einstellungen und die Schritte für den Jahresabschlussprozess im Hauptbuch beschrieben.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 247c3286124da946937c8afd248a275e5a745044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725232"
---
# <a name="year-end-close"></a>Jahresabschluss

[!include [banner](../includes/banner.md)]

In diesem Thema werden die erforderlichen Einstellungen und die Schritte für den Jahresabschlussprozess im Hauptbuch beschrieben.

Am Ende eines Geschäftsjahrs müssen Sie den Jahresabschlussprozess ausführen, um Anfangssalden in das neue Jahr zu übertragen. Die meisten Organisationen führen den Jahresabschlussprozess mehrmals aus. Die erste Ausführung verschiebt die Salden in das neue Geschäftsjahr. Dieser Prozess kann dann so oft wie nötig erneut ausgeführt werden, um die Salden aus den Regulierungseinträgen in das neue Geschäftsjahr zu verschieben.

Während des Jahresabschlusses werden zwei Arten von möglichen Buchungen erstellt. Eine Primobuchung wird immer generiert und verwendet, um die Anfangssalden im neuen Geschäftsjahr zu erstellen. Die Primobuchung zeigt die Bilanzsachkontosalden im neuen Geschäftsjahr und die Salden der Gewinn- und Verlust-Sachkonten im Sachkonto für nicht ausgeschüttete Gewinne im neuen Geschäftsjahr. Die Abschlussbuchung wird optional erstellt, um die Salden der Gewinn- und Verlustkonten für das endende Geschäftsjahr auf Null zu bringen.

## <a name="prepare-to-run-the-year-end-close"></a>Vorbereitungen auf den Jahresabschluss

Validieren Sie die Einstellungen für folgende Elemente, ehe Sie den Jahresabschlussprozess durchführen:

Auf der Seite **Hauptkonto**:

- Stellen Sie sicher, dass das **Hauptkontotyp** Feld für jedes Hauptkonto richtig gesetzt ist. Der Hauptkontotyp wird verwendet, um zu bestimmen, ob der Saldo des Hauptkontos als Anfangssaldo oder Abschlusssaldo in die nicht ausgeschütteten Gewinne in der Primobuchung übernommen werden.
- Das Eröffnungskonto kann für die Übertragung des Hauptkontosaldos in das neue Hauptkonto während des Jahresabschlusses verwendet werden. Das neue Hauptkonto wird in das Feld **Eröffnungskonto** eingegeben. In der Regel wird dieses Feld für Bilanzhauptkonten verwendet, wenn das Hauptkonto deaktiviert ist und ein neues Hauptkonto für das neue Geschäftsjahr verwendet wird.

Auf der Seite **Hauptbuchparameter** unter **Geschäftsjahresschluss**:

- Die Option **Bestehende Jahresabschlussbuchungen löschen, wenn das Jahr erneut geschlossen wird** wird verwendet, um anzugeben, ob die von System generierte Primobuchung aus einem vorherigen Jahresabschluss gelöscht werden soll, wenn der Jahresabschluss erneut ausgeführt wird. Ist die Option auf **Ja** festgelegt, wird die vorherige Primobuchung gelöscht und eine neue Primobuchung basierend auf den aktuellen Salden erstellt. Ist die Option auf **Nein** festgelegt, bleibt die vorherige Primobuchung erhalten und es wird eine weitere Primobuchung erstellt, um die Salden aus angepassten Buchungen zu übertragen, die nach dem vorherigen Jahresabschluss gebucht wurden.
- Die Option **Abschlussbuchungen bei Umbuchung erstellen** wird verwendet, um Abschlussbuchungen für das Geschäftsjahr zu erstellen, das abgeschlossen wird, um die Salden aller Hauptkonten auf 0 (Null) zu bringen. Ist die Option auf **Ja** festgelegt, werden die Erüffnungsbuchung und die Abschlussbuchung erstellt. Ist die Option auf **Nein** festgelegt, wird nur die Eröffnungsbuchung für das nächste Geschäftsjahr erstellt, um die Salden zu übertragen. Die Hauptkonto-Salden verbleiben am Ende des Geschäftsjahrs.
- Die Option **Geschäftsjahresstatus auf dauerhaft abgeschlossen festlegen** wird verwendet, um den Geschäftsjahresstatus dauerhaft auf abgeschlossen zu setzen. Verwenden Sie diese Option mit Bedacht, da Perioden, die einen dauerhaft geschlossenen Status haben, nicht wieder geöffnet werden können. Anpassungen können daher nicht auf das Geschäftsjahr gebucht werden. Es hat sich bewährt, diese Option auf **Nein** festzulegen.
- Die **Gutscheinnummer muss ausgefüllt werden** Option wurde entfernt. Ein Beleg ist jetzt erforderlich, wenn der Jahresabschlussprozess ausgeführt wird. Zu diesem Zeitpunkt wird die Gutscheinnummer manuell eingegeben.

Auf der Seite **Steuerkalender**:

- Das nächste Geschäftsjahr muss vorhanden sein, bevor der Jahresabschluss ausgeführt wird. Andernfalls können die Anfangssalden nicht in der Eröffnungsperiode erstellt werden.

Auf der Seite **Sachkontokalender**:

- Optional: Jeder Finanzzeitraum für das zu schließende Geschäftsjahr kann auf **Gesperrt** gesetzt werden, damit keine neuen Buchungen eingegeben werden können. Wenn Regulierungseingaben identifiziert werden, können die gesperrt Perioden erneut geöffnet werden, um neue Regulierungseinträge zu buchen, auch wenn der Jahresabschlussprozess bereits durchgeführt wurde.

Auf der **Einrichtung der Vorlage für den Jahresabschluss** Seite:

- Wenn **Verbesserungen im Hauptbuch zum Jahresende** aktiviert ist, wird das Einrichten der Jahresabschlussvorlage von der Ausführung des Jahresabschlusses getrennt. Die Vorlage kann auf definiert werden unter der **Einrichtung der Vorlage für den Jahresabschluss** Seite (**Hauptbuch \> Ledger-Einrichtung \> Einrichtung der Vorlage für den Jahresabschluss**) oder kann über den Jahresabschlussprozess aufgerufen werden.

## <a name="define-year-end-close-templates"></a>Definieren von Jahresabschlussvorlagen

Nachdem das System konfiguriert wurde, kann der Jahresabschlussprozess ausgeführt werden. Auf der Seite **Jahresabschlussvorlage einrichte** kann eine Vorlage für die Gruppe von juristischen Personen, für die der Jahresabschlussprozess durchgeführt wird, definiert werden. Die Vorlage wird bei jedem Jahresabschluss wiederverwendet, kann jedoch bei Änderungen in Ihrer Organisation geändert werden.

Definieren Sie zunächst das Feld **Gruppennamen**, und wählen Sie dann den Steuerkalender. Anhand des Gruppennamens sollte die enthaltene Gruppe von juristischen Personen identifiziert werden können. Beachten Sie beim Festlegen der Gruppen juristischer Personen, dass juristische Personen nur dann in dieselbe Gruppe aufgenommen werden können, wenn für sie derselbe Steuerkalender ausgewählt ist. Beispielsweise können die Vorlagen basierend auf der Geografie eingerichtet werden mit separaten Gruppen für juristische Personen aus Nordamerika, juristische Personen aus Europa, dem Nahen Osten und Afrika (EMEA) und juristische Personen aus Asien.

Danach können die juristischen Personen zur Vorlage hinzugefügt werden. Juristische Personen können hinzugefügt werden, indem entweder eine Organisationshierarchie oder juristischen Personen ausgewählt werden. Wenn eine Organisationshierarchie ausgewählt ist, werden nur juristische Personen in der Hierarchie, die den ausgewählten Steuerkalender verwenden, zur Vorlage hinzugefügt. Wenn Sie die Option für das Hinzufügen von juristischen Personen zur Vorlage verwenden, können nur juristischen Personen mit dem gleichen Steuerkalender hinzugefügt werden. Der gleiche Steuerkalender ist erforderlich, da der Jahresabschluss über die Auswahl eines Geschäftsjahres ausgeführt wird. Dieses kann von Kalender zu Kalender unterschiedlich sein.

Nachdem die juristischen Personen hinzugefügt wurden, definieren Sie die Hauptkonten für nicht ausgeschüttete Gewinne für die einzelnen juristischen Personen.

Die Registerkarte **Finanzdimension** wird verwendet, um festzulegen, welche Finanzdimensionen für das Öffnen der Transaktion verwendet werden. Beachten Sie, dass die Einstellungen auf dieser Registerkarte nur für die juristische Person relevant sind, die im Raster **Juristische Personen** ausgewählt sind. Sie müssen die Einrichtung für alle juristischen Personen im Raster wiederholen.

Die Option **Bilanzdimensionen übertragen** wird verwendet, um festzulegen, ob die Finanzdimensionen für die Buchungen, die auf den Bilanzkonten gebucht wurden, in der Transaktionen geöffnet werden. Es hat sich bewährt, diese Option auf **Ja** festzulegen. Die Einstellung für die Bilanzdimensionen wirkt sich nicht auf vorhandene Salden in den Sachkonten für einbehaltene Einnahmen aus. Diese Salden werden durch die Gewinn- und Verlustdimensionen bestimmt, die im nächsten Abschnitt definiert werden. Das Geschäftsjahr 2019 war beispielsweise das erste abgeschlossene Jahr, und die **Alle schließen** Option wurde verwendet, um die **Abteilung** und **Kostenstelle** Dimension zu schließen. In diesem Fall wurde für jede Kombination aus Abteilung und Kostenstelle ein separates Gewinnvortragskonto angelegt. Beim Jahresabschluss für das Geschäftsjahr 2020 bleiben die Gewinnrücklagen des Vorjahres unverändert, auch wenn die **Bilanzdimensionen übertragen** auf **Nein** festgelegt ist. Salden, die aus früheren Jahresabschlüssen in die Gewinnrücklagen gebucht wurden, werden nie geändert.

Die Option **Gewinn- und Verlustdimensionen übertragen** wird verwendet, um festzulegen, welche Finanzdimensionen in Buchungen, die auf dem Gewinn- und Verlustkonto gebucht wurden, auf das Hauptkonto für nicht ausgeschüttete Gewinne übertragen werden sollen. Identifizieren Sie dazu zunächst die Finanzdimensionen, die für die ausgewählte juristische Person relevant sind. Dazu zählen sämtliche Finanzdimensionen, die während des Jahres gebu cht wurden, auch wenn die Finanzdimension nicht Teil einer aktiven Kontostruktur ist. Definieren Sie als Nächstes jede Dimension entweder als **Einzeln abschließen** oder **Alle abschließen**. Die Standardoption ist **Alle schließen**. Dabei bleiben die ursprünglichen Finanzdimsionswerte aus vorgenommenen Buchungen erhalten. Diese werden zum Erstellen von Anfangssalden für das Konto nicht ausgeschütteter Gewinne verwendet. Einzelne Anfangssalden für nicht ausgeschüttete Gewinnen werden für jede eindeutige Kombination von Finanzdimensionswerten erstellt. Wird **Einzeln abschließen** gewählt, werden alle mit der Finanzdimension vorgenommenen Transaktionen zu einem Anfangssaldo nicht ausgeschütteter Gewinne für den Dimensionswert zusammengefasst, der im Feld nach **Einzeln abschließen** angegeben ist. Angenommen, alle Buchungen für das Geschäftsjahr wurden mit der Kontostruktur **Hauptkonto - Abteilung** vorgenommen. Für die Finanzdimension **Abteilung** auf der Vorlage ist **Einzeln abschließen** ausgewählt, und als Wert ist **100** eingegeben. Wenn das Gesamteinkommen aller Buchungen für die Abteilungen 200, 300 und 400 100.000 Euro ist, wird eine Primobuchung für nicht **ausgeschüttete Gewinne - 100** erstellt. Wenn Sie **Einzeln abschließen** wählen aber keinen Wert für die Finanzdimension angeben, werden alle Buchungen für die nicht ausgeschütteten Gewinne ohne diesen Wert vorgenommen.

## <a name="run-the-year-end-close-process"></a>Ausführen des Jahresabschlussprozesses

Nachdem die Vorlagen für den Jahresabschluss erstellt wurden, können Sie den Jahresabschlussprozess auf der **Jahresabschluss** Seite (**Hauptbuch \> Zeitraum schließen \> Jahresabschluss**) initieren. Bevor Sie den Jahresabschluss ausführen, können Sie neue Vorlagen für den Jahresabschluss hinzufügen oder vorhandene Vorlagen ändern, indem Sie **Einrichtung der Vorlage für den Jahresabschluss** auswählen, um die Einrichtungsseite für die Vorlagen zu öffnen.

Wählen Sie die Vorlage für den Jahresabschluss aus, und wählen Sie dann im Aktivitätsbereich **Jahresende abschließen**. Wählen Sie entweder alle oder eine Untergruppe von juristischen Personen aus der Vorlage aus, für die der Jahresabschluss ausgeführt werden soll. Wenn Sie den Jahresabschluss das erste Mal in einem Geschäftsjahr ausführen, werden Sie vermutlich alle juristischen Personen auswählen, um Anfangssalden für alle juristischen Personen zu erstellen. Wenn Sie den Jahresabschluss erneut ausführen, möchten Sie diese allenfalls nur für die juristischen Personen durchführen, für die Regulierungseinträge gebucht wurden.

Dann wählen Sie das Geschäftsjahr aus, für das Sie den Jahresabschlussprozess durchführen möchten. Existiert für die letzte Periode des Geschäftsjahres mehr als eine Abschlussperiode, wird das Feld **Periodenname** verfügbar. Sie können dann die Abschlussperiode auswählen, die zum Buchen des Abschlussgeschäfts verwendet werden soll, wenn die Einrichtung zum Erstellen des Abschlussgeschäfts definiert ist.

Geben Sie als Nächstes eine Gutscheinnummer ein. Die Belegnummer wird für alle juristischen Personen verwendet, die Sie für den Jahresabschlussprozess ausgewählt wurden. Die Belegnummer wird nicht mit einem Nummernkreis generiert.

Der Jahresabschlussprozess wird standardmäßig im Stapelverarbeitungsmodus ausgeführt. Daher können Sie nach der Initiierung zu anderen Aktivitäten zurückkehren.

Da sich Kontenstrukturen im Laufe eines Geschäftsjahres ändern können, kann die relevante Kontenstruktur nicht immer identifiziert werden. Deshalb muss sich der Jahresabschlussprozess sich nicht an Kontostrukturen orientieren. Wenn offene Buchungen erstellt werden, werden die Salden mit Finanzdimensionen übertragen, wie in der Jahresabschlussvorlage definiert. Die Anfangssaldeneinträge können Finanzdimensionen enthalten, die nicht mehr in der aktuellen Kontostruktur enthalten sind, sowie auc Segmentkombinationen, die nicht mehr länger für die aktuelle Kontostruktur gelten. Wenn Ihre Organisation eine Finanzdimension für den Anfangssaldo nicht ausgeschütteter Gewinne ausschließen möchte, setzen Sie die Finanzdimension auf **Einzeln abschließen** und lassen den Dimensionswert leer.

Nach Abschluss des Prozesses wird für jede Kombination aus einer juristischen Person und einem Geschäftsjahr ein Datensatz erstellt. Sier sehen nur die Informationen für die juristischen Personen, auf die sie zugreifen können. Jeder Datensatz enthält das Systemdatum und die Uhrzeit, zu der der Prozess ausgeführt wurde, sowie einen direkten Link zu den Belegen, die für den Jahresabschluss erstellt wurden.

[![Datensätze, die auf dem Inforegister zum Jahresende-Abschlussverlauf des Inforegisters der Abschlussseite zum Jahresende erstellt wurden](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Wenn Sie den Jahresabschluss erneut ausführen, sehen Sie je nach Einstellung der Einstellung für jede Kombination aus juristischer Person und Geschäftsjahr einen oder mehrere Datensätze **Vorhandene Jahresendeinträge beim Jahresabschluss löschen** Option auf der **Hauptbuchparameter** Seite:

- Ist die vorherige Option **Ja** eingestellt, wird der vorherige Abschluss gelöscht. Der Datensatz ist markiert als **Umgekehrt**, und mit dem Datum und der Uhrzeit der Stornierung versehen. Außerdem wird der Link zur Gutscheinnummer entfernt. Wenn der Jahresabschluss abgeschlossen ist, wird ein neuer Datensatz für den neu erstellten Beleg erstellt.
- Wenn die Option auf **Nein** festgelegt wird, bleibt der Datenstz für den letzten Jahresabschluss zusammen mit der Verknüpfung zum Gutschein erhalten. Jedes Mal, wenn der Jahresabschluss wiederholt wird, wird ein neuer Datensatz erstellt, zusammen mit einer Verknüpfung zu den neuen Gutscheinen.

## <a name="reverse-the-year-end-close-process"></a>Jahresabschlussprozesses rückgängig machen

Auf der **Jahresabschluss** Seite können Sie einen Jahresabschluss stornieren. Wählen Sie den Datensatz für die Kombination aus juristischer Person und Geschäftsjahr aus, die storniert werden muss, und wählen Sie dann **Jahresschluss rückgängig machen**. Der Stornoprozess löscht alle Eröffnungs- und Schlussbelege, die für das Geschäftsjahr erstellt wurden. Der Datensatz ist markiert als **Umgekehrt**, und mit dem Datum und der Uhrzeit der Stornierung versehen. Außerdem wird der Link zur Gutscheinnummer entfernt. Die Stornierung wird wie der Jahresabschlussprozess standardmäßig im Stapelverarbeitungsmodus ausgeführt.

Im  **Stornieren** Kontrollkästchen, das über dem Raster verfügbar ist, können Sie die Datensätze für stornierte Jahresabschlussprozesse ein- oder ausblenden. Nachdem Sie den Prozess **Jahresschluss rückgängig machen** ausgeführt haben, müssen Sie möglicherweise das Kontrollkästchen **Umgekehrt anzeigen** auswählen, um den Datensatz anzuzeigen. Sie können zusätzliche Filter festlegen, um andere Informationen anzuzeigen.

[![Verwenden des Kontrollkästchens Umgekehrt anzeigen, um Datensätze für stornierte Jahresabschlussprozesse auf der Seite Jahresabschluss anzuzeigen](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Weitere Informationen erhalten Sie unter [Abschluss des Hauptbuchs am Ende der Periode.](close-general-ledger-at-period-end.md) und [Geschäftsjahr beenden](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
