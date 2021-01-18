---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522918"
---
# <span data-ttu-id="bc1ef-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="bc1ef-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="bc1ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1ef-103">Tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-103">Removes an action group.</span></span>

## <span data-ttu-id="bc1ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc1ef-104">SYNTAX</span></span>

### <span data-ttu-id="bc1ef-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="bc1ef-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc1ef-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc1ef-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc1ef-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc1ef-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc1ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc1ef-108">DESCRIPTION</span></span>
<span data-ttu-id="bc1ef-109">Cmdleten **Remove-AzActionGroup** tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="bc1ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc1ef-110">EXAMPLES</span></span>

### <span data-ttu-id="bc1ef-111">Exempel 1: ta bort en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="bc1ef-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="bc1ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc1ef-112">PARAMETERS</span></span>

### <span data-ttu-id="bc1ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1ef-113">-DefaultProfile</span></span>
<span data-ttu-id="bc1ef-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bc1ef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc1ef-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc1ef-115">-InputObject</span></span>
<span data-ttu-id="bc1ef-116">Resurs för åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="bc1ef-116">The action group resource</span></span>

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

### <span data-ttu-id="bc1ef-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc1ef-117">-Name</span></span>
<span data-ttu-id="bc1ef-118">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-118">The name of the action group.</span></span>

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

### <span data-ttu-id="bc1ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc1ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="bc1ef-120">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="bc1ef-120">The resource group nam</span></span>

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

### <span data-ttu-id="bc1ef-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc1ef-121">-ResourceId</span></span>
<span data-ttu-id="bc1ef-122">Resursen i</span><span class="sxs-lookup"><span data-stu-id="bc1ef-122">The resource i</span></span>

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

### <span data-ttu-id="bc1ef-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc1ef-123">-Confirm</span></span>
<span data-ttu-id="bc1ef-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc1ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc1ef-125">-WhatIf</span></span>
<span data-ttu-id="bc1ef-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc1ef-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc1ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1ef-128">CommonParameters</span></span>
<span data-ttu-id="bc1ef-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc1ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1ef-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc1ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1ef-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc1ef-131">INPUTS</span></span>

### <span data-ttu-id="bc1ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bc1ef-132">System.String</span></span>

### <span data-ttu-id="bc1ef-133">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="bc1ef-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="bc1ef-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc1ef-134">OUTPUTS</span></span>

### <span data-ttu-id="bc1ef-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bc1ef-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bc1ef-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc1ef-136">NOTES</span></span>

## <span data-ttu-id="bc1ef-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc1ef-137">RELATED LINKS</span></span>

<span data-ttu-id="bc1ef-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="bc1ef-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
