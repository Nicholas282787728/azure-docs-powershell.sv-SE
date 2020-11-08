---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 297800cd65f6527a36c8bc486a0ee73e84d98339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088106"
---
# <span data-ttu-id="4f678-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4f678-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="4f678-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f678-102">SYNOPSIS</span></span>
<span data-ttu-id="4f678-103">Tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="4f678-103">Removes an action group.</span></span>

## <span data-ttu-id="4f678-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f678-104">SYNTAX</span></span>

### <span data-ttu-id="4f678-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="4f678-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f678-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f678-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f678-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f678-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f678-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f678-108">DESCRIPTION</span></span>
<span data-ttu-id="4f678-109">Cmdleten **Remove-AzActionGroup** tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="4f678-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="4f678-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f678-110">EXAMPLES</span></span>

### <span data-ttu-id="4f678-111">Exempel 1: ta bort en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="4f678-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="4f678-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f678-112">PARAMETERS</span></span>

### <span data-ttu-id="4f678-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f678-113">-DefaultProfile</span></span>
<span data-ttu-id="4f678-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4f678-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f678-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f678-115">-InputObject</span></span>
<span data-ttu-id="4f678-116">Resurs för åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="4f678-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f678-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f678-117">-Name</span></span>
<span data-ttu-id="4f678-118">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f678-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f678-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f678-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f678-120">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4f678-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f678-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f678-121">-ResourceId</span></span>
<span data-ttu-id="4f678-122">Resursen i</span><span class="sxs-lookup"><span data-stu-id="4f678-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f678-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f678-123">-Confirm</span></span>
<span data-ttu-id="4f678-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f678-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f678-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f678-125">-WhatIf</span></span>
<span data-ttu-id="4f678-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f678-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f678-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f678-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f678-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f678-128">CommonParameters</span></span>
<span data-ttu-id="4f678-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f678-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f678-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f678-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f678-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f678-131">INPUTS</span></span>

### <span data-ttu-id="4f678-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4f678-132">System.String</span></span>

### <span data-ttu-id="4f678-133">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="4f678-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="4f678-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f678-134">OUTPUTS</span></span>

### <span data-ttu-id="4f678-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4f678-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4f678-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f678-136">NOTES</span></span>

## <span data-ttu-id="4f678-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f678-137">RELATED LINKS</span></span>

<span data-ttu-id="4f678-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="4f678-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
