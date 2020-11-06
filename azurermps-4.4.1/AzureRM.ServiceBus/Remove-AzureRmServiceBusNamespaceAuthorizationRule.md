---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575844"
---
# <span data-ttu-id="e82cd-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e82cd-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="e82cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e82cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e82cd-103">Tar bort auktoriseringsregeln för ett Service Bus-namnområde från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e82cd-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e82cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e82cd-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e82cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e82cd-105">DESCRIPTION</span></span>
<span data-ttu-id="e82cd-106">Cmdleten **Remove-AzureRmServiceBusNamespaceAuthorizationRule** tar bort auktoriseringsregeln för ett Service Bus-namnområde för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e82cd-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="e82cd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e82cd-107">EXAMPLES</span></span>

### <span data-ttu-id="e82cd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e82cd-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="e82cd-109">Tar bort auktoriseringsregeln `SBAuthoRule1` för namn område `SB-Example1` från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e82cd-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="e82cd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e82cd-110">PARAMETERS</span></span>

### <span data-ttu-id="e82cd-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e82cd-111">-Confirm</span></span>
<span data-ttu-id="e82cd-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e82cd-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e82cd-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e82cd-113">-WhatIf</span></span>
<span data-ttu-id="e82cd-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e82cd-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e82cd-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e82cd-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e82cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82cd-116">-DefaultProfile</span></span>
<span data-ttu-id="e82cd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e82cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e82cd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e82cd-118">-Name</span></span>
<span data-ttu-id="e82cd-119">Namn på AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e82cd-119">Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e82cd-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e82cd-120">-Namespace</span></span>
<span data-ttu-id="e82cd-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="e82cd-121">Namespace Name.</span></span>

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

### <span data-ttu-id="e82cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="e82cd-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e82cd-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82cd-124">CommonParameters</span></span>
<span data-ttu-id="e82cd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82cd-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82cd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e82cd-127">INPUTS</span></span>

### <span data-ttu-id="e82cd-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e82cd-128">-ResourceGroup</span></span>
 <span data-ttu-id="e82cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e82cd-129">System.String</span></span>

### <span data-ttu-id="e82cd-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e82cd-130">-NamespaceName</span></span>
 <span data-ttu-id="e82cd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e82cd-131">System.String</span></span>

### <span data-ttu-id="e82cd-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e82cd-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e82cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e82cd-133">System.String</span></span>

## <span data-ttu-id="e82cd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e82cd-134">OUTPUTS</span></span>

### <span data-ttu-id="e82cd-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e82cd-135">System.Boolean</span></span>

## <span data-ttu-id="e82cd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e82cd-136">NOTES</span></span>

## <span data-ttu-id="e82cd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e82cd-137">RELATED LINKS</span></span>

