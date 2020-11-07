---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757362"
---
# <span data-ttu-id="427e3-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="427e3-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="427e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="427e3-102">SYNOPSIS</span></span>
<span data-ttu-id="427e3-103">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="427e3-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="427e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="427e3-104">SYNTAX</span></span>

### <span data-ttu-id="427e3-105">DevSpacesControllerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="427e3-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="427e3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="427e3-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="427e3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="427e3-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="427e3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="427e3-108">DESCRIPTION</span></span>
<span data-ttu-id="427e3-109">Uppdatera DevSpaces-styrenheten för att lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="427e3-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="427e3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="427e3-110">EXAMPLES</span></span>

### <span data-ttu-id="427e3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="427e3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="427e3-112">Tagga en DevSpaces-försvarare.</span><span class="sxs-lookup"><span data-stu-id="427e3-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="427e3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="427e3-113">PARAMETERS</span></span>

### <span data-ttu-id="427e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427e3-114">-DefaultProfile</span></span>
<span data-ttu-id="427e3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="427e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="427e3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="427e3-116">-InputObject</span></span>
<span data-ttu-id="427e3-117">Ett PSController-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="427e3-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="427e3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="427e3-118">-Name</span></span>
<span data-ttu-id="427e3-119">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="427e3-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="427e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="427e3-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="427e3-121">Resource group name</span></span>

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

### <span data-ttu-id="427e3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="427e3-122">-ResourceId</span></span>
<span data-ttu-id="427e3-123">Resurs-ID för DevSpaces</span><span class="sxs-lookup"><span data-stu-id="427e3-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="427e3-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="427e3-124">-Tag</span></span>
<span data-ttu-id="427e3-125">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="427e3-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="427e3-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="427e3-126">-Confirm</span></span>
<span data-ttu-id="427e3-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="427e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="427e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="427e3-128">-WhatIf</span></span>
<span data-ttu-id="427e3-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="427e3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="427e3-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="427e3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="427e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427e3-131">CommonParameters</span></span>
<span data-ttu-id="427e3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="427e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427e3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="427e3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427e3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="427e3-134">INPUTS</span></span>

### <span data-ttu-id="427e3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="427e3-135">System.String</span></span>

### <span data-ttu-id="427e3-136">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="427e3-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="427e3-137">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="427e3-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="427e3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="427e3-138">OUTPUTS</span></span>

### <span data-ttu-id="427e3-139">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="427e3-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="427e3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="427e3-140">NOTES</span></span>

## <span data-ttu-id="427e3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="427e3-141">RELATED LINKS</span></span>
