---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: dec858fe113725876e7e46d72cf996d9338b34eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920124"
---
# <span data-ttu-id="63cff-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="63cff-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="63cff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63cff-102">SYNOPSIS</span></span>
<span data-ttu-id="63cff-103">Tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="63cff-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="63cff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63cff-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63cff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63cff-105">DESCRIPTION</span></span>
<span data-ttu-id="63cff-106">Cmdleten **Remove-AzRelayNamespace** tar bort namn området från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="63cff-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="63cff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63cff-107">EXAMPLES</span></span>

### <span data-ttu-id="63cff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63cff-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="63cff-109">Tar bort relä namnområdet `TestNameSpace-Relay1` från den angivna resurs gruppen `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="63cff-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="63cff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63cff-110">PARAMETERS</span></span>

### <span data-ttu-id="63cff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cff-111">-DefaultProfile</span></span>
<span data-ttu-id="63cff-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63cff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63cff-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="63cff-113">-Name</span></span>
<span data-ttu-id="63cff-114">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="63cff-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="63cff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cff-115">-ResourceGroupName</span></span>
<span data-ttu-id="63cff-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="63cff-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="63cff-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63cff-117">-Confirm</span></span>
<span data-ttu-id="63cff-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63cff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63cff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cff-119">-WhatIf</span></span>
<span data-ttu-id="63cff-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63cff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63cff-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63cff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63cff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cff-122">CommonParameters</span></span>
<span data-ttu-id="63cff-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cff-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63cff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cff-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63cff-125">INPUTS</span></span>

### <span data-ttu-id="63cff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="63cff-126">System.String</span></span>

## <span data-ttu-id="63cff-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63cff-127">OUTPUTS</span></span>

### <span data-ttu-id="63cff-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="63cff-128">System.Void</span></span>

## <span data-ttu-id="63cff-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63cff-129">NOTES</span></span>

## <span data-ttu-id="63cff-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63cff-130">RELATED LINKS</span></span>
