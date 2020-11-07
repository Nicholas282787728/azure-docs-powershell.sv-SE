---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756067"
---
# <span data-ttu-id="23dea-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="23dea-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="23dea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23dea-102">SYNOPSIS</span></span>
<span data-ttu-id="23dea-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23dea-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23dea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23dea-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23dea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23dea-105">DESCRIPTION</span></span>
<span data-ttu-id="23dea-106">Cmdleten **Remove-AzureRmServiceBusNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23dea-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="23dea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23dea-107">EXAMPLES</span></span>

### <span data-ttu-id="23dea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23dea-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="23dea-109">Tar bort Service Bus-namnområdet `SB-Example1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="23dea-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="23dea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23dea-110">PARAMETERS</span></span>

### <span data-ttu-id="23dea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dea-111">-DefaultProfile</span></span>
<span data-ttu-id="23dea-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23dea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23dea-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="23dea-113">-Name</span></span>
<span data-ttu-id="23dea-114">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="23dea-114">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23dea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23dea-115">-ResourceGroupName</span></span>
<span data-ttu-id="23dea-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="23dea-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23dea-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23dea-117">-Confirm</span></span>
<span data-ttu-id="23dea-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23dea-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23dea-119">-WhatIf</span></span>
<span data-ttu-id="23dea-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23dea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23dea-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23dea-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dea-122">CommonParameters</span></span>
<span data-ttu-id="23dea-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23dea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dea-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23dea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dea-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23dea-125">INPUTS</span></span>

### <span data-ttu-id="23dea-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23dea-126">-ResourceGroup</span></span>
 <span data-ttu-id="23dea-127">System. String</span><span class="sxs-lookup"><span data-stu-id="23dea-127">System.String</span></span>

### <span data-ttu-id="23dea-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="23dea-128">-NamespaceName</span></span>
 <span data-ttu-id="23dea-129">System. String</span><span class="sxs-lookup"><span data-stu-id="23dea-129">System.String</span></span>

## <span data-ttu-id="23dea-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23dea-130">OUTPUTS</span></span>

### <span data-ttu-id="23dea-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="23dea-131">System.Object</span></span>

## <span data-ttu-id="23dea-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23dea-132">NOTES</span></span>

## <span data-ttu-id="23dea-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23dea-133">RELATED LINKS</span></span>

