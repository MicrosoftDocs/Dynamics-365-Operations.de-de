---
title: Fehlerbehebung von Produktinformationen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben können, die bei der Arbeit mit Produktinformationen auftreten können.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841526"
---
# <a name="troubleshoot-product-information"></a>Fehlersuche bei Produktinformationen

In diesem Thema wird beschrieben, wie Sie Probleme beheben können, die bei der Arbeit mit Produktinformationen auftreten können.

## <a name="i-cant-delete-a-released-product"></a>Ich kann ein freigegebenes Produkt nicht löschen.

### <a name="issue-description"></a>Problembeschreibung

Sie können ein freigegebenes Produkt und alle seine Varianten nur löschen, wenn das freigegebene Produkt keine zugehörigen Transaktionen hat.

### <a name="issue-resolution"></a>Problemlösung

Gehen Sie folgendermaßen vor, um ein freigegebenes Produkt oder einen Produktstamm zu löschen.

1. Schließen Sie alle offenen Transaktionen für die Elemente.
1. Reduzieren Sie den Bestand auf 0 (Null).
1. Führen Sie den Bestandsabschluss durch.
1. Löschen Sie alle Produktvarianten für den Produktstamm, den Sie löschen möchten.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Kann ich die Artikelnummer eines freigegebenen Produkts ändern?

In den meisten Fällen können Sie die Artikelnummern für freigegebene Produkte nicht bearbeiten, da diese Änderung zu einer Verfälschung der Daten führen würde. Sie können die Artikelnummer nur dann bearbeiten, wenn Sie eine Datenbeschädigung reparieren müssen, die durch eine frühere Umbenennung des Primärschlüssels dieses freigegebenen Produkts verursacht wurde, wie in der Liste der [entfernten oder außer Betrieb genommenen Funktionen für Finance and Operations 10.0.0 mit Plattform-Update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) erwähnt.

Wenn Sie die Möglichkeit haben möchten, Artikelnummern für freigegebene Produkte zu bearbeiten, [stimmen Sie im Ideen-Portal für diese Idee ab](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Das voreingestellte Bezugsprinzip vom Produkt wird nicht in der Stücklistenzeile eingetragen.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie ein Element zu einer Stücklistenzeile hinzufügen, verwendet das System nicht die Standardinformationen zum Bezugsprinzip, die für das Element festgelegt wurden. Mit anderen Worten: Das Bezugsprinzip des Elements wird nicht auf der Seite **Stückliste** angezeigt.

### <a name="issue-resolution"></a>Problemlösung

Wenn Sie ein Bezugsprinzip in einer Stücklistenzeile angeben, gilt es für diese Stückliste. Wenn das Bündelungsprinzip jedoch leer ist oder nicht auf einer Stückliste festgelegt ist, gilt das Bündelungsprinzip, das auf dem Element festgelegt ist, trotzdem für diese Stückliste, auch wenn es nicht auf der Stückliste angezeigt wird.

Die Voreinstellungslogik für andere Funktionen in Microsoft Dynamics 365 Supply Chain Management funktioniert normalerweise nicht auf diese Weise. Das aktuelle Verhalten kann jedoch nicht geändert werden. Andernfalls könnten einige bestehende Anpassungen, die sich darauf verlassen, kaputt gehen.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Das System erlaubt das Speichern von doppelten Barcodes für verschiedene Elemente oder für dasselbe Element, das unterschiedliche Dimensionen hat.

Das System erzwingt derzeit keine eindeutigen Barcodes, und das Hinzufügen dieser Einschränkung wäre eine bahnbrechende Änderung. Tatsächlich hat Microsoft Hinweise darauf, dass einige bestehende Kundeninstallationen durch diese Änderung beschädigt werden würden. Wir werden jedoch eine breitere Designänderung in Betracht ziehen, um diese Funktion in Zukunft zu ermöglichen.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Ich erhalte die folgende Fehlermeldung, wenn ich Artikeldatensatzvorlagen bearbeite: „Der Lagerort kann nicht erstellt werden, da das Element nicht auf Lager ist. Um Artikel auf Lager zu haben, muss die Option Lagerndes Produkt in der zugehörigen Artikelmodellgruppe ausgewählt sein.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem tritt auf, wenn Sie mit den folgenden Schritten versuchen, eine Vorlage für einen Artikel zu erstellen, der nicht auf Lager ist.

1. Öffnen Sie ein freigegebenes Produkt, das nicht vorrätig ist.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Optionen** die Option **Datensatzinfo**.
1. Wählen Sie im Dialogfeld **Datensatzinformationen** die Option **Betriebskontenvorlage**.

In diesem Fall erhalten Sie die folgende Fehlermeldung:

> Der Lagerplatz kann nicht erstellt werden, da das Element nicht auf Lager ist. Um Artikel auf Lager zu haben, muss die Option Lagerndes Produkt auf der zugehörigen Artikelmodellgruppe ausgewählt sein.

### <a name="issue-resolution"></a>Problemlösung

Der Prozess des Erstellens von Produktvorlagen erfordert zusätzliche produktspezifische Logik. Daher können Sie die generische **Firmenkontenvorlage**-Schaltfläche für diesen Zweck nicht verwenden. Führen Sie stattdessen die folgenden Schritte aus.

1. Öffnen Sie ein freigegebenes Produkt.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Neu** die Option **Vorlage \> Gemeinsame Vorlage erstellen**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Standard-Hilfetext, der in Produktattributen hinzugefügt wird, wird in einem freigegebenen Produkt nicht eingetragen.

Eine Beschreibung und ein Hilfetext, die in den Produktattributen hinzugefügt werden, sind in den freigegebenen Produkten nicht sichtbar oder standardmäßig eingegeben. Dieses Verhalten ist beabsichtigt.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Die Standardmenge, die eingegeben wird, unterscheidet sich bei der Registrierung aus einer Stückliste und bei der Registrierung aus einer Stücklistenversion.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie ein Element zu einer Stückliste hinzufügen, wird die Menge standardmäßig auf 1 festgelegt und nicht auf die Menge, die im Feld **Min. Bestellmenge** auf der Seite **Standardbestellungseinstellungen** für ein ausgewähltes Produkt definiert ist. Wenn Sie jedoch ein Element aus einer Stücklistenversion hinzufügen und das Element und die Variante ausgewählt sind, berücksichtigt die Menge, die standardmäßig eingegeben wird, die Mindestmenge, die in den Standard-Bestellungseinstellungen für die spezifischen Dimensionen festgelegt ist.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten wird erwartet. Dass die Logik in der Stückliste und der Stücklistenversion unterschiedlich ist, ist jedoch ein bekanntes Problem. Trotzdem wird dieses Verhalten nicht geändert, da eine Änderung viele verschiedene Kundenszenarien betreffen könnte.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>In den freigegebenen Produktdetails kann ich die angehängten Bilder, die aus der Datenentität „Produktdokument-Anhänge“ hochgeladen wurden, nicht ändern.

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann auftreten, wenn Sie ein Bild an ein Element anhängen, indem Sie die Datenentität *Produktdokument-Anhänge* verwenden. In diesem Fall wird das Elementbild für das Element angezeigt. Wenn Sie jedoch **Bild ändern** wählen, wird in der Liste der hochgeladenen Bilder nichts angezeigt. Außerdem werden keine Anhänge für das Element angezeigt.

### <a name="issue-resolution"></a>Problemlösung

Die Entität *EcoResProductDocumentAttachmentEntity* (*Produktdokumentanhänge*) importiert Dokumentanhänge für *Produkte*, aber nicht für *freigegebene Produkte*. (Freigegebene Produkte werden auch als *Artikel* bezeichnet.) Um die Anhänge für einen Artikel auf der Seite **Freigegebene Produktdetails** anzuzeigen, müssen Sie stattdessen die Entität *EcoResReleasedProductDocumentAttachmentEntity* (*Freigegebene Produktdokument-Anhänge*) verwenden.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Der Konnektor Microsoft Flow zeigt die folgende Fehlermeldung an: „Update nicht erlaubt für Feld 'ProductNumber'.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem tritt auf, wenn Sie versuchen, das Feld **Produktnummer** mit Hilfe der Entität *Veröffentlichte Produkte* V2 und Microsoft Flow zu aktualisieren.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten wird erwartet. Die Möglichkeit, die Produktnummer für ein freigegebenes Produkt zu bearbeiten, wurde in Dynamics 365 Finance and Operations 10.0.0 mit Plattform-Update 24 entfernt, um Datenbeschädigungen zu vermeiden. In Ausnahmefällen, in denen Sie eine Datenbeschädigung reparieren müssen, die durch eine frühere Umbenennung des Primärschlüssels eines freigegebenen Produkts verursacht wurde, können Sie den Microsoft Support bitten, diese Einschränkung vorübergehend aufzuheben.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Ich kann eine freigegebene Produktvariante in einer anderen juristischen Entität nicht erstellen.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, einen Produktstamm ohne Varianten freizugeben und dann die Varianten in jeder juristischen Entität (Firma) so erstellen, wie sie benötigt werden, werden Sie nicht in der Lage sein, die Varianten mit Hilfe von Variantenvorschlägen freizugeben. Sie werden auch nicht in der Lage sein, die Varianten manuell zu erstellen.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Die Beziehungen eines Produktstamms und die Dimensionen, die der Stamm annehmen kann, werden auf einer gemeinsamen Ebene gehalten. Daher können Sie die verfügbaren Dimensionen für einen gemeinsamen Produktstamm nicht in der spezifischen juristischen Entität erstellen, in der diese Dimensionen freigegeben sind, und den Prozess dann in jeder juristischen Entität, in der die Dimensionen benötigt werden, replizieren. Stattdessen müssen Sie Ihren Freigabeprozess ändern, um ihn an den entworfenen Prozess anzupassen.

Hier ist der Prozess für die Freigabe von Produkten.

1. Erstellen Sie den gemeinsamen Produktstamm und die Dimensionen, die für die juristischen Entitäten freigegeben werden können.
1. Geben Sie die Produkte für die juristischen Entitäten frei, indem Sie entweder Variantenvorschläge verwenden oder die freizugebenden Kombinationen manuell hinzufügen.

Alternativ können Sie das freigegebene Produkt auch direkt erstellen.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Wenn ich eine Variante in einer anderen Firma freigebe, erhalte ich die folgende Fehlermeldung: „Produktvariante mit angegebenen Dimensionen wurde bereits erstellt.“

### <a name="issue-description"></a>Problembeschreibung

Wenn eine Produktvariante bereits in einer Firma A freigegeben wurde und Sie versuchen, diese in Firma B über die Schaltfläche **Neu** auf der Seite **Freigegebene Produktvarianten** freizugeben, erhalten Sie folgende Fehlermeldung:

> Eine Produktvariante mit den angegebenen Dimensionen wurde bereits erstellt.

### <a name="issue-resolution"></a>Problemlösung

Die Schaltfläche **Neu** auf der Seite **Freigegebene Produktvarianten** erstellt die Variante und gibt sie im Firmenkontext frei. Wenn die Variante bereits erstellt wurde, können Sie die **Neu**-Schaltfläche nicht verwenden, um sie in einer anderen Firma freizugeben.

Um das Problem zu beheben, öffnen Sie die Seite **Produktstamm** und wählen Sie **Produkt freigeben**, um die vorhandene Variante in der gewünschten Firma freizugeben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]