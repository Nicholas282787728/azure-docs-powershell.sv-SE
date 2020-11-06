---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583783"
---
# <span data-ttu-id="b77fd-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="b77fd-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="b77fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b77fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b77fd-103">Hämtar de primära och sekundära anslutnings strängarna för Service Bus-ämnet.</span><span class="sxs-lookup"><span data-stu-id="b77fd-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b77fd-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b77fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b77fd-106">Cmdleten **Get-AzureRmServiceBusTopicKey** returnerar primära och sekundära anslutnings strängar för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="b77fd-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="b77fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b77fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b77fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b77fd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="b77fd-109">Returnerar de primära och sekundära anslutnings strängarna för den angivna tjänst Bus artikeln.</span><span class="sxs-lookup"><span data-stu-id="b77fd-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="b77fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b77fd-110">PARAMETERS</span></span>

### <span data-ttu-id="b77fd-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b77fd-111">-ResourceGroup</span></span>
<span data-ttu-id="b77fd-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b77fd-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b77fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77fd-113">-DefaultProfile</span></span>
<span data-ttu-id="b77fd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b77fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b77fd-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b77fd-115">-Name</span></span>
<span data-ttu-id="b77fd-116">Ämnes namn för AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b77fd-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fd-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b77fd-117">-Namespace</span></span>
<span data-ttu-id="b77fd-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b77fd-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fd-119">-Ämne</span><span class="sxs-lookup"><span data-stu-id="b77fd-119">-Topic</span></span>
<span data-ttu-id="b77fd-120">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="b77fd-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77fd-121">CommonParameters</span></span>
<span data-ttu-id="b77fd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77fd-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77fd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b77fd-124">INPUTS</span></span>

### <span data-ttu-id="b77fd-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b77fd-125">-ResourceGroup</span></span>
 <span data-ttu-id="b77fd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b77fd-126">System.String</span></span>
 

### <span data-ttu-id="b77fd-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b77fd-127">-NamespaceName</span></span>
 <span data-ttu-id="b77fd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b77fd-128">System.String</span></span>
 

### <span data-ttu-id="b77fd-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b77fd-129">-TopicName</span></span>
 <span data-ttu-id="b77fd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b77fd-130">System.String</span></span>
 

### <span data-ttu-id="b77fd-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b77fd-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b77fd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b77fd-132">System.String</span></span>

## <span data-ttu-id="b77fd-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b77fd-133">OUTPUTS</span></span>

### <span data-ttu-id="b77fd-134">Microsoft. Azure. commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b77fd-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="b77fd-135">PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-till pic_exampl1 SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-till pic_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="b77fd-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="b77fd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b77fd-136">NOTES</span></span>

## <span data-ttu-id="b77fd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b77fd-137">RELATED LINKS</span></span>

