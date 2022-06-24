---
title: Änderungsmanagement für vorhandene Produkte aktivieren
description: Dieser Artikel erklärt, wie Sie die Änderungsverwaltung für bestehende Produkte aktivieren können. Es beschreibt auch Fälle, in denen Ihre Möglichkeiten zur Aktivierung der Änderungsverwaltung eingeschränkt sind.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9f99529abebdf5490f158c6f0a7be4519449e9f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893467"
---
# <a name="enable-change-management-on-existing-products"></a>Änderungsmanagement für vorhandene Produkte aktivieren

[!include [banner](../../includes/banner.md)]

Dieser Artikel erklärt, wie Sie die Änderungsverwaltung für bestehende Produkte aktivieren können. Es beschreibt auch Fälle, in denen Ihre Möglichkeiten zur Aktivierung der Änderungsverwaltung eingeschränkt sind.

Wenn Sie die Änderungsverwaltung für ein bestehendes Produkt aktivieren, können Sie Versionen dieses Produkts erstellen und Änderungen, die daran vorgenommen werden, während seiner gesamten Lebensdauer verfolgen. Daher können Sie diese Änderungen mit Hilfe von Änderungsaufträgen nachverfolgen. Um die Änderungsverwaltung zu aktivieren, müssen Sie die entsprechenden Produkte in *technische Artikel* (auch als technische Produkte bezeichnet) umwandeln. Technische Produkte sind Produkte, die versioniert sind und über die Änderungsverwaltung verwaltet werden. Ein Assistent führt Sie durch den Konvertierungsprozess.

## <a name="turn-this-feature-on-or-off"></a>Schalten Sie diese Funktion ein oder aus

Für die in diesem Artikel beschriebene Funktionalität müssen die Funktionen *Verwaltung für technische Änderung* und *Änderungsmanagement für vorhandene Produkte aktivieren* für Ihr System eingeschaltet sein. Einzelheiten zum Ein- und Ausschalten dieser Funktionen finden Sie unter [Verwaltung für technische Änderung – Übersicht](product-engineering-overview.md).

## <a name="restrictions-and-limitations"></a>Beschränkungen und Einschränkungen

Nicht alle Produkttypen können in alle anderen Typen umgewandelt werden. Es gelten die folgenden Einschränkungen und Begrenzungen:

- Wenn Sie ein Produkt in ein technisches Produkt umwandeln, bleibt es ein *Produkt*. Es wird nicht zu einem *Produktstamm*.
- Wenn Sie einen Produktstamm konvertieren, der eine bestimmte festgelegte Anzahl von Dimensionen hat, werden diese Dimensionen nach der Änderung beibehalten. Wenn Sie z. B. einen Produktstamm konvertieren, der die Dimension „Größe“ hat, wird die Dimension „Größe“ beibehalten.

Wenn Sie also ein eindeutiges Produkt haben, können Sie es nur in ein technisches Produkt umwandeln, das die Produktdimension in Transaktionen nicht verfolgt (d.h. die Versionsverwaltung wird nicht verwendet). In den übrigen Abschnitten dieses Artikels finden Sie weitere Informationen zu diesen Themen.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Bereiten Sie die Konvertierung vor, indem Sie alle erforderlichen Kategorien für technische Produkte erstellen

Jedem technischen Produkt muss eine *Technische Produktkategorie* zugewiesen werden. Diese Zuordnung nehmen Sie vor, wenn Sie den **Assistenten zur Konvertierung in technische Produkte** ausführen. Technische Produktkategorien müssen für alle relevanten Standardprodukte vorhanden sein, *bevor* Sie diese Produkte konvertieren können.

Die technische Produktkategorie bietet eine Grundlage für das Erstellen eines technischen Produkts und legt eine Reihe von Standardwerten und Richtlinien fest. Technische Attribute und ihre Standardwerte (wie für die technische Kategorie definiert) werden auch auf das resultierende technische Produkt angewendet. Sie können die Attributwerte bearbeiten und/oder dem resultierenden Produkt nach Bedarf weitere technische Attribute hinzufügen.

Die technische Produktkategorie muss mit dem Produkt übereinstimmen, dem Sie sie zuweisen. Zum Beispiel müssen der Produkttyp und die Dimensionsgruppe sowohl mit dem Produkt als auch mit seiner technischen Produktkategorie übereinstimmen. Weitere Informationen finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).

> [!IMPORTANT]
> Der **Assistent zur Konvertierung in technisches Produkt** kann nur Produkte in technische Produkte konvertieren, bei denen die Version nicht in Transaktionen verfolgt wird. Daher muss die Option **Version in Transaktionen verfolgen** für technische Produktkategorien, die Sie zum Konvertieren bestehender Produkte erstellen, auf *Nein* festgelegt werden.

Wie Sie technische Produktkategorien erstellen, erfahren Sie unter [Versionsverwaltung und technische Produktkategorien](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Führen Sie den Assistenten zur Konvertierung in technische Produkte aus

Der **Assistent zur Konvertierung in technisches Produkt** hilft Ihnen, ein oder mehrere vorhandene Produkte in technische Produkte zu konvertieren. Er konvertiert die Produkte in technische Produkte (Produkte mit Versionsangabe), bei denen die Version in Transaktionen nicht nachverfolgt wird (d.h. die Dimension Version wird nicht verwendet). Nach Abschluss der Konvertierung können Sie die Produkte mit der Verwaltung für technische Änderungen verwalten.

Die Konvertierung ist permanent. Daher können Sie sie später nicht mehr rückgängig machen. 

Jedes konvertierte technische Produkt wird weiterhin in denselben Firmen freigegeben, in denen auch das ursprüngliche Produkt freigegeben wurde. Die technischen Stücklisten und Routen werden jedoch nicht automatisch für diese Firmen freigegeben.

Führen Sie die folgenden Schritte aus, um den Assistenten **In technisches Produkt konvertieren** auszuführen und ein Produkt in ein technisches Produkt zu konvertieren.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Aktivieren Sie im Raster das Kontrollkästchen für jedes Produkt, das Sie konvertieren möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Technisch** in der Gruppe **Verwaltung für technische Änderungen** die Option **In technisches Produkt konvertieren**, um den Assistenten zu öffnen.
1. Die erste Seite des Assistenten ist die Seite **Willkommen**. Wenn Sie mit dem Konvertierungsprozess noch nicht vertraut sind, lesen Sie die Informationen auf dieser Seite sorgfältig durch. Wenn Sie bereit sind, fortzufahren, wählen Sie **Weiter**.
1. Die Seite **Details für die zu konvertierenden Produkte auswählen** zeigt jedes Produkt an, das Sie vor dem Öffnen des Assistenten ausgewählt haben. Prüfen Sie die Liste. Verwenden Sie die Schaltflächen **Neu** und **Löschen** in der Symbolleiste, um Produkte nach Bedarf hinzuzufügen oder zu entfernen.
1. Verwenden Sie die folgenden Felder am oberen Rand des Rasters, um jedem aufgelisteten Produkt Standardwerte zuzuweisen. (Sie können diese Werte für einzelne Produkte ändern, nachdem die Konvertierung abgeschlossen ist). Den Produkten, denen bereits ein entsprechender Wert zugewiesen wurde, werden keine Standardwerte zugewiesen.

    - **Standardkategorie für technische Produkte** - Wählen Sie eine anfängliche Kategorie für technische Produkte, die jedem aufgelisteten Produkt zugewiesen wird. Die von Ihnen gewählte Kategorie wird nur auf Produkte angewendet, die mit ihr kompatibel sind.
    - **Standardversion** - Geben Sie die anfängliche Produktversion ein, die jedem aufgelisteten Produkt zugewiesen werden soll. Jedes technische Produkt hat mindestens eine technische Version.
    - **Standard-Llebenszyklusstatus** - Wählen Sie den anfänglichen Llebenszyklusstatus des Produkts, der jedem aufgelisteten Produkt zugewiesen werden soll.
    - **Aktuelle Stückliste wird Teil des technischen Produkts** - Aktivieren Sie dieses Kontrollkästchen, wenn die aktuelle Stückliste für jedes aufgelistete Produkt als Stückliste für das technische Produkt verwendet werden soll.

    Weitere Informationen zu den Produkteinstellungen finden Sie im nächsten Schritt.

1. Überprüfen Sie jedes Produkt, das im Raster aufgelistet ist, und bewerten Sie, inwieweit die von Ihnen zugewiesenen Standardwerte auf das Produkt zutreffen. Überprüfen Sie für jede Zeile die folgenden Informationen und legen Sie alle relevanten Felder fest:

    - **Produktnummer** - Die Produktnummer.
    - **Produktname** - Der Name des Produkts.
    - **Technische Kategorie** - Wählen Sie die Kategorie des technischen Produkts, zu der das Produkt nach der Umwandlung gehören soll. Für jedes Produkt muss bereits eine passende Kategorie vorhanden sein, wie im vorigen Abschnitt dieses Artikels erklärt wurde. Sie müssen jedem Produkt eine Kategorie zuweisen.
    - **Version** - Geben Sie die Produktversion ein, die dem Produkt nach der Konvertierung zugewiesen werden soll. Sie können zum Beispiel eine Nummer wählen, die in die Sequenz passt, die Ihre Kategorie bereits verwendet. Jede Engineering-Version speichert die Engineering-relevanten Daten, die spezifisch für diese Version sind. Weitere Informationen finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).
    - **Produktlebenszyklusstatus** - Wählen Sie den Llebenszyklusstatus, in dem sich das Produkt nach der Konvertierung befinden soll. Mit dem Llebenszyklusstatus des Produkts können Sie steuern, welche Transaktionen für eine bestimmte technische Version erlaubt sind. Weitere Informationen finden Sie unter [Produktlebenszyklusstatus und Transaktionen](product-lifecycle-state-transactions.md).
    - **Hat Stückliste** - Ein aktiviertes Kontrollkästchen zeigt an, dass das Produkt eine Stückliste hat. Die Einstellung dieses Kontrollkästchens kann Ihnen helfen zu entscheiden, wie Sie das Kontrollkästchen **Aktuelle Stückliste wird Teil des technischen Produkts** festlegen.
    - **Aktuelle Stückliste wird Teil des technischen Produkts** - Aktivieren Sie dieses Kontrollkästchen, wenn die aktuelle Stückliste des Produkts als Stückliste für das technische Produkt verwendet werden soll. Diese Stückliste wird dann von der Verwaltung für technische Änderungen verwaltet. Wenn das Produkt keine Stückliste hat, oder wenn Sie es vorziehen, später manuell eine Stückliste für das konvertierte Produkt zu erstellen, deaktivieren Sie dieses Kontrollkästchen.
    - **Hat Fehler** - Ein markiertes Kontrollkästchen zeigt an, dass das Einrichten des Produkts einen oder mehrere Fehler hat. Zum Beispiel könnte der Produkttyp oder die Dimensionsgruppe in der Kategorie nicht übereinstimmen. Produkte, die Fehler aufweisen, werden übersprungen und nicht konvertiert.

1. Wenn Sie fertig sind, wählen Sie **Validieren** in der Symbolleiste, um das Produkt-Setup zu validieren. Für jede Zeile wird das Kontrollkästchen **Hat Fehler** aktualisiert, um den Status des Produkts anzuzeigen. Passen Sie die Werte an, bis das Einrichten eines jeden Produkts fehlerfrei ist.
1. Wenn alle Produkte korrekt festgelegt sind, wählen Sie **Weiter**, um fortzufahren.
1. Die Seite **Auswahl bestätigen** zeigt die Anzahl der Produkte an, die keine Fehler in ihrer Einrichtung haben und daher bereit für die Konvertierung sind. Sie zeigt auch die Anzahl der Produkte an, die aufgrund von Fehlern übersprungen werden. Um die Konvertierung als Batch-Job auszuführen, legen Sie die Option **Ausführen im Batch** auf *Ja* fest.
1. Wählen Sie **Fertigstellen**, um Ihre Einstellungen zu übernehmen und die Konvertierung der Produkte in technische Produkte zu starten.

> [!NOTE]
> Wenn Ihr System so festgelegt ist, dass Produkte vor der Freigabe manuell angenommen werden, müssen Sie jedes konvertierte Produkt über die Seite **Produktfreigaben öffnen** in den entsprechenden Firmen annehmen. Weitere Informationen finden Sie unter [Prüfen und akzeptieren Sie das Produkt, bevor Sie es in der lokalen Firma freigeben](engineering-scenarios.md#accept).
