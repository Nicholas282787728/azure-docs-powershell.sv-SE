---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919376"
---
# <span data-ttu-id="425e2-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="425e2-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="425e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="425e2-102">SYNOPSIS</span></span>
<span data-ttu-id="425e2-103">Hämtar primära och sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="425e2-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="425e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="425e2-104">SYNTAX</span></span>

### <span data-ttu-id="425e2-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="425e2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="425e2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="425e2-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="425e2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="425e2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="425e2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="425e2-108">DESCRIPTION</span></span>
<span data-ttu-id="425e2-109">Cmdleten **Get-AzRelayKey** returnerar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="425e2-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="425e2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="425e2-110">EXAMPLES</span></span>

### <span data-ttu-id="425e2-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="425e2-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="425e2-112">Exempel 2 – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="425e2-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="425e2-113">Exempel 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="425e2-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="425e2-114">Primära och sekundära anslutnings strängar till angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="425e2-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="425e2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="425e2-115">PARAMETERS</span></span>

### <span data-ttu-id="425e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425e2-116">-DefaultProfile</span></span>
<span data-ttu-id="425e2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="425e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425e2-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="425e2-118">-HybridConnection</span></span>
<span data-ttu-id="425e2-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="425e2-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="425e2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="425e2-120">-Name</span></span>
<span data-ttu-id="425e2-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="425e2-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="425e2-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="425e2-122">-Namespace</span></span>
<span data-ttu-id="425e2-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="425e2-123">Namespace Name.</span></span>

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

### <span data-ttu-id="425e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="425e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="425e2-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="425e2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="425e2-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="425e2-126">-WcfRelay</span></span>
<span data-ttu-id="425e2-127">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="425e2-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="425e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425e2-128">CommonParameters</span></span>
<span data-ttu-id="425e2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425e2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="425e2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425e2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="425e2-131">INPUTS</span></span>

### <span data-ttu-id="425e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="425e2-132">System.String</span></span>

## <span data-ttu-id="425e2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="425e2-133">OUTPUTS</span></span>

### <span data-ttu-id="425e2-134">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="425e2-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="425e2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="425e2-135">NOTES</span></span>

## <span data-ttu-id="425e2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="425e2-136">RELATED LINKS</span></span>
