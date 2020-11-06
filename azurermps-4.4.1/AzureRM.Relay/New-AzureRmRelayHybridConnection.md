---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574540"
---
# <span data-ttu-id="b4caf-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="b4caf-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="b4caf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4caf-102">SYNOPSIS</span></span>
<span data-ttu-id="b4caf-103">Skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="b4caf-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4caf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4caf-104">SYNTAX</span></span>

### <span data-ttu-id="b4caf-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4caf-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4caf-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b4caf-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4caf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4caf-107">DESCRIPTION</span></span>
<span data-ttu-id="b4caf-108">New-AzureRmRelayHybridConnection cmdlet skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="b4caf-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="b4caf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4caf-109">EXAMPLES</span></span>

### <span data-ttu-id="b4caf-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="b4caf-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="b4caf-111">Skapar en ny HybirdConnection \` TestHybirdConnection2 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="b4caf-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="b4caf-112">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="b4caf-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="b4caf-113">Skapar en ny HybirdConnection \` TestHybirdConnection1 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="b4caf-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="b4caf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4caf-114">PARAMETERS</span></span>

### <span data-ttu-id="b4caf-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b4caf-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b4caf-116">sant om klient godkännande behövs för denna HybridConnections; annars falskt</span><span class="sxs-lookup"><span data-stu-id="b4caf-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="b4caf-117">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b4caf-117">-UserMetadata</span></span>
<span data-ttu-id="b4caf-118">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="b4caf-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="b4caf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4caf-119">-Confirm</span></span>
<span data-ttu-id="b4caf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4caf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4caf-121">-WhatIf</span></span>
<span data-ttu-id="b4caf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4caf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4caf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4caf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4caf-124">-InputObject</span></span>
<span data-ttu-id="b4caf-125">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="b4caf-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4caf-126">-Name</span></span>
<span data-ttu-id="b4caf-127">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="b4caf-127">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-128">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b4caf-128">-Namespace</span></span>
<span data-ttu-id="b4caf-129">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b4caf-129">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4caf-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4caf-131">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b4caf-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4caf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4caf-132">-DefaultProfile</span></span>
<span data-ttu-id="b4caf-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4caf-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4caf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4caf-134">CommonParameters</span></span>
<span data-ttu-id="b4caf-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4caf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4caf-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4caf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4caf-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4caf-137">INPUTS</span></span>

### <span data-ttu-id="b4caf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4caf-138">-ResourceGroupName</span></span>
<span data-ttu-id="b4caf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4caf-139">System.String</span></span>

### <span data-ttu-id="b4caf-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b4caf-140">-NamespaceName</span></span>
<span data-ttu-id="b4caf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4caf-141">System.String</span></span>

### <span data-ttu-id="b4caf-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="b4caf-142">-HybridConnectionsName</span></span>
<span data-ttu-id="b4caf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b4caf-143">System.String</span></span>

### <span data-ttu-id="b4caf-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4caf-144">-InputObject</span></span>
<span data-ttu-id="b4caf-145">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="b4caf-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="b4caf-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b4caf-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b4caf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4caf-147">System.Boolean</span></span>

### <span data-ttu-id="b4caf-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b4caf-148">-UserMetadata</span></span>
<span data-ttu-id="b4caf-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b4caf-149">System.String</span></span>

## <span data-ttu-id="b4caf-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4caf-150">OUTPUTS</span></span>

### <span data-ttu-id="b4caf-151">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="b4caf-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="b4caf-152">Exempel-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="b4caf-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="b4caf-153">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: User meta data-ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 Name: TestHybirdConnection2 typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="b4caf-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="b4caf-154">Exempel-2: egenskaper</span><span class="sxs-lookup"><span data-stu-id="b4caf-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="b4caf-155">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: User meta data-ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 namn: TestHybirdConnection1 typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="b4caf-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="b4caf-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4caf-156">NOTES</span></span>

## <span data-ttu-id="b4caf-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4caf-157">RELATED LINKS</span></span>

