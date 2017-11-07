---
title: Bankgarantien
description: "Dieser Artikel enthält Informationen zu Garantiebriefen. Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank, einen bestimmten Geldbetrag an eine andere Person zu zahlen, falls seitens eines Debitors der Bank eine regelmäßige Zahlungsverpflichtung gegenüber dieser Person besteht."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7144a979b98b3dbd2052661945e6d4fe22220a7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="letters-of-guarantee"></a>Bankgarantien

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Garantiebriefen. Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank, einen bestimmten Geldbetrag an eine andere Person zu zahlen, falls seitens eines Debitors der Bank eine regelmäßige Zahlungsverpflichtung gegenüber dieser Person besteht. 

Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank (der Bürge), einen bestimmten Geldbetrag an eine andere Person zu zahlen (den Begünstigten), falls seitens eines Debitors der Bank (der Auftraggeber) eine regelmäßige Zahlungsverpflichtung gegenüber dem Begünstigten besteht. Garantiebriefe sind nicht übertragbar. Sie richten sich nur an den Begünstigten, der in der Vereinbarung benennt wird. Der Auftraggeber kann im Rahmen der Bedingungen der Vereinbarung eine Erhöhung oder Verringerung des Werts eines Garantiebriefs fordern. 

Um einen Garantiebrief zu liquidieren, muss der Begünstigte den ursprünglichen Garantiebrief übermitteln und die Bank vor dem Ablaufdatum von der regelmäßigen Zahlungsverpflichtung seitens des Auftraggebers unterrichten. Die Bank zahlt den fälligen Betrag anschließend gemäß der Vereinbarung im Garantiebrief auf das Konto des Begünstigten. Die Bank reserviert einen Anteil der Zahlung als Gewinnspanne. Der Prozentsatz wird vereinbart und in den Vereinbarungsbedingungen angegeben. 

Sie können einen Code erstellen, um den Zweck eines Garantiebriefs nachzuverfolgen. Sie können auch die Gründe angeben, die einem Garantiebrief zugeordnet werden, wenn der Brief storniert wird. Sie können die Zweckcodes und die Gründe der Bank auf den Seiten **Zahlungszweckcode** den **Ursachen für Bankbuchungen** anzeigen. 

Verwenden Sie die Seite **Garantiebrief**, um die folgenden Aufgaben durchführen:

-   Erstellen von korrekten Sachkontoeinträgen und Löschen von manuellen Eingaben.
-   Erfassen aller geld- und nicht geldbezogenen Transaktionen und Nachverfolgung der Garantiebriefsalden.
-   Erfassen und Nachverfolgen des Status und des Ablaufdatums des Garantiebriefs.
-   Generieren eines Berichts, in dem die Banken aufgeführt sind, die Garantiebriefe besitzen.

In der folgenden Tabelle werden die Aktivitäten beschrieben, die mit einem Garantiebrief ausgeführt werden können.

| Aktion              | Verwendungszweck                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| An Bank übermitteln      | Übermittlung der Garantiebriefanforderung an die Bank.                                                                       |
| Empfang von der Bank   | Nachdem die Bank die übermittelte Anforderung bestätigt hat, wird der Garantiebrief bei der Bank einkassiert.                            |
| Übergabe an den Begünstigten | Wenn Sie den Garantiebrief von der Bank erhalten haben, übergeben Sie den Garantiebrief an den Begünstigten.              |
| Erhöhung des Werts      | Wenn der Begünstigte und der Auftraggeber eine entsprechende Vereinbarung treffen, kann der Geldwert erhöht werden.                                                  |
| Verringerung des Werts      | Wenn der Begünstigte und der Auftraggeber eine entsprechende Vereinbarung treffen, kann der Geldwert verringert werden.                                                  |
| Verlängern              | Wenn Sie den Garantiebrief an den Begünstigten übergeben haben, verlängern Sie ggf. die Gültigkeitsdauer. |
| Stornieren              | Wenn der Zweck, zu dem der Garantiebrief angefordert wurde, nicht mehr zutrifft, stornieren Sie die Vereinbarung.                  |
| Tilgen           | Wenn der Begünstigte den Garantiebrief bei der Bank vorlegt, kann dieser Garantiebrief liquidiert werden.                      |


Weitere Informationen finden Sie in folgenden Themen:

[Bankgarantiebuchung](tasks/letter-guarantee-transaction.md)

[Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten](tasks/set-up-bank-facilities-posting-profiles.md)



