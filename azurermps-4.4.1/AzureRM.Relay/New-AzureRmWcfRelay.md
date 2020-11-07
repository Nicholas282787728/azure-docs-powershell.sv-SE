---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756863"
---
# <span data-ttu-id="1d473-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="1d473-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="1d473-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d473-102">SYNOPSIS</span></span>
<span data-ttu-id="1d473-103">Skapar en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="1d473-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d473-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d473-104">SYNTAX</span></span>

### <span data-ttu-id="1d473-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d473-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d473-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1d473-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d473-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d473-107">DESCRIPTION</span></span>
<span data-ttu-id="1d473-108">New-AzureRmWcfRelay cmdlet skapar en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="1d473-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="1d473-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d473-109">EXAMPLES</span></span>

### <span data-ttu-id="1d473-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="1d473-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="1d473-111">Skapar en ny WcfRelay \` TestWCFRelay2 \` i det angivna relä namn området \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="1d473-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="1d473-112">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="1d473-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="1d473-113">Skapar en ny WcfRelay \` TestWCFRelay \` i det angivna relä namn området \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="1d473-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="1d473-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d473-114">PARAMETERS</span></span>

### <span data-ttu-id="1d473-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d473-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="1d473-116">sant om klient godkännande behövs för detta relä. annars falskt</span><span class="sxs-lookup"><span data-stu-id="1d473-116">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d473-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="1d473-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="1d473-118">sant om transportsäkerhet behövs för detta relä. annars falskt</span><span class="sxs-lookup"><span data-stu-id="1d473-118">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d473-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1d473-119">-UserMetadata</span></span>
<span data-ttu-id="1d473-120">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="1d473-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="1d473-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="1d473-121">-WcfRelayType</span></span>
<span data-ttu-id="1d473-122">WcfRelay-typ.</span><span class="sxs-lookup"><span data-stu-id="1d473-122">WcfRelay Type.</span></span>
<span data-ttu-id="1d473-123">Möjliga värden är: ' NetTcp ' eller ' http '</span><span class="sxs-lookup"><span data-stu-id="1d473-123">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d473-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d473-124">-Confirm</span></span>
<span data-ttu-id="1d473-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d473-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d473-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d473-126">-WhatIf</span></span>
<span data-ttu-id="1d473-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d473-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d473-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d473-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d473-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d473-129">-InputObject</span></span>
<span data-ttu-id="1d473-130">WcfRelay-objekt.</span><span class="sxs-lookup"><span data-stu-id="1d473-130">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d473-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d473-131">-Name</span></span>
<span data-ttu-id="1d473-132">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="1d473-132">WcfRelay Name.</span></span>

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

### <span data-ttu-id="1d473-133">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1d473-133">-Namespace</span></span>
<span data-ttu-id="1d473-134">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1d473-134">Namespace Name.</span></span>

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

### <span data-ttu-id="1d473-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d473-135">-ResourceGroupName</span></span>
<span data-ttu-id="1d473-136">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1d473-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="1d473-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d473-137">-DefaultProfile</span></span>
<span data-ttu-id="1d473-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d473-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d473-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d473-139">CommonParameters</span></span>
<span data-ttu-id="1d473-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d473-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d473-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d473-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d473-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d473-142">INPUTS</span></span>

### <span data-ttu-id="1d473-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d473-143">-ResourceGroupName</span></span>
<span data-ttu-id="1d473-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1d473-144">System.String</span></span>

### <span data-ttu-id="1d473-145">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1d473-145">-NamespaceName</span></span>
<span data-ttu-id="1d473-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1d473-146">System.String</span></span>

### <span data-ttu-id="1d473-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1d473-147">-WcfRelayName</span></span>
<span data-ttu-id="1d473-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1d473-148">System.String</span></span>

### <span data-ttu-id="1d473-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d473-149">-InputObject</span></span>
<span data-ttu-id="1d473-150">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1d473-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="1d473-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="1d473-151">-WcfRelayType</span></span>
<span data-ttu-id="1d473-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1d473-152">System.String</span></span>

### <span data-ttu-id="1d473-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="1d473-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="1d473-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d473-154">System.Boolean</span></span>

### <span data-ttu-id="1d473-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="1d473-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="1d473-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d473-156">System.Boolean</span></span>

### <span data-ttu-id="1d473-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1d473-157">-UserMetadata</span></span>
<span data-ttu-id="1d473-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1d473-158">System.String</span></span>

## <span data-ttu-id="1d473-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d473-159">OUTPUTS</span></span>

### <span data-ttu-id="1d473-160">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="1d473-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="1d473-161">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1d473-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="1d473-162">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: falskt RequiresTransportSecurity: true IsDynamic: false UserMetadata: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel i rad/namnrymder/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 namn: TestWCFRelay2 typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="1d473-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="1d473-163">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="1d473-163">Example 2 - Properties</span></span>

### <span data-ttu-id="1d473-164">Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1d473-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="1d473-165">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: meta data-ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel i rad/namnrymder/TestNameSpace-Relay1/WcfRelays/TestWCFRelay namn: TestWCFRelay typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="1d473-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="1d473-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d473-166">NOTES</span></span>

## <span data-ttu-id="1d473-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d473-167">RELATED LINKS</span></span>

