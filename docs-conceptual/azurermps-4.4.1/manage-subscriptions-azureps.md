---
title: Hantera Azure-prenumerationer med Azure PowerShell | Microsoft Docs
description: Hantera Azure-prenumerationer med Azure PowerShell
keywords: Azure PowerShell, prenumeration
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 12e304f32f585c1af40d20579cd46999e0a12395
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587677"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="0e97f-104">Hantera flera Azure-prenumerationer</span><span class="sxs-lookup"><span data-stu-id="0e97f-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="0e97f-105">Om du är nybörjare på Azure har du förmodligen bara en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0e97f-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="0e97f-106">Men om du har använt Azure ett tag kanske du har skapat flera Azure-prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0e97f-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="0e97f-107">Du kan konfigurera Azure PowerShell för att köra kommandon mot en viss prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0e97f-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="0e97f-108">Hämta en lista över alla prenumerationer i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="0e97f-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="0e97f-109">Ange standard.</span><span class="sxs-lookup"><span data-stu-id="0e97f-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="0e97f-110">Verifiera ändringen genom att köra `Get-AzureRmContext`-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e97f-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="0e97f-111">När du ställer in din standardprenumeration körs alla efterföljande Azure PowerShell-kommandon mot den här prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0e97f-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
