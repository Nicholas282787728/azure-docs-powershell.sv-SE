---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577440"
---
# <span data-ttu-id="f7fc3-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7fc3-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f7fc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fc3-103">Hämtar en beskrivning av den angivna auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7fc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7fc3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7fc3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f7fc3-106">Cmdleten **Get-AzureRmServiceBusNamespaceAuthorizationRule** hämtar beskrivningen av den angivna auktoriseringsregeln i det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="f7fc3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="f7fc3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7fc3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="f7fc3-109">Returnerar den angivna beskrivningen för auktoriseringsregeln för ett angivet namn område.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="f7fc3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7fc3-110">PARAMETERS</span></span>

### <span data-ttu-id="f7fc3-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f7fc3-111">-ResourceGroup</span></span>
<span data-ttu-id="f7fc3-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7fc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fc3-113">-DefaultProfile</span></span>
<span data-ttu-id="f7fc3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7fc3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7fc3-115">-Name</span></span>
<span data-ttu-id="f7fc3-116">Namn på ServiceBus namn område.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7fc3-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f7fc3-117">-Namespace</span></span>
<span data-ttu-id="f7fc3-118">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f7fc3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fc3-119">CommonParameters</span></span>
<span data-ttu-id="f7fc3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fc3-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7fc3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fc3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7fc3-122">INPUTS</span></span>

### <span data-ttu-id="f7fc3-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f7fc3-123">-ResourceGroup</span></span>
 <span data-ttu-id="f7fc3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f7fc3-124">System.String</span></span>
 

### <span data-ttu-id="f7fc3-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f7fc3-125">-NamespaceName</span></span>
 <span data-ttu-id="f7fc3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f7fc3-126">System.String</span></span>
 

### <span data-ttu-id="f7fc3-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f7fc3-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f7fc3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f7fc3-128">System.String</span></span>

## <span data-ttu-id="f7fc3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7fc3-129">OUTPUTS</span></span>

### <span data-ttu-id="f7fc3-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f7fc3-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f7fc3-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules namn: AuthoRule1 Location: tagg: Rights: {Listener, Send}</span><span class="sxs-lookup"><span data-stu-id="f7fc3-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f7fc3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7fc3-132">NOTES</span></span>

## <span data-ttu-id="f7fc3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7fc3-133">RELATED LINKS</span></span>

