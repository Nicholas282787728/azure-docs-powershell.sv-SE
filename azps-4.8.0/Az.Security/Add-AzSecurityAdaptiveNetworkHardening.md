---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258632"
---
# <span data-ttu-id="60eb4-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="60eb4-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="60eb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="60eb4-103">Tillämpar de angivna reglerna på NSG (s) som listas i begäran</span><span class="sxs-lookup"><span data-stu-id="60eb4-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="60eb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60eb4-104">SYNTAX</span></span>

### <span data-ttu-id="60eb4-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="60eb4-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60eb4-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60eb4-106">DESCRIPTION</span></span>
<span data-ttu-id="60eb4-107">Anpassningsbara nätverks Härdningar beräknas automatiskt av Azure Security Center, Använd denna cmdlet för att tillämpa de angivna reglerna på NSG (erna) i begäran.</span><span class="sxs-lookup"><span data-stu-id="60eb4-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="60eb4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60eb4-108">EXAMPLES</span></span>

### <span data-ttu-id="60eb4-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="60eb4-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="60eb4-110">Tillämpar de angivna reglerna på NSG (s) som listas i begäran</span><span class="sxs-lookup"><span data-stu-id="60eb4-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="60eb4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60eb4-111">PARAMETERS</span></span>

### <span data-ttu-id="60eb4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60eb4-112">-DefaultProfile</span></span>
<span data-ttu-id="60eb4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60eb4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60eb4-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="60eb4-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="60eb4-115">Namnet på resursen för anpassningsbar nätverks härdning.</span><span class="sxs-lookup"><span data-stu-id="60eb4-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60eb4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60eb4-116">-ResourceGroupName</span></span>
<span data-ttu-id="60eb4-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="60eb4-117">Resource group name.</span></span>

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

### <span data-ttu-id="60eb4-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="60eb4-118">-ResourceName</span></span>
<span data-ttu-id="60eb4-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="60eb4-119">Resource name.</span></span>

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

### <span data-ttu-id="60eb4-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="60eb4-120">-ResourceNamespace</span></span>
<span data-ttu-id="60eb4-121">Namn området för resursen.</span><span class="sxs-lookup"><span data-stu-id="60eb4-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="60eb4-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="60eb4-122">-ResourceType</span></span>
<span data-ttu-id="60eb4-123">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="60eb4-123">The type of the resource.</span></span>

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

### <span data-ttu-id="60eb4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60eb4-124">-SubscriptionId</span></span>
<span data-ttu-id="60eb4-125">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="60eb4-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60eb4-126">-Regler</span><span class="sxs-lookup"><span data-stu-id="60eb4-126">-Rules</span></span>
<span data-ttu-id="60eb4-127">Vilka regler som ska tillämpas.</span><span class="sxs-lookup"><span data-stu-id="60eb4-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60eb4-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="60eb4-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="60eb4-129">Azure Resource-ID: na för de effektiva nätverks säkerhets grupper som kommer att uppdateras med de säkerhets regler som har skapats från reglerna för anpassad nätverks härdning.</span><span class="sxs-lookup"><span data-stu-id="60eb4-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60eb4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60eb4-130">-PassThru</span></span>
<span data-ttu-id="60eb4-131">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="60eb4-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="60eb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60eb4-132">CommonParameters</span></span>
<span data-ttu-id="60eb4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60eb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60eb4-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60eb4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60eb4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60eb4-135">INPUTS</span></span>

### <span data-ttu-id="60eb4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60eb4-136">System.String</span></span>

### <span data-ttu-id="60eb4-137">Microsoft. Azure. commands. SecurityCenter. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="60eb4-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="60eb4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60eb4-138">OUTPUTS</span></span>

### <span data-ttu-id="60eb4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60eb4-139">System.Boolean</span></span>

## <span data-ttu-id="60eb4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60eb4-140">NOTES</span></span>

## <span data-ttu-id="60eb4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60eb4-141">RELATED LINKS</span></span>