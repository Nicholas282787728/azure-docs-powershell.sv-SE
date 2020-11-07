---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 9f0145cee1facbd409406b86b2a6fc15f034737a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747232"
---
# <span data-ttu-id="d7297-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d7297-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="d7297-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7297-102">SYNOPSIS</span></span>
<span data-ttu-id="d7297-103">Skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="d7297-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d7297-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7297-104">SYNTAX</span></span>

### <span data-ttu-id="d7297-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7297-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7297-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d7297-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7297-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7297-107">DESCRIPTION</span></span>
<span data-ttu-id="d7297-108">New-AzRelayHybridConnection cmdlet skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="d7297-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d7297-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7297-109">EXAMPLES</span></span>

### <span data-ttu-id="d7297-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="d7297-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="d7297-111">Skapar en ny HybirdConnection \` TestHybirdConnection2 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="d7297-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="d7297-112">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="d7297-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="d7297-113">Skapar en ny HybirdConnection \` TestHybirdConnection1 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="d7297-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="d7297-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7297-114">PARAMETERS</span></span>

### <span data-ttu-id="d7297-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7297-115">-DefaultProfile</span></span>
<span data-ttu-id="d7297-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7297-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7297-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7297-117">-InputObject</span></span>
<span data-ttu-id="d7297-118">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="d7297-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7297-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7297-119">-Name</span></span>
<span data-ttu-id="d7297-120">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="d7297-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7297-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d7297-121">-Namespace</span></span>
<span data-ttu-id="d7297-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="d7297-122">Namespace Name.</span></span>

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

### <span data-ttu-id="d7297-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7297-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="d7297-124">sant om klient godkännande behövs för denna HybridConnections; annars falskt</span><span class="sxs-lookup"><span data-stu-id="d7297-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7297-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7297-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7297-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d7297-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="d7297-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d7297-127">-UserMetadata</span></span>
<span data-ttu-id="d7297-128">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="d7297-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7297-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7297-129">-Confirm</span></span>
<span data-ttu-id="d7297-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7297-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7297-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7297-131">-WhatIf</span></span>
<span data-ttu-id="d7297-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7297-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7297-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7297-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7297-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7297-134">CommonParameters</span></span>
<span data-ttu-id="d7297-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7297-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7297-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7297-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7297-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7297-137">INPUTS</span></span>

### <span data-ttu-id="d7297-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d7297-138">System.String</span></span>

### <span data-ttu-id="d7297-139">Microsoft. Azure. commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="d7297-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

### <span data-ttu-id="d7297-140">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7297-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d7297-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7297-141">OUTPUTS</span></span>

### <span data-ttu-id="d7297-142">Microsoft. Azure. commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="d7297-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="d7297-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7297-143">NOTES</span></span>

## <span data-ttu-id="d7297-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7297-144">RELATED LINKS</span></span>
