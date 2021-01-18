---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522321"
---
# <span data-ttu-id="ef180-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ef180-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ef180-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef180-102">SYNOPSIS</span></span>
<span data-ttu-id="ef180-103">Tar bort HybridConnection från det angivna HybridConnection-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="ef180-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="ef180-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef180-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef180-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef180-105">DESCRIPTION</span></span>
<span data-ttu-id="ef180-106">Cmdleten **Remove-AzRelayHybridConnection** tar bort HybridConnection från det angivna relä namn området.</span><span class="sxs-lookup"><span data-stu-id="ef180-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="ef180-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef180-107">EXAMPLES</span></span>

### <span data-ttu-id="ef180-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef180-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="ef180-109">Tar bort HybridConnection `TestHybridConnection` från namn området `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ef180-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ef180-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef180-110">PARAMETERS</span></span>

### <span data-ttu-id="ef180-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef180-111">-DefaultProfile</span></span>
<span data-ttu-id="ef180-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef180-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef180-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef180-113">-Name</span></span>
<span data-ttu-id="ef180-114">HybridConnections namn.</span><span class="sxs-lookup"><span data-stu-id="ef180-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ef180-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ef180-115">-Namespace</span></span>
<span data-ttu-id="ef180-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ef180-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ef180-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef180-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef180-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ef180-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef180-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef180-119">-Confirm</span></span>
<span data-ttu-id="ef180-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef180-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef180-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef180-121">-WhatIf</span></span>
<span data-ttu-id="ef180-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef180-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef180-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef180-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef180-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef180-124">CommonParameters</span></span>
<span data-ttu-id="ef180-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef180-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef180-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef180-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef180-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef180-127">INPUTS</span></span>

### <span data-ttu-id="ef180-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ef180-128">System.String</span></span>

## <span data-ttu-id="ef180-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef180-129">OUTPUTS</span></span>

### <span data-ttu-id="ef180-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="ef180-130">System.Void</span></span>

## <span data-ttu-id="ef180-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef180-131">NOTES</span></span>

## <span data-ttu-id="ef180-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef180-132">RELATED LINKS</span></span>
