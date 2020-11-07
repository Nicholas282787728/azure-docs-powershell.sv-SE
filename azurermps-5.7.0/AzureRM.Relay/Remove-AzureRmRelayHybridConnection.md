---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 872683cbf4e26601ec16f05256f0011b0441127c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756469"
---
# <span data-ttu-id="9943a-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="9943a-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="9943a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9943a-102">SYNOPSIS</span></span>
<span data-ttu-id="9943a-103">Tar bort HybridConnection från det angivna HybridConnection-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="9943a-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9943a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9943a-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9943a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9943a-105">DESCRIPTION</span></span>
<span data-ttu-id="9943a-106">Cmdleten **Remove-AzureRmRelayHybridConnection** tar bort HybridConnection från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="9943a-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="9943a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9943a-107">EXAMPLES</span></span>

### <span data-ttu-id="9943a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9943a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="9943a-109">Tar bort HybridConnection `TestHybridConnection` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9943a-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9943a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9943a-110">PARAMETERS</span></span>

### <span data-ttu-id="9943a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9943a-111">-DefaultProfile</span></span>
<span data-ttu-id="9943a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9943a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9943a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9943a-113">-Name</span></span>
<span data-ttu-id="9943a-114">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="9943a-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9943a-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9943a-115">-Namespace</span></span>
<span data-ttu-id="9943a-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="9943a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="9943a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9943a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9943a-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9943a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="9943a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9943a-119">-Confirm</span></span>
<span data-ttu-id="9943a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9943a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9943a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9943a-121">-WhatIf</span></span>
<span data-ttu-id="9943a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9943a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9943a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9943a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9943a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9943a-124">CommonParameters</span></span>
<span data-ttu-id="9943a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9943a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9943a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9943a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9943a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9943a-127">INPUTS</span></span>

### <span data-ttu-id="9943a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9943a-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="9943a-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9943a-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="9943a-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="9943a-130">-Name</span></span>
    System.String

## <span data-ttu-id="9943a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9943a-131">OUTPUTS</span></span>

### <span data-ttu-id="9943a-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="9943a-132">System.Object</span></span>

## <span data-ttu-id="9943a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9943a-133">NOTES</span></span>

## <span data-ttu-id="9943a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9943a-134">RELATED LINKS</span></span>

