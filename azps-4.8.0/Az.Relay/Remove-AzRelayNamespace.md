---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260426"
---
# <span data-ttu-id="fd92f-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="fd92f-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="fd92f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd92f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd92f-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fd92f-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="fd92f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd92f-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd92f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd92f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd92f-106">Cmdleten **Remove-AzRelayNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fd92f-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="fd92f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd92f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd92f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd92f-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="fd92f-109">Tar bort relä namnområdet `TestNameSpace-Relay1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="fd92f-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="fd92f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd92f-110">PARAMETERS</span></span>

### <span data-ttu-id="fd92f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd92f-111">-DefaultProfile</span></span>
<span data-ttu-id="fd92f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd92f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd92f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd92f-113">-Name</span></span>
<span data-ttu-id="fd92f-114">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="fd92f-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="fd92f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd92f-115">-ResourceGroupName</span></span>
<span data-ttu-id="fd92f-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fd92f-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd92f-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd92f-117">-Confirm</span></span>
<span data-ttu-id="fd92f-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd92f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd92f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd92f-119">-WhatIf</span></span>
<span data-ttu-id="fd92f-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd92f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd92f-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd92f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd92f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd92f-122">CommonParameters</span></span>
<span data-ttu-id="fd92f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd92f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd92f-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd92f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd92f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd92f-125">INPUTS</span></span>

### <span data-ttu-id="fd92f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fd92f-126">System.String</span></span>

## <span data-ttu-id="fd92f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd92f-127">OUTPUTS</span></span>

### <span data-ttu-id="fd92f-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="fd92f-128">System.Void</span></span>

## <span data-ttu-id="fd92f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd92f-129">NOTES</span></span>

## <span data-ttu-id="fd92f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd92f-130">RELATED LINKS</span></span>
