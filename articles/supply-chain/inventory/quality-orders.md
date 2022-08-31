---
title: Qualitätsprüfungsaufträge
description: Dieser Artikel beschreibt, wie Sie manuell oder automatisch Qualitätsprüfungsaufträge erstellen und wie Sie damit arbeiten, um in Microsoft Dynamics 365 Supply Chain Management Inspektionen durchzuführen und Testergebnisse zu erfassen.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb7ab1de0fb4d93ed18f1862630c1af7af7f3095
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857778"
---
# <a name="quality-orders"></a>Qualitätsprüfungsaufträge

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie manuell oder automatisch Qualitätsprüfungsaufträge erstellen und wie Sie damit arbeiten, um in Microsoft Dynamics 365 Supply Chain Management Inspektionen durchzuführen und Testergebnisse zu erfassen.

## <a name="automatically-created-quality-orders"></a>Automatisch erstellte Qualitätsprüfungsaufträge

Sie können das System so konfigurieren, dass es automatisch Qualitätsprüfungsaufträge erstellt, basierend auf den Regeln für die Artikelmusteraufnahme. Weitere Informationen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahme](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Qualitätsprüfungsaufträge manuell erstellen

Um einen Qualitätsprüfungsauftrag manuell zu erstellen, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Dialogfeld **Qualitätsprüfungsaufträge** im Feld **Referenztyp** die Bestandsreferenz, auf die sich Ihr Qualitätsprüfungsauftrag beziehen soll. Eine Beschreibung der Referenztypen, die zur Auswahl stehen, finden Sie im Abschnitt [Referenztypen für Qualitätsprüfungsaufträge](#ref-types) weiter unten in diesem Artikel.

    > [!NOTE]
    > Der Bestand, der sich auf die ausgewählte Referenz bezieht, muss vorhanden sein. Wenn für die von Ihnen gewählte Kombination aus Referenztyp, Menge und Bestandsdimensionen kein Bestand verfügbar ist, erhalten Sie eine Fehlermeldung.

1. Führen Sie einen dieser Schritte aus, je nach dem Wert, den Sie im Feld **Bezugstyp** ausgewählt haben:

    - Wenn Sie **Bestand** gewählt haben, sind keine zusätzlichen Referenzinformationen erforderlich.
    - Wenn Sie **Verkauf** oder **Einkauf** gewählt haben, geben Sie die folgenden Informationen an:

        - **Kontoauswahl** – Verweisen Sie auf die Kunden- oder Lieferantennummer.
        - **Referenznummer** – Verweist auf die Nummer des Verkaufsauftrags oder der Einkaufsbestellung.
        - **Referenzlos** – Verweisen Sie auf die spezifische Zeile des Verkaufsauftrags oder der Einkaufsbestellung.

    - Wenn Sie **Produktion**, **Quarantäne** oder **Kuppelprodukt-Produktion** gewählt haben, referenzieren Sie im Feld **Referenznummer** die Produktionsauftrags-, Batch- oder Quarantäneauftragsnummer.
    - Wenn Sie **Arbeitsplanvorgang** gewählt haben, geben Sie die folgenden Informationen an:

        - **Referenznummer** – Verweist auf die Produktionsauftrags- oder Batchauftragsnummer.
        - **Betriebsnr.** - Verweisen Sie auf die spezifische Nummer des Arbeitsplanvorgangs.
        - **Vorgang** – Verweisen Sie auf den spezifischen Arbeitsplanvorgang.
        - **Ressource** – Verweisen Sie auf die spezifische Ressource, die mit dem Arbeitsplanvorgang verwendet werden muss.

1. Wählen Sie im Feld **Testgruppe** die Gruppe von Tests, die durchgeführt werden müssen.
1. Geben Sie in das Feld **Menge** die Menge der Elemente ein, die getestet werden müssen.
1. Geben Sie im Bereich **Bestandsdimensionen** alle zusätzlichen Bestandsdimensionen ein, die für das ausgewählte Element erforderlich sind.
1. Wählen Sie **OK**.

Nachdem ein Qualitätsprüfungsauftrag erstellt wurde, können Sie damit beginnen, den Bestand zu prüfen und die Prüfergebnisse zu erfassen. Weitere Informationen über das Aufzeichnen und Validieren von Prüfergebnissen finden Sie unter [Prüfen der Qualität von Waren](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Referenztypen für Qualitätsprüfungsaufträge

Qualitätsprüfungsaufträge werden verwendet, um die Details zu Inspektionen und Testergebnissen für bestimmte Bestände in Ihrem Lagerort zu verfolgen. Ein Qualitätsprüfungsauftrag muss eine Referenz enthalten, die die Quelle des zu prüfenden Bestands darstellt. Qualitätsprüfungsaufträge können mit den folgenden Referenztypen verknüpft werden:

- **Bestand** – Dieser Referenztyp zeigt an, dass Sie den Bestand prüfen, der sich im Lagerbestand befindet. Inspektionen dieser Art sind typischerweise zufällig oder ungeplant und werden durchgeführt, wenn eine Arbeitskraft am Lagerort ein Problem feststellt.
- **Verkauf** – Dieser Referenztyp zeigt an, dass Sie einen Bestand prüfen, der mit einem bestimmten Verkaufsauftrag verbunden ist. Inspektionen dieses Typs beziehen sich typischerweise auf Kundenspezifikationen oder die Erstellung eines Zertifikats für die Analyse (CoA), das einem Debitor als Teil einer Lieferung zur Verfügung gestellt werden muss. (Ein CoA wird manchmal auch als Konformitätszertifikat bezeichnet \[CoC\]).
- **Einkauf** – Dieser Referenztyp zeigt an, dass Sie einen Bestand prüfen, der mit einer Einkaufsbestellung verknüpft ist. Inspektionen dieses Typs werden oft verwendet, um eingehende Waren zu prüfen, bevor sie in den Bestand aufgenommen oder in Produktionsprozessen verbraucht werden.
- **Produktion** – Dieser Referenztyp zeigt an, dass Sie einen Bestand inspizieren, der mit einem Produktionsauftrag zusammenhängt. Inspektionen dieses Typs werden oft verwendet, um fertige Waren zu prüfen, bevor sie in den Bestand aufgenommen werden.
- **Quarantäne** – Dieser Referenztyp zeigt an, dass Sie Bestände prüfen, die mit einem Quarantäneauftrag verbunden sind. Quarantäneaufträge sind ein spezieller Auftragstyp, der den Bestand in einem abgetrennten Lagerort oder einem abgetrennten Bereich in Ihrem Lager verfolgt. Inspektionen dieses Typs werden oft verwendet, um Waren zu inspizieren, die ein Debitor zurückgegeben hat oder die zur weiteren Analyse in Quarantäne gestellt wurden. Quarantäneaufträge können aus Qualitätsprüfungsaufträgen generiert werden. Alternativ können sie aus anderen Quellen erzeugt werden, und dann können Qualitätsprüfungsaufträge mit den Quarantäneaufträgen verknüpft werden.
- **Arbeitsplanvorgang** – Dieser Referenztyp zeigt an, dass Sie Bestände prüfen, die sich auf einen bestimmten Schritt des Arbeitsplans für einen Produktionsauftrag beziehen. Inspektionen dieses Typs werden typischerweise verwendet, um die Ressource in Fertigung (RIF) eines Produkts zu analysieren, bevor es in den nächsten Schritt des Produktionsprozesses übergeht.
- **Kuppelprodukt-Produktion** – Dieser Referenztyp zeigt an, dass Sie einen Bestand prüfen, der sich auf ein Kuppelprodukt eines Produktionsauftrags bezieht. Inspektionen dieses Typs werden typischerweise verwendet, um das Kuppelprodukt eines Batchauftrags zu prüfen, bevor das Kuppelprodukt in den Bestand aufgenommen wird.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Qualitätsprüfungsaufträge aus verschiedenen Teilen des Systems anzeigen und erstellen

Qualitätsprüfungsaufträge können manuell erstellt werden. Alternativ können sie automatisch erstellt werden, basierend auf den Qualitätszuordnungen, die Sie definieren. Weitere Informationen über das Erstellen und Verwalten der automatischen Erstellung von Qualitätsprüfungsaufträgen finden Sie unter [Qualitätsverbünde](quality-associations.md).

Sie können die Seite „Qualitätsprüfungsauftrag“ verwenden, um manuell einen neuen Qualitätsprüfungsauftrag zu erstellen oder den Status eines Qualitätsprüfungsauftrags anzuzeigen, der mit einem anderen Datensatz verknüpft ist. Es gibt mehrere Möglichkeiten für den Zugriff auf die Seite Qualitätsprüfungsauftrag.

### <a name="from-the-quality-orders-page"></a>Von der Seite Qualitätsprüfungsaufträge

Um Qualitätsprüfungsaufträge manuell zu erstellen und alle vorhandenen Qualitätsprüfungsaufträge anzuzeigen, gehen Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**. Die verbleibenden Abschnitte dieses Artikels beschreiben, wie Sie mit der Seite **Qualitätsprüfungsaufträge** arbeiten können.

### <a name="from-sales-orders"></a>Von Verkaufsaufträgen

Um mit Qualitätsprüfungsaufträgen zu arbeiten, die mit Ihren Verkaufsaufträgen zusammenhängen, gehen Sie zu **Vertrieb und Marketing \> Verkaufsaufträge \> Alle Verkaufsaufträge**, und folgen Sie dann einem dieser Schritte:

- Öffnen Sie einen Verkaufsauftrag, oder wählen Sie ihn im Raster aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Entnehmen und Packen** in der Gruppe **Qualitätsmanagement** die Option **Qualitätsprüfungsaufträge**, um die Seite **Qualitätsprüfungsaufträge** zu öffnen. Dort können Sie Qualitätsprüfungsaufträge anzeigen, erstellen oder aktualisieren, die sich auf den Verkaufsauftrag beziehen.
- Öffnen Sie einen Verkaufsauftrag und wählen Sie dann auf der Registerkarte **Kopfzeile** die Registerkarte **Allgemein**. Das Feld **Qualitätsprüfungsauftrag-Status** zeigt den Gesamtstatus aller Qualitätsprüfungsaufträge, die sich auf den Kundenauftrag beziehen.
- Öffnen Sie einen Verkaufsauftrag und wählen Sie dann auf der Registerkarte **Zeilen** die Registerkarte **Verkaufsauftragszeilen**. Die Spalte **Qualitätsprüfungsauftrag Status** zeigt den Status jeder Zeile des Verkaufsauftrags an.

### <a name="from-purchase-orders"></a>Aus Einkaufsbestellungen

Um mit Qualitätsprüfungsaufträgen zu arbeiten, die sich auf Ihre Bestellungen beziehen, gehen Sie zu **Beschaffung und Quellen \> Einkaufsbestellungen \> Alle Bestellungen**, und folgen Sie dann einem der folgenden Schritte:

- Öffnen Sie eine Einkaufsbestellung, oder wählen Sie sie im Raster aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Empfang** in der Gruppe **Qualitätsmanagement** den Eintrag **Qualitätsprüfungsaufträge**, um die Seite **Qualitätsprüfungsaufträge** zu öffnen. Dort können Sie Qualitätsprüfungsaufträge anzeigen, erstellen oder aktualisieren, die sich auf die Einkaufsbestellung beziehen.
- Öffnen Sie eine Einkaufsbestellung und wählen Sie dann auf der Registerkarte **Kopf** die Registerkarte **Allgemein** aus. Das Feld **Qualitätsbestellstatus** zeigt den Gesamtstatus aller Qualitätsprüfungsaufträge an, die sich auf die Bestellung beziehen.
- Öffnen Sie eine Bestellung und wählen Sie dann auf der Registerkarte **Zeilen** das Inforegister **Bestellzeilen**. Die Spalte **Qualitätsprüfungsauftrag Status** zeigt den Status jeder Zeile der Einkaufsbestellung an.

### <a name="from-production-orders"></a>Aus Produktionsaufträgen

Um mit Qualitätsprüfungsaufträgen zu arbeiten, die sich auf Ihre Arbeitsaufträge beziehen, gehen Sie zu **Produktionskontrolle \> Produktionsaufträge \> Alle Produktionsaufträge**, und folgen Sie dann einem der folgenden Schritte:

- Öffnen Sie einen Produktionsauftrag, oder wählen Sie ihn im Raster aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Ansicht** in der Gruppe **Qualität verwalten** den Eintrag **Qualitätsaufträge**, um die Seite **Qualitätsaufträge** zu öffnen. Dort können Sie Qualitätsprüfungsaufträge, die sich auf den Produktionsauftrag beziehen, anzeigen, erstellen oder aktualisieren.
- Öffnen Sie einen Produktionsauftrag, oder wählen Sie ihn im Raster aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Produktionsdetails** den Eintrag **Arbeitsplan**, um die Seite **Produktionsplan** zu öffnen. Um die Qualitätsprüfungsaufträge anzuzeigen, die sich auf einen Arbeitsplan-Vorgang beziehen, führen Sie einen der folgenden Schritte aus:

    - Wählen Sie den gewünschten Arbeitsplanvorgang im Raster aus. Wählen Sie dann im Aktivitätsbereich **Abfragen \> Qualitätsprüfungsaufträge**.
    - Wählen Sie den Wert im Feld **Vorgang. Nr.** Feld für den Arbeitsplanvorgang des Ziels, um dessen **Produktionsplan**-Detailseite zu öffnen. Auf der Registerkarte **Allgemein** zeigt das Feld **Status des Qualitätsprüfungsauftrags** den Status für die Qualitätsprüfungsaufträge an, die sich auf den Arbeitsplanvorgang beziehen.

- Öffnen Sie einen Produktionsauftrag, und wählen Sie das Inforegister **Allgemein**. Das Feld **Qualitätsprüfungsauftrag-Status** zeigt den Status der Qualitätsprüfungsaufträge an, die sich auf den Fertigungsauftrag beziehen.

### <a name="from-quarantine-orders"></a>Aus Quarantäneaufträgen

Um mit Qualitätsprüfungsaufträgen zu arbeiten, die sich auf Ihre Quarantäneaufträge beziehen, gehen Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Quarantäneaufträge**, und folgen Sie dann einem dieser Schritte:

- Überprüfen Sie die Werte in der Spalte **Qualitätsprüfungsauftrag Status**. Auf diese Weise können Sie sich über den Gesamtstatus aller Qualitätsprüfungsaufträge informieren, die mit jedem Quarantäneauftrag im Raster verbunden sind.
- Wählen Sie einen Quarantäneauftrag im Raster aus und wählen Sie dann im Aktivitätsbereich **Qualitätsprüfungsaufträge**, um Qualitätsprüfungsaufträge anzuzeigen, zu erstellen oder zu aktualisieren, die mit dem Quarantäneauftrag zusammenhängen.

## <a name="advanced-actions-for-quality-orders"></a>Erweiterte Aktionen für Qualitätsprüfungsaufträge

Sie können verschiedene Aktionen für Qualitätsprüfungsaufträge durchführen, um den Status zu verwalten, Dokumente zu generieren und zusätzliche Details anzufragen.

### <a name="reopen-a-quality-order"></a>Wiederöffnen eines Qualitätsprüfungsauftrags

Standardmäßig können Sie einen Qualitätsprüfungsauftrag nicht mehr bearbeiten oder aktualisieren, nachdem er validiert wurde und die Tests bestanden wurden. In einigen Fällen kann es jedoch vorkommen, dass Sie einen Qualitätsprüfungsauftrag erneut öffnen müssen, nachdem er abgeschlossen wurde.

Um einen Qualitätsprüfungsauftrag wieder zu öffnen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Öffnen Sie den validierten Qualitätsprüfungsauftrag, oder wählen Sie ihn im Raster aus.
1. Wählen Sie im Aktionsbereich **Qualitätsprüfungsauftrag wieder öffnen**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Ein Zertifikat für einen Qualitätsprüfungsauftrag erstellen

Ein CoA ist ein Bericht, der vom Qualitätssicherungs-Team einer Organisation erstellt wird. Es prüft, ob ein Produkt bestimmte Vorschriften oder Anforderungen erfüllt. Ihre Debitoren oder behördliche Einrichtungen an Ihrem geopolitischen Lagerplatz benötigen möglicherweise CoAs. Sie können auch abhängig von Ihrer Branche und der Art der Produkte, die Sie handhaben, kaufen, produzieren oder verkaufen, erforderlich sein.

Mit Supply Chain Management können Sie einen CoA aus einem Qualitätsprüfungsauftrag erzeugen. Der Bericht enthält die Ergebnisse aller Tests des Qualitätsprüfungsauftrags, bei denen die Option **Analysebericht** auf *Ja* festgelegt ist. Diese Option kann standardmäßig festgelegt werden, basierend auf dem Test, den Sie auf der Seite **Tests** definieren. Sie können jedoch die Einstellung für bestimmte Tests für einen bestimmten Qualitätsprüfungsauftrag außer Kraft setzen.

Um einen CoA für einen Qualitätsprüfungsauftrag zu generieren, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie den Qualitätsprüfungsauftrag, für den Sie einen CoA erstellen wollen.
1. Wählen Sie im Aktivitätsbereich **Abfragen \> Zertifikat der Analyse**.
1. Wählen Sie auf der Seite **Zertifikat der Analyse** im Aktivitätsbereich **Neu**.
1. Optional: Wählen Sie im Feld **Kontakt** den Ansprechpartner, an den das Zertifikat gerichtet werden soll.
1. Wählen Sie im Aktivitätsbereich **Drucken**.
1. Legen Sie im Dialogfeld **Analysezertifikat** fest, wie der Bericht gedruckt werden soll. Wählen Sie dann **OK**, um den Bericht auf einem Drucker, auf dem Bildschirm, in einer Datei oder per E-Mail zu drucken.
1. Schließen Sie die Seiten.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Bestand für einen Qualitätsprüfungsauftrag sperren oder entsperren

Wenn ein Qualitätsprüfungsauftrag automatisch aus einer Qualitätsvereinigung generiert wird, kann die Artikelmusteraufnahme, die der Qualitätsvereinigung zugeordnet ist, so konfiguriert werden, dass die volle Bestandsmenge der zu prüfenden Referenz gesperrt wird. Weitere Informationen über Artikelmusteraufnahmen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahmen](quality-item-sampling.md).

Wenn Sie keine vollständige Sperrung verwenden oder wenn Sie einen Qualitätsprüfungsauftrag manuell erstellen, erstellt das System automatisch einen Datensatz zur Bestandssperrung für die Menge des Elements, das auf dem Qualitätsprüfungsauftrag geprüft werden soll. In dem Datensatz, der auf der Seite **Bestandssperrung** erstellt wird, ist das Feld **Bestandssperrungstyp** auf *Qualitätsprüfungsauftrag* festgelegt.

Um die Bestandssperrung für einen Qualitätsprüfungsauftrag anzuzeigen und zu bearbeiten, der auf der Seite **Bestandssperrung** ausgewählt ist, wählen Sie im Aktivitätsbereich **Abfragen \> Bestandssperrung**. Weitere Informationen finden Sie unter [Bestandssperrung](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Abfrage der Details eines Qualitätsprüfungsauftrags

Verwenden Sie die folgenden Schaltflächen im Aktivitätsbereich der Seite **Qualitätsprüfungsaufträge**, um weitere Informationen über einen Qualitätsprüfungsauftrag anzuzeigen oder sich auf diesen zu beziehen:

- **Abfragen \> Arbeitsdetails** – Öffnet eine Seite, auf der Sie Lagerortarbeiten ansehen können, die mit dem Qualitätsprüfungsauftrag zusammenhängen.
- **Abfragen \> Qualitätsmängel** – Öffnet eine Seite, auf der Sie alle Qualitätsmängel anzeigen können, die mit dem Qualitätsprüfungsauftrag zusammenhängen.
- **Bestand** – Die Befehle in diesem Menü sind für alle Transaktionen im Bestand allgemein. Sie können sie verwenden, um Details wie Transaktionen, Lagerbestände, Reservierungen und Markierungen anzuzeigen oder zu aktualisieren.

### <a name="create-cases-related-to-quality-orders"></a>Erzeugen von Vorgängen zu Qualitätsprüfungsaufträgen

Sie können Fälle erstellen, die sich auf Qualitätsprüfungsaufträge beziehen. Auf diese Weise können Sie Details zu Problemen verfolgen und auf eine Lösung hinarbeiten. Sie können dann die Workflow-Funktionen der Fallverwaltung verwenden, um einen Fall durch einen vordefinierten Geschäftsprozess zu leiten, um zusätzliche Genehmigungen zu erhalten oder mehr Informationen über ein bestimmtes Problem zu bekommen. Sie können auch die Funktion „Wissensartikel“ verwenden, um eine Wissensbasis mit Lösungen für allgemeine Probleme zu erstellen.

## <a name="case-management-examples-for-quality-management"></a>Beispiele für Case Management im Qualitätsmanagement

### <a name="example-1"></a>Beispiel 1

Sie arbeiten für eine produzierende Firma, die strenge Vorschriften befolgen muss, die mit der Produktion von regulierten Produkten wie z. B. Lebensmitteln zusammenhängen. Qualitätsprüfungsaufträge werden verwendet, um Details über die Qualität von Elementen während des gesamten Produktionsprozesses zu erfassen und zu verfolgen. Wenn ein Qualitätsprüfungsauftrag bestimmte Tests nicht besteht, liegt möglicherweise ein Problem mit dem Gerät vor. Fälle werden verwendet, um einem Geschäftsprozess zu folgen und das Problem an die richtigen technischen Mitarbeiter zu eskalieren, damit die Grundursache ermittelt werden kann. Um Geschäftsprozesse leichter nachvollziehbar zu machen, führt die Firma eine Wissensdatenbank mit allgemeinen Problemen, die mit Qualitätsprüfungsaufträgen und Geräteproblemen zusammenhängen.

### <a name="example-2"></a>Beispiel 2

Sie arbeiten für eine Firma, die Produkte ausliefert, die für verschiedene Länder und Regionen angepasst werden können. Einige Debitoren haben strenge Vorgaben, die befolgt werden müssen. Andernfalls können Gebühren und Rücksendungen oder Rückbuchungen anfallen. Sie verwenden Qualitätsprüfungsaufträge, um die Details zu jedem Test und die Ergebnisse zu verfolgen, die den Anforderungen des Debitors entsprechen. Fälle werden verwendet, um die Details für das CoA zu überprüfen und zu genehmigen, bevor das Dokument erstellt und zusammen mit anderen Versandpapieren angehängt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagementprozesse](quality-management-processes.md)
- [Qualitätstest](quality-tests.md)
- [Qualitätsmanagement-Testgruppen](quality-test-groups.md)
- [Qualitätszuordnungen](quality-associations.md)
- [Qualitätsmanagementprozesse](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
