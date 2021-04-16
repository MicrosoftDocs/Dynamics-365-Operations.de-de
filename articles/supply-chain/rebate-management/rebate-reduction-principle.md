---
title: Prinzipien zur Rückvergütungsreduzierung
description: In diesem Thema wird beschrieben, wie Reduzierungsprinzipien eingerichtet werden. Reduzierungsprinzipien steuern das Verhalten, wenn auf denselben Artikel oder dieselbe Transaktion mehrere Rückvergütungen angewendet werden.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 79f7e481b65ec40f0fb7e259037cd4988b3b5c07
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831697"
---
# <a name="rebate-reduction-principles"></a>Prinzipien zur Rückvergütungsreduzierung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sie können Rückvergütungsverwaltungsdeals in *Reduzierungsprinzipien* gruppieren, um andere Rückstellungen zu reduzieren, die mit einem Artikel verbunden sind, und/oder die resultierenden Werte von Rückvergütungsberechnungen zu reduzieren. Nachdem die Prinzipien zur Rückvergütungsreduzierung festgelegt wurden, können Sie sie optional nach Bedarf den Positionen Ihrer Rückvergütungsverwaltungsdeals zuweisen.

Die Regeln für Prinzipien zur Rückvergütungsverwaltung gelten nur, wenn sich Rückvergütungsdeals überlappen. Daher können sie in Situationen, in denen nicht mehrere Rückvergütungen geschuldet werden, mehrere Rückvergütungen gewähren.

## <a name="manage-rebate-reduction-principles"></a>Prinzipien zur Rückvergütungsreduzierung verwalten

Um mit den Prinzipien zur Rückvergütungsreduzierung zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Einstellungen \> Prinzipien zur Rückvergütungsreduzierung**. Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um bei Bedarf Reduzierungsprinzipien hinzuzufügen und zu entfernen. Legen Sie für jedes Prinzip die Felder wie in der folgenden Tabelle beschrieben fest.

| Feld | Beschreibung |
|---|---|
| Prinzip zur Rückvergütungsreduzierung | Geben Sie dem Prinzip zur Rückvergütungsreduzierung einen eindeutigen Namen. |
| Beschreibung | Geben Sie eine Beschreibung des Prinzips zur Rückvergütungsreduzierung ein. |
| Reduzierung anwenden | Aktivieren Sie dieses Kontrollkästchen, um eine Reduzierungsbasis auf Rückvergütungen anzuwenden, die zu diesem Prinzip zur Rückvergütungsreduzierung gehören. |
| Reduzierungsbasis | Wenn Sie das Kontrollkästchen **Reduzierung anwenden** aktiviert haben, wählen Sie die Reduzierungsbasis aus (*Rückstellung*, *Rückvergütungen* oder *Beide*). Wenn Sie *Beide* auswählen und sowohl eine Rückstellung als auch eine Rückvergütung für einen früheren Deal gebucht haben, wird nur die Rückvergütung angewendet. |
| Von Reduzierung ausschließen | Wenn dieses Kontrollkästchen aktiviert ist, werden Rückstellungen und Rückvergütungen, die zu diesem Prinzip zur Rückvergütungsreduzierung gehören, von nachfolgenden Reduzierungen ausgeschlossen. Die Einstellung des Felds **Reduzierungsbasis** gilt nicht für diese Einstellung. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Beispiele für Einstellungen mit Prinzipien zur Rückvergütungsreduzierung

Die folgende Tabelle zeigt einige typische Beispiele für Einstellungen mit Prinzipien zur Rückvergütungsreduzierung. Für jedes dieser Prinzipien zur Rückvergütungsreduzierung gibt der Wert des Felds **Beschreibung** den Zweck des Prinzips zur Rückvergütungsreduzierung an.

| Prinzip zur Rückvergütungsreduzierung | Beschreibung | Reduzierung anwenden | Reduzierungsbasis | Von Reduzierung ausschließen |
|---|---|---|---|---|
| Verzögert | Rückvergütung reduzieren | Ja | Beides | Nr. |
| Exclreb | Rückvergütung ausschließen | Ja | Rückvergütung | Ja |
| Mehrfach | Mehrere Rückvergütungen | Ja | Beides | Ja |
| Keines | Nur Rückstellungen und Rückvergütungen | Nr. | Beides | Ja |
| Bereitstellung | Nur Rückstellung | Ja | Bereitstellung | Nr. |
| Rückvergütung | Nur Rückvergütung | Ja | Rückvergütung | Ja |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Beispiele für Berechnungen von Prinzipien zur Rückvergütungsreduzierung

Sie haben einen Auftrag mit einer einzelnen Auftragsposition. Der Wert dieser Position ist 1.000 EUR. Für den Auftrag gelten die folgenden Deals:

- **Deal 1:** 10 % auf 1.000 EUR
- **Deal 2:** 15 % auf 1.000 EUR
- **Deal 3:** 20 % auf 1.000 EUR
- **Deal 4:** 25 % auf 1.000 EUR

Die Reihenfolge der Verarbeitung ist sehr wichtig. Die Verarbeitungsreihenfolge basiert auf Ihrer Arbeitsweise, wie in [Rückvergütungen verarbeiten, überprüfen und buchen](process-review-post.md) beschrieben.

In der folgenden Tabelle wird beispielsweise das Ergebnis zusammengefasst, wenn Sie die Reihenfolge *1, 2, 3, 4* verwenden und wenn Sie nur die Rückstellungen verarbeiten.

| Handel | Beschreibung und Einstellungen | Rückstellungsergebnis |
|---|---|---|
| 1 | <p>Die Klassifizierung überprüft andere Deals nicht auf Reduzierungen. Die Prüfung erfolgt sowohl für Rückstellungen als auch für Rückvergütungen.</p><ul><li>**Reduzierung anwenden:** *Nein*</li><li>**Reduzierungsbasis:** *Beide*</li><li>**Von Reduzierung ausschließen:** *Nein*</li></ul> | 1.000 EUR x 10 % = 100 EUR |
| 2 | <p>Die Klassifizierung überprüft andere Deals auf Reduzierungen, ist jedoch gekennzeichnet, sodass sie selbst ignoriert wird. Die Prüfung erfolgt nur für Rückvergütungen.</p><ul><li>**Reduzierung anwenden:** *Ja*</li><li>**Reduzierungsbasis:** *Rückvergütung*</li><li>**Von Reduzierung ausschließen:** *Ja*</li></ul> | 1.000 EUR x 15 % = 150 EUR |
| 3 | <p>Die Klassifizierung überprüft andere Deals auf Reduzierungen. Die Prüfung erfolgt sowohl für Rückstellungen als auch für Rückvergütungen.</p><ul><li>**Reduzierung anwenden:** *Ja*</li><li>**Reduzierungsbasis:** *Beide*</li><li>**Von Reduzierung ausschließen:** *Nein*</li></ul> | (1.000 EUR – Deal 1) x 20 % = 180 EUR |
| 4 | <p>Die Klassifizierung überprüft andere Deals auf Reduzierungen. Die Prüfung erfolgt sowohl für Rückstellungen als auch für Rückvergütungen.</p><ul><li>**Reduzierung anwenden:** *Ja*</li><li>**Reduzierungsbasis:** *Beide*</li><li>**Von Reduzierung ausschließen:** *Nein*</li></ul> | (1.000 EUR – Deal 1 – Deal 3) × 25 % = 180 EUR |

Die folgende Tabelle zeigt einige Beispiele, bei denen die Rückstellungen in unterschiedlichen Reihenfolgen verarbeitet wird, weshalb sich die Ergebnisse unterscheiden. Die Abweichung in den Rückstellungen hängt von der Reihenfolge ab, in der das System die Deals verarbeitet. Es ist wichtig, dass Sie verstehen, wie sich die Reihenfolge der Verarbeitung auf den endgültigen Betrag der Rückvergütung auswirkt.

| Sequenz | Herstellkostenkalkulation |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Deal 1:** 1.000 EUR x 10 % = 100 EUR</li><li>**Deal 2:** 1.000 EUR x 15 % = 150 EUR</li><li>**Deal 3:** (1.000 EUR – Deal 1) x 20 % = 180 EUR</li><li>**Deal 4:** (1.000 EUR – Deal 1 – Deal 2) x 25 % = 180 EUR</li><li>**Gesamtrückstellung:** 610 EUR</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Deal 4:** 1.000 EUR x 25 % = 250 EUR</li><li>**Deal 3:** (1.000 EUR – Deal 4) x 20 % = 150 EUR</li><li>**Deal 2:** 1.000 EUR x 15 % = 150 EUR</li><li>**Deal 1:** 1.000 EUR x 10 % = 100 EUR</li><li>**Gesamtrückstellung:** 650 EUR</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Deal 3:** 1.000 EUR x 20 % = 200 EUR</li><li>**Deal 2:** 1.000 EUR x 15 % = 150 EUR</li><li>**Deal 1:** 1.000 EUR x 10 % = 100 EUR</li><li>**Deal 4:** (1.000 EUR – Deal 3 – Deal 1) x 25 % = 175 EUR</li><li>**Gesamtrückstellung:** 625 EUR</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Deal 2:** 1.000 EUR x 15 % = 150 EUR</li><li>**Deal 4:** 1.000 EUR x 25 % = 250 EUR</li><li>**Deal 1:** 1.000 EUR x 10 % = 100 EUR</li><li>**Deal 3:** (1.000 EUR – Deal 4 – Deal 1) x 20 % = 130 EUR</li><li>**Gesamtrückstellung:** 630 EUR</li></ul> |
