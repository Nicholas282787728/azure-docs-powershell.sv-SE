---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259171"
---
# <span data-ttu-id="fb157-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="fb157-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="fb157-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb157-102">SYNOPSIS</span></span>
<span data-ttu-id="fb157-103">Hämtar primära och sekundära anslutnings strängar för angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb157-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fb157-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb157-104">SYNTAX</span></span>

### <span data-ttu-id="fb157-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb157-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb157-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb157-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb157-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb157-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb157-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb157-108">DESCRIPTION</span></span>
<span data-ttu-id="fb157-109">Cmdleten **Get-AzRelayKey** returnerar de primära och sekundära anslutnings strängarna för angivna relä enheter (namnrymd/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb157-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fb157-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb157-110">EXAMPLES</span></span>

### <span data-ttu-id="fb157-111">Exempel 1: namnrymd</span><span class="sxs-lookup"><span data-stu-id="fb157-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="fb157-112">Exempel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fb157-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="fb157-113">Exempel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb157-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fb157-114">Primära och sekundära anslutnings strängar till angivna relä enheter (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fb157-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fb157-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb157-115">PARAMETERS</span></span>

### <span data-ttu-id="fb157-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb157-116">-DefaultProfile</span></span>
<span data-ttu-id="fb157-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb157-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb157-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fb157-118">-HybridConnection</span></span>
<span data-ttu-id="fb157-119">HybridConnection namn.</span><span class="sxs-lookup"><span data-stu-id="fb157-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="fb157-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb157-120">-Name</span></span>
<span data-ttu-id="fb157-121">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="fb157-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="fb157-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fb157-122">-Namespace</span></span>
<span data-ttu-id="fb157-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="fb157-123">Namespace Name.</span></span>

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

### <span data-ttu-id="fb157-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb157-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb157-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fb157-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb157-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fb157-126">-WcfRelay</span></span>
<span data-ttu-id="fb157-127">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="fb157-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="fb157-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb157-128">CommonParameters</span></span>
<span data-ttu-id="fb157-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb157-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb157-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb157-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb157-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb157-131">INPUTS</span></span>

### <span data-ttu-id="fb157-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fb157-132">System.String</span></span>

## <span data-ttu-id="fb157-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb157-133">OUTPUTS</span></span>

### <span data-ttu-id="fb157-134">Microsoft. Azure. commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="fb157-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="fb157-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb157-135">NOTES</span></span>

## <span data-ttu-id="fb157-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb157-136">RELATED LINKS</span></span>
