---
title: Eine juristische Person vom Typ Tochtergesellschaft für die Konsolidierung einrichten
description: In diesem Thema wird erläutert, wie Sie mit Kontenplänen für Konsolidierungsunternehmen arbeiten.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 44bd184514b24a816cc83f6b0070a5e08163921b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204808"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Eine juristische Person vom Typ Tochtergesellschaft für die Konsolidierung einrichten

[!include [banner](../includes/banner.md)]

Die Methode, die Sie verwenden, um Konten von Tochtergesellschaften für die Konsolidierung vorzubereiten, ist zum Teil davon abhängig, inwieweit die Struktur des Kontenplans in der juristischen Personen der Tochtergesellschaft den Kontenplan in der konsolidierten juristischen Person widerspiegelt.

Führen Sie vor dem Beginn einer Konsolidierung am Periodenabschluss die Schritte für die Vorbereitung des Periodenabschlusses aus. Warten Sie jedoch mit dem Kontenabschluss für die Tochtergesellschaft, bis die Konsolidierung abgeschlossen ist. Weitere Informationen zum Periodenabschluss erhalten Sie unter [Abschluss des Hauptbuchs am Ende der Periode](close-general-ledger-at-period-end.md) und [Geschäftsjahr abschließen](tasks/close-fiscal-year.md).

> [!NOTE]
>  Wir empfehlen die Verwendung vom Management Reporter für Microsoft Dynamics 365 Finance, um die Finanzergebnisse mehrerer juristischer Personen in einem konsolidierten Format zu kombinieren. Mithilfe vom Management Reporter können Sie konsolidierte Finanzberichte für alle juristischen Personen erstellen, mithilfe von Excel Konsolidierungsdaten aus anderen Quellen importieren und Beträge in eine beliebige Anzahl von Berichtswährungen umrechnen, ohne den Konsolidierungsprozess in Dynamics 365 Finance ausführen zu müssen.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Hauptkonten der Tochtergesellschaft konsolidierten Hauptkonten zuordnen

Wenn der Kontenplan in der juristischen Personen der Tochtergesellschaft nicht dem Kontenplan in der konsolidierten juristischen Person entspricht, können Sie die Hauptkonten in der Tochtergesellschaft den Hauptkonten in der konsolidierten juristischen Person zuordnen.

1. Rufen Sie in der *juristischen Person der Tochtergesellschaft* **Hauptbuch \> Einrichtung** \> **Kontenplan \> Kontenplan** auf.
2. Wählen Sie einen Kontenplan aus. Wählen Sie im Inforegister **Hauptkonten** ein Hauptkonto und anschließend **Bearbeiten** aus.
3. Wählen Sie die einzelnen Hauptkonten der Tochtergesellschaft aus, die einem konsolidierten Hauptkonto zugeordnet werden müssen. Geben Sie im Inforegister **Allgemein** im Feld **Konsolidierungskonto** das Konto in der konsolidierten juristischen Person ein, auf das der Saldo oder die Buchungen des ausgewählten Hauptkontos der Tochtergesellschaft übertragen werden müssen. Sie können dasselbe konsolidierte Hauptkonto für verschiedene Tochtergesellschaftskonten verwenden.

    > [!NOTE]
    > Wenn sich die Hauptkontotypen der Tochtergesellschaftskonten, die zugeordnet werden, von den Hauptkontotypen der Konten in der konsolidierten juristischen Person unterscheiden, werden die Werte von Konten, die den Hauptkontotyp **Gesamt** haben, während der Konsolidierung überschrieben.

4. Erstellen Sie auf Finanzdimensionen basierende Berichte und Finanzaufstellungen für die konsolidierte juristische Person. Führen Sie die folgenden Schritte aus, um die in den Tochtergesellschaftskonten verwendeten Finanzdimensionen den Finanzdimensionen in der konsolidierten juristischen Person zuzuordnen:

    1. Rufen Sie in der *juristischen Person der Tochtergesellschaft* **Hauptbuch \> Einrichtung \> Finanzdimensionen \> Finanzdimensionen** auf. Wählen Sie eine Finanzdimension und anschließend **Finanzdimensionswerte** aus.
    2. Wählen Sie den Finanzdimensionswert aus, der einem anderen Finanzdimensionswert in der konsolidierten juristischen Person zugeordnet werden soll.
    3. Geben Sie im Inforegister **Allgemein** im Feld **Gruppendimension** die Finanzdimension in der konsolidierten juristischen Person ein. Während der Konsolidierung wird diese Finanzdimension den Buchungen und Salden zugewiesen, die die ausgewählte Finanzdimension in der juristischen Personen der Tochtergesellschaft verwenden. Die Finanzdimensionen, die Sie hier eingeben, müssen in der konsolidierten juristischen Person verwendet werden. Sie können die Finanzdimension zuweisen, die als Gruppenfinanzdimension für mehrere Finanzdimensionen der Tochtergesellschaft verwendet wird.

5. Wenn Sie eine Online-Konsolidierung durchführen, führen Sie die folgenden Schritte aus, um sicherzustellen, dass die Übertragungen wie beabsichtigt erfolgen:

    1. Rufen Sie in der *konsolidierte juristischen Person* **Hauptbuch \> Periodisch \> Konsolidieren \> Konsolidieren \[Exportieren nach\]** auf, um die Seite **Konsolidieren \[Online\]** zu öffnen.
    2. Aktivieren Sie auf der Registerkarte **Kriterien** das Kontrollkästchen **Konsolidierungskonto verwenden**.
    3. Wählen Sie auf der Registerkarte **Finanzdimensionen** die entsprechenden Finanzdimensionen aus.
    4. Geben Sie für jede Finanzdimension, die Sie auswählen, eine Zahl in das Feld **Segmentreihenfolge** ein, um die Reihenfolge festzulegen, in der die Dimensionen angezeigt werden sollen.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Denselben Kontenplan in der Tochtergesellschaft und in der konsolidierten juristischen Personen pflegen

Die Hauptkonten in der juristischen Personen der Tochtergesellschaft verfügen möglicherweise über die gleichen Kontonummern und die gleiche Struktur für den Kontenplan wie die Hauptkonten in der konsolidierten juristischen Person. In diesem Fall müssen Sie die Hauptkonten in der Tochtergesellschaft den Hauptkonten in der konsolidierten juristischen Person nicht manuell zuordnen.

Führen Sie die folgenden Schritte aus, bevor Sie mit der Konsolidierung beginnen.

1. Rufen Sie in der *konsolidierte juristischen Person* **Hauptbuch \> Periodisch \> Konsolidieren \> Konsolidieren \[Exportieren nach\]** auf, um die Seite **Konsolidieren \[Online\]** zu öffnen.
2. Aktivieren Sie das Kontrollkästchen **Konsolidierungskonto verwenden**. Während der Konsolidierung werden Buchungen und Salden automatisch an das korrekte Konto übertragen.

> [!NOTE]
> Sollten die Konten nicht übereinstimmen, wird die Konsolidierung angehalten und eine entsprechende Meldung angezeigt.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Einen Kontenplan für die konsolidierte juristische Person auf Basis eines vorhandenen Kontenplans erstellen

Sie können eine Konsolidierung durchführen, auch wenn in der konsolidierten juristischen Person noch kein Kontenplan erstellt wurde.

- Wenn Sie die Kontostruktur, die in der konsolidierten juristischen Person verwendet werden soll, geplant haben, können Sie die Konten der Tochtergesellschaft dieser Struktur zuordnen.
- Wenn Sie keine Tochtergesellschaftskonten zuordnen, werden die Konten in der konsolidierten juristischen Person automatisch erstellt, wenn die Daten der Tochtergesellschaft an die konsolidierte juristische Person übertragen werden. Diese Konten basieren auf dem Hauptkonto. Weitere Daten werden in Konten in der konsolidierten juristischen Person kumuliert, die dieselbe Kontonummer wie die Tochtergesellschaftskonten haben.

Unabhängig davon, ob Sie Konten zugeordnet haben, müssen Sie das Kontrollkästchen **Konsolidierungskonto** auf der Seite **Konsolidieren** in der konsolidierten juristischen Person deaktivieren, bevor Sie diese Art der Konsolidierung ausführen.

> [!NOTE]
> Mithilfe dieser Methode können Sie im konsolidierten Unternehmen einen Kontenplan erstellen, der auf dem Kontenplan einer der Tochtergesellschaften basiert. (Weitere Informationen finden Sie unter [Konsolidierungskontengruppen und zusätzliche Konsolidierungskonten](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Weisen Sie dann jedem konsolidierten Hauptkonto ein geeignetes Prinzip für die Konsolidierungskonvertierung zu, und führen Sie die Konsolidierung für alle juristischen Personen der Tochtergesellschaft aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]