---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261692"
---
# <span data-ttu-id="fc279-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc279-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="fc279-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc279-102">SYNOPSIS</span></span>
<span data-ttu-id="fc279-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="fc279-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="fc279-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc279-104">SYNTAX</span></span>

### <span data-ttu-id="fc279-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fc279-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc279-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc279-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc279-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc279-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc279-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc279-108">DESCRIPTION</span></span>
<span data-ttu-id="fc279-109">Det **uppringda aliaset get-AzServiceBusGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="fc279-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="fc279-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc279-110">EXAMPLES</span></span>

### <span data-ttu-id="fc279-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc279-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="fc279-112">Hämtar alias "SampleDRConfigName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="fc279-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="fc279-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc279-113">PARAMETERS</span></span>

### <span data-ttu-id="fc279-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc279-114">-DefaultProfile</span></span>
<span data-ttu-id="fc279-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc279-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc279-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc279-116">-InputObject</span></span>
<span data-ttu-id="fc279-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="fc279-117">Namespace Object</span></span>

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

### <span data-ttu-id="fc279-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc279-118">-Name</span></span>
<span data-ttu-id="fc279-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="fc279-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="fc279-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fc279-120">-Namespace</span></span>
<span data-ttu-id="fc279-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="fc279-121">Namespace Name</span></span>

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

### <span data-ttu-id="fc279-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc279-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc279-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fc279-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fc279-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc279-124">-ResourceId</span></span>
<span data-ttu-id="fc279-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="fc279-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc279-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc279-126">CommonParameters</span></span>
<span data-ttu-id="fc279-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc279-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc279-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc279-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc279-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc279-129">INPUTS</span></span>

### <span data-ttu-id="fc279-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc279-130">System.String</span></span>

### <span data-ttu-id="fc279-131">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fc279-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fc279-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc279-132">OUTPUTS</span></span>

### <span data-ttu-id="fc279-133">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fc279-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="fc279-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc279-134">NOTES</span></span>

## <span data-ttu-id="fc279-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc279-135">RELATED LINKS</span></span>
