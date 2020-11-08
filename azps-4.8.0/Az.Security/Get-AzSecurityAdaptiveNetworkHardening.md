---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258023"
---
# <span data-ttu-id="93213-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="93213-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="93213-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93213-102">SYNOPSIS</span></span>
<span data-ttu-id="93213-103">Hämtar en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="93213-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="93213-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93213-104">SYNTAX</span></span>

### <span data-ttu-id="93213-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="93213-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="93213-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93213-106">DESCRIPTION</span></span>
<span data-ttu-id="93213-107">Anpassningsbara nätverks Härdningar beräknas automatiskt av Azure Security Center, Använd denna cmdlet för att få en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="93213-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="93213-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93213-108">EXAMPLES</span></span>

### <span data-ttu-id="93213-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93213-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="93213-110">Hämtar en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="93213-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="93213-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="93213-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="93213-112">Få en enda anpassningsbar resurs för nätverks Härdningar</span><span class="sxs-lookup"><span data-stu-id="93213-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="93213-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93213-113">PARAMETERS</span></span>

### <span data-ttu-id="93213-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93213-114">-DefaultProfile</span></span>
<span data-ttu-id="93213-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93213-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93213-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93213-116">-ResourceGroupName</span></span>
<span data-ttu-id="93213-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="93213-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93213-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93213-118">-ResourceName</span></span>
<span data-ttu-id="93213-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="93213-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93213-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="93213-120">-ResourceNamespace</span></span>
<span data-ttu-id="93213-121">Namn området för resursen.</span><span class="sxs-lookup"><span data-stu-id="93213-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93213-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="93213-122">-ResourceType</span></span>
<span data-ttu-id="93213-123">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="93213-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93213-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="93213-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="93213-125">Namnet på resursen för anpassningsbar nätverks härdning.</span><span class="sxs-lookup"><span data-stu-id="93213-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93213-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93213-126">-SubscriptionId</span></span>
<span data-ttu-id="93213-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="93213-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="93213-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93213-128">CommonParameters</span></span>
<span data-ttu-id="93213-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93213-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93213-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93213-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93213-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93213-131">INPUTS</span></span>

### <span data-ttu-id="93213-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93213-132">System.String</span></span>

## <span data-ttu-id="93213-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93213-133">OUTPUTS</span></span>

### <span data-ttu-id="93213-134">Microsoft. Azure. commands. Security. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="93213-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="93213-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93213-135">NOTES</span></span>

## <span data-ttu-id="93213-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93213-136">RELATED LINKS</span></span>