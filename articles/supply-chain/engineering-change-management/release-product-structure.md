---
title: Produktstrukturen freigeben
description: In diesem Thema wird erklärt, wie Sie zusätzlich zur Freigabe von Produkten zusammen mit ihren Engineering-Versionen auch komplette Produktstrukturen freigeben können. Auf diese Weise können Sie sicherstellen, dass ingenieurrelevante Produktdaten in verschiedenen juristischen Entitäten einfach wiederverwendet werden können.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 971ff16b862a48581365523edc6b64052b29c380
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967230"
---
# <a name="release-product-structures"></a>Produktstrukturen freigeben

[!include [banner](../includes/banner.md)]

Um sicherzustellen, dass ingenieurrelevante Produktdaten in verschiedenen juristischen Entitäten einfach wiederverwendet werden können, können Sie zusätzlich zur Freigabe von Produkten zusammen mit ihren Engineering-Versionen auch komplette Produktstrukturen freigeben. Daher können Sie mehrstufige Stücklistenstrukturen zusammen mit der übergeordneten Stückliste in einer einzigen Freigabeaktion freigeben. In diesem Fall werden auch die Stückliste und die untergeordneten Produkte freigegeben.

Technische Produkte werden von ihrer Entwicklungsfirma so erstellt und gewartet, dass sie die Qualitätsanforderungen so erfüllen, wie sie entworfen wurden. Jedes operative Unternehmen, das ein Produkt herstellt, benötigt dasselbe Produkt und dieselbe zugrunde liegende Stückliste. Je nach Produktionsbetrieb wird der Arbeitsplan möglicherweise lokal erstellt. In diesem Fall geben Sie den Arbeitsplan nicht zusammen mit dem Produkt frei. Für juristische Entitäten, die die Produkte verkaufen, aber nicht herstellen, ist die Stückliste möglicherweise nicht erforderlich.

Um den Prozess effizienter zu gestalten, können alle Engineering-relevanten Daten gleichzeitig für andere operative Unternehmen freigegeben werden. Zu diesen Daten gehört auch die Produktstruktur. Während des Freigabeprozesses können Sie wählen, welcher Teil der Produktdaten freigegeben werden soll.

Weitere Informationen über Engineering-Firmen und operative Firmen finden Sie unter [Engineering-Firmen und Dateneigentumsregeln](engineering-org-data-ownership-rules.md).

Beachten Sie, dass Sie sowohl Standardprodukte als auch Engineering-Produkte zusammen mit der Freigabe der Produktstruktur freigeben können. Bei diesem Vorgang wird die gesamte Produktstruktur freigegeben, auch die Stückliste und der Arbeitsplan der Firma, in der die Produkte freigegeben werden.

Ein Beispiel für die Freigabe eines Produkts finden Sie unter [Freigeben eines Engineering-Produkts an eine lokale Firma](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Freigegebene Daten für ein Produkt, wenn die Freigabeproduktstruktur verwendet wird

Die folgenden Daten sind in der Freigabe von Engineering-Produkten enthalten:

- **Produktdaten** - Ein neues freigegebenes Produkt wird erstellt.
- **Engineering-Versionsdaten** - Die Engineering-Version und ihre Daten werden erstellt oder aktualisiert. Beachten Sie, dass die Engineering-Daten überschrieben werden, wenn Sie dieselbe Engineering-Version erneut für eine operative Firma freigeben.
- **Engineering-Attribute** - Die Engineering-Attribute und deren Werte werden erstellt oder aktualisiert.
- **Engineering-Stückliste** - Die Engineering-Stückliste und ihre Zeilen können erstellt oder aktualisiert werden. Weitere Informationen zum Datenbesitz finden Sie unter [Produktbesitzer](product-owner.md).
- **Engineering-Arbeitspläne** - Die Engineering-Arbeitspläne und ihre Vorgänge können erstellt oder aktualisiert werden. Weitere Informationen zum Datenbesitz finden Sie unter [Produktbesitzer](product-owner.md).
- **Engineering-Dokumente** - Die Engineering-Dokumente, die mit der Engineering-Version verbunden sind, werden erstellt oder aktualisiert.

Wenn Sie die Verwaltung für technische Änderung auf Ihrem System einschalten, ist die Struktur der Freigabeprodukte verfügbar. Darüber hinaus werden bei der Freigabe von Standardprodukten deren Stücklisten und Arbeitspläne eingefügt.

## <a name="product-acceptance"></a>Produktakzeptanz

**Produktannahme** ist ein wichtiger Parameter, der den Freigabeprozess beeinflusst. Sie können diesen Parameter für jede Firma festlegen, indem Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderungsparameter** gehen. Weitere Informationen finden Sie unter [Parameter für die Verwaltung für technische Änderung](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatische Produktabnahme

Jede Freigabe von Engineering-Produkten beginnt, wenn jemand aus dem Engineering-Unternehmen ein Produkt zur Freigabe auswählt. Wenn der Parameter **Produktannahme** auf *Automatisch* festgelegt ist, entscheidet der Benutzer in der Engineering-Firma, welche Produktdaten automatisch an die operativen Gesellschaften freigegeben werden sollen. Das Produkt wird dann automatisch für die Firmen freigegeben, die im Freigabe-Assistenten ausgewählt sind.

### <a name="manual-product-acceptance"></a>Manuelle Produktannahme

Jede Freigabe von Engineering-Produkten beginnt, wenn jemand aus dem Engineering-Unternehmen ein Produkt zur Freigabe auswählt. Wenn der Parameter **Produktannahme** auf *Manuell* festgelegt ist, entscheidet der Benutzer in der Engineering-Firma, welche Produktdaten an die Betriebsfirmen freigegeben werden sollen. Ein Benutzer aus jeder Betriebsfirma prüft dann die Produktdaten und entscheidet, ob er die Freigabe akzeptiert. Der Benutzer in der Betriebsfirma kann beim Empfang der Daten die folgenden Optionen festlegen:

- Wenn die Produkte (Updates) für die Betriebsfirma nicht relevant sind, kann der Benutzer entscheiden, die Freigabe nicht zu akzeptieren.
- Der Benutzer kann die Elementvorlage für neue Produkte ändern.
- Der Benutzer kann wählen, ob die Produkte zusammen mit ihren Stücklisten und/oder Arbeitsplänen freigegeben werden sollen, und ob sie als genehmigt und aktiv freigegeben werden sollen.
- Der Benutzer kann die Gültig-ab-Daten der Produkte ändern.

Ein Beispiel für die Annahme eines Produkts finden Sie unter [Prüfen und akzeptieren Sie das Produkt, bevor Sie es in der lokalen Firma freigeben](engineering-scenarios.md#accept).

> [!NOTE]
> Für Standardprodukte können Sie von jeder juristischen Entität an jede andere juristische Entität freigeben. Bei Engineering-Produkten ist die einzige juristische Entität, von der Sie freigeben können, die Engineering-Firma.

## <a name="release-policies"></a>Richtlinien für die Freigabe

Nicht alle Betriebsfirmen benötigen die gleichen Produktdaten. Im Allgemeinen benötigen Betriebsfirmen, die Engineering-Produkte herstellen, eine Stückliste, während Betriebsfirmen, die nur Engineering-Produkte verkaufen, keine Stückliste benötigen. Mit Freigabe-Richtlinien können Sie die Parameter festlegen, die für die Freigabe von Produkten verwendet werden.

Für technische Produkte wird die Richtlinie in der Kategorie für technische Produkte zugewiesen, und das Feld ist obligatorisch. Für Standardprodukte wird die Richtlinie dem gemeinsamen Produkt zugewiesen, und das Feld ist optional.

Weitere Informationen über Engineering-Produktkategorien finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).

Während des Freigabeprozesses können Sie die Einstellungen beeinflussen.

## <a name="create-and-manage-product-release-policies"></a>Richtlinien zur Produktfreigabe erstellen und verwalten

Um mit Produktfreigabe-Richtlinien zu arbeiten, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Produktfreigabe-Richtlinien**. Führen Sie dann einen der folgenden Schritte aus.

- Um eine neue Richtlinie zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder fest, wie in den folgenden Unterabschnitten beschrieben.
- Um eine bestehende Richtlinie zu bearbeiten, wählen Sie sie im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder wie in den folgenden Unterabschnitten beschrieben fest.
- Um eine bestehende Richtlinie zu löschen, markieren Sie sie im Listenbereich, wählen Sie **Bearbeiten** im Aktivitätsbereich und stellen Sie dann auf der Registerkarte **Allgemein** sicher, dass die Option **Aktiv** auf *Nein* festgelegt ist. Wählen Sie dann **Löschen** im Aktivitätsbereich.

### <a name="header"></a>Übergeordnet

Legen Sie die folgenden Felder in der Kopfzeile einer Produktfreigabe-Richtlinie fest.

| Feld | Beschreibung |
|---|---|
| Name | Geben Sie einen Namen für die Richtlinie ein. |
| Beschreibung | Geben Sie eine Beschreibung für die Richtlinie ein. |

### <a name="general-fasttab"></a>Allgemeines Inforegister

Legen Sie die folgenden Felder auf der Inforegisterkarte **Allgemein** einer Richtlinie fest.

| Feld | Beschreibung |
|---|---|
| Produkttyp | Wählen Sie, ob die Richtlinie für Produkte vom Typ *Element* oder *Service* gilt. Sie können diese Einstellung nicht mehr ändern, nachdem Sie den Datensatz gespeichert haben. |
| Vorlagen anwenden | Wählen Sie eine der folgenden Optionen, um festzulegen, ob und wie Produktfreigabevorlagen angewendet werden sollen, wenn die Richtlinie verwendet wird:<ul><li>**Immer** - Eine Produktfreigabevorlage muss immer für Freigaben verwendet werden. Wenn Sie diese Option wählen, verwenden Sie das Inforegister **Alle Produkte**, um die Vorlage anzugeben, die für jede Firma verwendet wird, für die Sie eine Freigabe erteilen. Wenn Sie nicht für jede Firma, die auf dem Inforegister **Alle Produkte** aufgeführt ist, eine Vorlage angeben, erhalten Sie einen Fehler, wenn Sie versuchen, die Richtlinie zu speichern.</li><li>**Optional** - Wenn für eine Firma, die auf der Registerkarte **Alle Produkte** Inforegister aufgeführt ist, eine Vorlage für freigegebene Produkte angegeben ist, wird diese Vorlage verwendet, wenn Sie für diese Firma freigeben. Andernfalls wird keine Vorlage verwendet. Wenn Sie diese Option wählen, können Sie die Richtlinie speichern, ohne allen Firmen Vorlagen zuzuweisen. (Es wird keine Warnung angezeigt.)</li><li>**Niemals** - Es wird keine Vorlage verwendet, wenn Sie ein Produkt für eine Firma freigeben, auch wenn eine Vorlage für Firmen angegeben ist, die auf **Alle Produkte** Inforegister aufgeführt sind. Die Vorlagenspalten werden nicht verfügbar sein.</li></ul> |
| Aktiv | Verwenden Sie diese Option, um die Einhaltung Ihrer Richtlinien für die Freigabe zu erleichtern. Legen Sie sie für alle von Ihnen verwendeten Richtlinien auf *Ja* fest. Legen Sie sie auf *Nein* fest, um eine Freigabe-Richtlinie als inaktiv zu markieren, wenn sie nicht verwendet wird. Beachten Sie, dass Sie eine Richtlinie, die einer technischen Produktkategorie zugewiesen ist, nicht inaktivieren können, und dass Sie nur inaktive Richtlinien löschen können. |

### <a name="all-products-fasttab"></a>Inforegister Alle Produkte

Fügen Sie auf dem Inforegister **Alle Produkte** eine Zeile für jede Betriebsfirma hinzu, für die Sie diese Richtlinie zur Freigabe verwenden wollen. Verwenden Sie die Schaltflächen auf der Inforegisterkarte **Alle Produkte**, um Zeilen nach Bedarf hinzuzufügen oder zu entfernen. Legen Sie für jede Zeile, die Sie hinzufügen, die folgenden Felder fest.

> [!NOTE]
> Die Einstellungen auf der Inforegisterkarte **Alle Produkte** gelten sowohl für technische Produkte als auch für Standardprodukte.

| Feld | Beschreibung |
|---|---|
| Unternehmenskontokennung | Wählen Sie die Firma, für die die Zeile gilt. Die Parameter in der Zeile gelten, wenn Produkte für diese Firma freigegeben werden. |
| Von Vorlage freigegebenes Produkt | Fügen Sie eine Vorlage für das Produkt hinzu. |
| Stücklistengenehmigung kopieren | Aktivieren Sie dieses Kontrollkästchen, um den Freigabestatus der Stückliste in die empfangende Firma zu kopieren. |
| Stücklistenaktivierung kopieren | Aktivieren Sie dieses Kontrollkästchen, um den Aktivierungsstatus der Stückliste in die empfangende Firma zu kopieren. |
| Arbeitsplangenehmigung kopieren | Aktivieren Sie dieses Kontrollkästchen, um den Arbeitsplan-Freigabestatus zur empfangenden Firma zu kopieren.|
| Arbeitsplanaktivierung kopieren | Aktivieren Sie dieses Kontrollkästchen, um den Aktivierungsstatus des Arbeitsplans in die empfangende Firma zu kopieren. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Optionsparameter für Engineering-Produkte Inforegister

Jedes Mal, wenn Sie auf der Inforegisterkarte **Alle Produkte** eine Zeile hinzufügen, wird auch auf der Inforegisterkarte **Optionsparameter für Engineering-Firmen** eine Zeile erstellt, die einen passenden **Firmenkonten-ID**-Wert hat. Wenn Sie dann eine Zeile aus dem Inforegister **Alle Produkte** entfernen, wird die Zeile, die einen passenden **Firmenkonten-ID**-Wert hat, auch aus dem Inforegister **Optionsparameter für Engineering-Produkte** entfernt.

Legen Sie für jede Zeile, die auf dem Inforegister **Optionsparameter für technische Produkte** angezeigt wird, die folgenden Felder fest.

> [!NOTE]
> Die Einstellungen auf der Registerkarte **Optionsparameter für technische Produkte** gelten nur für technische Produkte.

| Feld | Beschreibung |
|---|---|
| Vorlagenstückliste | Wenn ein Produkt, das eine Stückliste hat, freigegeben wird, werden die Zeilen der angegebenen Vorlage Stückliste hinzugefügt. Dieses Feld ist nützlich, um lokale Komponenten hinzuzufügen, z. B. Verpackungen oder Anleitungen in der Landessprache. |
| Vorlagenarbeitsplan | Wenn ein Produkt, das einen Arbeitsplan hat, freigegeben wird, werden die Zeilen der angegebenen Vorlage hinzugefügt. |
| Gültigkeit kopieren | Wählen Sie aus, ob bei der Freigabe von Produkten Gültigkeitsdaten von der Engineering-Firma zur Betriebsfirma kopiert werden sollen. |
| Automatisch dem Freigabevorschlag hinzufügen | Aktivieren Sie dieses Kontrollkästchen für Produkte, die automatisch auf dem Änderungsauftrag für das Engineering freigegeben werden sollen. Auf diese Weise können Produkte, die zu Engineering-Produktkategorien gehören, die diese Richtlinie zur Freigabe verwenden, automatisch für Betriebsfirmen freigegeben werden, bei denen diese Option festgelegt ist. (Weitere Informationen finden Sie unter [Verwalten von Änderungen an Verwaltung für technische Änderung](engineering-change-management.md)).

### <a name="review-each-product-when-you-release-it"></a>Überprüfen Sie jedes Produkt, wenn Sie es freigeben

Wenn Engineering-Produkte, die Stücklisten oder Arbeitspläne haben, freigegeben werden, werden die Parameter auf Standardwerte festgelegt, wie in der Richtlinie zur Freigabe angegeben. Als Benutzer können Sie dieses Verhalten auf der freigebenden Seite beeinflussen, wenn Sie die Produktstruktur freigeben verwenden.

Um Engineering-Produkte freizugeben, wählen Sie auf der Seite **Freigegebene Produkte** die freizugebenden Produkte aus und wählen dann **Produktstruktur freigeben**, um den Freigabeassistenten zu öffnen. Auf der Seite **Wählen Sie freizugebende technische Produkte** werden die Produkte angezeigt. Wählen Sie ein einzelnes Produkt aus und wählen Sie dann **Freigabedetails**, um die Freigabedetails für das Produkt zu prüfen.

Auf der Seite **Freigabedetails** können Sie den Wert der Felder **Stückliste empfangen**, **Stückliste freigeben**, **Stückliste aktivieren**, **Stückliste empfangen**, **Arbeitsplan freigeben** und **Arbeitsplan aktivieren** ändern. Im Push-Pull-Szenario können Sie den Wert derselben Felder auf der empfangenden Seite ändern, vorausgesetzt, dass die Stückliste und der Arbeitsplan freigegeben sind.

## <a name="product-owners-and-product-releases"></a>Produktbesitzer und Produktfreigaben

Da Produktbesitzer wissen, welche juristischen Entitäten ihre Produkte benötigen, kann ein Produkt nur von den Mitgliedern der Produktbesitzergruppe dieses Produkts freigegeben werden. Andere Benutzer können keine Produkte freigeben, deren Eigentümer sie nicht sind.

Dieses Verhalten gilt nur, wenn ein Produkt direkt zur Freigabe ausgewählt wird. Produkte, die über eine Stückliste *Teil der Struktur eines anderen Produkts sind, können* von Nicht-Besitzern freigegeben werden, wenn sie das übergeordnete Produkt freigeben, vorausgesetzt, sie besitzen das übergeordnete Produkt.

Beispiel: Produkt X ist der Eigentümergruppe *Designschränke* zugewiesen. Produkt X ist auch Teil der Stückliste von Produkt Y, das der Produktbesitzer-Gruppe *Design-Lautsprecher* zugeordnet ist. Wenn ein Benutzer aus der Produktbesitzer-Gruppe *Design-Lautsprecher* das Produkt Y und dessen Stückliste freigibt, wird das Produkt X zusammen mit dem Produkt Y freigegeben.

Weitere Informationen finden Sie unter [Produktbesitzer](product-owner.md).
