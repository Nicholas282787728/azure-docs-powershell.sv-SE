---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263286"
---
# <span data-ttu-id="2b978-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2b978-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="2b978-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b978-102">SYNOPSIS</span></span>
<span data-ttu-id="2b978-103">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="2b978-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2b978-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b978-104">SYNTAX</span></span>

### <span data-ttu-id="2b978-105">DevSpacesControllerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2b978-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b978-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b978-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b978-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b978-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b978-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b978-108">DESCRIPTION</span></span>
<span data-ttu-id="2b978-109">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="2b978-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2b978-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b978-110">EXAMPLES</span></span>

### <span data-ttu-id="2b978-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2b978-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="2b978-112">Tagga en DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="2b978-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="2b978-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b978-113">PARAMETERS</span></span>

### <span data-ttu-id="2b978-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b978-114">-DefaultProfile</span></span>
<span data-ttu-id="2b978-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b978-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b978-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b978-116">-InputObject</span></span>
<span data-ttu-id="2b978-117">Ett PSController-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b978-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2b978-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b978-118">-Name</span></span>
<span data-ttu-id="2b978-119">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="2b978-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="2b978-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b978-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b978-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2b978-121">Resource group name</span></span>

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

### <span data-ttu-id="2b978-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b978-122">-ResourceId</span></span>
<span data-ttu-id="2b978-123">Resurs-ID för DevSpaces</span><span class="sxs-lookup"><span data-stu-id="2b978-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="2b978-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2b978-124">-Tag</span></span>
<span data-ttu-id="2b978-125">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="2b978-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2b978-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b978-126">-Confirm</span></span>
<span data-ttu-id="2b978-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b978-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b978-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b978-128">-WhatIf</span></span>
<span data-ttu-id="2b978-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b978-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b978-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b978-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b978-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b978-131">CommonParameters</span></span>
<span data-ttu-id="2b978-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b978-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b978-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b978-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b978-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b978-134">INPUTS</span></span>

### <span data-ttu-id="2b978-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2b978-135">System.String</span></span>

### <span data-ttu-id="2b978-136">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="2b978-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2b978-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b978-137">OUTPUTS</span></span>

### <span data-ttu-id="2b978-138">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="2b978-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2b978-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b978-139">NOTES</span></span>

## <span data-ttu-id="2b978-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b978-140">RELATED LINKS</span></span>
