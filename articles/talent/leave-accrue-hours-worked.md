---
title: Arbeitsfreie Zeit auf Grundlage der gearbeiteten Stunden abgrenzen
description: In diesem Thema wird beschrieben, wie Urlaubpläne konfiguriert werden können, um Freizeit auf Grundlage der gearbeiteten Stunden abzugrenzen.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006077"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Arbeitsfreie Zeit auf Grundlage der gearbeiteten Stunden abgrenzen

## <a name="overview"></a>Übersicht

Organisationen mit Stundensatz-Mitarbeitern können Freizeit auf Grundlage der Stunden vergeben, die anstelle der Eigentümerschaft mit der Organisation geändert werden. Die Daten der gearbeiteten Stunden werden in der Regel in einem Zeit- und in einem Anwesenheitssystem gespeichert. 

## <a name="leave-plans"></a>Urlaubspläne

Innerhalb des Urlaubplans kann entweder der Abgrenzungstyp Dienstmonat oder gearbeitete Stunden abgegrenzt werden. Wenn gearbeitete Stunden ausgewählt wird, gibt es zwei Typen von Stunden, die zur Antizipieren verwendet werden können: reguläre Stunden und Überstunden.

Um einen Urlaubplan einzurichten mit gearbeiteten Stunden, folgen Sie diesen Schritten:

1. Auf der Seite **Urlaub- und Abwesenheitspläne** klicken Sie auf **Neuen Plan erstellen**.
2. Geben Sie einen Namen für den Urlaubplan ein.
3. Wählen Sie die Antizipierungshäufigkeit des Urlaubsplans.
5. Wählen Sie das Startdatum für den Plan.
6. Wählen Sie die Abgrenzungsperiodegrundlage und wählen Sie das mitarbeiterspezifische Datum, sofern zutreffend.
7. Für den Abgrenzungszeitplan wählen Sie **Gearbeitete Stunden** für den Abgrenzungstyp aus.
8. Hier werden die Stundentypen gewählt, die für Abgrenzung verwendet werden.
9. Geben Sie die Anzahl der Arbeitsstunden ein und den dazugehörigen Abgrenzungsbetrag, den Mindestsaldo und den Höchstwert für den Übertrag oder der gewährte Betrag.

Der Abgrenzungsprozess für gearbeitet Stunden nutzt die Antizipierungshäufigkeit, zusammen mit der Abgrenzungsperiodengrundalge, die die abzugrenzenden Stunden bestimmt.

## <a name="annual-accrual-frequency"></a>Jährliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Monatliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Halb-monatliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 8.1                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Wöchentliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Mitarbeitern zugewiesene Urlaubspläne

In den den Mitarbeitern zugewiesenen Urlaubpläne wird die Basisebene und die Art der Stunden für die Pläne angezeigt, wenn die gearbeiteten Stunden als Abgrenzungstyp definiert wird. Für aktive Pläne werden die tatsächlichen Arbeitsstunden für die Abgrenzungsperioden ab dem aktuellen Datum ebenfalls als Referenz angezeigt. 

## <a name="loading-data"></a>Daten werden geladen...

Tatsächliche Stunden können mithilfe von Urlaubs- und Abwesenheitsstunden der Entität in der Datenverwaltung verwendet werden. Wenn Sie Arbeitszeitkalender verwenden, überprüft der Import, dass die regulären gearbeiteten Stunden die geplanten Stunden in einem Tag nicht überschreitet, die anhand des Kalenders definiert werden. Der Import prüft auch, dass die Stunden, die für einen bestimmten Tag gearbeitet werden, nicht über 24 Stunden hinausgehen. 

Die folgenden Informationen werden benötigt, um die tatsächlichen Arbeitsstunden, die im Urlaubabgrenzungsprozess verwendet werden zu importieren:

+ Personalnummer 
+ Datum Arbeitstag
+ Typ
+ Stunden

Ein einzelnes Datum kann nur je einen zugeordneten Typ haben.

| PERSONALNUMMER       | ARBEITSDATUM           | TYP                  | STUNDEN                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regelmäßig               | 8                    |       
| 000337                | 8/7/2018             | Regelmäßig               | 8                    |
| 000337                | 8/7/2018             | Überstunden              | 3                    |
| 000337                | 8/8/2018             | Regelmäßig               | 8                    |
| 000337                | 8/7/2018             | Regelmäßig               | 8                    |
| 000337                | 8/9/2018             | Regelmäßig               | 8                    |
