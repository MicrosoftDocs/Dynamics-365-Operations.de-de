---
title: Zustände und Transaktionen im Produktlebenszyklus
description: In diesem Thema wird erläutert, wie Sie steuern können, welche Transaktionen für die einzelnen Lebenszyklusstatus zulässig sind, während ein Engineering-Produkt seinen Lebenszyklus durchläuft.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8bb3d5848b7e2c50a8fdaba1c6a1a7c0087d1390
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6016955"
---
# <a name="product-lifecycle-states-and-transactions"></a>Zustände und Transaktionen im Produktlebenszyklus

[!include [banner](../includes/banner.md)]

Da ein technisches Produkt seinen Lebenszyklus durchläuft, ist es wichtig, dass Sie steuern können, welche Transaktionen für jeden Lebenszyklus-Status erlaubt sind. Zum Beispiel sollten Produkte, die sich noch nicht in einem ausgereiften Zustand befinden, nicht in einen Auftrag eingelagert werden. Oder, wenn ein Produkt seinen End-of-Life-Status erreicht, möchten Sie vielleicht den Zufluss dieses Produkts kontrollieren.

Bei einem technischen Produkt sind Änderungen des Lebenszyklusstatus mit den technischen Versionen des Produkts verbunden. Daher kann der Lebenszyklusstatus des Produkts auch mit seinen Engineering-Versionen verbunden sein. Wenn der Lebenszyklusstatus des Produkts mit einer Engineering-Version verbunden ist, können Sie mit dem Lebenszyklusstatus steuern, welche Transaktionen für die Engineering-Version erlaubt sind.

## <a name="create-and-manage-product-lifecycle-states"></a>Erstellen und Verwalten von Produktlebenszyklusstatus

Um mit Produktlebenszyklusstatus zu arbeiten, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Produktlebenszyklusstatus**. Führen Sie dann einen der folgenden Schritte aus.

- Um einen neuen Lebenszyklusstatus zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder fest, wie in den folgenden Unterabschnitten beschrieben.
- Um einen vorhandenen Status zu bearbeiten, wählen Sie ihn im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder wie in den folgenden Unterabschnitten beschrieben fest.
- Um einen vorhandenen Status zu löschen, wählen Sie ihn im Listenbereich aus und wählen Sie dann **Löschen** im Aktivitätsbereich.

> [!NOTE]
> Technische Produkte verwenden die gleichen Produktlebenszyklusstatus wie Standardprodukte (nicht technische Produkte). Sie können die Seite **Produktlebenszyklusstatus**, die in diesem Thema beschrieben wird, auch öffnen, indem Sie zu **Produktinformationsmanagement \> Einrichten \> Produktlebenszyklusstatus** gehen. Weitere Informationen über den Status des Produktlebenszyklus, sowohl für technische Produkte als auch für Standardprodukte, finden Sie unter [Übersicht über den Status des Produktlebenszyklus](../pim/product-lifecycle.md).

### <a name="header"></a>Übergeordnet

Legen Sie die folgenden Felder in der Kopfzeile eines Produktlebenszyklusstatus fest.

| Feld | Beschreibung |
|---|---|
| Staat | Geben Sie einen Namen für den Produktlebenszyklus-Status ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Produktlebenszyklus-Status ein. |

### <a name="general-fasttab"></a>Allgemeines Inforegister

Legen Sie die folgenden Felder auf dem Inforegister **Allgemein** fest.

| Feld | Beschreibung |
|---|---|
| Standard bei Freigabe an eine juristische Entität | Für Standardprodukte legen Sie diese Option auf *Ja* fest, wenn dieser Status des Produktlebenszyklus standardmäßig auf alle Produkte angewendet werden soll, wenn sie zum ersten Mal freigegeben werden. Legen Sie sie auf *Nein* fest, wenn dieser Lebenszyklus-Status später manuell angewendet werden soll.<p>Diese Festlegung gilt nicht für Engineering-Produkte. Der Lebenszyklus-Status einer Engineering-Produktversion, nachdem sie in der Engineering-Firma erstellt wurde, wird in ihrer Engineering-Änderungskategorie angegeben. Wenn das Produkt an eine Betriebsfirma freigegeben wird, wird der Lebenszyklus-Status des Produkts kopiert. Mit anderen Worten: Wenn ein Engineering-Produkt für eine Betriebsfirma freigegeben wird, hat es denselben Lebenszyklusstatus wie in der Engineering-Firma. Der Status des Lebenszyklus kann in der Betriebsfirma überschrieben werden.</p> |
| Aktiv für die Planung | Legen Sie diese Option auf *Ja* fest, um Produkte, die sich in diesem Status befinden, in Berechnungen auf der Ebene der Produktprogrammplanung und der Stückliste einzubeziehen. Legen Sie sie auf *Nein* fest, um Produkte, die sich in diesem Status des Lebenszyklus befinden, von den Berechnungen auszuschließen. |

### <a name="enabled-business-processes-fasttab"></a>Aktivierte Geschäftsprozesse Inforegister

Verwenden Sie die Inforegister-Registerkarte **Aktivierte Geschäftsprozesse**, um zu steuern, welche der verfügbaren Geschäftsprozesse mit Produkten im aktuellen Status des Lebenszyklus verwendet werden können. Die Prozesse, die auf dieser Inforegisterkarte aufgelistet sind, werden automatisch auf folgende Weise gefunden:

- Wenn Sie zum ersten Mal einen neuen Lebenszyklusstatus speichern, lädt die Seite die Geschäftsprozesse, die derzeit verfügbar sind.
- Wenn Sie Ihrem System neue Geschäftsprozesse hinzufügen, können Sie die Liste auf der Inforegister **Aktivierte Geschäftsprozesse** für einen vorhandenen Lifecycle-Status aktualisieren, indem Sie im Aktivitätsbereich **Aktualisierung prüfen** wählen.

Die folgenden Felder sind für jeden Prozess verfügbar, der auf der Registerkarte **Aktivierte Geschäftsprozesse** aufgelistet ist.

| Feld | Beschreibung |
|---|---|
| Bearbeiten | Dieses schreibgeschützte Feld zeigt den Namen eines vorhandenen Geschäftsprozesses an. |
| Prozessbereich | Dieses Nur-Lese-Feld zeigt den Namen eines vorhandenen Prozessbereichs an. |
| Richtlinie | Wählen Sie einen der folgenden Werte, um zu steuern, ob und wie der aktuelle Prozess für Produkte zugelassen wird, die sich in diesem Lebenszyklus-Status befinden:<ul><li>**Aktiviert** - Der Geschäftsprozess ist erlaubt.</li><li>**Blockiert** - Der Prozess ist nicht erlaubt. Wenn ein Benutzer versucht, den Prozess für ein Produkt zu verwenden, das sich in diesem Status befindet, wird das System den Versuch blockieren und stattdessen einen Fehler anzeigen. So können Sie z. B. verhindern, dass Produkte mit abgelaufenem Lebenszyklus gekauft werden.</li><li>**Aktiviert mit Warnung** - Der Prozess ist erlaubt, aber es wird eine Warnung angezeigt. Sie könnten z.B. ein Prototyp-Produkt auf einen Produktionsauftrag einlagern, der von der Forschungs- und Entwicklungsabteilung erstellt wird. Andere Abteilungen sollten jedoch wissen, dass sie das Produkt noch nicht produzieren sollen.</li></ul> |

Wenn Sie weitere Regeln für den Status des Lebenszyklus als Anpassung hinzufügen, können Sie diese Regeln in der Benutzeroberfläche (UI) anzeigen, indem Sie **Prozesse aktualisieren** im oberen Fensterbereich auswählen. Die Schaltfläche **Prozesse aktualisieren** ist nur für Administratoren verfügbar.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Lebenszyklusstatus für freigegebene Produkte und Produktvarianten

Für ein Produkt mit Varianten (Produktmaster und Varianten) hat das Produkt (Produktmaster) einen Lebenszyklusstatus, und jede der Varianten kann auch einen anderen Lebenszyklusstatus haben.

Wenn für bestimmte Prozesse entweder die Variante oder das Produkt blockiert ist, wird der Prozess ebenfalls blockiert. Um festzustellen, ob ein Prozess blockiert ist, führt das System die folgenden Überprüfungen durch:

- Für technisch gesteuerte Produkte:
  - Wenn die aktuelle technische Version blockiert ist, blockieren Sie den Prozess.
  - Wenn die aktuelle Variante blockiert ist, blockieren Sie den Prozess.
  - Wenn das freigegebene Produkt blockiert ist, blockieren Sie den Prozess.
- Für Standardprodukte:
  - Wenn die aktuelle Variante blockiert ist, blockieren Sie den Prozess.
  - Wenn das freigegebene Produkt blockiert ist, blockieren Sie den Prozess.

Angenommen, Sie möchten nur eine Variante (rot) eines bestimmten Produkts (T-Shirt) verkaufen und den Verkauf aller anderen Varianten vorerst blockieren. Sie können dies mit dem folgenden Setup erreichen:

- Weisen Sie dem Produkt einen Lebenszyklusstatus zu, der den Prozess ermöglicht. Weisen Sie dem T-Shirt-Produkt beispielsweise einen Lebenszyklusstatus von *Verkäuflich* zu, sodass der Geschäftsprozess *Auftrag* möglich ist.
- Weisen Sie der verkäuflichen Variante einen Lebenszyklusstatus zu, der den Prozess ermöglicht. Weisen Sie der roten Variante beispielsweise auch einen Lebenszyklusstatus von *Verkäuflich* zu.
- Allen anderen Varianten wird ein anderer Lebenszyklusstatus zugewiesen, in dem der Prozess blockiert ist. Weisen Sie beispielsweise der weißen Variante (und allen anderen Varianten) einen Lebenszyklusstatus von *Nicht verkäuflich* zu, die den Geschäftsprozess *Auftrag* blockiert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
