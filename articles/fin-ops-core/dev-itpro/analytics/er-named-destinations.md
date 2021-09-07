---
title: Konfigurieren von Druckmanagement-Datensatz-spezifischen ER-Zielen
description: Dieses Thema erklärt, wie Sie Druckmanagement-Datensätze-spezifische Ziele für ein elektronisches Berichtsformat (ER) konfigurieren, das für die Erzeugung ausgehender Belege konfiguriert ist.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1e06fafe8d8bbe92ddf4fcd94d7271a1fbb6362a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413595"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Konfigurieren von Druckmanagement-Datensatz-spezifischen ER-Zielen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie ein Benutzer in der Rolle Systemadministrator oder Debitorenbuchhalter die folgenden Aufgaben durchführen kann:

- Konfigurieren Sie benannte [Elektronisches Reporting (ER)](general-electronic-reporting.md)-Ziele für eine ER-Lösung, die Freitext-Rechnungen generiert.
- Ein ER-Ziel einem einzelnen [Druckmanagement](document-reporting-services.md) Datensatz zuordnen.

Die Vorgänge können in der Firma USMF abgeschlossen werden. Eine Codierung ist nicht erforderlich.

## <a name="introduction"></a>Einführung

Sie können [Ziele](electronic-reporting-destinations.md) für jeden Ordner in der Dateiausgabekomponente eines ER [Formats](general-electronic-reporting.md#FormatComponentOutbound) [Konfiguration](general-electronic-reporting.md#Configuration) konfigurieren, das zur Erzeugung eines ausgehenden Belegs verwendet wird. Wenn Sie ein solches ER-Format ausführen und über die entsprechenden Zugriffsrechte verfügen, können Sie die festgelegten Zieleinstellungen auch zur Laufzeit ändern.

In Microsoft Dynamics 365 Finance **Version 10.0.17 und später** kann für ein ER-Format ein Aktionscode [festgelegt](er-apis-app10-0-17.md) werden, um die Aktion festzulegen, die Benutzer beim Ausführen dieses ER-Formats ausführen. So können Sie z.B. im Modul **Debitoren** in den Einstellungen der Druckverwaltung ein ER-Format auswählen, das einen bestimmten Beleg erzeugt, z.B. eine Freitext-Rechnung. Sie können dann **Ansicht** auswählen, um eine Vorschau der Rechnung anzuzeigen, oder **Drucken**, um es an einen Drucker zu senden. Wenn zur Laufzeit eine Aktion für das ausgeführte ER-Format übergeben wird, können Sie [unterschiedliche ER-Ziele für unterschiedliche Benutzeraktionen konfigurieren](er-action-dependent-destinations.md).

In Finance **Version 10.0.21 und höher** kann ein benanntes Ziel [für ein ER-Format festgelegt](er-apis-app10-0-21.md) und dem Druckverwaltungsdatensatz zugewiesen werden, der verarbeitet wird, wenn dieses ER-Format ausgeführt wird. Zum Beispiel möchten Sie im Modul **Debitoren** in den Druckverwaltungseinstellungen den Datensatz **Original** so festlegen, dass er die folgenden Aktionen ausführt:

- Ein ER-Format ausführen.
- Senden Sie die erzeugte Rechnung per E-Mail an einen Debitor.
- Konfigurieren Sie den Datensatz **Kopie**, um das gleiche Format auszuführen.
- Drucken Sie eine Kopie der Rechnung auf einem Netzwerkdrucker.

In diesem Fall müssen Sie verschiedene ER-Ziele für das ausgeführte ER-Format konfigurieren und Sie müssen die Ziele für verschiedene Datensätze der Druckverwaltung auswählen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, muss die Funktion **Erlauben, ER-Ziele pro Element der Druckverwaltung festzulegen** im Arbeitsbereich [Funktionsverwaltung](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) eingeschaltet werden. Außerdem muss der Quellcode geändert werden, um die Konfiguration von benannten ER-Zielen in der aktuellen Finance-Instanz zuzulassen und um die [Neue](er-apis-app10-0-21.md) ER-API zu aktivieren.

Zusätzlich muss die **Freitext-Rechnung (Excel)** ER-Konfiguration in Ihre Finance-Instanz [importiert](er-download-configurations-global-repo.md) werden.

## <a name="configure-a-new-er-destination"></a>Konfigurieren Sie ein neues ER-Ziel

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Wählen Sie eine Rechnung für das Kundenkonto **US-001**.
3. Wählen Sie auf der Seite **Freitextrechnung** auf der Registerkarte **Rechnung** in der Gruppe **Druckverwaltung** die Option **Druckverwaltung**.
4. Erweitern Sie auf der Seite **Druckverwaltung einrichten** das **Modul - Debitoren** \> **Dokumente** \> **Freitext-Rechnung**, wählen Sie den Datensatz **Original** und führen Sie dann die folgenden Schritte aus:

    1.  Beachten Sie die aktuellen Einstellungen des ausgewählten Datensatzes:
        -   Der Standard-SSRS-Report **FreeTextInvoice.Report** ist im Feld **Reportformat** ausgewählt.
        -   Im Feld **Ziel** wird der Name **\<Default\>** angezeigt, der darüber informiert, dass kein angepasstes Ziel für den zugewiesenen SSRS-Report ausgewählt ist. 
    2.  Wählen Sie im Feld **Reportformat** die Konfiguration **Freitext-Rechnung (Excel)** ER-Format.
        -   Der Name des Feldes **Ziel** wird in **Zielname** geändert.
        -   Der Name **\<No named destination\>** wird im Feld **Zielname** angezeigt und informiert darüber, dass kein benanntes Ziel für das zugewiesene ER-Format ausgewählt ist.
    3.  Wählen Sie die Pfeil-Schaltfläche rechts neben dem Feld **Zielname**.    
    4. Geben Sie auf der Seite **Benanntes Ziel für elektronische Berichte** im Feld **Name** **Hauptziel** ein.
    5. Wählen Sie **Speichern** aus.
    6. Auf der Seite **Dateiziel** Inforegister [konfigurieren](er-destination-type-email.md) Sie das Ziel **Email** für die Komponente **Report**.
    7. Schließen Sie die Seite **Elektronisches Berichtswesen benanntes Ziel**.
    8. Wählen Sie auf der Seite **Einrichtung der Druckverwaltung** im Feld **Zielname** das **Hauptziel** genanntes Ziel.

    ![Konfigurieren eines benannten ER-Ziels für das ausgewählte ER-Format und Zuweisen zu einem konfigurierten Datensatz auf der Seite Einrichtung der Druckverwaltung](./media/er-named-destinations-01.gif)

    Sie haben jetzt das benannte ER-Ziel **Hauptziel** für das Format **Freitext-Rechnung (Excel)** konfiguriert und es dem **Original** Druckmanagement-Datensatz unter **Modul - Debitoren** \> **Belege** \> **Freitext-Rechnung** zugewiesen.

5. Erweitern Sie **Modul - Debitoren** \> **Konto - US-001** \> **Freitext-Rechnung**, wählen Sie den Datensatz **Original** und führen Sie dann die folgenden Schritte aus:

    1. Halten Sie den Datensatz gedrückt (oder klicken Sie mit der rechten Maustaste) und wählen Sie **Überschreiben**.
    2. Wählen Sie die Pfeil-Schaltfläche rechts neben dem Feld **Zielname**.
    3. Wählen Sie auf der Seite **Elektronischer Bericht benanntes Ziel** im Aktionsbereich **Neu**.
    4. Geben Sie in das Feld **Name** **US-001 Ziel** ein.
    5. Auf der Registerkarte **Dateiziel** Inforegister [konfigurieren](er-destination-type-print.md) Sie den **Drucker** als Ziel für die Komponente **Report**.
    6. Schließen Sie die Seite **Elektronisches Berichtswesen benanntes Ziel**.
    7. Wählen Sie auf der Seite **Einrichtung der Druckverwaltung** im Feld **Zielname** das benannte Ziel **US-001 Ziel**.

    ![Konfigurieren eines benannten ER-Ziels für das gewählte ER-Format und Zuweisen zu dem konfigurierten Datensatz auf der Seite Einrichtung der Druckverwaltung](./media/er-named-destinations-02.gif)

    Sie haben jetzt das benannte ER-Ziel **US-001-Ziel** für das Format **Freitext-Rechnung (Excel)** konfiguriert und es dem **Original** Druckmanagement-Datensatz unter **Modul - Debitoren** \> **Konto - US-001** \> **Freitext-Rechnung** zugewiesen.

Wenn nun eine Freitext-Rechnung verarbeitet wird, wird das ER-Format **Freitext-Rechnung (Excel)** ausgeführt, und eines der folgenden Ereignisse tritt ein:

- Wenn die Freitext-Rechnung für einen anderen Debitor als US-001 ist, wird der generierte Beleg per E-Mail gesendet.
- Wenn die Freitext-Rechnung für den Debitor US-001 ist, wird der generierte Beleg gedruckt.

> [!NOTE]
> Wenn für einen Druckmanagement-Datensatz, der zur Laufzeit verarbeitet wird, kein benanntes Ziel definiert wurde, werden die Standard-ER-Ziele verwendet, wenn sie für das ausgeführte ER-Format verfügbar sind.

> [!IMPORTANT]
> Auf der Seite **Elektronisches Berichtsziel** (**Organisationsverwaltung** \> **Elektronisches Berichtsziel** \> **Elektronisches Berichtsziel**) werden Sie über das Vorhandensein von benannten Zielen benachrichtigt, wenn Sie ein ER-Format auswählen, für das mindestens ein benanntes Ziel konfiguriert wurde.
>
> ![Benachrichtigung über das Vorhandensein von konfigurierten benannten Zielen für das ausgewählte ER-Format auf der Seite Elektronisches Berichtsziel](./media/er-named-destinations-03.png)
>
> Wenn Sie das Standardziel löschen, werden auch alle benannten Ziele gelöscht. Wenn diese benannten Ziele für Datensätze der Druckverwaltung ausgewählt wurden, wird die Auswahl dieser benannten Ziele aufgehoben.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Kopieren eines vorhandenen ER-Ziels als neues benanntes Ziel

Wenn das standardmäßige benannte ER-Ziel für ein ER-Format vorhanden ist, kann es als Vorlage für neue ER-Ziele verwendet werden. Um ein neues ER-Ziel zu erstellen, das auf dem Standardziel basiert, wählen Sie **Vorgabe kopieren** auf der Seite **Benanntes Ziel für elektronische Berichte**. Das neue Ziel erhält den Namen **Standard**. Sie können diesen Schritt so oft wie nötig wiederholen.

Sie können jedes vorhandene benannte Ziel als Vorlage für ein neues benanntes Ziel auswählen. Um ein neues benanntes ER-Ziel zu erstellen, das auf einem ausgewählten benannten Ziel basiert, wählen Sie **Kopieren** auf der Seite **Benanntes Ziel für elektronisches Reporting**. Das neue Ziel hat den gleichen Namen wie das ausgewählte benannte Ziel, aber das Suffix "Kopie" wird hinzugefügt. Sie können diesen Schritt so oft wie nötig wiederholen.

## <a name="security-considerations"></a>Sicherheitsaspekte

Sie können benannte ER-Ziele auf der Seite **Druckverwaltung einrichten** nur festlegen, wenn Sie die [Berechtigung](../sysadmin/role-based-security.md#permissions) haben, diese Aufgabe auszuführen. Die Berechtigung kann Ihnen erteilt werden, wenn die **Ziel für elektronisches Berichtsformat konfigurieren** [Aufgabe](../sysadmin/role-based-security.md#duties) einer Ihrer [Sicherheitsrollen](../sysadmin/role-based-security.md#security-roles) zugewiesen ist. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die elektronische Berichterstellung (EB)](general-electronic-reporting.md)

[Zielorte für elektronische Berichterstellung (ER)](electronic-reporting-destinations.md)

[Änderungen an der Framework-API für elektronische Berichterstellung für Application Update 10.0.17](er-apis-app10-0-17.md)

[Änderungen an der Framework-API für elektronische Berichterstellung für Application Update 10.0.21](er-apis-app10-0-21.md)

[Ändern Sie den Code, damit Benutzer benannte ER-Ziele konfigurieren und verwenden können](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
