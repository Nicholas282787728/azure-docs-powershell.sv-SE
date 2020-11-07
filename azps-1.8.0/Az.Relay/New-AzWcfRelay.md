---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 3d15269f525047677c20c679311cde877f25fbe4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747229"
---
# <span data-ttu-id="f8464-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8464-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="f8464-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8464-102">SYNOPSIS</span></span>
<span data-ttu-id="f8464-103">Skapar en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f8464-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f8464-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8464-104">SYNTAX</span></span>

### <span data-ttu-id="f8464-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8464-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8464-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f8464-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8464-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8464-107">DESCRIPTION</span></span>
<span data-ttu-id="f8464-108">New-AzWcfRelay cmdlet skapar en WcfRelay i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="f8464-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f8464-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8464-109">EXAMPLES</span></span>

### <span data-ttu-id="f8464-110">Exempel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="f8464-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="f8464-111">Skapar en ny WcfRelay \` TestWCFRelay2 \` i det angivna relä namn området \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="f8464-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="f8464-112">Exempel 2 – egenskaper</span><span class="sxs-lookup"><span data-stu-id="f8464-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="f8464-113">Skapar en ny WcfRelay \` TestWCFRelay \` i det angivna relä namn området \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="f8464-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="f8464-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8464-114">PARAMETERS</span></span>

### <span data-ttu-id="f8464-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8464-115">-DefaultProfile</span></span>
<span data-ttu-id="f8464-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8464-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8464-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8464-117">-InputObject</span></span>
<span data-ttu-id="f8464-118">WcfRelay-objekt.</span><span class="sxs-lookup"><span data-stu-id="f8464-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="f8464-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8464-119">-Name</span></span>
<span data-ttu-id="f8464-120">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="f8464-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f8464-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f8464-121">-Namespace</span></span>
<span data-ttu-id="f8464-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="f8464-122">Namespace Name.</span></span>

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

### <span data-ttu-id="f8464-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="f8464-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="f8464-124">sant om klient godkännande behövs för detta relä. annars falskt</span><span class="sxs-lookup"><span data-stu-id="f8464-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="f8464-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="f8464-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="f8464-126">sant om transportsäkerhet behövs för detta relä. annars falskt</span><span class="sxs-lookup"><span data-stu-id="f8464-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="f8464-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8464-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8464-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f8464-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8464-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="f8464-129">-UserMetadata</span></span>
<span data-ttu-id="f8464-130">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="f8464-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="f8464-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="f8464-131">-WcfRelayType</span></span>
<span data-ttu-id="f8464-132">WcfRelay-typ.</span><span class="sxs-lookup"><span data-stu-id="f8464-132">WcfRelay Type.</span></span>
<span data-ttu-id="f8464-133">Möjliga värden är: ' NetTcp ' eller ' http '</span><span class="sxs-lookup"><span data-stu-id="f8464-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="f8464-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8464-134">-Confirm</span></span>
<span data-ttu-id="f8464-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8464-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8464-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8464-136">-WhatIf</span></span>
<span data-ttu-id="f8464-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8464-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8464-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8464-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8464-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8464-139">CommonParameters</span></span>
<span data-ttu-id="f8464-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8464-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8464-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8464-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8464-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8464-142">INPUTS</span></span>

### <span data-ttu-id="f8464-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f8464-143">System.String</span></span>

### <span data-ttu-id="f8464-144">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f8464-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="f8464-145">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f8464-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f8464-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8464-146">OUTPUTS</span></span>

### <span data-ttu-id="f8464-147">Microsoft. Azure. commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f8464-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="f8464-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8464-148">NOTES</span></span>

## <span data-ttu-id="f8464-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8464-149">RELATED LINKS</span></span>