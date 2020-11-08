---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091458"
---
# <span data-ttu-id="2c3f8-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3f8-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2c3f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3f8-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="2c3f8-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2c3f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c3f8-104">SYNTAX</span></span>

### <span data-ttu-id="2c3f8-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2c3f8-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3f8-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c3f8-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3f8-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f8-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c3f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c3f8-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3f8-109">Cmdleten **New-AzServiceBusGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="2c3f8-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="2c3f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c3f8-110">EXAMPLES</span></span>

### <span data-ttu-id="2c3f8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2c3f8-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="2c3f8-112">Skapar ett alias "SampleDRConfigName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="2c3f8-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="2c3f8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c3f8-113">PARAMETERS</span></span>

### <span data-ttu-id="2c3f8-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="2c3f8-114">-AlternateName</span></span>
<span data-ttu-id="2c3f8-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="2c3f8-115">AlternateName</span></span>

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

### <span data-ttu-id="2c3f8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c3f8-116">-AsJob</span></span>
<span data-ttu-id="2c3f8-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2c3f8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c3f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3f8-118">-DefaultProfile</span></span>
<span data-ttu-id="2c3f8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c3f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c3f8-120">-InputObject</span></span>
<span data-ttu-id="2c3f8-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="2c3f8-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f8-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c3f8-122">-Name</span></span>
<span data-ttu-id="2c3f8-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="2c3f8-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="2c3f8-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="2c3f8-124">-Namespace</span></span>
<span data-ttu-id="2c3f8-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="2c3f8-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f8-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="2c3f8-126">-PartnerNamespace</span></span>
<span data-ttu-id="2c3f8-127">DR-konfiguration PartnerNamespace (ARM-ID för PartnerNamespace [sekundärt namn område])</span><span class="sxs-lookup"><span data-stu-id="2c3f8-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="2c3f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c3f8-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2c3f8-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c3f8-130">-ResourceId</span></span>
<span data-ttu-id="2c3f8-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="2c3f8-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2c3f8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c3f8-132">-Confirm</span></span>
<span data-ttu-id="2c3f8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c3f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3f8-134">-WhatIf</span></span>
<span data-ttu-id="2c3f8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c3f8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3f8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c3f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3f8-137">CommonParameters</span></span>
<span data-ttu-id="2c3f8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3f8-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3f8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3f8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c3f8-140">INPUTS</span></span>

### <span data-ttu-id="2c3f8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c3f8-141">System.String</span></span>

### <span data-ttu-id="2c3f8-142">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2c3f8-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2c3f8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c3f8-143">OUTPUTS</span></span>

### <span data-ttu-id="2c3f8-144">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2c3f8-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2c3f8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c3f8-145">NOTES</span></span>

## <span data-ttu-id="2c3f8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c3f8-146">RELATED LINKS</span></span>