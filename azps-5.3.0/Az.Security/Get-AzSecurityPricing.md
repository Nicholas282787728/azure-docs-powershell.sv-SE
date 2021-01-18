---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525646"
---
# <span data-ttu-id="9573b-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9573b-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="9573b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9573b-102">SYNOPSIS</span></span>

<span data-ttu-id="9573b-103">Hämtar Azure Defender-abonnemang för en prenumeration i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="9573b-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="9573b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9573b-104">SYNTAX</span></span>

### <span data-ttu-id="9573b-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="9573b-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9573b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9573b-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9573b-107">ID</span><span class="sxs-lookup"><span data-stu-id="9573b-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9573b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9573b-108">DESCRIPTION</span></span>

<span data-ttu-id="9573b-109">Du kan visa varje Azure Defender-plan per abonnemang med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9573b-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="9573b-110">Mer information om Azure Defender och tillgängliga abonnemang finns i [Introduktion till Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="9573b-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="9573b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9573b-111">EXAMPLES</span></span>

### <span data-ttu-id="9573b-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9573b-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="9573b-113">Hämtar statusen för varje Azure Defender-abonnemang för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9573b-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="9573b-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9573b-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="9573b-115">Hämtar priser för det specifika resurs-ID: t.</span><span class="sxs-lookup"><span data-stu-id="9573b-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="9573b-116">Där ResourceId är ett av de ID som returneras av `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="9573b-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="9573b-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9573b-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="9573b-118">Hämtar priser för det namngivna Azure Defender-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9573b-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="9573b-119">Var `name` ett av namnen returnerades av `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="9573b-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="9573b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9573b-120">PARAMETERS</span></span>

### <span data-ttu-id="9573b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9573b-121">-DefaultProfile</span></span>

<span data-ttu-id="9573b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9573b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9573b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9573b-123">-Name</span></span>

<span data-ttu-id="9573b-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9573b-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9573b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9573b-125">-ResourceId</span></span>

<span data-ttu-id="9573b-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9573b-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9573b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9573b-127">CommonParameters</span></span>

<span data-ttu-id="9573b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9573b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9573b-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9573b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9573b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9573b-130">INPUTS</span></span>

### <span data-ttu-id="9573b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9573b-131">System.String</span></span>

## <span data-ttu-id="9573b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9573b-132">OUTPUTS</span></span>

### <span data-ttu-id="9573b-133">Microsoft. Azure. kommandon. Security. Models. priser. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9573b-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9573b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9573b-134">NOTES</span></span>

## <span data-ttu-id="9573b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9573b-135">RELATED LINKS</span></span>
