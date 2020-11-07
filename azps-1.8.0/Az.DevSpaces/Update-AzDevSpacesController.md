---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 2a94d74fb8c6ba6cc9f6c2873269f3009c2f7e9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754190"
---
# <span data-ttu-id="ced1f-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="ced1f-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="ced1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ced1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ced1f-103">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="ced1f-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="ced1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ced1f-104">SYNTAX</span></span>

### <span data-ttu-id="ced1f-105">DevSpacesControllerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ced1f-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced1f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced1f-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced1f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced1f-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced1f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ced1f-108">DESCRIPTION</span></span>
<span data-ttu-id="ced1f-109">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="ced1f-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="ced1f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ced1f-110">EXAMPLES</span></span>

### <span data-ttu-id="ced1f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ced1f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="ced1f-112">Tagga en DevSpaces-försvarare.</span><span class="sxs-lookup"><span data-stu-id="ced1f-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="ced1f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ced1f-113">PARAMETERS</span></span>

### <span data-ttu-id="ced1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced1f-114">-DefaultProfile</span></span>
<span data-ttu-id="ced1f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ced1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced1f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ced1f-116">-InputObject</span></span>
<span data-ttu-id="ced1f-117">Ett PSController-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ced1f-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ced1f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ced1f-118">-Name</span></span>
<span data-ttu-id="ced1f-119">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="ced1f-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="ced1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="ced1f-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ced1f-121">Resource group name</span></span>

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

### <span data-ttu-id="ced1f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced1f-122">-ResourceId</span></span>
<span data-ttu-id="ced1f-123">Resurs-ID för DevSpaces</span><span class="sxs-lookup"><span data-stu-id="ced1f-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="ced1f-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ced1f-124">-Tag</span></span>
<span data-ttu-id="ced1f-125">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ced1f-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced1f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ced1f-126">-Confirm</span></span>
<span data-ttu-id="ced1f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ced1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced1f-128">-WhatIf</span></span>
<span data-ttu-id="ced1f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ced1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced1f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ced1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced1f-131">CommonParameters</span></span>
<span data-ttu-id="ced1f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced1f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced1f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced1f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ced1f-134">INPUTS</span></span>

### <span data-ttu-id="ced1f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ced1f-135">System.String</span></span>

### <span data-ttu-id="ced1f-136">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="ced1f-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="ced1f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ced1f-137">OUTPUTS</span></span>

### <span data-ttu-id="ced1f-138">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="ced1f-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="ced1f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ced1f-139">NOTES</span></span>

## <span data-ttu-id="ced1f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ced1f-140">RELATED LINKS</span></span>
