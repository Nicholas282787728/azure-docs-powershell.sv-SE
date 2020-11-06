---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575541"
---
# <span data-ttu-id="707c3-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="707c3-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="707c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="707c3-102">SYNOPSIS</span></span>
<span data-ttu-id="707c3-103">Uppdaterar beskrivningen av en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="707c3-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="707c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="707c3-104">SYNTAX</span></span>

### <span data-ttu-id="707c3-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="707c3-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="707c3-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="707c3-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707c3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="707c3-107">DESCRIPTION</span></span>
<span data-ttu-id="707c3-108">Set-AzureRmWcfRelay cmdlet uppdaterar beskrivningen för WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="707c3-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="707c3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="707c3-109">EXAMPLES</span></span>

### <span data-ttu-id="707c3-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="707c3-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="707c3-111">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="707c3-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="707c3-112">Uppdaterar angivet WcfRelay med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="707c3-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="707c3-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="707c3-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="707c3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="707c3-114">PARAMETERS</span></span>

### <span data-ttu-id="707c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707c3-115">-DefaultProfile</span></span>
<span data-ttu-id="707c3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="707c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="707c3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707c3-117">-InputObject</span></span>
<span data-ttu-id="707c3-118">WcfRelay-objekt.</span><span class="sxs-lookup"><span data-stu-id="707c3-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="707c3-119">-Name</span></span>
<span data-ttu-id="707c3-120">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="707c3-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c3-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="707c3-121">-Namespace</span></span>
<span data-ttu-id="707c3-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="707c3-122">Namespace Name.</span></span>

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

### <span data-ttu-id="707c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="707c3-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="707c3-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="707c3-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="707c3-125">-UserMetadata</span></span>
<span data-ttu-id="707c3-126">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="707c3-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="707c3-127">-Confirm</span></span>
<span data-ttu-id="707c3-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="707c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="707c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707c3-129">-WhatIf</span></span>
<span data-ttu-id="707c3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="707c3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707c3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="707c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="707c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707c3-132">CommonParameters</span></span>
<span data-ttu-id="707c3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707c3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707c3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707c3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="707c3-135">INPUTS</span></span>

### <span data-ttu-id="707c3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707c3-136">-ResourceGroupName</span></span>
<span data-ttu-id="707c3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="707c3-137">System.String</span></span>

### <span data-ttu-id="707c3-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="707c3-138">-NamespaceName</span></span>
<span data-ttu-id="707c3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="707c3-139">System.String</span></span>

### <span data-ttu-id="707c3-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="707c3-140">-WcfRelayName</span></span>
<span data-ttu-id="707c3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="707c3-141">System.String</span></span>

### <span data-ttu-id="707c3-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707c3-142">-InputObject</span></span>
<span data-ttu-id="707c3-143">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="707c3-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="707c3-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="707c3-144">-WcfRelayType</span></span>
<span data-ttu-id="707c3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="707c3-145">System.String</span></span>

### <span data-ttu-id="707c3-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="707c3-146">-UserMetadata</span></span>
<span data-ttu-id="707c3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="707c3-147">System.String</span></span>

## <span data-ttu-id="707c3-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="707c3-148">OUTPUTS</span></span>

### <span data-ttu-id="707c3-149">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="707c3-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="707c3-150">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="707c3-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="707c3-151">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="707c3-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="707c3-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: UserMetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. den kan användas för att lagra DESC riptive-data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="707c3-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="707c3-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel i rad/namn områden/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 namn: TestWCFRelay2: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="707c3-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="707c3-154">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="707c3-154">Example 2 - Properties</span></span>

### <span data-ttu-id="707c3-155">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="707c3-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="707c3-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: meta data-ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel i rad/namnrymder/TestNameSpace-Relay1/WcfRelays/TestWCFRelay namn: TestWCFRelay typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="707c3-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="707c3-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="707c3-157">NOTES</span></span>

## <span data-ttu-id="707c3-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="707c3-158">RELATED LINKS</span></span>

