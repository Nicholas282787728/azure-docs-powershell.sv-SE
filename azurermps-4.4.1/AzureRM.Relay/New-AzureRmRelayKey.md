---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582228"
---
# <span data-ttu-id="5454a-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="5454a-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="5454a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5454a-102">SYNOPSIS</span></span>
<span data-ttu-id="5454a-103">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="5454a-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5454a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5454a-104">SYNTAX</span></span>

### <span data-ttu-id="5454a-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5454a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5454a-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5454a-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5454a-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5454a-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5454a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5454a-108">DESCRIPTION</span></span>
<span data-ttu-id="5454a-109">Cmdleten **New-AzureRmRelayKey** skapar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5454a-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5454a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5454a-110">EXAMPLES</span></span>

### <span data-ttu-id="5454a-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="5454a-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="5454a-112">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5454a-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="5454a-113">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5454a-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="5454a-114">Återskapar primära eller sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5454a-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5454a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5454a-115">PARAMETERS</span></span>

### <span data-ttu-id="5454a-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5454a-116">-Confirm</span></span>
<span data-ttu-id="5454a-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5454a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5454a-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5454a-118">-HybridConnection</span></span>
<span data-ttu-id="5454a-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="5454a-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="5454a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5454a-120">-Name</span></span>
<span data-ttu-id="5454a-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="5454a-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="5454a-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5454a-122">-Namespace</span></span>
<span data-ttu-id="5454a-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="5454a-123">Namespace Name.</span></span>

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

### <span data-ttu-id="5454a-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5454a-124">-RegenerateKey</span></span>
<span data-ttu-id="5454a-125">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="5454a-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="5454a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5454a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5454a-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5454a-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5454a-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5454a-128">-WcfRelay</span></span>
<span data-ttu-id="5454a-129">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="5454a-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="5454a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5454a-130">-WhatIf</span></span>
<span data-ttu-id="5454a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5454a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5454a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5454a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5454a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5454a-133">-DefaultProfile</span></span>
<span data-ttu-id="5454a-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5454a-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5454a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5454a-135">CommonParameters</span></span>
<span data-ttu-id="5454a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5454a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5454a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5454a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5454a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5454a-138">INPUTS</span></span>

### <span data-ttu-id="5454a-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="5454a-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="5454a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-140">System.String</span></span> 

### <span data-ttu-id="5454a-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5454a-141">-NamespaceName</span></span>
 <span data-ttu-id="5454a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-142">System.String</span></span> 
 

### <span data-ttu-id="5454a-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="5454a-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="5454a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-144">System.String</span></span> 

### <span data-ttu-id="5454a-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="5454a-145">-WcfRelayName</span></span>
 <span data-ttu-id="5454a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-146">System.String</span></span> 

### <span data-ttu-id="5454a-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="5454a-147">-Name</span></span>
 <span data-ttu-id="5454a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-148">System.String</span></span>

### <span data-ttu-id="5454a-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="5454a-149">-RegenerateKeys</span></span>
 <span data-ttu-id="5454a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5454a-150">System.String</span></span>

## <span data-ttu-id="5454a-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5454a-151">OUTPUTS</span></span>

### <span data-ttu-id="5454a-152">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5454a-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="5454a-153">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="5454a-153">Example 1 - Namespace</span></span>
<span data-ttu-id="5454a-154">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 01 # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5454a-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="5454a-155">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5454a-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="5454a-156">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5454a-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="5454a-157">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5454a-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="5454a-158">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5454a-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="5454a-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5454a-159">NOTES</span></span>

## <span data-ttu-id="5454a-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5454a-160">RELATED LINKS</span></span>

