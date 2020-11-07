---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 1e844ecfbcbbbef32471c4aafe9091b1cc6dab0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747248"
---
# <span data-ttu-id="3f544-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="3f544-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="3f544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f544-102">SYNOPSIS</span></span>
<span data-ttu-id="3f544-103">Hämtar en beskrivning för den angivna HybridConnection i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="3f544-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3f544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f544-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f544-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f544-105">DESCRIPTION</span></span>
<span data-ttu-id="3f544-106">Cmdleten **Get-AzRelayHybridConnection** hämtar en beskrivning för den angivna HybridConnection i relä namn området.</span><span class="sxs-lookup"><span data-stu-id="3f544-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3f544-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f544-107">EXAMPLES</span></span>

### <span data-ttu-id="3f544-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f544-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="3f544-109">Returnerar beskrivningen av HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="3f544-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="3f544-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f544-110">PARAMETERS</span></span>

### <span data-ttu-id="3f544-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f544-111">-DefaultProfile</span></span>
<span data-ttu-id="3f544-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f544-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f544-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f544-113">-Name</span></span>
<span data-ttu-id="3f544-114">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="3f544-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="3f544-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="3f544-115">-Namespace</span></span>
<span data-ttu-id="3f544-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="3f544-116">Namespace Name.</span></span>

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

### <span data-ttu-id="3f544-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f544-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f544-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3f544-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f544-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f544-119">CommonParameters</span></span>
<span data-ttu-id="3f544-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f544-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f544-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f544-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f544-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f544-122">INPUTS</span></span>

### <span data-ttu-id="3f544-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3f544-123">System.String</span></span>

## <span data-ttu-id="3f544-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f544-124">OUTPUTS</span></span>

### <span data-ttu-id="3f544-125">Microsoft. Azure. commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="3f544-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="3f544-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f544-126">NOTES</span></span>

## <span data-ttu-id="3f544-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f544-127">RELATED LINKS</span></span>
