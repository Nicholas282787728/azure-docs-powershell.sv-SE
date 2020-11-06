---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581276"
---
# <span data-ttu-id="6dc8d-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6dc8d-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="6dc8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6dc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc8d-103">Återskapar primära och sekundära anslutnings strängar för Service Bus namn området.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dc8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6dc8d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dc8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6dc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc8d-106">**New-AzureRmServiceBusNamespace-** cmdleten skapar nya primära eller sekundära anslutnings strängar för det angivna namn området och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="6dc8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6dc8d-107">EXAMPLES</span></span>

### <span data-ttu-id="6dc8d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6dc8d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="6dc8d-109">Återskapar primära eller sekundära anslutnings strängar för namn området.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="6dc8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6dc8d-110">PARAMETERS</span></span>

### <span data-ttu-id="6dc8d-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="6dc8d-111">-RegenerateKeys</span></span>
<span data-ttu-id="6dc8d-112">Återskapa nycklar: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc8d-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6dc8d-113">-ResourceGroup</span></span>
<span data-ttu-id="6dc8d-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc8d-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6dc8d-115">-Confirm</span></span>
<span data-ttu-id="6dc8d-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc8d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc8d-117">-WhatIf</span></span>
<span data-ttu-id="6dc8d-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc8d-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc8d-120">-DefaultProfile</span></span>
<span data-ttu-id="6dc8d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc8d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6dc8d-122">-Name</span></span>
<span data-ttu-id="6dc8d-123">Namn på auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="6dc8d-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6dc8d-124">-Namespace</span></span>
<span data-ttu-id="6dc8d-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-125">Namespace Name.</span></span>

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

### <span data-ttu-id="6dc8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc8d-126">CommonParameters</span></span>
<span data-ttu-id="6dc8d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc8d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc8d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc8d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6dc8d-129">INPUTS</span></span>

### <span data-ttu-id="6dc8d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6dc8d-130">-ResourceGroup</span></span>
 <span data-ttu-id="6dc8d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc8d-131">System.String</span></span>
 

### <span data-ttu-id="6dc8d-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6dc8d-132">-NamespaceName</span></span>
 <span data-ttu-id="6dc8d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc8d-133">System.String</span></span>
 

### <span data-ttu-id="6dc8d-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="6dc8d-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="6dc8d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc8d-135">System.String</span></span>
 

### <span data-ttu-id="6dc8d-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="6dc8d-136">-RegenerateKeys</span></span>
 <span data-ttu-id="6dc8d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc8d-137">System.String</span></span>

## <span data-ttu-id="6dc8d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6dc8d-138">OUTPUTS</span></span>

### <span data-ttu-id="6dc8d-139">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6dc8d-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="6dc8d-140">PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6dc8d-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="6dc8d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6dc8d-141">NOTES</span></span>

## <span data-ttu-id="6dc8d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6dc8d-142">RELATED LINKS</span></span>

