---
title: Hantera Azure-prenumerationer med Azure PowerShell
description: Hantera Azure-prenumerationer med Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: e1606ddb02adf1de2cb5496917d61755ac3dad23
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018470"
---
# <a name="manage-multiple-azure-subscriptions"></a>Hantera flera Azure-prenumerationer

Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration. Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer. Du kan konfigurera Azure PowerShell för att köra kommandon mot en viss prenumeration.

1. Hämta en lista över alla prenumerationer i ditt konto.

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. Ange standard.

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. Verifiera ändringen genom att köra `Get-AzureRmContext`-cmdleten.

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

När du ställer in din standardprenumeration körs alla efterföljande Azure PowerShell-kommandon mot den här prenumerationen.
