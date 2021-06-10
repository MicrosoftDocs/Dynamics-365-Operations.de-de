---
title: Gleitzeitgruppen
description: In diesem Thema wird beschrieben, wie Gleitzeitgruppen in Zeit und Anwesenheit verwendet werden.
author: johanhoffmann
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgFlexGroup, JmgFlexCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7628f2fc3d3a7e5bb1175edf59f856bc40f9b987
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102829"
---
# <a name="flex-groups"></a>Gleitzeitgruppen

[!include[banner](../includes/banner.md)]

Flexible Arbeitsstunden lassen Unternehmen Zahlungen für Überstunden minimieren, indem sie Arbeitskräften Verlängerungen für die Perioden anbieten, wenn die Arbeitsauslastung gering ist. Diese Funktion ist beispielsweise in den Segmenten relevant, die Saisonänderungen in der Arbeitslast ermitteln.

Gleitzeitgruppen können Sie verwenden, um die folgenden Regeln und die Prinzipien für den Gleitzeitsaldo einer Arbeitskraft festzulegen:

- Regeln für Gleitzeitbestimmungen
- Prinzip für das Berechnen des Gleitzeitsaldos der Arbeitskraft

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Flexible Arbeitsstunden der Einstellung in den Gleitzeitgruppen

- Wählen Sie **Zeit und Anwesenheit** \> **Einstellungen** \> **Gruppen** \> **Gleitzeitgruppen**, um  Gleitzeiten für Gleitzeitgruppen einzurichten.

## <a name="associate-workers-with-flex-groups"></a>Weisen Sie Arbeitskräfte zu mit Gleitzeitgruppen

- Wählen Sie **Zeit und Anwesenheit** \> **Einstellungen** \> **Zeiterfassung für Arbeitskräfte**.

## <a name="rules-for-flex-regulations"></a>Regeln für Gleitzeitbestimmungen

Sie können Regeln verwenden, damit Gleitzeitbestimmungen oder Gleitzeitlimiten oder die minimale und maximale Anzahl von Stunden definieren, die im Gleitzeitkonto der Arbeitskraft zulässig sind. Die Gleitzeitgrenze wird für die Gleitzeitgruppe eingerichtet. Wenn die Gleitzeitlimite überschritten werden, können Gleitzeitsaldo und Vergütung einer Arbeitskraft angepasst werden.

Wenn das Gleitzeitminimum einer Arbeitskraft überschritten wird (das heißt, wenn die Anzahl der Stunden im Gleitzeitkonto kleiner ist als das angegebene Minimum), können Sie diese Methoden nutzen, um den Gleitzeitsaldo der Arbeitskraft zu regulieren, indem Sie eine Gleitzeitbestimmung treffen:

- Die Gleitzeitrechnung der Arbeitskraft kann ausgeglichen werden auf das angegebene zulässige Minimum, aber ohne den Lohn der Arbeitskraft für die Anzahl von Stunden abzuziehen, die unter dem zulässigen Minimum liegen.
- Der Lohn der Arbeitskraft kann für die Stundenzahl abgezogen werden, die unter dem zulässigen Minimum im Gleitzeitkonto liegt. Dieser Abzug wird ausgeführt, indem Lohnelemente für eine bestimmte Lohnart generiert werden, die eine positive oder negative Lohneinheit haben.

Wenn die zulässige maximale Gleitzeit einer Arbeitskraft überschritten wird, können Sie diese Methoden nutzen, um den Gleitzeitsaldo der Arbeitskraft zu regulieren, indem Sie eine Gleitzeitbestimmung treffen:

- Die Gleitzeitrechnung der Arbeitskraft kann auf das angegebene zulässige Maximum zurückgesetzt werden, aber ohne den Lohn der Arbeitskraft für die Anzahl von Stunden zu kompensieren, die über dem zulässigen Maximum liegen.
- Die Anzahl der Stunden, die die Arbeitskraft über dem erlaubten Maximum gearbeitet hat, kann in eine Bezahlung konvertiert werden. Diese Konvertierung wird ausgeführt, indem Lohnelemente für eine bestimmte Lohnart generiert werden.

Sie können zum Anpassen der Gleitzeitsalden auch  folgende Zeiten auswählen:

- Wenn eine Zahlungsdatei, die auf den Lohndaten basiert, exportiert wird, indem Sie den **Übergangslohn** verwendet. Die Lohndaten, die generiert werden, wenn Sie die Anmeldung der Arbeitskraft von der Seite **Genehmigen** übertragen.
- Wenn der **Gleitzeitsaldo anpassen** Einzelvorgang verarbeitet wird.

> [!NOTE]
> Gleitzeitbestimmungen treten erst für die tägliche Genehmigung und Übertragung von Erfassungen auf der Seite **Genehmigen** auf.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Prinzip für das Berechnen des Gleitzeitsaldos der Arbeitskraft

Das Prinzip für die Stunden, dass der Gleitzeitsaldo der Arbeitskraft beendet reguliert werden, wird im eingerichtet der Gleitzeitgruppe. Wählen Sie **Zeit und Anwesenheit** \> **Einstellungen** \> **Gruppen** \> **Gleitzeitgruppen** aus. 

Folgende zwei Prinzipien stehen zur Verfügung:

- **Zeit** – Die Gleitzeitstunden der Arbeitskraft werden von der erfassten Zeit für den Tag berechnet. Bei der täglichen Erfassungen durch die Arbeitskraft wird die Anzahl der Flex+- und Flexstunden für den Tag von den Flex+- und Flexzonen berechnet, die im Zeitprofil der Arbeitskraft definiert werden.
- **Lohnarten** – Der Gleitzeitsaldo der Arbeitskraft wird auf Grundlage der Einnahmen der Lohnart für Gleitzeit+ " berechnet, die in der Lohnvereinbarung der Arbeitskraft definiert werden. Die Lohnvereinbarung wird der Zeiterfassung zugeordnet. Sie müssen Lohnarten verwenden, um Gleitzeitkonten zu verwalten, wenn Sie z. B. das Gleitzeitkonto für eine Arbeitskraft über einen bestimmten Faktor in mindestens einer Gleitzeitzonen erhöhen möchten.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Szenario 1: Anpassen des Lohns und des Gleitzeitkontos einer Arbeitskraft, weil das zulässige Gleitzeitminimum überschritten wurde

Eine Arbeitskraft, die in Gleitzeit arbeiten kann, hat ein negatives Gleitzeitkonto.

- **Gleitzeitkonto:** -4

Die Arbeitskraft ist mit einer Gleitzeitgruppe verknüpft, die die folgende Unternehmenskonfiguration hat:

- **Gleitzeit-Minimum** -0.5
- **Mindestlohnart** 1302
- **Lohnartfaktor** -1.00

Während die Differenz zwischen dem Gleitzeitkonto der Arbeitskraft und dem Gleitzeitminimum angibt, hat die Arbeitskraft die zulässige Gleitzeitminimum mit 3,5 Stunden überschritten.

Wenn der Lohnadministrator die Lohndaten der Arbeitskraft überträgt, indem er den **Zur Lohnabrechnung übertragen** oder Einzelvorgang **Gleitzeitregulierung** nutzt, werden folgende Korrekturen vorgenommen:

- Die Gleitzeitrechnung der Arbeitskraft wird durch 3,5 Stunden ausgeglichen. Daher wird der Gleitzeitsaldo von -4,0 Stunden im zulässigen Gleitzeitminimum von -0,5 Stunden für die Arbeitskraft zulässig.
- Eine Lohnartikel für Lohnart 1302 wird erstellt. Diese Zahlung weist auf eine Lohneinheit von -3,5 Stunden, die vom Lohn der Arbeitskraft abgezogen werden. In diesem Fall ist die Lohneinheit eine negative Zahl, da die positive Regulierung von 3,5 Stunden mit dem negativen Lohnartfaktor von -1,0 multipliziert wird, der auf der Gleitzeitgruppe definiert wird. Dieser Zahlung ist ein Teil der Lohndatei, die vom Einzelvorgang **Zur Lohnabrechnung übertragen** erstellt wird.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Szenario 2: Anpassen des Lohns und des Gleitzeitkontos einer Arbeitskraft, weil das zulässige Gleitzeitmaximum überschritten wurde

Eine Arbeitskraft, die in Gleitzeit arbeiten kann, hat ein positives Gleitzeitkonto.

- **Gleitzeitkonto:** -6

Die Arbeitskraft ist mit einer Gleitzeitgruppe verknüpft, die die folgende Unternehmenskonfiguration hat:

- **Gleitzeit-Maximum** 2,0
- **Mindestlohnart** 1302
- **Lohnartfaktor** -1,0

Während die Differenz zwischen dem Gleitzeitkonto der Arbeitskraft und dem Gleitzeitmaximum angibt, hat die Arbeitskraft die zulässige Gleitzeitmaximum mit 4,0 Stunden überschritten.

Wenn der Lohnadministrator die Lohndaten der Arbeitskraft überträgt, indem er den **Zur Lohnabrechnung übertragen** oder Einzelvorgang **Gleitzeitregulierung** nutzt, werden folgende Korrekturen vorgenommen:

- Die Gleitzeitrechnung der Arbeitskraft wird durch 4,0 Stunden ausgeglichen. Daher wird der Gleitzeitsaldo von 6,0 Stunden im zulässigen Gleitzeitmaximum von 2,0 Stunden für die Arbeitskraft zulässig.
- Eine Lohnartikel für Lohnart 1302 wird erstellt. Diese Zahlung weist auf eine Lohneinheit von 4,0 Stunden hin, die dem Lohn der Arbeitskraft hinzugefügt wird. In diesem Fall ist die Lohneinheit eine positive Zahl, da die positive Regulierung von 4,0 Stunden mit dem positiven Lohnartfaktor von -1,0 multipliziert wird, der in der Gleitzeitgruppe definiert wird. Dieser Zahlung ist ein Teil der Lohndatei, die vom Einzelvorgang **Zur Lohnabrechnung übertragen** erstellt wird.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Szenario 3: Verwaltung des Gleitzeitsaldos einer Arbeitskraft basierend auf Lohnarten

Wie wir früher bereits erklärten, können Gleitzeitkonten verwaltet werden basierend entweder auf der Zeit, die in den Flex+- und Flexzonen erfasst werden, in denen das Zeitprofil der Arbeitskraft definiert ist oder auf den Lohnarten, die in Lohnvereinbarungen der Arbeitskraft definiert werden. Wenn Lohnart verwendet werden, wird die Gleitzeitrechnung einer Arbeitskraft nach den Lohnelementen ausgeglichen, die generiert werden, wenn Sie die Erfassung der Arbeitskraft von der Seite **Genehmigen** übertragen. Sie müssen Lohnarten verwenden, um Gleitzeitkonten zu verwalten, wenn Sie z. B. das Gleitzeitkonto für eine Arbeitskraft über einen bestimmten Faktor in mindestens einer Gleitzeitzonen erhöhen möchten.

Das Szenario nutzt das folgende Flex-Profil für den Arbeitstag.

| Profiltyp  | Start    | Beenden      |
|---------------|----------|----------|
| Gleitzeit+         | 12:00 (vormittags) | 08:00 (vormittags) |
| Einstempeln      | 08:00 (vormittags) | 08:00 (vormittags) |
| Gleitzeit-         | 08:00 (vormittags) | 09:00 (vormittags) |
| Standardzeit | 09:00 (vormittags) | 11:30 (vormittags) |
| Entlohnte Pause    | 11:30 (vormittags) | 12:00 (nachmittags) |
| Gleitzeit-         | 12:00 (nachmittags) | 04:00 (nachmittags) |
| Ausstempeln     | 04:00 (nachmittags) | 04:00 (nachmittags) |
| Gleitzeit+         | 04:00 (nachmittags) | 12:00 (vormittags) |

In diesem Fall sollten Sie in der Lage sein, den Gleitzeitsaldo basierend auf den Lohnarten der Arbeitskraft zu verwalten. Daher müssen Sie die Option **Basierend auf Lohnarten** auf **Ja** setzen in der Gleitzeitgruppe der Arbeitskraft.

Um die Gleitzeit zu berücksichtigen, müssen Sie auch eine Lohnart definieren. Für dieses Szenario wird die Lohnart **FlexCnt** lauten.

| Lohnart | Beschreibung  |
|----------|--------------|
| FlexCnt  | Gleitzeitzähler |

Danach gehen Sie folgendermaßen vor, um eine Lohnarten einzurichten und Positionen des neuen Typs einem Lohnprofil hinzuzufügen.

1. Wählen Sie **Zeit und Anwesenheit** \> **Einstellungen** \> **Gruppen** \> **Gleitzeitgruppen** aus und wählen Sie dann **Neu**.
2. Wählen Sie im Feld **Gleitzeit+** und im Feld **Gleitzeit-** die neue Lohnart **FlexCnt** aus.
3. Wählen Sie **Zeit und Anwesenheit** \> **Einstellungen** \> **Lohnvereinbarungen**, und wählen Sie dann **Vereinbarungspositionen** aus.
4. Für **Montag** für den Profiltyp **Gleitzeit+**, fügen Sie die folgenden drei Positionen hinzu.

    | Lohnart | Beschreibung  | Von Uhrzeit | Bis Uhrzeit  | Minimum | Maximum | Faktor |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Gleitzeitzähler | 12:00 (vormittags)  | 06:00 (nachmittags) | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Gleitzeitzähler | 06:00 (nachmittags)  | 12:00 (vormittags) | 00,00   | 02,00   | 1.50   |
    | FlexCnt  | Gleitzeitzähler | 06:00 (nachmittags)  | 12:00 (vormittags) | 02,00   | 06,00   | 2.00   |

    > [!NOTE]
    > Jede Position wird für ein Intervall der verschiedenen Zeitfenster verwendet und hat einen anderen Faktor. Die Gleitzeitstunden, die die Arbeitskraft in einem Zeitintervall arbeitet, werdem mit den Faktor für diese Position multipliziert. Beispielsweise werden Stunden, die von 06:00 Uhr bis 08:00 Uhr gearbeitet werden mit 1,50 multipliziert. Der Faktor wird im Feld **Faktor** auf der Registerkarte **Allgemeines** der Seite **Lohnvereinbarungspositionen** angezeigt.

Die Arbeitskraft gibt die folgenden Erfassungen für den Tag ein.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 07:00 (vormittags) | 07:00 (vormittags) |
| Produktionseinzelvorgang            | 07:00 (vormittags) | 09:00 (nachmittags) |
| Ausstempeln                 | 09:00 (nachmittags) | 09:00 (nachmittags) |

Der Betrag, der gezahlt werden muss, wird auf der Seite **Genehmigen** basierend auf der Erfassung der Arbeitskraft berechnet. Nachdem die Erfassung berechnet wurde, können Sie die Auswirkung auf der Registerkarte **Zeiten** anzeigen. Für dieses Szenario sind Sie an folgenden Feldern interessiert.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

Der Betrag von Flex+-Zeit beträgt sechs Stunden, und die Berechnung basiert auf den Gleitzeitzonen im Zeitprofil. Dieser Betrag besteht aus einer Stunden aus Flex+-Zeit von 07:00 bis 08:00 und bis zu fünf Stunden Flex+-Zeit von 04:00 Uhr bis 09:00 Uhr.

Wenn Sie die Erfassungen übertragen, sollten Sie daran denken, dass der Betrag von Flex+-Zeit von 6,0 Stunden auf 8,0 Stunden geändert wird.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Diese Änderung erfolgt nach der Übertragung, da der Gleitzeitsaldo basierend auf Lohnarten anstelle der Zeit berechnet wurde. Die folgende Tabelle zeigt, wie die acht Stunden berechnet werden.

| Von     | Nach       | Zeit | Faktor    | Gleitzeitkonto |
|----------|----------|------|-----------|--------------|
| 07:00 (vormittags) | 08:00 (vormittags) | 1    | 1         | 1            |
| 04:00 (nachmittags) | 06:00 (nachmittags) | 2    | 1         | 2            |
| 06:00 (nachmittags) | 08:00 (nachmittags) | 2    | 1.5       | 3            |
| 08:00 (nachmittags) | 09:00 (nachmittags) | 1    | 2         | 2            |
|          |          |      | **Summe** | **8**        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]