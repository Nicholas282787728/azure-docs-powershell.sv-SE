---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416608"
---
# <span data-ttu-id="1937f-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="1937f-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="1937f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1937f-102">SYNOPSIS</span></span>
<span data-ttu-id="1937f-103">Uppdaterar beskrivningen av en HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="1937f-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="1937f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1937f-104">SYNTAX</span></span>

### <span data-ttu-id="1937f-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1937f-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1937f-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1937f-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1937f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1937f-107">DESCRIPTION</span></span>
<span data-ttu-id="1937f-108">Set-AzRelayHybridConnection cmdlet uppdaterar beskrivningen för HybridConnection i det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="1937f-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="1937f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1937f-109">EXAMPLES</span></span>

### <span data-ttu-id="1937f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1937f-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

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

### <span data-ttu-id="1937f-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1937f-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

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

<span data-ttu-id="1937f-112">Uppdaterar angivet HybridConnection med en ny beskrivning i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="1937f-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="1937f-113">Det här exemplet uppdaterar egenskapen UserMetadata med nytt värde.</span><span class="sxs-lookup"><span data-stu-id="1937f-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="1937f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1937f-114">PARAMETERS</span></span>

### <span data-ttu-id="1937f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1937f-115">-DefaultProfile</span></span>
<span data-ttu-id="1937f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1937f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1937f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1937f-117">-InputObject</span></span>
<span data-ttu-id="1937f-118">HybridConnections-objekt.</span><span class="sxs-lookup"><span data-stu-id="1937f-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1937f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1937f-119">-Name</span></span>
<span data-ttu-id="1937f-120">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="1937f-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="1937f-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1937f-121">-Namespace</span></span>
<span data-ttu-id="1937f-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1937f-122">Namespace Name.</span></span>

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

### <span data-ttu-id="1937f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1937f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1937f-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1937f-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="1937f-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1937f-125">-UserMetadata</span></span>
<span data-ttu-id="1937f-126">Hämtar eller anger usermetadata är en plats hållare för lagring av användardefinierade sträng data för HybridConnection-slutpunkten. till exempel den kan användas för att lagra beskrivande data, till exempel en lista över team och deras kontakt information, även användardefinierade konfigurations inställningar.</span><span class="sxs-lookup"><span data-stu-id="1937f-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="1937f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1937f-127">-Confirm</span></span>
<span data-ttu-id="1937f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1937f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1937f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1937f-129">-WhatIf</span></span>
<span data-ttu-id="1937f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1937f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1937f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1937f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1937f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1937f-132">CommonParameters</span></span>
<span data-ttu-id="1937f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1937f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1937f-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1937f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1937f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1937f-135">INPUTS</span></span>

### <span data-ttu-id="1937f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1937f-136">System.String</span></span>

### <span data-ttu-id="1937f-137">Microsoft. Azure. commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="1937f-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="1937f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1937f-138">OUTPUTS</span></span>

### <span data-ttu-id="1937f-139">Microsoft. Azure. commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="1937f-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="1937f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1937f-140">NOTES</span></span>

## <span data-ttu-id="1937f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1937f-141">RELATED LINKS</span></span>
