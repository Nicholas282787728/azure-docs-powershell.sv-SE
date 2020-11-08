---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269526"
---
# <span data-ttu-id="ff7d5-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="ff7d5-101">Get-AzSubscription</span></span>

## <span data-ttu-id="ff7d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7d5-103">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="ff7d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff7d5-104">SYNTAX</span></span>

### <span data-ttu-id="ff7d5-105">ListByIdInTenant (standard)</span><span class="sxs-lookup"><span data-stu-id="ff7d5-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff7d5-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="ff7d5-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff7d5-107">DESCRIPTION</span></span>
<span data-ttu-id="ff7d5-108">Get-AzSubscription cmdlet får prenumerations-ID, prenumerations namn och hem klient organisation för abonnemang som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="ff7d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff7d5-109">EXAMPLES</span></span>

### <span data-ttu-id="ff7d5-110">Exempel 1: Hämta alla prenumerationer i alla innehavare</span><span class="sxs-lookup"><span data-stu-id="ff7d5-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="ff7d5-111">Det här kommandot får alla prenumerationer i alla innehavare som är godkända för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="ff7d5-112">Exempel 2: Hämta alla prenumerationer för en viss klient organisation</span><span class="sxs-lookup"><span data-stu-id="ff7d5-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="ff7d5-113">Lista alla prenumerationer i den klient organisation som är behörig för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="ff7d5-114">Exempel 3: Hämta alla prenumerationer i den aktuella innehavaren</span><span class="sxs-lookup"><span data-stu-id="ff7d5-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="ff7d5-115">Det här kommandot får alla prenumerationer i den aktuella innehavaren som är behörig för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="ff7d5-116">Exempel 4: ändra den aktuella kontexten till att använda ett visst abonnemang</span><span class="sxs-lookup"><span data-stu-id="ff7d5-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="ff7d5-117">Det här kommandot hämtar det angivna abonnemanget och anger sedan den aktuella kontexten för att använda den.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="ff7d5-118">Alla efterföljande cmdlets i den här sessionen använder det nya abonnemanget (contoso-abonnemang 1) som standard.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="ff7d5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff7d5-119">PARAMETERS</span></span>

### <span data-ttu-id="ff7d5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff7d5-120">-AsJob</span></span>
<span data-ttu-id="ff7d5-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7d5-122">-DefaultProfile</span></span>
<span data-ttu-id="ff7d5-123">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff7d5-123">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7d5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff7d5-124">-SubscriptionId</span></span>
<span data-ttu-id="ff7d5-125">Anger ID för det abonnemang du vill ha.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7d5-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ff7d5-126">-SubscriptionName</span></span>
<span data-ttu-id="ff7d5-127">Anger namnet på den prenumeration du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7d5-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ff7d5-128">-TenantId</span></span>
<span data-ttu-id="ff7d5-129">Anger ID för den klient organisation som innehåller prenumerationer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7d5-130">CommonParameters</span></span>
<span data-ttu-id="ff7d5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7d5-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7d5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7d5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff7d5-133">INPUTS</span></span>

### <span data-ttu-id="ff7d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ff7d5-134">System.String</span></span>

## <span data-ttu-id="ff7d5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff7d5-135">OUTPUTS</span></span>

### <span data-ttu-id="ff7d5-136">Microsoft. Azure. commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ff7d5-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ff7d5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff7d5-137">NOTES</span></span>

## <span data-ttu-id="ff7d5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff7d5-138">RELATED LINKS</span></span>
