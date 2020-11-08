---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: fe0d8f29650498e895e19e18bcb080107b2dbf35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271905"
---
# <span data-ttu-id="a93fe-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a93fe-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="a93fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a93fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a93fe-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="a93fe-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a93fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a93fe-104">SYNTAX</span></span>

### <span data-ttu-id="a93fe-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a93fe-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a93fe-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a93fe-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a93fe-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a93fe-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a93fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a93fe-108">DESCRIPTION</span></span>
<span data-ttu-id="a93fe-109">Cmdleten **New-AzEventHubGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="a93fe-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a93fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a93fe-110">EXAMPLES</span></span>

### <span data-ttu-id="a93fe-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a93fe-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="a93fe-112">Skapar ett alias "SampleDRConfigName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="a93fe-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a93fe-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a93fe-113">PARAMETERS</span></span>

### <span data-ttu-id="a93fe-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="a93fe-114">-AlternateName</span></span>
<span data-ttu-id="a93fe-115">AlternateName krävs när DR-konfigurationsfilen är samma som det primära namn området</span><span class="sxs-lookup"><span data-stu-id="a93fe-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="a93fe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a93fe-116">-AsJob</span></span>
<span data-ttu-id="a93fe-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a93fe-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a93fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93fe-118">-DefaultProfile</span></span>
<span data-ttu-id="a93fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a93fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a93fe-120">-InputObject</span></span>
<span data-ttu-id="a93fe-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="a93fe-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a93fe-122">-Name</span></span>
<span data-ttu-id="a93fe-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="a93fe-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a93fe-124">-Namespace</span></span>
<span data-ttu-id="a93fe-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="a93fe-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="a93fe-126">-PartnerNamespace</span></span>
<span data-ttu-id="a93fe-127">PartnerNamespace för DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="a93fe-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="a93fe-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a93fe-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a93fe-130">-ResourceId</span></span>
<span data-ttu-id="a93fe-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="a93fe-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a93fe-132">-Confirm</span></span>
<span data-ttu-id="a93fe-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a93fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93fe-134">-WhatIf</span></span>
<span data-ttu-id="a93fe-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a93fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93fe-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a93fe-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93fe-137">CommonParameters</span></span>
<span data-ttu-id="a93fe-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93fe-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93fe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93fe-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a93fe-140">INPUTS</span></span>

### <span data-ttu-id="a93fe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a93fe-141">System.String</span></span>

### <span data-ttu-id="a93fe-142">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a93fe-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a93fe-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a93fe-143">OUTPUTS</span></span>

### <span data-ttu-id="a93fe-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a93fe-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="a93fe-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a93fe-145">NOTES</span></span>

## <span data-ttu-id="a93fe-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a93fe-146">RELATED LINKS</span></span>
