---
title: Aktivitätsabhängige EB-Ziele konfigurieren
description: In diesem Artikel wird erläutert, wie für ein EB-Format (elektronische Berichterstellung), das zum Generieren ausgehender Dokumente konfiguriert wird, aktivitätsabhängige Ziele konfiguriert werden.
author: kfend
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 80a432a431891c02e4bf5c71cfe2bd9642c41c75
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843796"
---
# <a name="configure-action-dependent-er-destinations"></a>Aktivitätsabhängige EB-Ziele konfigurieren

[!include [banner](../includes/banner.md)]

Sie können [Ziele](electronic-reporting-destinations.md) für jede Ausgabekomponenten (Ordner oder Datei) für das Format für die [Elektronische Berichterstellung (EB)](general-electronic-reporting.md) [Konfiguration](general-electronic-reporting.md#Configuration) konfigurieren, die zum Generieren eines ausgehenden Dokuments verwendet wird. Benutzer, die ein Eb-Format dieses Typs ausführen und über entsprechende Zugriffsrechte verfügen, können die konfigurierten Zieleinstellungen zur Laufzeit auch ändern.

In Microsoft Dynamics 365 Finance **Version 10.0.17 und höher** kann ein EB-Format ausgeführt werden durch [Bereitstellung](er-apis-app10-0-17.md) eines Aktionscodes, den die Benutzer durch Ausführen dieses EB-Formats ausführen. Zum Beispiel im Modul **Debitoren** können Sie in den Einstellungen für die Druckverwaltung ein EB-Format auswählen, das ein bestimmtes Geschäftsdokument generiert, z. B. eine Freitextrechnung. Sie können dann **Ansicht** auswählen, um eine Vorschau der Rechnung anzuzeigen, oder **Drucken**, um es an einen Drucker zu senden. Wenn zur Laufzeit eine Benutzeraktion für das laufende EB-Format übergeben wird, können Sie verschiedene EB-Ziele für verschiedene Benutzeraktionen konfigurieren. In diesem Artikel wird erläutert, wie EB-Ziele für diese Art von EB-Format konfiguriert werden.

## <a name="make-action-dependent-er-destinations-available"></a>Aktivitätsabhängige EB-Ziele verfügbar machen

Um aktivitätsabhängige EB-Ziele in der aktuellen Finance-Instanz zu konfigurieren und die [neue](er-apis-app10-0-17.md) EB-API zu konfigurieren, öffnen Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace), und aktivieren Sie die Funktion **Bestimmte EB-Ziele konfigurieren, die für verschiedene PM-Aktivitäten verwendet werden sollen**. Um konfigurierte EB-Ziele für Berichte zur Laufzeit zu verwenden, aktivieren Sie die Funktion **Ausgabe von PM-Berichten basierend auf EB-Zielen weiterleiten, die für Benutzeraktionen spezifisch sind (Zyklus 1)** feature.

## <a name="configure-action-dependent-er-destinations"></a>Aktivitätsabhängige EB-Ziele konfigurieren

Wenn Sie die Funktion **Bestimmte EB-Ziele konfigurieren, die für verschiedene PM-Aktivitäten verwendet werden sollen** aktivieren, können Sie aktivitätsabhängige EB-Ziele auf dem Inforegister **Dateiziel** der Seite **Ziel der elektronischen Berichterstellung** konfigurieren. Für jede Komponente können Sie einen Datensatz hinzufügen und bestimmte EB-Ziele aktivieren. Für jeden Datensatz müssen Sie den Dokumenttyp angeben, für den die konfigurierten EB-Ziele angewendet werden sollen. In dem Feld **Dokumenttyp** wählen Sie einen der folgenden Werte aus:

- Wählen Sie **Elektronisch** aus, um die konfigurierten Ziele anzuwenden, wenn zur Laufzeit kein Benutzeraktionscode bereitgestellt wird.
- Wählen Sie **Druckverwaltung** aus, um die konfigurierten Ziele anzuwenden, wenn zur Laufzeit ein Benutzeraktionscode bereitgestellt wird.
- Wählen Sie **Beliebige** aus, um die konfigurierten Ziele immer anzuwenden, unabhängig davon, ob zur Laufzeit eine Benutzeraktion bereitgestellt wird.

Wenn Sie den Dokumenttyp **Druckverwaltung** auswählen, müssen Sie die Benutzeraktionen angeben, für die die konfigurierten EB-Ziele angewendet werden sollen. In dem Feld **Druckverwaltungsaktion** wählen Sie einen der folgenden Werte aus:

- Wählen Sie **Ansicht** aus, um die konfigurierten Ziele anzuwenden, wenn zur Laufzeit die Benutzeraktion **Ansicht** bereitgestellt wird.
- Wählen Sie **Drucken** aus, um die konfigurierten Ziele anzuwenden, wenn zur Laufzeit die Benutzeraktion **Drucken** bereitgestellt wird.
- Wählen Sie **Senden** aus, um die konfigurierten Ziele anzuwenden, wenn zur Laufzeit die Benutzeraktion **Senden** bereitgestellt wird.

> [!NOTE]
> Für einen einzelnen Zieldatensatz können mehrere Aktivitäten ausgewählt werden.

Wenn Sie den Dokumenttyp **Beliebige** auswählen, wird im Feld **Druckverwaltungsaktion** automatisch **Automatisch erkennen** als Benutzeraktion ausgewählt, und das folgende Verhalten tritt auf:

- Wenn zur Laufzeit kein Benutzeraktionscode bereitgestellt wird, werden alle konfigurierten EB-Ziele angewendet.
- Wenn zur Laufzeit ein Benutzeraktionscode bereitgestellt wird, wird ein EB-Ziel angewendet, das für eine bestimmte Aktion vordefiniert ist, **unabhängig davon, ob es aktiviert wurde**:

    - Wenn die Aktion **Ansicht** zur Laufzeit bereitgestellt wird, wird das EB-Ziel **Bildschirm** angewendet.
    - Wenn die Aktion **Senden** zur Laufzeit bereitgestellt wird, wird das EB-Ziel **E-Mail** angewendet.
    - Wenn die Aktion **Drucken** zur Laufzeit bereitgestellt wird, wird das EB-Ziel **Drucker** angewendet.

Zum Beispiel können Sie das EB-Format **Freitextrechnung (Excel)** verwenden, um eine [Freitextrechnung](../../../finance/accounts-receivable/create-free-text-invoice-new.md) zu drucken, wenn Sie sie buchen. Um ein generiertes Dokument weiterzuleiten, müssen Sie EB-Ziele für dieses EB-Format konfigurieren. Beispielsweise müssen Sie diese EB-Ziele möglicherweise so konfigurieren, dass für ein generiertes Dokument Folgendes ausgeführt wird:

- Archivieren Sie das Dokument, wenn das EB-Format ausgeführt wird, aber kein Aktionscode bereitgestellt wird (z. B. wenn das Dokument elektronisch gesendet wird).
- Zeigen Sie eine Vorschau des Dokuments in einem Webbrowser an, wenn ein Benutzer die Aktion **Ansicht** ausführt.
- Archivieren und drucken Sie das Dokument, wenn ein Benutzer die Aktion **Drucken** ausführt.
- Archivieren Sie das Dokument und senden Sie es per E-Mail als Anhang einer ausgehenden E-Mail-Nachricht, wenn ein Benutzer die Aktivität **Senden** ausführt.

Die folgende Abbildung zeigt, wie Sie diese Konfiguration von EB-Zielen als Satz einzelner Zieldatensätze erreichen können, wenn jeder Datensatz für eine einzelne Benutzeraktion konfiguriert ist:

![Zielseite für die elektronische Berichterstellung mit aktivitätsabhängigen Zieleinstellungen für ein EB-Format, wenn jeder Zieldatensatz für eine einzelne Benutzeraktion konfiguriert ist.](./media/er-destination-action-dependent-01.png)

Die folgende Abbildung zeigt, wie Sie das Gleiche erreichen können, indem Sie alternativ EB-Ziele als Satz einzelner Zieldatensätze konfigurieren, wenn jeder Datensatz für ein einzelnes Ziel konfiguriert ist:

![Zielseite für die elektronische Berichterstellung mit aktivitätsabhängigen Zieleinstellungen für ein EB-Format, wenn jeder Zieldatensatz für ein einzelnes Ziel konfiguriert ist.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Wenn für das laufende EB-Format ein Aktionscode bereitgestellt wird, für diesen Aktionscode jedoch keine Ziele konfiguriert wurden, wird das [standardmäßige](electronic-reporting-destinations.md#default-behavior) Zielverhalten angewendet.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Aktivitätsabhängige EB-Ziele zur Laufzeit ändern

Wenn ein EB-Format ausgeführt wird und Benutzeraktionen von Benutzern bereitgestellt wurden, die über die entsprechenden [Berechtigungen](electronic-reporting-destinations.md#security-considerations) verfügen, um die konfigurierten Zieleinstellungen zur Laufzeit zu ändern, wird ein Dialogfeld angezeigt, in dem die konfigurierten Zieleinstellungen geändert werden können. Dieses Dialogfeld ist optional und hängt davon ab, wie der Aufruf des EB-Frameworks zum Ausführen eines EB-Formats implementiert wurde. Wenn dieses Dialogfeld angezeigt wird, werden die darin enthaltenen EB-Ziele entsprechend der bereitgestellten Benutzeraktion aktiviert.

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Ziele für elektronisches Berichterstellungsformat**, das angezeigt wird, wenn eine Freitextrechnung [gebucht wird](../../../finance/accounts-receivable/create-free-text-invoice-new.md) und das EB-Format **Freitextrechnung (Excel)** ausgeführt wird, um dieses Dokument zu generieren, wenn die Aktion **Drucker** bereitgestellt wurde und EB-Ziele für dieses Format konfiguriert wurden (siehe weiter oben in diesem Artikel).

![Dialogfeld, in dem Sie die anfänglich konfigurierten EB-Ziele für das laufende EB-Format ändern können.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Wenn Sie EB-Ziele für mehrere Komponenten des laufenden EB-Formats konfiguriert haben, wird für jede konfigurierte Komponente des EB-Formats eine separate Option angeboten.

Wenn mehrere ER-Formate als Berichtsvorlagen für das ausgewählte Dokument in Frage kommen, werden alle ER-Ziele für alle zutreffenden ER-Berichtsvorlagen im Dialogfeld angezeigt und stehen zur manuellen Anpassung zur Laufzeit zur Verfügung.

Wenn keine [SQL Server Reporting Services (SSRS)](SSRS-report.md) Berichtsvorlagen auf das ausgewählte Dokument anwendbar sind, wird die Standardauswahl der Druckverwaltungsziele dynamisch ausgeblendet.

Ab Finance-Version **10.0.31**, können Sie die zugewiesenen ER-Destinationen zur Laufzeit für die folgenden Geschäftsbelege manuell ändern:

- Debitorenkontoauszug
- Zinsrechnung
- Mahnung
- Zahlungsavis für Debitors
- Zahlungsavis des Kreditors

Um die Funktion zum Ändern der ER-Ziele in Runtime zu ändern, aktivieren Sie die Funktion **Anpassung der ER-Ziele zur Laufzeit erlauben** im [Funktionsverwaltung](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) Arbeitsbereich.

> [!IMPORTANT]
> Für die Berichte **Zahlungsavis für Debitors** und **Zahlungsavis des Kreditors** ist die Möglichkeit zum manuellen Ändern von ER-Zielen nur verfügbar, wenn der **ForcePrintJobSettings** Flight ist aktiviert.

[![ER-Ziele zur Laufzeit anpassen.](./media/ERdestinaiotnChangeUI.jpg)](./media/ERdestinaiotnChangeUI.jpg)

> [!NOTE]
> Wenn die Option **Druckverwaltungsziel verwenden** auf **Ja** eingestellt ist, verwendet das System die standardmäßig konfigurierten ER-Ziele für spezifische ER-Berichte. Alle manuellen Änderungen, die im Dialogfeld vorgenommen werden, werden ignoriert. Setzen Sie die Option **Druckverwaltungsziel verwenden** auf **Nein**, um Dokumente an die im Dialogfeld definierten ER-Ziele zu verarbeiten Box unmittelbar bevor Sie die Berichte ausführen.

Die folgenden Geschäftsdokumente setzen keine explizite Benutzerauswahl einer Aktion voraus, wenn sie ausgeführt werden:

- Debitorenkontoauszug
- Zinsrechnung
- Mahnung
- Zahlungsavis für Debitors
- Zahlungsavis des Kreditors

Die folgende Logik wird verwendet, um zu bestimmen, welche Aktion verwendet wird, während die vorherigen Berichte verarbeitet werden:

- Wenn der **ForcePrintJobSettings** Flight aktiviert ist:

    - Wenn die Option **Druckverwaltungsziel verwenden** auf **Ja** eingestellt ist, wird die Option **Drucken** Aktion wird verwendet.
    - Wenn die Option **Druckverwaltungsziel verwenden** auf **Nein** eingestellt ist, wird die Option **Ansicht** Aktion wird verwendet.

- Wenn der **ForcePrintJobSettings** Flight nicht aktiviert ist:

    - Wenn die Option **Druckverwaltungsziel verwenden** auf **Ja** eingestellt ist, wird die Aktion **Drucken** für die Berichte **Zahlungsavis für Debitors** und **Zahlungsavis des Kreditors** verwendet.
    - Wenn die Option **Druckverwaltungsziel verwenden** auf **Nein** eingestellt ist, wird immer die standardmäßige SSRS-Berichtsvorlage für die Berichte **Zahlungsavis für Debitors** und **Zahlungsavis des Kreditors**, unabhängig von konfigurierten ER-Einstellungen.
    - Die Aktion **Drucken** wird immer für die Berichte **Debitorenkontoauszug**, **Zinsrechnung**, und **Mahnung** verwendet.

Für die vorstehende Logik können die Aktionen **Drucken** oder **Anzeigen** verwendet werden, um aktionsabhängige ER-Berichtsziele zu konfigurieren. Zur Laufzeit werden im Dialogfeld nur EB-Ziele gefiltert, die für eine bestimmte Aktion konfiguriert sind.

## <a name="verify-the-provided-user-action"></a>Überprüfen der angegebenen Benutzeraktion

Sie können überprüfen, welche Benutzeraktion, falls vorhanden, für das ausgeführte EB-Format bereitgestellt wird, wenn Sie eine bestimmte Benutzeraktion ausführen. Diese Überprüfung ist wichtig, wenn Sie aktivitätsabhängige EB-Ziele konfigurieren müssen, aber nicht sicher sind, welcher Benutzeraktionscode, falls vorhanden, bereitgestellt wird. Wenn Sie z. B. anfangen, eine Freitextrechnung zu buchen und die Option **Rechnung drucken** im Dialogfeld **Freitextrechnung buchen** auf **Ja** setzen, können Sie die Option **Druckverwaltungsziel verwenden** auf **Ja** oder **Nein** setzen.

Befolgen Sie diese Schritte, um den bereitgestellten Benutzeraktionscode zu überprüfen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Im Dialogfeld **Benutzerparameter** [setzen](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) Sie die Option **Im Debugmodus ausführen** auf **Ja**.
4. Führen Sie eine Benutzeraktion aus, indem Sie ein EB-Format ausführen. Beachten Sie, dass die EB-Benutzerparameter benutzerspezifisch und unternehmensspezifisch sind.
5. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurations-Debug-Protokolle**.
6. Auf der Seite **Konfigurations-Debug-Protokolle** filtern Sie die EB-Ausführungsprotokolle, um das Protokoll für Ihre EB-Formatausführung zu finden.
7. Überprüfen Sie die Protokolleinträge, die den Datensatz enthalten müssen, der den bereitgestellten Benutzeraktionscode enthält, wenn für die EB-Formatausführung eine Aktion bereitgestellt wurde.

    ![Protokollprotokollseite für elektronische Berichterstellung, die Informationen zum Benutzeraktionscode enthält, der für die gefilterte Ausführung eines EB-Formats bereitgestellt wurde.](./media/er-destination-action-dependent-03.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die elektronische Berichterstellung (EB)](general-electronic-reporting.md)

[Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)

[Änderungen an der Framework-API für elektronische Berichterstellung für Application Update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
