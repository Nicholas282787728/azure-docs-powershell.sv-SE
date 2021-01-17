---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403856"
---
# <span data-ttu-id="2ec25-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="2ec25-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="2ec25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ec25-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec25-103">Hämtar en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="2ec25-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="2ec25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ec25-104">SYNTAX</span></span>

### <span data-ttu-id="2ec25-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="2ec25-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="2ec25-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ec25-106">DESCRIPTION</span></span>
<span data-ttu-id="2ec25-107">Anpassningsbara nätverks Härdningar beräknas automatiskt av Azure Security Center, Använd denna cmdlet för att få en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="2ec25-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="2ec25-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ec25-108">EXAMPLES</span></span>

### <span data-ttu-id="2ec25-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ec25-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="2ec25-110">Hämtar en lista över anpassningsbara nätverks härdnings resurser i omfattning av en utökad resurs.</span><span class="sxs-lookup"><span data-stu-id="2ec25-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="2ec25-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2ec25-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="2ec25-112">Få en enda anpassningsbar resurs för nätverks Härdningar</span><span class="sxs-lookup"><span data-stu-id="2ec25-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="2ec25-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ec25-113">PARAMETERS</span></span>

### <span data-ttu-id="2ec25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec25-114">-DefaultProfile</span></span>
<span data-ttu-id="2ec25-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec25-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec25-116">-ResourceGroupName</span></span>
<span data-ttu-id="2ec25-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2ec25-117">Resource group name.</span></span>

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

### <span data-ttu-id="2ec25-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2ec25-118">-ResourceName</span></span>
<span data-ttu-id="2ec25-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2ec25-119">Resource name.</span></span>

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

### <span data-ttu-id="2ec25-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="2ec25-120">-ResourceNamespace</span></span>
<span data-ttu-id="2ec25-121">Namn området för resursen.</span><span class="sxs-lookup"><span data-stu-id="2ec25-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="2ec25-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2ec25-122">-ResourceType</span></span>
<span data-ttu-id="2ec25-123">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="2ec25-123">The type of the resource.</span></span>

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

### <span data-ttu-id="2ec25-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="2ec25-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="2ec25-125">Namnet på resursen för anpassningsbar nätverks härdning.</span><span class="sxs-lookup"><span data-stu-id="2ec25-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="2ec25-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ec25-126">-SubscriptionId</span></span>
<span data-ttu-id="2ec25-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2ec25-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="2ec25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec25-128">CommonParameters</span></span>
<span data-ttu-id="2ec25-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec25-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec25-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec25-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ec25-131">INPUTS</span></span>

### <span data-ttu-id="2ec25-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec25-132">System.String</span></span>

## <span data-ttu-id="2ec25-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ec25-133">OUTPUTS</span></span>

### <span data-ttu-id="2ec25-134">Microsoft. Azure. commands. Security. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="2ec25-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="2ec25-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ec25-135">NOTES</span></span>

## <span data-ttu-id="2ec25-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ec25-136">RELATED LINKS</span></span>