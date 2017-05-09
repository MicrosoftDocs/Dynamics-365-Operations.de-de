---
title: "Einrichten der Optionen für Verarbeitungsoptionen"
description: "Dieses Thema enthält Informationen dazu, wie Aufträge für Callcenter mithilfe Microsoft Dynamics 365 for Operations - Retail verarbeitet werden."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>Einrichten der Optionen für Verarbeitungsoptionen

[!include[banner](includes/banner.md)]


Dieses Thema enthält Informationen dazu, wie Aufträge für Callcenter mithilfe Microsoft Dynamics 365 for Operations - Retail verarbeitet werden. 

Einzelhandel und Handel in Microsoft Dynamics 365 for Operations unterstützt mehrere Einzelhandelskanäle, wie Onlineshops, Callcenter und physische Geschäfte und Callcenter. In Callcentern nehmen Arbeitskräfte Aufträge von Kunden per Telefon entgegen und erstellen Aufträge. In diesem Thema wird beschrieben, wie ein Callcenter erstellt wird und Callcenteroptionen konfiguriert werden. Jedes Callcenter kann eigene Benutzer, Zahlungsmethoden, Preisgruppen, Finanzdimensionen und Lieferarten haben. Sie können diese Optionen konfigurieren, wenn Sie das Callcenter erstellen. **Wichtig:** Bevor die Callcenterworkflows verwendet werden können, wenn der aktuelle Dynamics AX-Benutzer Aufträge erstellt, muss der Benutzer dem Callcenter als Callcenterbenutzer zugewiesen werden. Darüber hinaus können Sie die Seite **Callcenter** verwenden, um Gruppen von Funktionen zu aktivieren oder zu deaktivieren, die für Callcenter eindeutig sind. Die folgenden Gruppen von Funktionen können aktiviert werden:

-   **Auftragsabschluss** – Diese Gruppe umfasst Funktionen, die mit Zahlungen und Auftragsabschluss auf der Seite **Auftrag** verknüpft sind.
-   **Direktverkauf** – Diese Gruppe umfasst Funktionen, die Quellcodes, Skripts und Kataloganforderungen zugeordnet sind.

Wenn Sie diese Funktionen in den Callcentereinstellungen aktivieren, sind sie auf der Seite **Auftrag** für Benutzer verfügbar, die dem Callcenter zugeordnet sind. Die meisten dieser Funktionen erfordern zusätzliche Einstellungen, bevor sie verwendet werden können. Bilder und Skripts werden als Teil der Direktverkaufeinstellung für das betreffende Callcenter aktiviert. Wenn dieses Funktion aktiviert ist, werden die Skripts und die Produktbilder im Infoboxbereich der Seite **Auftrag** angezeigt. Das standardmäßige Bild, das für ein Produkt festgelegt ist, wird angezeigt. Skripts können für einen Artikel, einen Katalog, einen Debitor oder einen Artikel im Kontext eines Katalogs konfiguriert werden. Callcenteraufträge haben die Möglichkeit zum Anzeigen zusätzlicher Details, um aufzuzeigen, wie der Preis für eine bestimmte Auftragsposition berechnet wurde. Beispielsweise zeigt der Auftrag, welche Rabatte angewendet wurden. Sie aktivieren diese Funktionen unter **Debitoren** &gt; **Einstellung** &gt; **Debitorenparameter** &gt; **Preis** &gt; **Preisdetails**. Sie können über die Auswahlliste **Auftragszeile** auf der Seite **Preisdetails** darauf zugreifen. Sie können Auftragsereignisüberwachung für Prüfungszwecke verwenden, um die Aktivitäten zu überprüfen, die für einen Auftrag während des Lebenszyklus des Auftrags durchgeführt werden oder die Aktivitäten eines bestimmten Benutzers zu verfolgen. So können Sie beispielsweise die Aktivität jedes Mal erfassen, wenn ein Benutzer einen Auftrag erstellt, eine Sperre für einen Auftrag erteilt, eine Belastung überschreibt oder eine Auftragsposition aktualisiert. Sie können Auftragsereignisse einrichten, um Aktivitäten für bestimmte Benutzer, Benutzergruppen oder alle Benutzer für einen bestimmten Zeitraum zu verfolgen. Sie können die Aktivitäten anzeigen, die in einem Dokument ausgeführt wurden, indem das Formular **Aufträge** über den Aktivitätsbereich im Formular des jeweiligen Dokuments geöffnet wird. Sie können Auftragsereignisse unter **Vertrieb und Marketing** &gt; **Einstellungen** &gt; **Ereignisse** &gt; **Auftragsereignisse konfigurieren.** Wenn ein Auftrag eines Debitors nicht rechtzeitig versendet werden kann, kann ein Unternehmen automatisch Benachrichtigungs-E-Mails an den Debitor senden, um den Auftragsstatus darzulegen und dem Debitor die Gelegenheit zu bieten, den Auftrag zu stornieren. Wenn die Verzögerung sich über einen angegebenen Schwellenwert hinaus ausdehnt, kann der Auftrag automatisch storniert werden. Bis zu drei E-Mail-Nachrichten können in angegebenen Zeitintervallen gesendet werden:

1.  **Erste Stornierungsbenachrichtigung** – Der Debitor kann den Auftrag stornieren.
2.  **Zweite Stornierungsbenachrichtigung** – Der Debitor kann den Auftrag stornieren.
3.  **Endgültige Stornierungsbenachrichtigung** – Das System storniert den Auftrag, und der Debitor wird über die Stornierung informiert.

Sie können einzelne Debitoren und Produkte von dem automatischen Benachrichtigungs- und Stornierungsprozess befreien. Eine Gewinnspannenwarnung wird ausgelöst, wenn Sie einem Auftrag einen Artikel hinzufügen. Die Warnung enthält wichtige Informationen zum Artikel, einschließlich der Preisspanne und der Artikelrentabilität. Sie können diese Informationen verwenden, um zu entscheiden, ob eine Preisüberschreibung angemessen ist, wenn Sie dem Auftrag einen Artikel hinzufügen. Beispielsweise können Sie Schwellenwerte für Gewinnspannen einrichten, um anzugeben, dass ein Schwellenwert von 40 Prozent oder mehr über den Kosten für einen Artikel akzeptabel aber ein Schwellenwert von 20 bis 39 Prozent über den Kosten fragwürdig ist. In diesem Fall löst jeder Artikel, der einen Schwellenwert zwischen 20 und 39 Prozent hat, eine Warnung aus. Artikel, die einen Schwellenwert unter 20 Prozent über Kosten aufweisen, können nicht verkauft und der Artikelpreis nicht geändert werden. Sie können Gewinnspannenwarnungen unter **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter** &gt; **Gewinnspannenwarnungen konfigurieren**. Wenn Sie die Mehrwertsteuerzuweisung basierend auf den Standardregeln einrichten, können Sie eine entsprechende Priorität für Adressenelemente bestimmen. Beispielsweise können Sie angeben, dass die Zuordnung einer Mehrwertsteuergruppe nach Postleitzahl eine höhere Priorität hat als die Zuordnung einer Mehrwertsteuergruppe nach Status. Wenn Sie neue Debitorenadressedatensätze eingeben, wird die Mehrwertsteuergruppe automatisch zugeordnet, basierend auf Adressenentsprechungen des Debitors mit den standardmäßigen Regeln und der Prioritätszuordnung, die Sie definiert haben. Sie können diese Funktionen auf der Seite **Hauptbuchparameter** konfigurieren.




