---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929902"
---
# <span data-ttu-id="e67dc-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e67dc-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="e67dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e67dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e67dc-103">Tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="e67dc-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e67dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e67dc-104">SYNTAX</span></span>

### <span data-ttu-id="e67dc-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="e67dc-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67dc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e67dc-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e67dc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e67dc-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e67dc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e67dc-108">DESCRIPTION</span></span>
<span data-ttu-id="e67dc-109">Cmdleten **Remove-AzureRmActionGroup** tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="e67dc-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="e67dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e67dc-110">EXAMPLES</span></span>

### <span data-ttu-id="e67dc-111">Exempel 1: ta bort en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="e67dc-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="e67dc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e67dc-112">PARAMETERS</span></span>

### <span data-ttu-id="e67dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67dc-113">-DefaultProfile</span></span>
<span data-ttu-id="e67dc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e67dc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e67dc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e67dc-115">-InputObject</span></span>
<span data-ttu-id="e67dc-116">Resourc åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="e67dc-116">The action group resourc</span></span>

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

### <span data-ttu-id="e67dc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e67dc-117">-Name</span></span>
<span data-ttu-id="e67dc-118">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="e67dc-118">The name of the action group.</span></span>

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

### <span data-ttu-id="e67dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="e67dc-120">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e67dc-120">The resource group nam</span></span>

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

### <span data-ttu-id="e67dc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e67dc-121">-ResourceId</span></span>
<span data-ttu-id="e67dc-122">Resursen i</span><span class="sxs-lookup"><span data-stu-id="e67dc-122">The resource i</span></span>

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

### <span data-ttu-id="e67dc-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e67dc-123">-Confirm</span></span>
<span data-ttu-id="e67dc-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e67dc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e67dc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67dc-125">-WhatIf</span></span>
<span data-ttu-id="e67dc-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e67dc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e67dc-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e67dc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e67dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67dc-128">CommonParameters</span></span>
<span data-ttu-id="e67dc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67dc-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67dc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67dc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e67dc-131">INPUTS</span></span>

### <span data-ttu-id="e67dc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e67dc-132">System.String</span></span>

### <span data-ttu-id="e67dc-133">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e67dc-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="e67dc-134">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e67dc-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e67dc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e67dc-135">OUTPUTS</span></span>

### <span data-ttu-id="e67dc-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e67dc-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e67dc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e67dc-137">NOTES</span></span>

## <span data-ttu-id="e67dc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e67dc-138">RELATED LINKS</span></span>

<span data-ttu-id="e67dc-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e67dc-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
