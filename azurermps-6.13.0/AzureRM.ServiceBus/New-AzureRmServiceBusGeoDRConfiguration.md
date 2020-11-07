---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756124"
---
# <span data-ttu-id="12a82-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="12a82-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="12a82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12a82-102">SYNOPSIS</span></span>
<span data-ttu-id="12a82-103">Skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="12a82-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12a82-104">SYNTAX</span></span>

### <span data-ttu-id="12a82-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="12a82-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a82-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12a82-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a82-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a82-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12a82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12a82-108">DESCRIPTION</span></span>
<span data-ttu-id="12a82-109">Cmdleten **New-AzureRmServiceBusGeoDRConfiguration** skapar ett nytt alias (konfiguration för katastrof återställning)</span><span class="sxs-lookup"><span data-stu-id="12a82-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="12a82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12a82-110">EXAMPLES</span></span>

### <span data-ttu-id="12a82-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12a82-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="12a82-112">Skapar ett alias "SampleDRCongifName" med det primära namn området "SampleNamespace_Primary" med sekundärt namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="12a82-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="12a82-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12a82-113">PARAMETERS</span></span>

### <span data-ttu-id="12a82-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="12a82-114">-AlternateName</span></span>
<span data-ttu-id="12a82-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="12a82-115">AlternateName</span></span>

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

### <span data-ttu-id="12a82-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12a82-116">-AsJob</span></span>
<span data-ttu-id="12a82-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="12a82-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12a82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a82-118">-DefaultProfile</span></span>
<span data-ttu-id="12a82-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12a82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a82-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12a82-120">-InputObject</span></span>
<span data-ttu-id="12a82-121">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="12a82-121">Namespace Object</span></span>

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

### <span data-ttu-id="12a82-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="12a82-122">-Name</span></span>
<span data-ttu-id="12a82-123">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="12a82-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="12a82-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="12a82-124">-Namespace</span></span>
<span data-ttu-id="12a82-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="12a82-125">Namespace Name</span></span>

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

### <span data-ttu-id="12a82-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="12a82-126">-PartnerNamespace</span></span>
<span data-ttu-id="12a82-127">DR-konfiguration PartnerNamespace (ARM-ID för PartnerNamespace [sekundärt namn område])</span><span class="sxs-lookup"><span data-stu-id="12a82-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="12a82-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a82-128">-ResourceGroupName</span></span>
<span data-ttu-id="12a82-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="12a82-129">Resource Group Name</span></span>

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

### <span data-ttu-id="12a82-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12a82-130">-ResourceId</span></span>
<span data-ttu-id="12a82-131">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="12a82-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="12a82-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12a82-132">-Confirm</span></span>
<span data-ttu-id="12a82-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12a82-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12a82-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a82-134">-WhatIf</span></span>
<span data-ttu-id="12a82-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12a82-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a82-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12a82-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12a82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a82-137">CommonParameters</span></span>
<span data-ttu-id="12a82-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a82-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a82-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a82-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12a82-140">INPUTS</span></span>

### <span data-ttu-id="12a82-141">System. String</span><span class="sxs-lookup"><span data-stu-id="12a82-141">System.String</span></span>

### <span data-ttu-id="12a82-142">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="12a82-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="12a82-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12a82-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="12a82-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12a82-144">OUTPUTS</span></span>

### <span data-ttu-id="12a82-145">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="12a82-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="12a82-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12a82-146">NOTES</span></span>

## <span data-ttu-id="12a82-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12a82-147">RELATED LINKS</span></span>
