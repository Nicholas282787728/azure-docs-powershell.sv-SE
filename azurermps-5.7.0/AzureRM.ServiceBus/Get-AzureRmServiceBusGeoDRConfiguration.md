---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575504"
---
# <span data-ttu-id="03cfc-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="03cfc-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="03cfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="03cfc-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="03cfc-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03cfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03cfc-104">SYNTAX</span></span>

### <span data-ttu-id="03cfc-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="03cfc-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03cfc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="03cfc-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03cfc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03cfc-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03cfc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03cfc-108">DESCRIPTION</span></span>
<span data-ttu-id="03cfc-109">Det **uppringda aliaset get-AzureRmServiceBusGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="03cfc-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="03cfc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03cfc-110">EXAMPLES</span></span>

### <span data-ttu-id="03cfc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03cfc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="03cfc-112">Hämtar alias "SampleDRCongifName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="03cfc-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="03cfc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03cfc-113">PARAMETERS</span></span>

### <span data-ttu-id="03cfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03cfc-114">-DefaultProfile</span></span>
<span data-ttu-id="03cfc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03cfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03cfc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03cfc-116">-InputObject</span></span>
<span data-ttu-id="03cfc-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="03cfc-117">Namespace Object</span></span>

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

### <span data-ttu-id="03cfc-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="03cfc-118">-Name</span></span>
<span data-ttu-id="03cfc-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="03cfc-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03cfc-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="03cfc-120">-Namespace</span></span>
<span data-ttu-id="03cfc-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="03cfc-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03cfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03cfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="03cfc-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="03cfc-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03cfc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03cfc-124">-ResourceId</span></span>
<span data-ttu-id="03cfc-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="03cfc-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03cfc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03cfc-126">CommonParameters</span></span>
<span data-ttu-id="03cfc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03cfc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03cfc-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03cfc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03cfc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03cfc-129">INPUTS</span></span>

### <span data-ttu-id="03cfc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03cfc-130">System.String</span></span>
<span data-ttu-id="03cfc-131">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="03cfc-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="03cfc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03cfc-132">OUTPUTS</span></span>

### <span data-ttu-id="03cfc-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="03cfc-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="03cfc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03cfc-134">NOTES</span></span>

## <span data-ttu-id="03cfc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03cfc-135">RELATED LINKS</span></span>
