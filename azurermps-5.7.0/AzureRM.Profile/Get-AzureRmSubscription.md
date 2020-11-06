---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583112"
---
# <span data-ttu-id="28b6c-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="28b6c-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="28b6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="28b6c-103">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="28b6c-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28b6c-104">SYNTAX</span></span>

### <span data-ttu-id="28b6c-105">ListByIdInTenant (standard)</span><span class="sxs-lookup"><span data-stu-id="28b6c-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b6c-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="28b6c-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28b6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="28b6c-108">Get-AzureRmSubscription cmdlet får prenumerations-ID, prenumerations namn och hem klient organisation för abonnemang som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="28b6c-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="28b6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="28b6c-110">Exempel 1: Hämta alla prenumerationer i alla innehavare</span><span class="sxs-lookup"><span data-stu-id="28b6c-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="28b6c-111">Det här kommandot får alla prenumerationer i alla innehavare som är godkända för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="28b6c-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="28b6c-112">Exempel 2: Hämta alla prenumerationer för en viss klient organisation</span><span class="sxs-lookup"><span data-stu-id="28b6c-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="28b6c-113">Lista alla prenumerationer i den klient organisation som är behörig för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="28b6c-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="28b6c-114">Exempel 3: Hämta alla prenumerationer i den aktuella innehavaren</span><span class="sxs-lookup"><span data-stu-id="28b6c-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="28b6c-115">Det här kommandot får alla prenumerationer i den aktuella innehavaren som är behörig för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="28b6c-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="28b6c-116">Exempel 4: ändra den aktuella kontexten till att använda ett visst abonnemang</span><span class="sxs-lookup"><span data-stu-id="28b6c-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="28b6c-117">Det här kommandot hämtar det angivna abonnemanget och anger sedan den aktuella kontexten för att använda den.</span><span class="sxs-lookup"><span data-stu-id="28b6c-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="28b6c-118">Alla efterföljande cmdlets i den här sessionen använder det nya abonnemanget (contoso-abonnemang 1) som standard.</span><span class="sxs-lookup"><span data-stu-id="28b6c-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="28b6c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28b6c-119">PARAMETERS</span></span>

### <span data-ttu-id="28b6c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28b6c-120">-AsJob</span></span>
<span data-ttu-id="28b6c-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="28b6c-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b6c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b6c-122">-DefaultProfile</span></span>
<span data-ttu-id="28b6c-123">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="28b6c-123">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b6c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28b6c-124">-SubscriptionId</span></span>
<span data-ttu-id="28b6c-125">Anger ID för det abonnemang du vill ha.</span><span class="sxs-lookup"><span data-stu-id="28b6c-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b6c-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="28b6c-126">-SubscriptionName</span></span>
<span data-ttu-id="28b6c-127">Anger namnet på den prenumeration du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="28b6c-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b6c-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="28b6c-128">-TenantId</span></span>
<span data-ttu-id="28b6c-129">Anger ID för den klient organisation som innehåller prenumerationer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="28b6c-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b6c-130">CommonParameters</span></span>
<span data-ttu-id="28b6c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b6c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b6c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28b6c-133">INPUTS</span></span>

### <span data-ttu-id="28b6c-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="28b6c-134">None</span></span>
<span data-ttu-id="28b6c-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="28b6c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28b6c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28b6c-136">OUTPUTS</span></span>

### <span data-ttu-id="28b6c-137">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="28b6c-137">PSAzureSubscription</span></span>

## <span data-ttu-id="28b6c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28b6c-138">NOTES</span></span>

## <span data-ttu-id="28b6c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28b6c-139">RELATED LINKS</span></span>

