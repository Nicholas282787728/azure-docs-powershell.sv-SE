---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389919"
---
# <span data-ttu-id="9798d-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="9798d-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="9798d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9798d-102">SYNOPSIS</span></span>
<span data-ttu-id="9798d-103">Tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="9798d-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9798d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9798d-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9798d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9798d-105">DESCRIPTION</span></span>
<span data-ttu-id="9798d-106">Cmdleten **Remove-AzWcfRelay** tar bort WcfRelay från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="9798d-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9798d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9798d-107">EXAMPLES</span></span>

### <span data-ttu-id="9798d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9798d-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="9798d-109">Tar bort WcfRelay `TestWCFRelay1` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="9798d-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9798d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9798d-110">PARAMETERS</span></span>

### <span data-ttu-id="9798d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9798d-111">-DefaultProfile</span></span>
<span data-ttu-id="9798d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9798d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9798d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9798d-113">-Name</span></span>
<span data-ttu-id="9798d-114">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="9798d-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9798d-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9798d-115">-Namespace</span></span>
<span data-ttu-id="9798d-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="9798d-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9798d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9798d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9798d-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9798d-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="9798d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9798d-119">-Confirm</span></span>
<span data-ttu-id="9798d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9798d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9798d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9798d-121">-WhatIf</span></span>
<span data-ttu-id="9798d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9798d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9798d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9798d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9798d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9798d-124">CommonParameters</span></span>
<span data-ttu-id="9798d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9798d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9798d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9798d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9798d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9798d-127">INPUTS</span></span>

### <span data-ttu-id="9798d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9798d-128">System.String</span></span>

## <span data-ttu-id="9798d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9798d-129">OUTPUTS</span></span>

### <span data-ttu-id="9798d-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="9798d-130">System.Void</span></span>

## <span data-ttu-id="9798d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9798d-131">NOTES</span></span>

## <span data-ttu-id="9798d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9798d-132">RELATED LINKS</span></span>
