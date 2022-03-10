---
title: Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein
description: Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756702"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein

Fehlercodes: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern der Ladung %1 überein. Führen Sie die Konsistenzprüfung für die Ladung des Lagers aus, um die Gewichtsfelder neu zu berechnen.

## <a name="cause"></a>Ursache

Die Felder **Nettogewicht** und **Tara-Gewicht** werden in der Zeile der Ladung auf *0* (Null) festgelegt. Die Gewichtsfelder sind jedoch nicht auf *0* für die Messungen des Gewichts auf dem Produkt festgelegt. Wenn die Gewichtsfelder in der Zeile der Ladung nicht festgelegt sind, können Korrekturen der Menge in der Zeile der Ladung zu einer falschen Gewichtsberechnung der Ladung führen. Dieses Problem kann auftreten, wenn die Gewichte auf dem Produkt geändert wurden, seit die Zeile für die Ladung erstellt wurde.

## <a name="resolution"></a>Lösung

Standardmäßig werden beim Erstellen einer Ladungs-Zeile die Gewichtsfelder aus dem Produkt darauf eingetragen. Wenn das Gewicht Null ist, können Sie es mit Hilfe der Funktionalität *Konsistenzprüfung des Gewichts der Lagerorte* neu berechnen.

1. Gehen Sie zu **Systemverwaltung \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**.
1. Legen Sie im Dialogfeld **Konsistenzprüfung** das Feld **Modul** auf *Lagerortverwaltung* fest.
1. Legen Sie das Feld **Prüfen/Beheben** auf *Fehler beheben* fest.
1. Wählen Sie in der Liste der Kontrollkästchen das Kontrollkästchen **Konsistenz der Ladung** und stellen Sie sicher, dass nur die Zeile für dieses Kontrollkästchen markiert ist.
1. Wählen Sie oben in der Liste der Kontrollkästchen die Schaltfläche mit den Auslassungspunkten (**...**), und wählen Sie dann im Menü **Dialog**.
1. Legen Sie im Dialogfeld **Konsistenzprüfung des Gewichts der Ladung im Lagerort** die folgenden Felder fest, um die Kriterien anzugeben, nach denen die Konsistenzprüfung ausgeführt werden soll:

    - **Ladungs-ID:** Geben Sie eine Ladungs-ID an. Lassen Sie dies leer, um alle Ladung-IDs zu prüfen.
    - **Elementnummer:** Geben Sie eine Elementnummer an. Lassen Sie dies leer, um alle Elemente zu prüfen.
    - **Gewicht auf Ladungen immer neu berechnen:** Legen Sie diese Option auf *Ja* fest.
    - **Überschreiben von Gewicht auf Ladungs-Zeilen zulassen:** Legen Sie diese Option auf *Ja* fest.

1. Wählen Sie **OK**, um die Dialogbox **Prüfung der Konsistenz des Gewichts der Ladung im Lagerort** zu schließen.
1. Wählen Sie die Schaltfläche mit den Auslassungspunkten und dann **Ausführen** im Menü aus.

Das Gewicht wird auf der Grundlage der von Ihnen angegebenen Kriterien neu berechnet. Wählen Sie den Link **Meldungsdetails**, um das Ergebnis der Konsistenzprüfung anzuzeigen.
