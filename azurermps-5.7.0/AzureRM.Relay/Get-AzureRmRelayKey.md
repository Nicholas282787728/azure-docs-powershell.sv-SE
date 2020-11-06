---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574188"
---
# <span data-ttu-id="f8a0f-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="f8a0f-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="f8a0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a0f-103">Hämtar primära och sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f8a0f-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8a0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8a0f-104">SYNTAX</span></span>

### <span data-ttu-id="f8a0f-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f8a0f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a0f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a0f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a0f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8a0f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8a0f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8a0f-108">DESCRIPTION</span></span>
<span data-ttu-id="f8a0f-109">Cmdleten **Get-AzureRmRelayKey** returnerar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f8a0f-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f8a0f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8a0f-110">EXAMPLES</span></span>

### <span data-ttu-id="f8a0f-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="f8a0f-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="f8a0f-112">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8a0f-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="f8a0f-113">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f8a0f-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="f8a0f-114">Primära och sekundära anslutnings strängar till angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f8a0f-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f8a0f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8a0f-115">PARAMETERS</span></span>

### <span data-ttu-id="f8a0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a0f-116">-DefaultProfile</span></span>
<span data-ttu-id="f8a0f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8a0f-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f8a0f-118">-HybridConnection</span></span>
<span data-ttu-id="f8a0f-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f8a0f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8a0f-120">-Name</span></span>
<span data-ttu-id="f8a0f-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f8a0f-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f8a0f-122">-Namespace</span></span>
<span data-ttu-id="f8a0f-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-123">Namespace Name.</span></span>

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

### <span data-ttu-id="f8a0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8a0f-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f8a0f-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8a0f-126">-WcfRelay</span></span>
<span data-ttu-id="f8a0f-127">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f8a0f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a0f-128">CommonParameters</span></span>
<span data-ttu-id="f8a0f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a0f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a0f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a0f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a0f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8a0f-131">INPUTS</span></span>

### <span data-ttu-id="f8a0f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a0f-132">-ResourceGroupName</span></span>
 <span data-ttu-id="f8a0f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a0f-133">System.String</span></span> 

### <span data-ttu-id="f8a0f-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f8a0f-134">-NamespaceName</span></span>
 <span data-ttu-id="f8a0f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a0f-135">System.String</span></span> 
 

### <span data-ttu-id="f8a0f-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="f8a0f-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="f8a0f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a0f-137">System.String</span></span> 

### <span data-ttu-id="f8a0f-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="f8a0f-138">-WcfRelayName</span></span>
 <span data-ttu-id="f8a0f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a0f-139">System.String</span></span> 

### <span data-ttu-id="f8a0f-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8a0f-140">-Name</span></span>
 <span data-ttu-id="f8a0f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a0f-141">System.String</span></span>

## <span data-ttu-id="f8a0f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8a0f-142">OUTPUTS</span></span>

### <span data-ttu-id="f8a0f-143">Microsoft. Azure. commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f8a0f-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="f8a0f-144">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="f8a0f-144">Example 1 - Namespace</span></span>
<span data-ttu-id="f8a0f-145">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # 01 # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f8a0f-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="f8a0f-146">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f8a0f-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="f8a0f-147">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f8a0f-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="f8a0f-148">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f8a0f-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="f8a0f-149">PrimaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: slut punkt = SB://testnamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Filnamn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f8a0f-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="f8a0f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8a0f-150">NOTES</span></span>

## <span data-ttu-id="f8a0f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8a0f-151">RELATED LINKS</span></span>

