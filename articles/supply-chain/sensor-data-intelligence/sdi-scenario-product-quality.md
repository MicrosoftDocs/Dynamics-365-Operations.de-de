---
title: Das Produktqualitätsszenario
description: Dieser Artikel enthält Informationen über das Szenario der Produktqualität. Dieses Szenario verwendet einen Sensor, um die Qualität einer Produktcharge zu messen, und generiert eine Warnung, wenn ein Messwert einen definierten Schwellenwert überschreitet.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690047"
---
# <a name="the-product-quality-scenario"></a>Das Produktqualitätsszenario

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Im *Produktqualität*-Szenario wird ein Sensor installiert, der die Qualität einer Produktcharge im Fertigungsbereich misst. Wenn eine Messung einen definierten Schwellenwert für das Produkt überschreitet, wird eine Benachrichtigung auf dem Dashboard des Supervisors angezeigt. Beispielsweise misst ein Sensor die Feuchtigkeit eines Lebensmittelprodukts, das aus der Produktionslinie kommt. Wenn die Messung außerhalb des zulässigen Mindest- oder Höchstwerts für die Feuchtigkeit des Produkts liegt, wird eine Benachrichtigung generiert.

## <a name="scenario-dependencies"></a>Szenarioabhängigkeiten

Das Szenario *Produktqualität* weist die Folgenden Abhängigkeiten auf:

- Ein Alert kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine läuft und diese Maschine ein Produkt produziert, das ein zugeordnetes Chargenattribut hat.
- Ein Signal, das das Chargenattribut darstellt, muss an den IoT-Hub gesendet werden und ein eindeutiger Eigenschaftsname muss enthalten sein.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Vorbereitung von Demodaten für das Szenario der Produktqualität

Wenn Sie ein Demosystem verwenden möchten, um das Szenario *Produktqualität* zu testen, verwenden Sie ein System, auf dem die Datei [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert ist, wählen Sie die *USMF* juristische Person (Firma) aus und bereiten Sie die zusätzlichen Demodaten wie in diesem Abschnitt beschrieben vor. Wenn Sie Ihre eigenen Sensoren und Daten verwenden, können Sie diesen Abschnitt überspringen.

In diesem Abschnitt richten Sie die Demodaten ein, damit Sie das freigegebene Produkt *P0111* (*Zusammengesetztes Gehäuse*) mit dem *Produktqualität*-Szenario verwenden können. In diesem Szenario verfolgt das System, ob ein Chargenattributwert, der von einem Sensor gemessen wird, außerhalb des definierten Schwellenwerts für ein Chargenattribut liegt, das dem Produkt zugeordnet ist.

### <a name="set-up-a-sensor-simulator"></a>Einen Sensorsimulator einrichten

Wenn Sie dieses Szenario ohne Verwendung eines physischen Sensors ausprobieren möchten, können Sie einen Simulator einrichten, um die erforderlichen Signale zu erzeugen. Weitere Informationen finden Sie unter [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Ordnen Sie dem Produkt P0111 ein Chargenattribut und eine Ressource zu

Befolgen Sie diese Schritte, um ein Chargenattribut dem Produkt *P0111* (*Zusammengesetztes Gehäuse*) zuzuordnen, und überprüfen Sie, dass Ressource *3118* (*Schaumschneidemaschine*) dafür verwendet wird.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen und wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *P0111* festgelegt ist.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Chargenattribute** auf **Produktspezifisch**.
1. Auf der **Produktspezifisch**-Seite wählen Sie **Neu**, um ein produktspezifisches Chargenattribut zu erstellen.
1. Legen Sie in der Kopfzeile die folgenden Felder fest:

    - **Attributcode** – Wählen Sie den Bereich der Attribute aus, die Sie überwachen möchten (*Tabelle*, *Gruppe* oder *Alle*). Wählen Sie für dieses Szenario *Tabelle*, da Sie immer ein einzelnes Attribut überwachen.
    - **Attributbeziehung** – Wählen Sie das Attribut aus, dessen Wert Sie mit dem Szenario *Produktqualität* überwachen wollen. Wählen Sie für dieses Beispiel *Konzentration* aus, ein Attribut, das in den Standard-Demodaten enthalten ist.

1. Legen Sie auf dem Inforegsiter **Werte** in den Feldern **Minimum** und **Maximum** den Bereich der akzeptablen Werte fest, die das Attribut melden muss, um die Qualitätsprüfung zu bestehen. Meldet der Sensor einen Wert außerhalb dieses Bereichs, erkennt das System dies als Qualitätsverstoß. Die anderen Felder auf diesem Inforegister sind für das *Produktqualität* Szenario nicht relevant. Die Standardwerte, die Sie derzeit sehen, stammen aus den Demodaten. Lassen Sie sie daher so, wie sie sind, und schließen Sie die **Produktspezifisch** Seite, um zur **Veröffentlichte Produktdetails** Seite für Artikel *P0111* zurückzukehren.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Techniker** in der Gruppe **Ansicht** die Option **Route** aus.
1. Auf der **Route**-Seite wählen Sie auf der **Überblick**-Registerkarte unten auf der Seite die Zeile aus, in der das Feld **Arbeitsgangnummer** auf *30* festgelegt ist.
1. Vergewissern Sie sich auf der Registerkarte **Ressourcenanforderungen** unten auf der Seite, dass die Ressource *3118* (*Schaumstoffschneidemaschine*) mit dem Vorgang verknüpft ist.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Anlegen und Freigeben eines Fertigungsauftrags für das Produkt P0111

Befolgen Sie diese Schritte, um einen Produktionsauftrag für das Produkt *P0111* zu erstellen und freizugeben.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**.
1. Wählen Sie auf der Seite **Alle Produktionsaufträge** im Aktivitätsbereich **Neuer Chargenauftrag**.
1. Legen Sie im Dialogfeld **Charge erstellen** die folgenden Werte fest:

    - **Artikelnummer:** *P0111*
    - **Menge** *10*

1. Wählen Sie **Erstellen**, um den Auftrag zu erstellen und zur Seite **Alle Produktionsaufträge** zurückzukehren.
1. Verwenden Sie das **Filter**-Feld für die Suche nach Fertigungsaufträgen, bei denen das **Artikelnummer**-Feld auf *P0111* eingestellt ist. Suchen Sie dann den soeben erstellten Produktionsauftrag und wählen Sie ihn aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Kalkulieren**.
1. Wählen Sie im Dialogfeld **Schätzen** die Option **OK**, um die Schätzung durchzuführen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Freigabe**.
1. Notieren Sie sich im Dialogfeld **Freigabe** die Nummer des soeben erstellten Chargenauftrags.
1. Wählen Sie **OK** aus, um den Auftrag freizugeben.

### <a name="configure-the-production-floor-execution-interface"></a>Produktionsausführungsschnittstelle konfigurieren

Falls noch nicht geschehen, konfigurieren Sie die Ausführungsschnittstelle für die Produktion so, dass Aufträge angezeigt werden, die der Ressource *3118* (*Schaumstoffschneidemaschine*) zugewiesen sind. Anweisungen finden Sie in den folgenden Abschnitten.

- [Produktionsausführungsoberfläche konfigurieren](sdi-scenario-equipment-downtime.md#config-pfe)
- [Aktivieren Sie die Suchoption auf der Ausführungsoberfläche der Produktionsstätte](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Starten Sie den ersten Einzelvorgang in der Chargenreihenfolge

Gehen Sie folgendermaßen vor, um den ersten Auftrag in der Chargenreihenfolge zu starten.

1. Gehen Sie zu **Produktionskontrolle \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Geben Sie im Feld **Badge-ID** den Wert *123* ein. Wählen Sie dann **Anmelden** aus.
1. Wenn Sie nach einem Abwesenheitsgrund gefragt werden, wählen Sie eine der Abwesenheitskarten aus und wählen Sie dann **OK**.
1. Geben Sie in das Feld **Suche** die Chargenauftragsnummer ein, die Sie sich zuvor notiert haben. Wählen Sie dann die **Eingabetaste**.
1. Wählen Sie den Auftrag und anschließend **Einzelvorgang starten** aus.
1. Wählen Sie im **Einzelvorgang starten**-Dialogfeld **Starten** aus.

## <a name="set-up-the-product-quality-scenario"></a>Das Produktqualitätsszenario einrichten

Gehen Sie folgendermaßen vor, um das Szenario *Produktqualität* in Supply Chain Management einzurichten.

1. Wechseln Sie zu **Produktionssteuerung \> Einrichtung \> Sensor Data Intelligence \> Szenarien**.
1. Wählen Sie im Szenariofeld **Produktqualität** die Option **Konfigurieren**, um den Einrichtungsassistenten für dieses Szenario zu öffnen.
1. Wählen Sie auf der Seite **Sensoren** die Option **Neu** aus, um dem Raster einen Sensor hinzuzufügen. Legen Sie dann die folgenden Felder fest:

    - **Sensor-ID** – Geben Sie die ID des verwendeten Sensors ein. (Wenn Sie den Raspberry PI Azure IoT Online Simulator verwenden und ihn wie in [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md) beschrieben eingerichtet haben, geben Sie *Qualität* ein.)
    - **Sensorbeschreibung** – Geben Sie eine detaillierte Beschreibung des Sensors ein.

1. Wiederholen Sie den vorherigen Schritt für jeden weiteren Sensor, den Sie jetzt hinzufügen möchten. Sie können jederzeit zurückkehren und weitere Sensoren hinzufügen.
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Geschäftsdatensatzzuordnung** im Abschnitt **Sensoren** den Datensatz für einen der Sensoren aus, den Sie gerade hinzugefügt haben.
1. Öffnen Sie im Abschnitt **Geschäftsdatensatzzuordnung** und wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. In der neuen Zeile sollte das Feld **Geschäftsdatensatztyp** automatisch auf *Resources(WrkCtrTable)* gesetzt werden. Legen Sie für das Feld **Geschäftsdatensatz** die Ressource fest, die Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie sie auf *3118, Schaumschneidemaschine*.)
1. Unmittelbar nachdem Sie einen Geschäftsdatensatztyp für die Zeile ausgewählt haben, die Sie im vorherigen Schritt hinzugefügt haben, wird dem Raster automatisch eine zweite Zeile hinzugefügt. In dieser Zeile sollte das **Geschäftsdatensatztyp**-Feld auf *Batch attributes(PdsBatchAttrib)* gesetzt werden. Legen Sie für das Feld **Geschäftsdatensatz** das Chargenattribut fest, das Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie sie auf *Konzentration, Konzentrationsporzentsatz*.)
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Sensoren aktivieren** im Raster den Sensor aus, den Sie hinzugefügt haben, und wählen Sie dann **Aktivieren**. Für jeden aktivierten Sensor im Raster erscheint ein Häkchen in der **Aktiv**-Spalte.
1. Wählen Sie **Fertig stellen** aus.

## <a name="work-with-the-product-quality-scenario"></a>Arbeiten mit dem Produktqualitätsszenario

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Zeigen Sie Produktqualitätsdaten auf der Seite „Ressourcenstatus“ an

Auf der **Ressourcenstatus**-Seite können Supervisoren eine Zeitleiste von Produktqualitätssignalen überwachen, die von den Sensoren empfangen werden, die jeder Maschinenressource zugeordnet sind. Gehen Sie folgendermaßen vor, um die Zeitleiste zu konfigurieren.

1. Gehen Sie zu **Produktionssteuerung \> Fertigungssteuerung \> Ressourcenstatus**.
1. Im angezeigten Dialogfeld **Konfigurieren** legen Sie die folgenden Felder fest:

    - **Ressource** – Wählen Sie die Ressourcen, die Sie überwachen möchten. (Wenn Sie mit den Demodaten arbeiten, wählen Sie *3118* aus.)
    - **Zeitreihe 1** – Wählen Sie den Datensatz (Metrikschlüssel) aus, dessen Name das folgende Format hat: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Anzeigename** – Geben Sie *Chargenattributwerte* ein.

Die folgende Abbildung zeigt ein Beispiel für Produktqualitätsdaten auf der **Ressourcenstatus** Seite, wenn der Wert im Bereich akzeptabler Werte liegt.

![Produktqualitätsdaten auf der Ressourcenstatusseite, wenn der Wert im Bereich liegt.](media/sdi-product-quality-in-range.png "Produktqualitätsdaten auf der Ressourcenstatusseite, wenn der Wert im Bereich liegt")

Die folgende Abbildung zeigt ein Beispiel für Produktqualitätsdaten, wenn ein außerhalb des Bereichs liegender Wert erkannt wird.

![Produktqualitätsdaten auf der Seite Ressourcenstatus, wenn ein Wert außerhalb des Bereichs erkannt wird.](media/sdi-product-quality-out-of-range.png "Produktqualitätsdaten auf der Seite Ressourcenstatus, wenn ein Wert außerhalb des Bereichs erkannt wird")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Zeigen Sie Produktqualitätsdaten auf der Seite „Benachrichtigungen“ an

Auf der **Benachrichtigungen**-Seite können Vorgesetzte die Benachrichtigungen anzeigen, die generiert werden, wenn der Sensor einen Chargenattributwert misst, der außerhalb des definierten Schwellenwerts für das Chargenattribut liegt. Jede Benachrichtigung bietet einen Überblick über den Produktionsauftrag, der von dem Ausfall betroffen ist, und bietet die Möglichkeit, den betroffenen Auftrag einer anderen Ressource zuzuweisen.

Um die Seite **Benachrichtigung** zu öffnen, gehen Sie zu **Produktionssteuerung \> Abfragen und Berichte \> Sensor Data Intelligence \> Benachrichtigungen**.

Die folgende Abbildung zeigt das Beispiel einer Produktqualitätsbenachrichtigung.

![Beispiel einer Produktqualitätsbenachrichtigung.](media/sdi-product-quality-notification.png "Beispiel einer Produktqualitätsbenachrichtigung")
