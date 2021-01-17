---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415400"
---
# <span data-ttu-id="cf3e8-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="cf3e8-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="cf3e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3e8-103">Returnerar en beskrivning för den angivna WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="cf3e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf3e8-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3e8-106">Cmdleten **Get-AzWcfRelay** returnerar en beskrivning av angiven WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="cf3e8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf3e8-107">EXAMPLES</span></span>

### <span data-ttu-id="cf3e8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cf3e8-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="cf3e8-109">Returnerar beskrivningen av WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="cf3e8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf3e8-110">PARAMETERS</span></span>

### <span data-ttu-id="cf3e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3e8-111">-DefaultProfile</span></span>
<span data-ttu-id="cf3e8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3e8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf3e8-113">-Name</span></span>
<span data-ttu-id="cf3e8-114">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3e8-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="cf3e8-115">-Namespace</span></span>
<span data-ttu-id="cf3e8-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-116">Namespace Name.</span></span>

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

### <span data-ttu-id="cf3e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf3e8-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="cf3e8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3e8-119">CommonParameters</span></span>
<span data-ttu-id="cf3e8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3e8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3e8-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3e8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3e8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf3e8-122">INPUTS</span></span>

### <span data-ttu-id="cf3e8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cf3e8-123">System.String</span></span>

## <span data-ttu-id="cf3e8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf3e8-124">OUTPUTS</span></span>

### <span data-ttu-id="cf3e8-125">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="cf3e8-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="cf3e8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf3e8-126">NOTES</span></span>

## <span data-ttu-id="cf3e8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf3e8-127">RELATED LINKS</span></span>
