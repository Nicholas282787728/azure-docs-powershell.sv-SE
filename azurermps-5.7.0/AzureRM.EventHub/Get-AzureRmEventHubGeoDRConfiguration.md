---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583167"
---
# <span data-ttu-id="75530-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="75530-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="75530-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75530-102">SYNOPSIS</span></span>
<span data-ttu-id="75530-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="75530-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75530-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75530-104">SYNTAX</span></span>

### <span data-ttu-id="75530-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="75530-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75530-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75530-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75530-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75530-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75530-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75530-108">DESCRIPTION</span></span>
<span data-ttu-id="75530-109">Det **uppringda aliaset get-AzureRmEventHubGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="75530-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="75530-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75530-110">EXAMPLES</span></span>

### <span data-ttu-id="75530-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75530-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="75530-112">Hämtar alias "SampleDRCongifName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="75530-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="75530-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75530-113">PARAMETERS</span></span>

### <span data-ttu-id="75530-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75530-114">-DefaultProfile</span></span>
<span data-ttu-id="75530-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75530-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75530-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75530-116">-InputObject</span></span>
<span data-ttu-id="75530-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="75530-117">Namespace Object</span></span>

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

### <span data-ttu-id="75530-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="75530-118">-Name</span></span>
<span data-ttu-id="75530-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="75530-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="75530-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="75530-120">-Namespace</span></span>
<span data-ttu-id="75530-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="75530-121">Namespace Name</span></span>

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

### <span data-ttu-id="75530-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75530-122">-ResourceGroupName</span></span>
<span data-ttu-id="75530-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="75530-123">Resource Group Name</span></span>

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

### <span data-ttu-id="75530-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75530-124">-ResourceId</span></span>
<span data-ttu-id="75530-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="75530-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="75530-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75530-126">CommonParameters</span></span>
<span data-ttu-id="75530-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75530-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75530-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75530-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75530-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75530-129">INPUTS</span></span>

### <span data-ttu-id="75530-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75530-130">System.String</span></span>
<span data-ttu-id="75530-131">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="75530-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="75530-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75530-132">OUTPUTS</span></span>

### <span data-ttu-id="75530-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes, Microsoft. Azure. commands. EventHub, version = 0.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="75530-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="75530-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75530-134">NOTES</span></span>

## <span data-ttu-id="75530-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75530-135">RELATED LINKS</span></span>
