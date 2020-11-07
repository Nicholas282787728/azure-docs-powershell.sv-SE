---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9398c2229b31e432e55e5c4b11e72d3360b52fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756075"
---
# <span data-ttu-id="c405f-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="c405f-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="c405f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c405f-102">SYNOPSIS</span></span>
<span data-ttu-id="c405f-103">Skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="c405f-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c405f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c405f-104">SYNTAX</span></span>

### <span data-ttu-id="c405f-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c405f-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c405f-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c405f-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c405f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c405f-107">DESCRIPTION</span></span>
<span data-ttu-id="c405f-108">New-AzureRmRelayHybridConnection cmdlet skapar en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="c405f-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="c405f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c405f-109">EXAMPLES</span></span>

### <span data-ttu-id="c405f-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="c405f-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

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

<span data-ttu-id="c405f-111">Skapar en ny HybirdConnection \` TestHybirdConnection2 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="c405f-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="c405f-112">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="c405f-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

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

<span data-ttu-id="c405f-113">Skapar en ny HybirdConnection \` TestHybirdConnection1 \` i det angivna relä namn området \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="c405f-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="c405f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c405f-114">PARAMETERS</span></span>

### <span data-ttu-id="c405f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c405f-115">-DefaultProfile</span></span>
<span data-ttu-id="c405f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c405f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c405f-117">-InputObject</span></span>
<span data-ttu-id="c405f-118">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="c405f-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c405f-119">-Name</span></span>
<span data-ttu-id="c405f-120">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="c405f-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c405f-121">-Namespace</span></span>
<span data-ttu-id="c405f-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="c405f-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="c405f-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="c405f-124">sant om klient godkännande behövs för denna HybridConnections; annars falskt</span><span class="sxs-lookup"><span data-stu-id="c405f-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c405f-125">-ResourceGroupName</span></span>
<span data-ttu-id="c405f-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c405f-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c405f-127">-UserMetadata</span></span>
<span data-ttu-id="c405f-128">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="c405f-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c405f-129">-Confirm</span></span>
<span data-ttu-id="c405f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c405f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c405f-131">-WhatIf</span></span>
<span data-ttu-id="c405f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c405f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c405f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c405f-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c405f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c405f-134">CommonParameters</span></span>
<span data-ttu-id="c405f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c405f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c405f-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c405f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c405f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c405f-137">INPUTS</span></span>

### <span data-ttu-id="c405f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c405f-138">-ResourceGroupName</span></span>
<span data-ttu-id="c405f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c405f-139">System.String</span></span>

### <span data-ttu-id="c405f-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c405f-140">-NamespaceName</span></span>
<span data-ttu-id="c405f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c405f-141">System.String</span></span>

### <span data-ttu-id="c405f-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="c405f-142">-HybridConnectionsName</span></span>
<span data-ttu-id="c405f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c405f-143">System.String</span></span>

### <span data-ttu-id="c405f-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c405f-144">-InputObject</span></span>
<span data-ttu-id="c405f-145">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="c405f-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="c405f-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="c405f-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="c405f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c405f-147">System.Boolean</span></span>

### <span data-ttu-id="c405f-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c405f-148">-UserMetadata</span></span>
<span data-ttu-id="c405f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c405f-149">System.String</span></span>

## <span data-ttu-id="c405f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c405f-150">OUTPUTS</span></span>

### <span data-ttu-id="c405f-151">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="c405f-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="c405f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c405f-152">NOTES</span></span>

## <span data-ttu-id="c405f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c405f-153">RELATED LINKS</span></span>

