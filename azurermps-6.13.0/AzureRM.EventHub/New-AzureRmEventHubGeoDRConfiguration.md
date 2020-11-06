---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: e2ac72ba5d563b4be902d424ad30c19b40bff9d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573969"
---
# <span data-ttu-id="b37ae-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b37ae-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="b37ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b37ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b37ae-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="b37ae-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b37ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b37ae-104">SYNTAX</span></span>

### <span data-ttu-id="b37ae-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b37ae-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37ae-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b37ae-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37ae-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37ae-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b37ae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b37ae-108">DESCRIPTION</span></span>
<span data-ttu-id="b37ae-109">Cmdleten **New-AzureRmEventHubGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="b37ae-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b37ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b37ae-110">EXAMPLES</span></span>

### <span data-ttu-id="b37ae-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b37ae-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="b37ae-112">Skapar ett alias "SampleDRCongifName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="b37ae-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="b37ae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b37ae-113">PARAMETERS</span></span>

### <span data-ttu-id="b37ae-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="b37ae-114">-AlternateName</span></span>
<span data-ttu-id="b37ae-115">AlternateName krävs när DR-konfigurationsfilen är samma som det primära namn området</span><span class="sxs-lookup"><span data-stu-id="b37ae-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="b37ae-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b37ae-116">-AsJob</span></span>
<span data-ttu-id="b37ae-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b37ae-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b37ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37ae-118">-DefaultProfile</span></span>
<span data-ttu-id="b37ae-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b37ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b37ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b37ae-120">-InputObject</span></span>
<span data-ttu-id="b37ae-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="b37ae-121">Namespace Object</span></span>

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

### <span data-ttu-id="b37ae-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b37ae-122">-Name</span></span>
<span data-ttu-id="b37ae-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b37ae-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="b37ae-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b37ae-124">-Namespace</span></span>
<span data-ttu-id="b37ae-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b37ae-125">Namespace Name</span></span>

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

### <span data-ttu-id="b37ae-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="b37ae-126">-PartnerNamespace</span></span>
<span data-ttu-id="b37ae-127">PartnerNamespace för DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b37ae-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="b37ae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37ae-128">-ResourceGroupName</span></span>
<span data-ttu-id="b37ae-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b37ae-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b37ae-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b37ae-130">-ResourceId</span></span>
<span data-ttu-id="b37ae-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="b37ae-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b37ae-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b37ae-132">-Confirm</span></span>
<span data-ttu-id="b37ae-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b37ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b37ae-134">-WhatIf</span></span>
<span data-ttu-id="b37ae-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b37ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b37ae-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b37ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37ae-137">CommonParameters</span></span>
<span data-ttu-id="b37ae-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37ae-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b37ae-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37ae-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b37ae-140">INPUTS</span></span>

### <span data-ttu-id="b37ae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b37ae-141">System.String</span></span>

### <span data-ttu-id="b37ae-142">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b37ae-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="b37ae-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b37ae-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b37ae-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b37ae-144">OUTPUTS</span></span>

### <span data-ttu-id="b37ae-145">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b37ae-145">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="b37ae-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b37ae-146">NOTES</span></span>

## <span data-ttu-id="b37ae-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b37ae-147">RELATED LINKS</span></span>
