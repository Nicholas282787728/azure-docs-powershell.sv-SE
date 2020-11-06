---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575877"
---
# <span data-ttu-id="82d7f-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="82d7f-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="82d7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="82d7f-103">Hämtar en beskrivning för den angivna HybridConnection i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="82d7f-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82d7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82d7f-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="82d7f-106">Cmdleten **Get-AzureRmRelayHybridConnection** hämtar en beskrivning för den angivna HybridConnection i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="82d7f-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="82d7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82d7f-107">EXAMPLES</span></span>

### <span data-ttu-id="82d7f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82d7f-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="82d7f-109">Returnerar beskrivningen av HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="82d7f-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="82d7f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82d7f-110">PARAMETERS</span></span>

### <span data-ttu-id="82d7f-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="82d7f-111">-Name</span></span>
<span data-ttu-id="82d7f-112">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="82d7f-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="82d7f-113">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="82d7f-113">-Namespace</span></span>
<span data-ttu-id="82d7f-114">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="82d7f-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82d7f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d7f-115">-ResourceGroupName</span></span>
<span data-ttu-id="82d7f-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="82d7f-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82d7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d7f-117">-DefaultProfile</span></span>
<span data-ttu-id="82d7f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82d7f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82d7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d7f-119">CommonParameters</span></span>
<span data-ttu-id="82d7f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d7f-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d7f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d7f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82d7f-122">INPUTS</span></span>

### <span data-ttu-id="82d7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d7f-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="82d7f-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="82d7f-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="82d7f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="82d7f-125">-Name</span></span>
    System.String

## <span data-ttu-id="82d7f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82d7f-126">OUTPUTS</span></span>

### <span data-ttu-id="82d7f-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="82d7f-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="82d7f-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: User meta data-ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection namn: TestHybridConnection typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="82d7f-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="82d7f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82d7f-129">NOTES</span></span>

## <span data-ttu-id="82d7f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82d7f-130">RELATED LINKS</span></span>

