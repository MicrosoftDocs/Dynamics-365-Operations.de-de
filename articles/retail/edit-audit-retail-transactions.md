---
title: Transaktionen im Einzelhandel bearbeiten und prüfen
description: In diesem Thema wird die Funktionalität zur Bearbeitung und Prüfung von Transaktionen im Einzelhandel beschrieben.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: f53573b8afb2003f6796930f5877185e533a4715
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693065"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Transaktionen im Einzelhandel bearbeiten und prüfen

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Dynamics 365 Retail-Kunden nutzen sowohl POS-Anwendungen (Point of Sale) von Microsoft als auch von Drittanbietern. Mit der POS-Anwendung von Microsoft werden Einzelhandelstransaktionen über einen Stapelverarbeitungsprozess aus den Kanälen in Retail Headquarters geholt. Bei Anwendungen von Drittanbietern werden Transaktionen über die Integration in Retail Headquarters geholt. In beiden Fällen muss nach dem Abruf von Transaktionen in Retail Headquarters ein Konsistenzprüfungsprozess durchgeführt werden, der mehrere Prüfungen für die Transaktionen durchführt, sodass nur erfolgreich geprüfte Transaktionen in die in Retail Headquarters zu buchende Aufstellung übernommen werden. 

Die Prüfung von Einzelhandelstransaktionen kann aus verschiedenen Gründen scheitern. So kann beispielsweise ein Fehler im Integrationscode oder ein Fehler in der POS-Anwendung zu inkonsistenten Daten führen, oder ein Benutzerfehler (z. B. das Löschen eines Produkts nach der Synchronisation mit dem Kanal oder das Schließen eines Finanzzeitraums ohne Buchung von Einzelhandelsgeschäften für diese Periode) kann zu inkonsistenten Daten führen.

Zwar werden diese Transaktionen markiert und von den Auszügen ausgeschlossen, sie können jedoch den laufenden Prozess der täglichen Buchung von Einzelhandelsumsätzen im Rechnungswesen eines Kunden stören.

In Retail können Sie die Einzelhandelstransaktionen bearbeiten, die die Prüfung nicht bestehen. Gleichzeitig werden alle Änderungen geprüft. 

## <a name="edit-and-audit-transactions"></a>Bearbeiten und Überprüfen von Transaktionen

In der Retail-Version 10.0.5 sind Abholungstransaktionen wie Verkäufe und Rückgaben die einzigen Transaktionen, die bearbeitet werden können. Die Bearbeitung von Kundenaufträgen oder Onlinebestellungen wird nicht unterstützt. Ab Retail-Version 10.0.6 wird auch die Bearbeitung von Bargeldverwaltungstransaktionen unterstützt.

1. Installieren Sie das Dynamics Excel-Add-in.

2. Wechseln Sie zum Arbeitsbereich **Finanzdaten für den Einzelhandelsshop**. Das Feld **Transaktionsüberprüfungsfehler** bietet eine vorgefilterte Ansicht der Einzelhandelstransaktionsform, die eine oder mehrere der Überprüfungsregeln nicht bestanden hat.
 
3. Öffnen Sie das Formular. Klicken Sie auf den Datensatz, der die Überprüfung nicht bestanden hat, klicken Sie auf **Office-Add-in**, und klicken Sie dann auf **Ausgewählte Transaktion bearbeiten**. Eine Excel-Datei mit den Daten der ausgewählten Transaktion mit den folgenden Arbeitsblättern wird geöffnet:

    - Positionen: Dieses Arbeitsblatt enthält den Kopf, die Produktpositionen und die Daten der Transaktion.
    - Zahlungen: Dieses Arbeitsblatt enthält die Daten der Zahlungspositionen für die Transaktion.
    - Rabatte: Dieses Arbeitsblatt enthält die rabattbezogenen Daten zur Transaktion.
    - Steuern: Dieses Arbeitsblatt enthält die steuerlichen Daten für die Transaktion.
    - Gebühren: Dieses Arbeitsblatt enthält die kostenbezogenen Daten für die Transaktion.

4. Andern Sie die entsprechenden Felder in der Excel-Datei, und laden Sie die Daten dann mit Hilfe der Veröffentlichungsfunktion des Dynamics Excel-Add-ins wieder in Retail Headquarters hoch. Nach der Veröffentlichung werden die Änderungen im System berücksichtigt. Während der Veröffentlichung wird keine Überprüfung der von den Benutzern vorgenommenen Änderungen durchgeführt.

5. Ein vollständiges Protokoll der Änderungen kann eingesehen werden, indem Sie auf **Audit-Trail anzeigen** im **Einzelhandelstransaktion**-Kopf (Änderungen auf Kopfebene) oder in den entsprechenden Abschnitt und Datensatz klicken. Beispielsweise werden alle Änderungen, die sich auf Verkaufspositionen beziehen, auf der Seite **Verkaufstransaktionen** angezeigt. Änderungen, die sich auf Zahlungen beziehen, werden auf der Seite **Zahlungstransaktionen** angezeigt usw. Die Auditdaten, die für die Änderungen gepflegt werden, lauten wie folgt.

   - Änderungsdatum und -uhrzeit
   - Feld 
   - Alter Wert
   - Neuer Wert
   - Geändert von

6. Nachdem Ihre Änderungen vorgenommen und veröffentlicht wurden, führen Sie die Option **Geschäftsbuchungen überprüfen** erneut aus, um die Konsistenz und Gültigkeit der von Ihnen vorgenommenen Änderungen zu überprüfen.

> [!NOTE]
> Sie können nur Transaktionen bearbeiten, bei denen die Prüfung fehlgeschlagen ist. Wenn Sie Transaktionen bearbeiten möchten, die die Prüfung bestanden haben, ändern Sie den Überprüfungsstatus der Transaktion, die Sie ändern möchten, auf **Fehler** oder **Keine**. Dann können Sie sie bearbeiten. 


## <a name="bulk-edit-transactions"></a>Massenbearbeitung von Transaktionen

Ab Retail-Version 10.0.6 wird die Möglichkeit der Massenbearbeitung von Einzelhandelstransaktionen auf Aufstellungsebene unterstützt. 

1. Verwenden Sie das Excel-Add-in, um eine Aufstellung zu öffnen, die Transaktionen enthält, die Sie mit den Schritten 1-3 oben ändern möchten.

2. Wählen Sie eine der folgenden Alternativen aus.

    - **Abholungstransaktionen bearbeiten**. Mit dieser Option können Sie alle in der Aufstellung enthaltenen Abholungstransaktionen bearbeiten. Folgende Excel-Arbeitsblätter sind verfügbar.
    
       - **Transaktion**: Dieses Arbeitsblatt enthält alle Informationen auf Kopfebene für die Verkaufstransaktionen.
       - **Verkaufstransaktion**: Dieses Arbeitsblatt enthält alle Informationen auf Positionsebene für die Verkaufstransaktionen.
       - **Zahlungstransaktionen**: Dieses Arbeitsblatt enthält alle Zahlungspositionsinformationen für die Verkaufstransaktionen.
       - **Rabatttransaktionen**: Dieses Arbeitsblatt enthält alle Informationen zu den Rabattpositionen für die Verkaufstransaktionen.
       - **Steuertransaktionen**: Dieses Arbeitsblatt enthält alle Steuerpositionsinformationen für die Verkaufstransaktionen.
       - **Gebührentransaktionen**: Dieses Arbeitsblatt enthält alle Gebührenpositionsinformationen für die Verkaufstransaktionen.

    - **Bargeldverwaltungstransaktionen bearbeiten**. Mit dieser Option können Sie alle in der Aufstellung enthaltenen Bargeldverwaltungstransaktionen bearbeiten. Folgende Excel-Arbeitsblätter sind verfügbar.
     
       - **Transaktion**: Dieses Arbeitsblatt enthält alle Informationen auf Kopfebene für die Bargeldverwaltungstransaktionen.
       - **Bankzahlungsmitteltransaktionen**: Dieses Arbeitsblatt enthält alle Informationen zu den Bankzahlungsmitteltransaktionen.
       - **Sichere Bankeinzahlungstransaktionen**: Dieses Arbeitsblatt enthält alle Informationen zu sicheren Bankeinzahlungstransaktionen.
       - **Bankzahlungsmitteldeklaration**: Dieses Arbeitsblatt enthält alle Informationen zu Bankzahlungsmitteldeklaration-Transaktionen.
       - **Einnahmen/Ausgaben-Transaktionen**: Dieses Arbeitsblatt enthält alle Informationen zu Einnahmen/Ausgaben-Transaktionen.
       - **Zahlungstransaktionen**: In diesem Arbeitsblatt finden Sie alle zahlungsrelevanten Informationen für den **Rechnungszahlung**-Vorgang sowie die Einnahmen-Ausgaben-Transaktion.

3.  Wenn Sie massenbearbeitete Transaktionen veröffentlichen, werden keine Prüfungen durchgeführt. Sie müssen sicherstellen, dass Ihre Bearbeitungen korrekt sind und die Datengenauigkeit in den Arbeitsblättern erhalten bleibt. Wenn Sie beispielsweise für Szenarien, in denen der Finanzzeitraum oder die Lagerbuchungsperiode für die offenen Einzelhandelstransaktion abgeschlossen ist, das Transaktionsdatum ändern möchten, müssen Sie das Datum in allen Excel-Arbeitsblättern ändern, die die Spalte **Geschäftsdatum** haben. Um Transaktionen nach der Bearbeitung zu prüfen, können Sie **Transaktionen neu prüfen** auf der Seite **Einzelhandelsaufstellungen** verwenden.
