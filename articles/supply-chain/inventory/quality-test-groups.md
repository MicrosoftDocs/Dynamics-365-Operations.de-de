---
title: Qualitätsmanagement Testgruppen
description: Dieses Thema beschreibt, wie Sie Testgruppen erstellen, so dass mehrere Tests mit Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 230e402c322509f3ea89d4f1dccb5555828377ff
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578391"
---
# <a name="quality-management-test-groups"></a>Qualitätsmanagement Testgruppen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Testgruppen erstellen, so dass mehrere Tests mit Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.

Sie verwenden die Seite **Testgruppen**, um Testgruppen und die einzelnen Tests, die ihnen zugeordnet sind, festzulegen, zu bearbeiten und anzuzeigen. Der obere Teil der Seite zeigt die Testgruppen und der untere Teil zeigt die Tests, die einer ausgewählten Testgruppe zugeordnet sind.

Sie ordnen einer Prüfgruppe mehrere Richtlinien zu, z.B. einen Stichprobenplan, eine akzeptable Qualitätsstufe (AQL) und die Anforderung für zerstörende Prüfungen. Wenn Sie dann einen individuellen Test einer Testgruppe zuordnen, definieren Sie zusätzliche Informationen, wie z.B. die Sequenz, Dokumente und Gültigkeitsdaten. Bei einem Mengentest zählen zu den zu definierenden Informationen auch die akzeptablen Messwerte. Bei einem Qualitätstest zählen hierzu auch die Testvariable und das Standardergebnis.

Die einem Qualitätsprüfungsauftrag zugeordnete Testgruppe definiert die Tests, die für den angegebenen Artikel ausgeführt werden müssen. Sie können jedoch Tests für den Qualitätsprüfungsauftrag hinzufügen, löschen oder ändern. Testergebnisse werden für jeden Test im Qualitätsprüfungsauftrag gemeldet.

Wenn Sie eine Testgruppe definieren, können Sie optional eine Artikelmusteraufnahme angeben. Artikelmusteraufnahmen werden verwendet, um die Menge des Produkts zu definieren, die getestet werden muss. Weitere Informationen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahme](quality-item-sampling.md). Sie können auch angeben, ob die Tests in einer Testgruppe destruktiv sind. Bei einer zerstörenden Prüfung wird die Artikelmusteraufnahme zerstört und die Menge aus dem Lagerbestand entfernt.

## <a name="example-of-a-test-group"></a>Beispiel für eine Testgruppe

Ein Produktionsunternehmen definiert eine Testgruppe für jede Abweichung von den Qualitätsrichtlinien. In den verschiedenen Testgruppen sind Unterschiede in den Musteraufnahmeplänen, die zusammen auszuführenden Tests, das akzeptable Qualitätsniveau und andere Faktoren enthalten. Bei Mengentests sind zudem Unterschiede hinsichtlich der akzeptablen Messwerte enthalten. Um ihre Qualitätsrichtlinien durchzusetzen, ordnet die Firma jeder Regel eine Prüfgruppe zu, die zur automatischen Generierung von Qualitätsprüfungsaufträgen auf der Seite **Qualitätszuordnungen** verwendet wird. Es weist auch Qualitätsprüfungsaufträgen, die manuell erstellt werden, eine Prüfgruppe zu.

## <a name="create-a-test-group"></a>Erstellen einer Testgruppe

Um eine Testgruppe zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Testgruppen**.
1. Wählen Sie im Aktionsbereich **Neu**, um dem Raster im oberen Teil der Seite eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Testgruppe** – Geben Sie eine eindeutige ID oder einen Namen für die Testgruppe ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Testgruppe ein.
    - **Akzeptable Qualitätsstufe** – Geben Sie den Gesamtprozentsatz der Testergebnisse ein, die bestanden werden müssen, damit die Gruppe von Tests als bestanden gilt.
    - **Elementmusteraufnahme** – Wählen Sie eine Elementmusteraufnahme. Weitere Informationen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahme](quality-item-sampling.md).
    - **Destruktiv** – Aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass die Testgruppe die getesteten Elemente zerstören wird.

1. Während die neue Zeile noch ausgewählt ist, wählen Sie die Registerkarte **Allgemein** im oberen Teil der Seite. Einige der Einstellungen für die Testgruppe, die auf der Registerkarte **Übersicht** festgelegt ist, werden hier wiederholt. Zusätzlich können Sie die folgenden Felder für die Gruppe festlegen:

    - **Bestand Batch-Attribut aktualisieren** – Wenn Sie diese Option hier auf *Ja* festlegen, wird sie automatisch auf *Ja* für jeden neuen Test festgelegt, der der Testgruppe im unteren Teil der Seite hinzugefügt wird.
    - **Batch-Disposition aktualisieren** – Wenn Sie diese Option auf *Ja* festlegen, wird die Batch-Disposition automatisch mit dem Wert aktualisiert, der im Feld **Fehlgeschlagener Qualitätsprüfungsauftrag Batch-Disposition** oder **Bestandener Qualitätsprüfungsauftrag Batch-Disposition** ausgewählt ist, wenn das Element, das getestet wird, chargengesteuert ist.
    - **Batch-Disposition für fehlgeschlagenen Qualitätsprüfungsauftrag** – Wählen Sie den Code für die Batch-Disposition, der zugewiesen werden soll, wenn ein Qualitätsprüfungsauftrag, der diese Testgruppe enthält, fehlschlägt, weil er den AQL nicht erfüllt.
    - **Bestandener Qualitätsprüfungsauftrag Batch-Disposition** – Wählen Sie den Code für die Batch-Disposition, der zugewiesen werden soll, wenn ein Qualitätsprüfungsauftrag, der diese Testgruppe enthält, bestanden wird, weil er den AQL erfüllt.
    - **Bestandsstatus aktualisieren** – Wenn Sie diese Option auf *Ja* festlegen, wird der Status automatisch mit dem Status aktualisiert, der im Feld **Status des Qualitätsprüfungsauftrags fehlgeschlagen** oder **Status des Qualitätsprüfungsauftrags bestanden** ausgewählt wurde, wenn **Bestandsstatus** in der Gruppe der Bestandsdimensionen für das zu testende Element aktiviert ist.
    - **Status des fehlgeschlagenen Qualitätsprüfungsauftrags** – Wählen Sie den Bestandsstatus, der dem Element zugewiesen werden soll, wenn ein Qualitätsprüfungsauftrag, der diese Testgruppe enthält, fehlschlägt, weil er den AQL nicht erfüllt.
    - **Status des Qualitätsprüfungsauftrags bestanden** – Wählen Sie den Bestandsstatus, der dem Element zugewiesen werden soll, wenn ein Qualitätsprüfungsauftrag, der diese Testgruppe enthält, bestanden wird, weil er den AQL erfüllt.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Fügen Sie einen qualitativen Test zu einer Testgruppe hinzu

Um einen qualitativen Test zu einer Testgruppe hinzuzufügen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Testgruppen**.
1. Wählen Sie auf der Registerkarte **Übersicht** im oberen Teil der Seite die Testgruppe aus, zu der Sie einen Test hinzufügen möchten.
1. Wählen Sie im unteren Teil der Seite auf der Registerkarte **Übersicht** in der Symbolleiste **Hinzufügen**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Sequenznummer** – Geben Sie eine ganze Zahl ein, um die Reihenfolge anzugeben, in der die Tests durchgeführt werden sollen. Tests, die kleinere Sequenznummern haben, werden vor Tests mit größeren Sequenznummern ausgeführt.

        > [!NOTE]
        > Wir empfehlen Ihnen, eine Lücke zwischen den Sequenznummern zu lassen. Legen Sie z. B. das Feld **Sequenznummer** für Ihren ersten Test auf *10* fest und erhöhen Sie dann den Wert für jeden weiteren Test um 10. Auf diese Weise können Sie später neue Tests hinzufügen, ohne die Zeilen zu löschen und neu zu erstellen, um sie in die gewünschte Reihenfolge zu bringen.

    - **Test** – Wählen Sie den Test, den Sie durchführen möchten. Wählen Sie für einen qualitativen Test einen Test, bei dem das Feld **Typ** auf *Option* festgelegt ist.
    - **Gültig bis** – Wählen Sie das erste Datum, an dem der Test gültig ist. Wenn Sie dieses Feld leer lassen, gibt es keine Begrenzung.
    - **Ablauf** – Wählen Sie das letzte Datum, an dem der Test gültig ist. Wenn Sie dieses Feld leer lassen oder es auf *Nie* festlegen, gibt es keine Begrenzung.
    - **Testwertbestimmung** – Wählen Sie, wie ein AQL bestimmt werden soll, wenn mehrere Ergebnisse für denselben Test erfasst werden. Für einen qualitativen Test kann nur *Manuell* ausgewählt werden. Wenn Sie einen der anderen Werte wählen (*Durchschnitt*, *Minimum* oder *Maximum*), erhalten Sie beim Speichern der Testgruppe eine Fehlermeldung.
    - **Attribut** – Wenn Sie Daten zu einem Batch-Attribut aufzeichnen möchten, wählen Sie das Attribut hier aus und aktivieren Sie das Kontrollkästchen **Bestand Batch-Attribut aktualisieren**.
    - **Bestandschargenattribut aktualisieren** – Aktivieren Sie dieses Kontrollkästchen, um die Testergebnisse für das Batch-Attribut zu erfassen, das im Feld **Attribut** ausgewählt ist.

1. Wählen Sie im unteren Teil der Seite die Registerkarte **Allgemein**. Einige der Einstellungen für den Test, der auf der Registerkarte **Übersicht** ausgewählt ist, werden hier wiederholt. Zusätzlich können Sie die folgenden Felder für den Test festlegen:

    - **Analysezertifikat-Bericht** – Legen Sie diese Option auf *Ja* fest, um anzugeben, dass die Testergebnisse auf dem Zertifikat der Analyse (CoA) gedruckt werden sollen. Dieser Bericht kann aus dem Qualitätsprüfungsauftrag erzeugt werden.
    - **Aktion bei Fehlschlag** – Wählen Sie entweder *Akzeptieren* oder *Fehlschlagen*, um anzugeben, ob der Test als bestanden oder fehlgeschlagen gelten soll, wenn der AQL für ihn nicht erfüllt ist.
    - **Akzeptable Qualitätsstufe** – Geben Sie den Gesamtprozentsatz der Testergebnisse ein, die bestanden werden müssen, damit der Test als bestanden gilt.

1. Legen Sie im unteren Teil der Seite, auf der Registerkarte **Test**, die folgenden Felder fest:

    - **Variable** – Wählen Sie die Testvariable, für die Sie die qualitativen Testergebnisse Datensätze erstellen wollen.
    - **Standard-Ergebnis** – Wählen Sie das Standard-Ergebnis, das für die Testergebnisse gespeichert werden soll.
    - **Testgerät** – Wählen Sie das Gerät aus, das für den Test verwendet werden soll. Wenn ein Testgerät definiert ist, wird es automatisch für den Test in der Testgruppe eingetragen.

1. Schließen Sie die Seite.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Fügen Sie einen quantitativen Test zu einer Testgruppe hinzu

Um einen quantitativen Test zu einer Testgruppe hinzuzufügen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Testgruppen**.
1. Wählen Sie auf der Registerkarte **Übersicht** im oberen Teil der Seite die Testgruppe aus, zu der Sie einen Test hinzufügen möchten.
1. Wählen Sie im unteren Teil der Seite auf der Registerkarte **Übersicht** in der Symbolleiste **Hinzufügen**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Sequenznummer** – Geben Sie eine ganze Zahl ein, um die Reihenfolge anzugeben, in der die Tests durchgeführt werden sollen. Tests, die kleinere Sequenznummern haben, werden vor Tests mit größeren Sequenznummern ausgeführt.

        > [!NOTE]
        > Wir empfehlen Ihnen, eine Lücke zwischen den Sequenznummern zu lassen. Legen Sie z. B. das Feld **Sequenznummer** für Ihren ersten Test auf *10* fest und erhöhen Sie dann den Wert für jeden weiteren Test um 10. Auf diese Weise können Sie später neue Tests hinzufügen, ohne die Zeilen zu löschen und neu zu erstellen, um sie in die gewünschte Reihenfolge zu bringen.

    - **Test** – Wählen Sie den Test, den Sie durchführen möchten. Für einen quantitativen Test wählen Sie einen Test, bei dem das Feld **Typ** auf *Fraktion* oder *Ganzzahl* festgelegt ist.
    - **Gültig bis** – Wählen Sie das erste Datum, an dem der Test gültig ist. Wenn Sie dieses Feld leer lassen, gibt es keine Begrenzung.
    - **Ablauf** – Wählen Sie das letzte Datum, an dem der Test gültig ist. Wenn Sie dieses Feld leer lassen oder es auf *Nie* festlegen, gibt es keine Begrenzung.
    - **Testwertbestimmung** – Wählen Sie, wie ein AQL bestimmt werden soll, wenn mehrere Ergebnisse für denselben Test erfasst werden. Die verfügbaren Optionen sind *Durchschnitt*, *Minimum*, *Maximum* und *Manuell*.
    - **Attribut** – Wenn Sie Daten zu einem Batch-Attribut aufzeichnen möchten, wählen Sie das Attribut hier aus und aktivieren Sie das Kontrollkästchen **Bestand Batch-Attribut aktualisieren**.
    - **Bestandschargenattribut aktualisieren** – Aktivieren Sie dieses Kontrollkästchen, um die Testergebnisse für das Batch-Attribut zu erfassen, das im Feld **Attribut** ausgewählt ist.

1. Wählen Sie im unteren Teil der Seite die Registerkarte **Allgemein**. Einige der Einstellungen für den Test, der auf der Registerkarte **Übersicht** ausgewählt ist, werden hier wiederholt. Zusätzlich können Sie die folgenden Felder für den Test festlegen:

    - **Analysezertifikat** – Legen Sie diese Option auf *Ja* fest, um anzugeben, dass die Testergebnisse auf dem CoA gedruckt werden sollen. Dieser Bericht kann aus dem Qualitätsprüfungsauftrag erzeugt werden.
    - **Aktion bei Fehlschlag** – Wählen Sie entweder *Akzeptieren* oder *Fehlschlagen*, um anzugeben, ob der Test als bestanden oder fehlgeschlagen gelten soll, wenn der AQL für ihn nicht erfüllt ist.
    - **Akzeptable Qualitätsstufe** – Geben Sie den Gesamtprozentsatz der Testergebnisse ein, die bestanden werden müssen, damit der Test als bestanden gilt.

1. Legen Sie im unteren Teil der Seite, auf der Registerkarte **Test**, die folgenden Felder fest:

    - **Standard** – Geben Sie den Betrag (Ganzzahl oder Bruch) ein, der für die Testergebnisse erwartet wird. Der Wert, den Sie eingeben, wird standardmäßig in die Testergebnisse eingetragen. Zusätzlich wird sie automatisch als Standardwert in die Felder **Min** und **Max** eingetragen.
    - **Min** – Geben Sie den minimal zulässigen Wert für die Testergebnisse an. Der Wert, den Sie eingeben, muss kleiner sein als der Betrag, der im Feld **Standard** festgelegt ist. Wenn Sie das **Min**-Feld aktualisieren, wird das **Min-Toleranz (%)**-Feld automatisch aktualisiert. Ebenso wird beim Aktualisieren des Feldes **Min-Toleranz (%)** das Feld **Min** automatisch aktualisiert.
    - **Max** – Geben Sie den maximal zulässigen Wert für die Testergebnisse ein. Der Wert, den Sie eingeben, muss größer sein als der Betrag, der im Feld **Standard** festgelegt ist. Wenn Sie das Feld **Max** aktualisieren, wird das Feld **Max-Toleranz (%)** automatisch aktualisiert. Ebenso wird, wenn Sie das Feld **Max Toleranz (%)** aktualisieren, das Feld **Max** automatisch aktualisiert.
    - **Testgerät** – Wählen Sie das Gerät aus, das für den Test verwendet werden soll. Wenn ein Testgerät definiert ist, wird es automatisch für den Test in der Testgruppe eingetragen.

1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement Testinstrumente](quality-management-processes.md)
- [Qualitätsmanagement-Tests](quality-management-processes.md)
- [Qualitätsmanagement-Testvariablen](quality-management-processes.md)
- [Qualitätszuordnungen](quality-management-processes.md)
- [Chargenattribute](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
