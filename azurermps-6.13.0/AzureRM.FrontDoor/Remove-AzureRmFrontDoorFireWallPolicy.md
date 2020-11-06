---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572748"
---
# <span data-ttu-id="f744f-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="f744f-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="f744f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f744f-102">SYNOPSIS</span></span>
<span data-ttu-id="f744f-103">Ta bort WAF policy</span><span class="sxs-lookup"><span data-stu-id="f744f-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f744f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f744f-104">SYNTAX</span></span>

### <span data-ttu-id="f744f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f744f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f744f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f744f-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f744f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f744f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f744f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f744f-108">DESCRIPTION</span></span>
<span data-ttu-id="f744f-109">Cmdleten **Remove-AzureRmFrontDoor** tar bort en WAF-princip under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="f744f-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="f744f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f744f-110">EXAMPLES</span></span>

### <span data-ttu-id="f744f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f744f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="f744f-112">Ta bort WAF policy $name i $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f744f-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="f744f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f744f-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="f744f-114">Ta bort alla WAF-principer i $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f744f-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="f744f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f744f-115">PARAMETERS</span></span>

### <span data-ttu-id="f744f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f744f-116">-DefaultProfile</span></span>
<span data-ttu-id="f744f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f744f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f744f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f744f-118">-InputObject</span></span>
<span data-ttu-id="f744f-119">WAF princip objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f744f-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f744f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f744f-120">-Name</span></span>
<span data-ttu-id="f744f-121">Namnet på den WAF-princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f744f-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f744f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f744f-122">-PassThru</span></span>
<span data-ttu-id="f744f-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="f744f-123">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f744f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f744f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f744f-125">Resurs gruppen som WAF policy tillhör.</span><span class="sxs-lookup"><span data-stu-id="f744f-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f744f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f744f-126">-ResourceId</span></span>
<span data-ttu-id="f744f-127">Resurs-ID för WAF princip som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f744f-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f744f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f744f-128">-Confirm</span></span>
<span data-ttu-id="f744f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f744f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f744f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f744f-130">-WhatIf</span></span>
<span data-ttu-id="f744f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f744f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f744f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f744f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f744f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f744f-133">CommonParameters</span></span>
<span data-ttu-id="f744f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f744f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f744f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f744f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f744f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f744f-136">INPUTS</span></span>

### <span data-ttu-id="f744f-137">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f744f-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="f744f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f744f-138">System.String</span></span>

### <span data-ttu-id="f744f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f744f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f744f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f744f-140">OUTPUTS</span></span>

### <span data-ttu-id="f744f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f744f-141">System.Boolean</span></span>

## <span data-ttu-id="f744f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f744f-142">NOTES</span></span>

## <span data-ttu-id="f744f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f744f-143">RELATED LINKS</span></span>

<span data-ttu-id="f744f-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f744f-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
