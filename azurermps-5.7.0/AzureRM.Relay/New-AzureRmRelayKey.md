---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582012"
---
# <span data-ttu-id="f07ca-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="f07ca-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="f07ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f07ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f07ca-103">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="f07ca-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f07ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f07ca-104">SYNTAX</span></span>

### <span data-ttu-id="f07ca-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f07ca-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07ca-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f07ca-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07ca-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f07ca-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f07ca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f07ca-108">DESCRIPTION</span></span>
<span data-ttu-id="f07ca-109">Cmdleten **New-AzureRmRelayKey** skapar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f07ca-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f07ca-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f07ca-110">EXAMPLES</span></span>

### <span data-ttu-id="f07ca-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="f07ca-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="f07ca-112">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f07ca-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="f07ca-113">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f07ca-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="f07ca-114">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f07ca-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f07ca-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f07ca-115">PARAMETERS</span></span>

### <span data-ttu-id="f07ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07ca-116">-DefaultProfile</span></span>
<span data-ttu-id="f07ca-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f07ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f07ca-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f07ca-118">-HybridConnection</span></span>
<span data-ttu-id="f07ca-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="f07ca-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f07ca-120">-Name</span></span>
<span data-ttu-id="f07ca-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="f07ca-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f07ca-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f07ca-122">-Namespace</span></span>
<span data-ttu-id="f07ca-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="f07ca-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f07ca-124">-RegenerateKey</span></span>
<span data-ttu-id="f07ca-125">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="f07ca-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="f07ca-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f07ca-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f07ca-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f07ca-128">-WcfRelay</span></span>
<span data-ttu-id="f07ca-129">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="f07ca-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f07ca-130">-Confirm</span></span>
<span data-ttu-id="f07ca-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f07ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07ca-132">-WhatIf</span></span>
<span data-ttu-id="f07ca-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f07ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07ca-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f07ca-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07ca-135">CommonParameters</span></span>
<span data-ttu-id="f07ca-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07ca-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07ca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07ca-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f07ca-138">INPUTS</span></span>

### <span data-ttu-id="f07ca-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="f07ca-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="f07ca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-140">System.String</span></span> 

### <span data-ttu-id="f07ca-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f07ca-141">-NamespaceName</span></span>
 <span data-ttu-id="f07ca-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-142">System.String</span></span> 
 

### <span data-ttu-id="f07ca-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="f07ca-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="f07ca-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-144">System.String</span></span> 

### <span data-ttu-id="f07ca-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="f07ca-145">-WcfRelayName</span></span>
 <span data-ttu-id="f07ca-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-146">System.String</span></span> 

### <span data-ttu-id="f07ca-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="f07ca-147">-Name</span></span>
 <span data-ttu-id="f07ca-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-148">System.String</span></span>

### <span data-ttu-id="f07ca-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f07ca-149">-RegenerateKeys</span></span>
 <span data-ttu-id="f07ca-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f07ca-150">System.String</span></span>

## <span data-ttu-id="f07ca-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f07ca-151">OUTPUTS</span></span>

### <span data-ttu-id="f07ca-152">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f07ca-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="f07ca-153">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="f07ca-153">Example 1 - Namespace</span></span>
<span data-ttu-id="f07ca-154">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 01 # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f07ca-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="f07ca-155">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f07ca-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="f07ca-156">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f07ca-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="f07ca-157">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f07ca-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="f07ca-158">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f07ca-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="f07ca-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f07ca-159">NOTES</span></span>

## <span data-ttu-id="f07ca-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f07ca-160">RELATED LINKS</span></span>

