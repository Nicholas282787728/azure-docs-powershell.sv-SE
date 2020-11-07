---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756566"
---
# <span data-ttu-id="7f21c-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="7f21c-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="7f21c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f21c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f21c-103">Uppdaterar beskrivningen av en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="7f21c-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f21c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f21c-104">SYNTAX</span></span>

### <span data-ttu-id="7f21c-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f21c-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f21c-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7f21c-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f21c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f21c-107">DESCRIPTION</span></span>
<span data-ttu-id="7f21c-108">Set-AzureRmRelayHybridConnection cmdlet uppdaterar beskrivningen för HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="7f21c-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="7f21c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f21c-109">EXAMPLES</span></span>

### <span data-ttu-id="7f21c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f21c-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="7f21c-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7f21c-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="7f21c-112">Uppdaterar angivet HybridConnection med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="7f21c-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="7f21c-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="7f21c-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="7f21c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f21c-114">PARAMETERS</span></span>

### <span data-ttu-id="7f21c-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7f21c-115">-UserMetadata</span></span>
<span data-ttu-id="7f21c-116">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="7f21c-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="7f21c-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f21c-117">-Confirm</span></span>
<span data-ttu-id="7f21c-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f21c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f21c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f21c-119">-WhatIf</span></span>
<span data-ttu-id="7f21c-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f21c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f21c-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f21c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f21c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f21c-122">-InputObject</span></span>
<span data-ttu-id="7f21c-123">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="7f21c-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f21c-124">-Name</span></span>
<span data-ttu-id="7f21c-125">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="7f21c-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="7f21c-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="7f21c-126">-Namespace</span></span>
<span data-ttu-id="7f21c-127">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="7f21c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="7f21c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f21c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f21c-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7f21c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f21c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f21c-130">-DefaultProfile</span></span>
<span data-ttu-id="7f21c-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f21c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f21c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f21c-132">CommonParameters</span></span>
<span data-ttu-id="7f21c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f21c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f21c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f21c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f21c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f21c-135">INPUTS</span></span>

### <span data-ttu-id="7f21c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f21c-136">-ResourceGroupName</span></span>
<span data-ttu-id="7f21c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7f21c-137">System.String</span></span>

### <span data-ttu-id="7f21c-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7f21c-138">-NamespaceName</span></span>
<span data-ttu-id="7f21c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7f21c-139">System.String</span></span>

### <span data-ttu-id="7f21c-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="7f21c-140">-WcfRelayName</span></span>
<span data-ttu-id="7f21c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7f21c-141">System.String</span></span>

### <span data-ttu-id="7f21c-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f21c-142">-InputObject</span></span>
<span data-ttu-id="7f21c-143">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="7f21c-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="7f21c-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7f21c-144">-UserMetadata</span></span>
<span data-ttu-id="7f21c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7f21c-145">System.String</span></span>

## <span data-ttu-id="7f21c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f21c-146">OUTPUTS</span></span>

### <span data-ttu-id="7f21c-147">Exempel-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="7f21c-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="7f21c-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 namn: TestHybirdConnection2 typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="7f21c-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="7f21c-149">Exempel-2: egenskaper</span><span class="sxs-lookup"><span data-stu-id="7f21c-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="7f21c-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata uppdaterades ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 namn: TestHybirdConnection1 typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="7f21c-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="7f21c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f21c-151">NOTES</span></span>

## <span data-ttu-id="7f21c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f21c-152">RELATED LINKS</span></span>

