---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576280"
---
# <span data-ttu-id="ace61-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ace61-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="ace61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ace61-102">SYNOPSIS</span></span>
<span data-ttu-id="ace61-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="ace61-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ace61-104">SYNTAX</span></span>

### <span data-ttu-id="ace61-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ace61-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace61-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ace61-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace61-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ace61-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace61-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ace61-108">DESCRIPTION</span></span>
<span data-ttu-id="ace61-109">Det **uppringda aliaset get-AzureRmEventHubGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="ace61-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ace61-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ace61-110">EXAMPLES</span></span>

### <span data-ttu-id="ace61-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ace61-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="ace61-112">Hämtar alias "SampleDRCongifName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="ace61-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="ace61-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ace61-113">PARAMETERS</span></span>

### <span data-ttu-id="ace61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace61-114">-DefaultProfile</span></span>
<span data-ttu-id="ace61-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ace61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace61-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ace61-116">-InputObject</span></span>
<span data-ttu-id="ace61-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="ace61-117">Namespace Object</span></span>

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

### <span data-ttu-id="ace61-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ace61-118">-Name</span></span>
<span data-ttu-id="ace61-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ace61-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ace61-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ace61-120">-Namespace</span></span>
<span data-ttu-id="ace61-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ace61-121">Namespace Name</span></span>

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

### <span data-ttu-id="ace61-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace61-122">-ResourceGroupName</span></span>
<span data-ttu-id="ace61-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ace61-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ace61-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace61-124">-ResourceId</span></span>
<span data-ttu-id="ace61-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="ace61-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ace61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace61-126">CommonParameters</span></span>
<span data-ttu-id="ace61-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace61-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace61-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ace61-129">INPUTS</span></span>

### <span data-ttu-id="ace61-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ace61-130">System.String</span></span>

### <span data-ttu-id="ace61-131">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ace61-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="ace61-132">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ace61-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ace61-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ace61-133">OUTPUTS</span></span>

### <span data-ttu-id="ace61-134">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ace61-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="ace61-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ace61-135">NOTES</span></span>

## <span data-ttu-id="ace61-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ace61-136">RELATED LINKS</span></span>
