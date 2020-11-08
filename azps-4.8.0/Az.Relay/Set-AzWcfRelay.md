---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258730"
---
# <span data-ttu-id="afb19-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="afb19-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="afb19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afb19-102">SYNOPSIS</span></span>
<span data-ttu-id="afb19-103">Uppdaterar beskrivningen av en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="afb19-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="afb19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afb19-104">SYNTAX</span></span>

### <span data-ttu-id="afb19-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afb19-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb19-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="afb19-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb19-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afb19-107">DESCRIPTION</span></span>
<span data-ttu-id="afb19-108">Set-AzWcfRelay cmdlet uppdaterar beskrivningen för WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="afb19-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="afb19-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afb19-109">EXAMPLES</span></span>

### <span data-ttu-id="afb19-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="afb19-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="afb19-111">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="afb19-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="afb19-112">Uppdaterar angivet WcfRelay med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="afb19-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="afb19-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="afb19-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="afb19-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afb19-114">PARAMETERS</span></span>

### <span data-ttu-id="afb19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb19-115">-DefaultProfile</span></span>
<span data-ttu-id="afb19-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afb19-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb19-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afb19-117">-InputObject</span></span>
<span data-ttu-id="afb19-118">WcfRelay-objekt.</span><span class="sxs-lookup"><span data-stu-id="afb19-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="afb19-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="afb19-119">-Name</span></span>
<span data-ttu-id="afb19-120">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="afb19-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="afb19-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="afb19-121">-Namespace</span></span>
<span data-ttu-id="afb19-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="afb19-122">Namespace Name.</span></span>

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

### <span data-ttu-id="afb19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb19-123">-ResourceGroupName</span></span>
<span data-ttu-id="afb19-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="afb19-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="afb19-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="afb19-125">-UserMetadata</span></span>
<span data-ttu-id="afb19-126">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för WcfRelay-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="afb19-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="afb19-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afb19-127">-Confirm</span></span>
<span data-ttu-id="afb19-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afb19-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb19-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb19-129">-WhatIf</span></span>
<span data-ttu-id="afb19-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afb19-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb19-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afb19-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb19-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb19-132">CommonParameters</span></span>
<span data-ttu-id="afb19-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb19-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb19-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb19-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb19-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afb19-135">INPUTS</span></span>

### <span data-ttu-id="afb19-136">System. String</span><span class="sxs-lookup"><span data-stu-id="afb19-136">System.String</span></span>

### <span data-ttu-id="afb19-137">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="afb19-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="afb19-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afb19-138">OUTPUTS</span></span>

### <span data-ttu-id="afb19-139">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="afb19-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="afb19-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afb19-140">NOTES</span></span>

## <span data-ttu-id="afb19-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afb19-141">RELATED LINKS</span></span>
