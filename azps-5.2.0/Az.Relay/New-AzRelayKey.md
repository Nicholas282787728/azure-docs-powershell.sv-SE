---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395024"
---
# <span data-ttu-id="1dd82-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="1dd82-101">New-AzRelayKey</span></span>

## <span data-ttu-id="1dd82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dd82-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd82-103">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="1dd82-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="1dd82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dd82-104">SYNTAX</span></span>

### <span data-ttu-id="1dd82-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1dd82-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd82-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dd82-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dd82-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dd82-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dd82-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd82-109">Cmdleten **New-AzRelayKey** skapar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1dd82-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1dd82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dd82-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd82-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="1dd82-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-112">Återskapar primära eller sekundära anslutnings strängar för angiven Relay-Namespace-enhet.</span><span class="sxs-lookup"><span data-stu-id="1dd82-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="1dd82-113">Exempel på 1,1-namn områdes-nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="1dd82-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-114">skapar de primära eller sekundära anslutnings strängarna för den angivna Relay-Namespace-enheten med nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="1dd82-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="1dd82-115">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1dd82-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-116">Återskapar primära eller sekundära anslutnings strängar för angiven Relay-WcfRelay-enhet.</span><span class="sxs-lookup"><span data-stu-id="1dd82-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="1dd82-117">Exempel på 2,1-WcfRelay angivet värde</span><span class="sxs-lookup"><span data-stu-id="1dd82-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-118">skapar de primära eller sekundära anslutnings strängarna för den angivna Relay-WcfRelay-enheten med nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="1dd82-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="1dd82-119">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1dd82-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-120">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1dd82-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="1dd82-121">Exempel på 3,1-HybridConnection angivet värde</span><span class="sxs-lookup"><span data-stu-id="1dd82-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1dd82-122">skapar de primära eller sekundära anslutnings strängarna för den angivna Relay-HybridConnection-enheten med nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="1dd82-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="1dd82-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dd82-123">PARAMETERS</span></span>

### <span data-ttu-id="1dd82-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd82-124">-DefaultProfile</span></span>
<span data-ttu-id="1dd82-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd82-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd82-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1dd82-126">-HybridConnection</span></span>
<span data-ttu-id="1dd82-127">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="1dd82-127">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd82-128">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="1dd82-128">-KeyValue</span></span>
<span data-ttu-id="1dd82-129">En Base64-kodad 256-bitars nyckel för signering och verifiering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="1dd82-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd82-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dd82-130">-Name</span></span>
<span data-ttu-id="1dd82-131">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="1dd82-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1dd82-132">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1dd82-132">-Namespace</span></span>
<span data-ttu-id="1dd82-133">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1dd82-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd82-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1dd82-134">-RegenerateKey</span></span>
<span data-ttu-id="1dd82-135">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="1dd82-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd82-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd82-136">-ResourceGroupName</span></span>
<span data-ttu-id="1dd82-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1dd82-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="1dd82-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1dd82-138">-WcfRelay</span></span>
<span data-ttu-id="1dd82-139">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="1dd82-139">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd82-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dd82-140">-Confirm</span></span>
<span data-ttu-id="1dd82-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dd82-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd82-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd82-142">-WhatIf</span></span>
<span data-ttu-id="1dd82-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dd82-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd82-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dd82-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd82-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd82-145">CommonParameters</span></span>
<span data-ttu-id="1dd82-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd82-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd82-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd82-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd82-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dd82-148">INPUTS</span></span>

### <span data-ttu-id="1dd82-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd82-149">System.String</span></span>

## <span data-ttu-id="1dd82-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dd82-150">OUTPUTS</span></span>

### <span data-ttu-id="1dd82-151">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1dd82-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="1dd82-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dd82-152">NOTES</span></span>

## <span data-ttu-id="1dd82-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dd82-153">RELATED LINKS</span></span>
