---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757365"
---
# <span data-ttu-id="d4b2e-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="d4b2e-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="d4b2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b2e-103">Ta bort en DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4b2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4b2e-104">SYNTAX</span></span>

### <span data-ttu-id="d4b2e-105">DevSpacesControllerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d4b2e-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b2e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b2e-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b2e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b2e-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b2e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="d4b2e-109">Ta bort en DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="d4b2e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4b2e-110">EXAMPLES</span></span>

### <span data-ttu-id="d4b2e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4b2e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="d4b2e-112">Ta bort en DevSpaces-styrenhet med namnet devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="d4b2e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4b2e-113">PARAMETERS</span></span>

### <span data-ttu-id="d4b2e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4b2e-114">-AsJob</span></span>
<span data-ttu-id="d4b2e-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d4b2e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4b2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b2e-116">-DefaultProfile</span></span>
<span data-ttu-id="d4b2e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4b2e-118">-InputObject</span></span>
<span data-ttu-id="d4b2e-119">Ett PSController-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b2e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4b2e-120">-Name</span></span>
<span data-ttu-id="d4b2e-121">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4b2e-122">-PassThru</span></span>
<span data-ttu-id="d4b2e-123">Returnerar sant om borttagningen lyckades</span><span class="sxs-lookup"><span data-stu-id="d4b2e-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="d4b2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4b2e-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d4b2e-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b2e-126">-ResourceId</span></span>
<span data-ttu-id="d4b2e-127">Resurs-ID för DevSpaces</span><span class="sxs-lookup"><span data-stu-id="d4b2e-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="d4b2e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4b2e-128">-Confirm</span></span>
<span data-ttu-id="d4b2e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b2e-130">-WhatIf</span></span>
<span data-ttu-id="d4b2e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b2e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b2e-133">CommonParameters</span></span>
<span data-ttu-id="d4b2e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b2e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b2e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b2e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4b2e-136">INPUTS</span></span>

### <span data-ttu-id="d4b2e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4b2e-137">System.String</span></span>

### <span data-ttu-id="d4b2e-138">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="d4b2e-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="d4b2e-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4b2e-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d4b2e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4b2e-140">OUTPUTS</span></span>

### <span data-ttu-id="d4b2e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4b2e-141">System.Boolean</span></span>

## <span data-ttu-id="d4b2e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4b2e-142">NOTES</span></span>

## <span data-ttu-id="d4b2e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4b2e-143">RELATED LINKS</span></span>
