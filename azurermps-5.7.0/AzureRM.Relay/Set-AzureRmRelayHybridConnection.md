---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 88f44a2b399f36f8edf6a57d2f1dc5821029a156
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575547"
---
# <span data-ttu-id="bba41-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="bba41-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="bba41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bba41-102">SYNOPSIS</span></span>
<span data-ttu-id="bba41-103">Uppdaterar beskrivningen av en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="bba41-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bba41-104">SYNTAX</span></span>

### <span data-ttu-id="bba41-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bba41-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bba41-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="bba41-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba41-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bba41-107">DESCRIPTION</span></span>
<span data-ttu-id="bba41-108">Set-AzureRmRelayHybridConnection cmdlet uppdaterar beskrivningen för HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="bba41-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="bba41-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bba41-109">EXAMPLES</span></span>

### <span data-ttu-id="bba41-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bba41-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="bba41-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bba41-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="bba41-112">Uppdaterar angivet HybridConnection med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="bba41-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="bba41-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="bba41-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="bba41-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bba41-114">PARAMETERS</span></span>

### <span data-ttu-id="bba41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba41-115">-DefaultProfile</span></span>
<span data-ttu-id="bba41-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bba41-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bba41-117">-InputObject</span></span>
<span data-ttu-id="bba41-118">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="bba41-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bba41-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="bba41-119">-Name</span></span>
<span data-ttu-id="bba41-120">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="bba41-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="bba41-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="bba41-121">-Namespace</span></span>
<span data-ttu-id="bba41-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="bba41-122">Namespace Name.</span></span>

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

### <span data-ttu-id="bba41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba41-123">-ResourceGroupName</span></span>
<span data-ttu-id="bba41-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bba41-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="bba41-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="bba41-125">-UserMetadata</span></span>
<span data-ttu-id="bba41-126">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="bba41-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="bba41-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bba41-127">-Confirm</span></span>
<span data-ttu-id="bba41-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bba41-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba41-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba41-129">-WhatIf</span></span>
<span data-ttu-id="bba41-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bba41-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba41-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bba41-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba41-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba41-132">CommonParameters</span></span>
<span data-ttu-id="bba41-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba41-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba41-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba41-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba41-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bba41-135">INPUTS</span></span>

### <span data-ttu-id="bba41-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba41-136">-ResourceGroupName</span></span>
<span data-ttu-id="bba41-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bba41-137">System.String</span></span>

### <span data-ttu-id="bba41-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bba41-138">-NamespaceName</span></span>
<span data-ttu-id="bba41-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bba41-139">System.String</span></span>

### <span data-ttu-id="bba41-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="bba41-140">-WcfRelayName</span></span>
<span data-ttu-id="bba41-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bba41-141">System.String</span></span>

### <span data-ttu-id="bba41-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bba41-142">-InputObject</span></span>
<span data-ttu-id="bba41-143">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="bba41-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="bba41-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="bba41-144">-UserMetadata</span></span>
<span data-ttu-id="bba41-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bba41-145">System.String</span></span>

## <span data-ttu-id="bba41-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bba41-146">OUTPUTS</span></span>

### <span data-ttu-id="bba41-147">Microsoft. Azure. commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="bba41-147">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="bba41-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bba41-148">NOTES</span></span>

## <span data-ttu-id="bba41-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bba41-149">RELATED LINKS</span></span>

