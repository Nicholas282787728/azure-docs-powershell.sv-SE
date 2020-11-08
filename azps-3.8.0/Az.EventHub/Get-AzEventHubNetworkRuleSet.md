---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089598"
---
# <span data-ttu-id="b54f6-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b54f6-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="b54f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b54f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b54f6-103">Hämtar information om en händelse hubbar NetworkruleSet i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b54f6-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b54f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b54f6-104">SYNTAX</span></span>

### <span data-ttu-id="b54f6-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b54f6-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b54f6-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b54f6-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b54f6-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b54f6-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b54f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b54f6-108">DESCRIPTION</span></span>
<span data-ttu-id="b54f6-109">Hämtar information om en händelse hubbar NetworkruleSet i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b54f6-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b54f6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b54f6-110">EXAMPLES</span></span>

### <span data-ttu-id="b54f6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b54f6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="b54f6-112">Få information om NetworkruleSet med hjälp av ResourceGroup och namespace parametrar.</span><span class="sxs-lookup"><span data-stu-id="b54f6-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="b54f6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b54f6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="b54f6-114">Få information om NetworkruleSet med namn områden som finns i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b54f6-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="b54f6-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b54f6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="b54f6-116">Få information om NetworkruleSet med resurs-ID för andra namn områden</span><span class="sxs-lookup"><span data-stu-id="b54f6-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="b54f6-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b54f6-117">PARAMETERS</span></span>

### <span data-ttu-id="b54f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54f6-118">-DefaultProfile</span></span>
<span data-ttu-id="b54f6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b54f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b54f6-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b54f6-120">-Namespace</span></span>
<span data-ttu-id="b54f6-121">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b54f6-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="b54f6-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b54f6-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54f6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b54f6-124">-ResourceId</span></span>
<span data-ttu-id="b54f6-125">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="b54f6-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54f6-126">CommonParameters</span></span>
<span data-ttu-id="b54f6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b54f6-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54f6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54f6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b54f6-129">INPUTS</span></span>

### <span data-ttu-id="b54f6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b54f6-130">System.String</span></span>

## <span data-ttu-id="b54f6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b54f6-131">OUTPUTS</span></span>

### <span data-ttu-id="b54f6-132">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b54f6-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b54f6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b54f6-133">NOTES</span></span>

## <span data-ttu-id="b54f6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b54f6-134">RELATED LINKS</span></span>