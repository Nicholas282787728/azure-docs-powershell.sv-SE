---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 2d3d62c7921812e45f514f5811500ccb277cced7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919226"
---
# <span data-ttu-id="c606e-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c606e-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="c606e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c606e-102">SYNOPSIS</span></span>
<span data-ttu-id="c606e-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="c606e-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c606e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c606e-104">SYNTAX</span></span>

### <span data-ttu-id="c606e-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c606e-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c606e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c606e-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c606e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c606e-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c606e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c606e-108">DESCRIPTION</span></span>
<span data-ttu-id="c606e-109">Det **uppringda aliaset get-AzServiceBusGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="c606e-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c606e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c606e-110">EXAMPLES</span></span>

### <span data-ttu-id="c606e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c606e-111">Example 1</span></span>
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

<span data-ttu-id="c606e-112">Hämtar alias "SampleDRConfigName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="c606e-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c606e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c606e-113">PARAMETERS</span></span>

### <span data-ttu-id="c606e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c606e-114">-DefaultProfile</span></span>
<span data-ttu-id="c606e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c606e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c606e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c606e-116">-InputObject</span></span>
<span data-ttu-id="c606e-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="c606e-117">Namespace Object</span></span>

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

### <span data-ttu-id="c606e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c606e-118">-Name</span></span>
<span data-ttu-id="c606e-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c606e-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c606e-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c606e-120">-Namespace</span></span>
<span data-ttu-id="c606e-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c606e-121">Namespace Name</span></span>

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

### <span data-ttu-id="c606e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c606e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c606e-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c606e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c606e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c606e-124">-ResourceId</span></span>
<span data-ttu-id="c606e-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="c606e-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c606e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c606e-126">CommonParameters</span></span>
<span data-ttu-id="c606e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c606e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c606e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c606e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c606e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c606e-129">INPUTS</span></span>

### <span data-ttu-id="c606e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c606e-130">System.String</span></span>

### <span data-ttu-id="c606e-131">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c606e-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c606e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c606e-132">OUTPUTS</span></span>

### <span data-ttu-id="c606e-133">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c606e-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c606e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c606e-134">NOTES</span></span>

## <span data-ttu-id="c606e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c606e-135">RELATED LINKS</span></span>
