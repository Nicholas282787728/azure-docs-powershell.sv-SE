---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388278"
---
# <span data-ttu-id="c0d47-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0d47-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c0d47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0d47-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d47-103">Hämtar alias (konfiguration för katastrof återställning) för primärt eller sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="c0d47-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c0d47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0d47-104">SYNTAX</span></span>

### <span data-ttu-id="c0d47-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c0d47-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d47-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0d47-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d47-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d47-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0d47-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0d47-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d47-109">Det **uppringda aliaset get-AzEventHubGeoDRConfiguration** returnerar (återställning efter katastrof återställning) för primärt eller sekundär namn området</span><span class="sxs-lookup"><span data-stu-id="c0d47-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c0d47-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0d47-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d47-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0d47-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="c0d47-112">Hämtar alias "SampleDRConfigName"-konfiguration för det primära namn området "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="c0d47-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c0d47-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0d47-113">PARAMETERS</span></span>

### <span data-ttu-id="c0d47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d47-114">-DefaultProfile</span></span>
<span data-ttu-id="c0d47-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d47-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0d47-116">-InputObject</span></span>
<span data-ttu-id="c0d47-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="c0d47-117">Namespace Object</span></span>

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

### <span data-ttu-id="c0d47-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0d47-118">-Name</span></span>
<span data-ttu-id="c0d47-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c0d47-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c0d47-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c0d47-120">-Namespace</span></span>
<span data-ttu-id="c0d47-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c0d47-121">Namespace Name</span></span>

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

### <span data-ttu-id="c0d47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d47-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0d47-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c0d47-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c0d47-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d47-124">-ResourceId</span></span>
<span data-ttu-id="c0d47-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="c0d47-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c0d47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d47-126">CommonParameters</span></span>
<span data-ttu-id="c0d47-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d47-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d47-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d47-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0d47-129">INPUTS</span></span>

### <span data-ttu-id="c0d47-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d47-130">System.String</span></span>

### <span data-ttu-id="c0d47-131">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c0d47-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c0d47-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0d47-132">OUTPUTS</span></span>

### <span data-ttu-id="c0d47-133">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c0d47-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c0d47-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0d47-134">NOTES</span></span>

## <span data-ttu-id="c0d47-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0d47-135">RELATED LINKS</span></span>
