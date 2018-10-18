---
title: Hantera Azure-prenumerationer med Azure PowerShell
description: Hantera Azure-prenumerationer med Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 3f1c1bab5f9903ee7df813bf1ef043c7107ebe79
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399135"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="b1853-103">Hantera flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="b1853-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="b1853-104">Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b1853-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="b1853-105">Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="b1853-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="b1853-106">Du kan konfigurera Azure PowerShell för att köra kommandon mot en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b1853-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="b1853-107">Hämta en lista över alla prenumerationer i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="b1853-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="b1853-108">Ange standard.</span><span class="sxs-lookup"><span data-stu-id="b1853-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="b1853-109">Verifiera ändringen genom att köra `Get-AzureRmContext`-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1853-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="b1853-110">När du ställer in din standardprenumeration körs alla Azure PowerShell-kommandon mot den här prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b1853-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
