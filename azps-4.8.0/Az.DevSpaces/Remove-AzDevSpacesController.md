---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262726"
---
# <span data-ttu-id="0195c-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="0195c-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="0195c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0195c-102">SYNOPSIS</span></span>
<span data-ttu-id="0195c-103">Ta bort en DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="0195c-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="0195c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0195c-104">SYNTAX</span></span>

### <span data-ttu-id="0195c-105">DevSpacesControllerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0195c-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0195c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0195c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0195c-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0195c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0195c-108">DESCRIPTION</span></span>
<span data-ttu-id="0195c-109">Ta bort en DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="0195c-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="0195c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0195c-110">EXAMPLES</span></span>

### <span data-ttu-id="0195c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0195c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="0195c-112">Ta bort en DevSpaces-styrenhet med namnet devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="0195c-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="0195c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0195c-113">PARAMETERS</span></span>

### <span data-ttu-id="0195c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0195c-114">-AsJob</span></span>
<span data-ttu-id="0195c-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0195c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0195c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0195c-116">-DefaultProfile</span></span>
<span data-ttu-id="0195c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0195c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0195c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0195c-118">-InputObject</span></span>
<span data-ttu-id="0195c-119">Ett PSController-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="0195c-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="0195c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0195c-120">-Name</span></span>
<span data-ttu-id="0195c-121">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="0195c-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="0195c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0195c-122">-PassThru</span></span>
<span data-ttu-id="0195c-123">Returnerar sant om borttagningen lyckades</span><span class="sxs-lookup"><span data-stu-id="0195c-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="0195c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0195c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0195c-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0195c-125">Resource group name</span></span>

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

### <span data-ttu-id="0195c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0195c-126">-ResourceId</span></span>
<span data-ttu-id="0195c-127">Resurs-ID för DevSpaces</span><span class="sxs-lookup"><span data-stu-id="0195c-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="0195c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0195c-128">-Confirm</span></span>
<span data-ttu-id="0195c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0195c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0195c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0195c-130">-WhatIf</span></span>
<span data-ttu-id="0195c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0195c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0195c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0195c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0195c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0195c-133">CommonParameters</span></span>
<span data-ttu-id="0195c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0195c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0195c-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0195c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0195c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0195c-136">INPUTS</span></span>

### <span data-ttu-id="0195c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0195c-137">System.String</span></span>

### <span data-ttu-id="0195c-138">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="0195c-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="0195c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0195c-139">OUTPUTS</span></span>

### <span data-ttu-id="0195c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0195c-140">System.Boolean</span></span>

## <span data-ttu-id="0195c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0195c-141">NOTES</span></span>

## <span data-ttu-id="0195c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0195c-142">RELATED LINKS</span></span>
