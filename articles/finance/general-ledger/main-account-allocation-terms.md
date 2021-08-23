---
title: Zuweisungsbedingungen
description: Dieses Thema enthält Informationen zur Verwendung von Zuweisungsbedingungen für ein Hauptkonto.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 957baba1364fbbd4a51c6f51b0fad5bf8db46680fa97b9d3d0474dc015064609
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776527"
---
# <a name="allocation-terms"></a>Zuweisungsbedingungen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur Verwendung von Zuweisungsbedingungen für ein Hauptkonto. Zuweisungsbedingungen werden verwendet, um Beträge auf mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.

Jede Zuweisungsbedingung, die Sie auf einem Hauptkonto erstellen, legt den Prozentsatz eines Gutscheins, der von einem Hauptkonto aus einer einzigen Quelle zugewiesen werden soll, und eine Kombination aus Finanzdimensionen fest. Darüber hinaus definieren Sie das Zielhauptkonto und die Finanzdimensionen, denen der Betrag zugewiesen wird. 

Wenn Sie die ursprüngliche Finanzdimension für die Zuweisung festlegen, können Sie bei jeder Dimension auswählen, ob sie spezifisch oder unspezifisch ist. Spezifisch bedeutet, dass die Finanzdimension für die ursprüngliche Buchung mit der ausgewählten Dimension übereinstimmen muss. Wenn Sie unspezifisch auswählen, bedeutet dies, dass jeder Wert der Finanzdimension zu einer Übereinstimmung zählen kann.

Wenn Sie das Zielsachkonto für eine Zuweisungsbedingung festlegen, müssen Sie das Hauptkonto angeben, dem Sie den Betrag zuordnen. Sie können dasselbe Hauptkonto verwenden, auf das die ursprüngliche Buchung gebucht wurde, oder ein anderes Hauptkonto. Wenn dasselbe Hauptkonto verwendet wird, wird beim Speichern des Datensatzes eine Warnung angezeigt. Neben dem Hauptkonto müssen Sie auch die Zieldimensionen angeben. Sie können für jede Dimension angeben, ob Sie den Wert der ursprünglichen Finanzdimension beibehalten oder ändern möchten. Wenn Sie „Nein“ auswählen, müssen Sie einen neuen Wert für die Finanzdimension auswählen. Wenn Sie „Ja“ auswählen, werden keine zusätzlichen Informationen angegeben und das System behält beim Buchen die ursprünglichen Finanzdimensionen bei.

Die Anzahl der Zuweisungsbedingungen, die Sie einem Hauptkonto hinzufügen können, ist unbegrenzt. Die Summe der Prozentsätze, die in einer Zuweisungsbedingung zulässig sind, darf jedoch 100 nicht überschreiten. Sie können Zuweisungen für weniger als 100 % erstellen, wenn ein Teil des ursprünglichen Gutscheinbetrags in den ursprünglichen Finanzdimensionen verbleiben soll. Zuweisungsbedingungen können einem Hauptkonto einer juristischen Persona als Außerkraftsetzung hinzugefügt werden. Wenn Sie einen gemeinsamen Kontenplan verwenden, müssen für jede juristische Person Zuweisungsbedingung festgelegt werden. Um auf die Schaltfläche **Zuweisungsbedingung** zuzugreifen, müssen Sie das Kontrollkästchen **Zuweisung** in der Außerkraftsetzung für die juristische Person aktivieren.

## <a name="allocation-term-example"></a>Beispiel für eine Zuweisungsbedingung
Sie haben für Ihre Organisation mit dem Namen CORPORATE eine Kostenstelle mit der Nummer 000 festgelegt. Wenn Rechnungen für Betriebskosten gebucht werden, werden sie für diese CORPORATE-Kostenstelle kodiert. Ihr Unternehmen hat eine Regel festgelegt, nach der alle Betriebskosten prozentual den einzelnen Kostenstellen zugewiesen werden sollen. Die anderen Finanzdimensionen für Abteilung und Unternehmenseinheit bleiben unverändert.

In diesem Beispiel würde eine neue Zuweisungsbedingung für das Hauptkonto der Betriebskosten erstellt werden. Für jede Kostenstelle wird eine Zeile mit dem zuzuweisenden Prozentsatz erstellt. Das **Auswahlkriterium** für die ursprüngliche Finanzdimensionen für jede Zeile ist **Spezifisch** für die **Kostenstelle** und der Wert würde auf „000: CORPORATE“ gesetzt. Für Abteilung und Unternehmenseinheit ist das **Auswahlkriterium** **Unspezifisch**.

Im Inforegister **Zielsachkonto** ist das Hauptkonto das gleiche Betriebskostenkonto, und **Ursprüngliche Finanzdimensionen beibehalten** auf **Ja** für die **Unternehmenseinheit** und **Abteilung** gesetzt. **Ursprüngliche Finanzdimensionen beibehalten** wird auf **Nein** für die **Kostenstelle** gesetzt und der ausgewählte Wert ist die jeweilige Kostenstelle, an welche eine Zuweisung erfolgt. Wenn drei Kostenstellen zugewiesen werden müssen, werden drei Datensätze für Zuweisungsbedingungen erstellt. Der einzige Unterschied zwischen den einzelnen Zuweisungsbedingungen besteht in der Kostenstelle, die auf dem Zielsachkonto angegeben ist.

## <a name="create-an-allocation-term-on-a-main-account"></a>Eine Zuweisungsbedingung für ein Hauptkonto erstellen

1. Gehen Sie im **Navigationsbereich** zu **Module > Hauptbuch > Kontenplan > Konten > Hauptkonten**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Im Inforegister **Außerkraftsetzung für juristische Person** wählen Sie **Hinzufügen**.
4. Wählen Sie **Unternehmen** und dann **Hinzufügen**.
5. Aktivieren Sie das Kontrollkästchen **Zuweisen**.
6. Wählen Sie **Zuteilungsbedingungen**.
7. Wählen Sie **Bearbeiten**, um den Standarddatensatz zu ändern, oder **Neu**, um einen Datensatz hinzuzufügen.
8. Im Feld **Prozent** geben Sie den Prozentsatz der Gutscheinbuchung ein, den Sie zuordnen möchten.
9. Im Inforegister **ursprüngliche Finanzdimension** wählen Sie für jede Finanzdimension unter **Auswahlkriterium** eine Option aus.
    - Wenn Sie **Spezifisch** auswählen, geben Sie den Wert für die Finanzdimension im Drop-down-Feld rechts aus.
    - Wenn Sie **Unspezifisch** auswählen, sind für die Finanzdimension keine zusätzlichen Informationen erforderlich.
10. Im Inforegister **Zielsachkonto** wählen Sie im Feld **Zielkonto** das Hauptkonto aus, dem Sie den Prozentsatz der Gutscheinbuchung zuordnen möchten.
11. Wählen Sie unter **Ursprüngliche Finanzdimensionen beibehalten** für jede Finanzdimension eine Option aus.
    - Wenn Sie **Nein** festlegen, wählen Sie den Wert für die Finanzdimension aus dem Drop-down-Feld rechts aus, dem die Gutscheinbuchung zugewiesen werden soll.
    - Wenn Sie **Ja** auswählen, sind keine zusätzlichen Informationen erforderlich. Das System behält den Wert auf dem Originalgutschein bei der Buchung der Zuweisung.
12. Wiederholen Sie die Schritte 7 bis 11 für jede weitere Zuweisung. Die Summe aller Zuweisungen ist im Feld **Gesamter Prozentsatz** angegeben. Dieser Betrag darf 100 nicht überschreiten.
13. Schließen Sie alle Seiten.

>[!NOTE] 
> Sie können optional die Schaltfläche **Kopieren** verwenden, um die ausgewählte Zuweisung zu duplizieren.

Wenn eine Zuweisungsbedingung für ein Hauptkonto erstellt wird, bucht das System automatisch einen neuen Gutschein, wenn ein Gutschein gebucht wird, der den ursprünglichen Finanzdimensionen der Zuweisungsbedingung entspricht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]