---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576831"
---
# <span data-ttu-id="aa7db-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="aa7db-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="aa7db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa7db-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7db-103">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="aa7db-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa7db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa7db-104">SYNTAX</span></span>

### <span data-ttu-id="aa7db-105">ListByIdInTenant (standard)</span><span class="sxs-lookup"><span data-stu-id="aa7db-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa7db-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="aa7db-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa7db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa7db-107">DESCRIPTION</span></span>
<span data-ttu-id="aa7db-108">Get-AzureRmSubscription cmdlet får prenumerations-ID, prenumerations namn och hem klient organisation för abonnemang som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="aa7db-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="aa7db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa7db-109">EXAMPLES</span></span>

### <span data-ttu-id="aa7db-110">Exempel 1: Hämta alla prenumerationer i alla innehavare</span><span class="sxs-lookup"><span data-stu-id="aa7db-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="aa7db-111">Det här kommandot får alla prenumerationer i alla innehavare som är godkända för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="aa7db-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="aa7db-112">Exempel 2: Hämta alla prenumerationer för en viss klient organisation</span><span class="sxs-lookup"><span data-stu-id="aa7db-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="aa7db-113">Lista alla prenumerationer i den klient organisation som är behörig för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="aa7db-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="aa7db-114">Exempel 3: Hämta alla prenumerationer i den aktuella innehavaren</span><span class="sxs-lookup"><span data-stu-id="aa7db-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="aa7db-115">Det här kommandot får alla prenumerationer i den aktuella innehavaren som är behörig för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="aa7db-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="aa7db-116">Exempel 4: ändra den aktuella kontexten till att använda ett visst abonnemang</span><span class="sxs-lookup"><span data-stu-id="aa7db-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="aa7db-117">Det här kommandot hämtar det angivna abonnemanget och anger sedan den aktuella kontexten för att använda den.</span><span class="sxs-lookup"><span data-stu-id="aa7db-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="aa7db-118">Alla efterföljande cmdlets i den här sessionen använder det nya abonnemanget (contoso-abonnemang 1) som standard.</span><span class="sxs-lookup"><span data-stu-id="aa7db-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="aa7db-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa7db-119">PARAMETERS</span></span>

### <span data-ttu-id="aa7db-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa7db-120">-AsJob</span></span>
<span data-ttu-id="aa7db-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="aa7db-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aa7db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7db-122">-DefaultProfile</span></span>
<span data-ttu-id="aa7db-123">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa7db-123">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa7db-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa7db-124">-SubscriptionId</span></span>
<span data-ttu-id="aa7db-125">Anger ID för det abonnemang du vill ha.</span><span class="sxs-lookup"><span data-stu-id="aa7db-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="aa7db-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="aa7db-126">-SubscriptionName</span></span>
<span data-ttu-id="aa7db-127">Anger namnet på den prenumeration du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="aa7db-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="aa7db-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="aa7db-128">-TenantId</span></span>
<span data-ttu-id="aa7db-129">Anger ID för den klient organisation som innehåller prenumerationer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="aa7db-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="aa7db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7db-130">CommonParameters</span></span>
<span data-ttu-id="aa7db-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7db-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7db-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7db-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa7db-133">INPUTS</span></span>

### <span data-ttu-id="aa7db-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7db-134">System.String</span></span>

## <span data-ttu-id="aa7db-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa7db-135">OUTPUTS</span></span>

### <span data-ttu-id="aa7db-136">Microsoft. Azure. commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="aa7db-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="aa7db-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa7db-137">NOTES</span></span>

## <span data-ttu-id="aa7db-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa7db-138">RELATED LINKS</span></span>
