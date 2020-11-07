---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927406"
---
# <span data-ttu-id="81728-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="81728-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="81728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81728-102">SYNOPSIS</span></span>
<span data-ttu-id="81728-103">Uppdaterar beskrivningen av en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="81728-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="81728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81728-104">SYNTAX</span></span>

### <span data-ttu-id="81728-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="81728-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81728-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="81728-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81728-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81728-107">DESCRIPTION</span></span>
<span data-ttu-id="81728-108">Set-AzWcfRelay cmdlet uppdaterar beskrivningen för WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="81728-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="81728-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81728-109">EXAMPLES</span></span>

### <span data-ttu-id="81728-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="81728-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="81728-111">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="81728-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="81728-112">Uppdaterar angivet WcfRelay med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="81728-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="81728-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="81728-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="81728-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81728-114">PARAMETERS</span></span>

### <span data-ttu-id="81728-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81728-115">-DefaultProfile</span></span>
<span data-ttu-id="81728-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81728-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81728-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81728-117">-InputObject</span></span>
<span data-ttu-id="81728-118">WcfRelay-objekt.</span><span class="sxs-lookup"><span data-stu-id="81728-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81728-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="81728-119">-Name</span></span>
<span data-ttu-id="81728-120">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="81728-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81728-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="81728-121">-Namespace</span></span>
<span data-ttu-id="81728-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="81728-122">Namespace Name.</span></span>

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

### <span data-ttu-id="81728-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81728-123">-ResourceGroupName</span></span>
<span data-ttu-id="81728-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="81728-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="81728-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="81728-125">-UserMetadata</span></span>
<span data-ttu-id="81728-126">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för WcfRelay-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="81728-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81728-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81728-127">-Confirm</span></span>
<span data-ttu-id="81728-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81728-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81728-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81728-129">-WhatIf</span></span>
<span data-ttu-id="81728-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81728-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81728-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81728-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81728-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81728-132">CommonParameters</span></span>
<span data-ttu-id="81728-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81728-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81728-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81728-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81728-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81728-135">INPUTS</span></span>

### <span data-ttu-id="81728-136">System. String</span><span class="sxs-lookup"><span data-stu-id="81728-136">System.String</span></span>

### <span data-ttu-id="81728-137">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="81728-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="81728-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81728-138">OUTPUTS</span></span>

### <span data-ttu-id="81728-139">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="81728-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="81728-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81728-140">NOTES</span></span>

## <span data-ttu-id="81728-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81728-141">RELATED LINKS</span></span>
