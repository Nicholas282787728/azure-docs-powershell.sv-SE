---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574948"
---
# <span data-ttu-id="50bef-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="50bef-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="50bef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50bef-102">SYNOPSIS</span></span>
<span data-ttu-id="50bef-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="50bef-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50bef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50bef-104">SYNTAX</span></span>

### <span data-ttu-id="50bef-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="50bef-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bef-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50bef-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bef-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50bef-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50bef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50bef-108">DESCRIPTION</span></span>
<span data-ttu-id="50bef-109">Cmdleten **New-AzureRmEventHubGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="50bef-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="50bef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50bef-110">EXAMPLES</span></span>

### <span data-ttu-id="50bef-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="50bef-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="50bef-112">Skapar ett alias "SampleDRCongifName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="50bef-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="50bef-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50bef-113">PARAMETERS</span></span>

### <span data-ttu-id="50bef-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="50bef-114">-AlternateName</span></span>
<span data-ttu-id="50bef-115">AlternateName krävs när DR-konfigurationsfilen är samma som det primära namn området</span><span class="sxs-lookup"><span data-stu-id="50bef-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="50bef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50bef-116">-AsJob</span></span>
<span data-ttu-id="50bef-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50bef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50bef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bef-118">-DefaultProfile</span></span>
<span data-ttu-id="50bef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50bef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50bef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50bef-120">-InputObject</span></span>
<span data-ttu-id="50bef-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="50bef-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="50bef-122">-Name</span></span>
<span data-ttu-id="50bef-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="50bef-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="50bef-124">-Namespace</span></span>
<span data-ttu-id="50bef-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="50bef-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="50bef-126">-PartnerNamespace</span></span>
<span data-ttu-id="50bef-127">PartnerNamespace för DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="50bef-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bef-128">-ResourceGroupName</span></span>
<span data-ttu-id="50bef-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="50bef-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50bef-130">-ResourceId</span></span>
<span data-ttu-id="50bef-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="50bef-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50bef-132">-Confirm</span></span>
<span data-ttu-id="50bef-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50bef-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bef-134">-WhatIf</span></span>
<span data-ttu-id="50bef-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50bef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50bef-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50bef-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bef-137">CommonParameters</span></span>
<span data-ttu-id="50bef-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="50bef-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50bef-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bef-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50bef-140">INPUTS</span></span>

### <span data-ttu-id="50bef-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50bef-141">System.String</span></span>
<span data-ttu-id="50bef-142">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="50bef-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="50bef-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50bef-143">OUTPUTS</span></span>

### <span data-ttu-id="50bef-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="50bef-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="50bef-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50bef-145">NOTES</span></span>

## <span data-ttu-id="50bef-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50bef-146">RELATED LINKS</span></span>
