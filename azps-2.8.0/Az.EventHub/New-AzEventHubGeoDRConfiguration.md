---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: cb1f3ba75b05fcd6950a8cb9bcff9fe899aaf471
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744204"
---
# <span data-ttu-id="8f7c4-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7c4-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="8f7c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7c4-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="8f7c4-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8f7c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f7c4-104">SYNTAX</span></span>

### <span data-ttu-id="8f7c4-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8f7c4-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7c4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f7c4-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7c4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f7c4-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f7c4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f7c4-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7c4-109">Cmdleten **New-AzEventHubGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="8f7c4-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8f7c4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f7c4-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7c4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8f7c4-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="8f7c4-112">Skapar ett alias "SampleDRConfigName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="8f7c4-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="8f7c4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f7c4-113">PARAMETERS</span></span>

### <span data-ttu-id="8f7c4-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="8f7c4-114">-AlternateName</span></span>
<span data-ttu-id="8f7c4-115">AlternateName krävs när DR-konfigurationsfilen är samma som det primära namn området</span><span class="sxs-lookup"><span data-stu-id="8f7c4-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="8f7c4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f7c4-116">-AsJob</span></span>
<span data-ttu-id="8f7c4-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8f7c4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f7c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7c4-118">-DefaultProfile</span></span>
<span data-ttu-id="8f7c4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f7c4-120">-InputObject</span></span>
<span data-ttu-id="8f7c4-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="8f7c4-121">Namespace Object</span></span>

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

### <span data-ttu-id="8f7c4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f7c4-122">-Name</span></span>
<span data-ttu-id="8f7c4-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7c4-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="8f7c4-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8f7c4-124">-Namespace</span></span>
<span data-ttu-id="8f7c4-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="8f7c4-125">Namespace Name</span></span>

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

### <span data-ttu-id="8f7c4-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="8f7c4-126">-PartnerNamespace</span></span>
<span data-ttu-id="8f7c4-127">PartnerNamespace för DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7c4-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="8f7c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f7c4-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8f7c4-129">Resource Group Name</span></span>

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

### <span data-ttu-id="8f7c4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7c4-130">-ResourceId</span></span>
<span data-ttu-id="8f7c4-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="8f7c4-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8f7c4-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f7c4-132">-Confirm</span></span>
<span data-ttu-id="8f7c4-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7c4-134">-WhatIf</span></span>
<span data-ttu-id="8f7c4-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7c4-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c4-137">CommonParameters</span></span>
<span data-ttu-id="8f7c4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c4-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f7c4-140">INPUTS</span></span>

### <span data-ttu-id="8f7c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8f7c4-141">System.String</span></span>

### <span data-ttu-id="8f7c4-142">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8f7c4-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8f7c4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f7c4-143">OUTPUTS</span></span>

### <span data-ttu-id="8f7c4-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8f7c4-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="8f7c4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f7c4-145">NOTES</span></span>

## <span data-ttu-id="8f7c4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f7c4-146">RELATED LINKS</span></span>
