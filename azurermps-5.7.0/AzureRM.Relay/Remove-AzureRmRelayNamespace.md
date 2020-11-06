---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575550"
---
# <span data-ttu-id="1590f-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1590f-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="1590f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1590f-102">SYNOPSIS</span></span>
<span data-ttu-id="1590f-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1590f-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1590f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1590f-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1590f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1590f-105">DESCRIPTION</span></span>
<span data-ttu-id="1590f-106">Cmdleten **Remove-AzureRmRelayNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1590f-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="1590f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1590f-107">EXAMPLES</span></span>

### <span data-ttu-id="1590f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1590f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="1590f-109">Tar bort relä namnområdet `TestNameSpace-Relay1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="1590f-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="1590f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1590f-110">PARAMETERS</span></span>

### <span data-ttu-id="1590f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1590f-111">-DefaultProfile</span></span>
<span data-ttu-id="1590f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1590f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1590f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1590f-113">-Name</span></span>
<span data-ttu-id="1590f-114">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="1590f-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1590f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1590f-115">-ResourceGroupName</span></span>
<span data-ttu-id="1590f-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1590f-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="1590f-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1590f-117">-Confirm</span></span>
<span data-ttu-id="1590f-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1590f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1590f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1590f-119">-WhatIf</span></span>
<span data-ttu-id="1590f-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1590f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1590f-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1590f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1590f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1590f-122">CommonParameters</span></span>
<span data-ttu-id="1590f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1590f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1590f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1590f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1590f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1590f-125">INPUTS</span></span>

### <span data-ttu-id="1590f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1590f-126">-ResourceGroupName</span></span>
 <span data-ttu-id="1590f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1590f-127">System.String</span></span>

### <span data-ttu-id="1590f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1590f-128">-Name</span></span>
 <span data-ttu-id="1590f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1590f-129">System.String</span></span>

## <span data-ttu-id="1590f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1590f-130">OUTPUTS</span></span>

### <span data-ttu-id="1590f-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="1590f-131">System.Object</span></span>

## <span data-ttu-id="1590f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1590f-132">NOTES</span></span>

## <span data-ttu-id="1590f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1590f-133">RELATED LINKS</span></span>

