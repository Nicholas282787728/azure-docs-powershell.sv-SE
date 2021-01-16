---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410056"
---
# <span data-ttu-id="278ef-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="278ef-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="278ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="278ef-102">SYNOPSIS</span></span>
<span data-ttu-id="278ef-103">Tar bort den tillhör ande IoT-rollen för en enhet.</span><span class="sxs-lookup"><span data-stu-id="278ef-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="278ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="278ef-104">SYNTAX</span></span>

### <span data-ttu-id="278ef-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="278ef-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278ef-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="278ef-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278ef-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="278ef-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="278ef-108">DESCRIPTION</span></span>
<span data-ttu-id="278ef-109">Cmdleten **Remove-AzStackEdgeRole** tar bort den tillhör ande IoT-rollen för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="278ef-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="278ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="278ef-110">EXAMPLES</span></span>

### <span data-ttu-id="278ef-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="278ef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="278ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="278ef-112">PARAMETERS</span></span>

### <span data-ttu-id="278ef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="278ef-113">-AsJob</span></span>
<span data-ttu-id="278ef-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="278ef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="278ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278ef-115">-DefaultProfile</span></span>
<span data-ttu-id="278ef-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="278ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278ef-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="278ef-117">-DeviceName</span></span>
<span data-ttu-id="278ef-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="278ef-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278ef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="278ef-119">-InputObject</span></span>
<span data-ttu-id="278ef-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="278ef-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="278ef-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="278ef-121">-Name</span></span>
<span data-ttu-id="278ef-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="278ef-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278ef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="278ef-123">-PassThru</span></span>
<span data-ttu-id="278ef-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="278ef-124">returns true if successful</span></span>

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

### <span data-ttu-id="278ef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278ef-125">-ResourceGroupName</span></span>
<span data-ttu-id="278ef-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="278ef-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278ef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="278ef-127">-ResourceId</span></span>
<span data-ttu-id="278ef-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="278ef-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278ef-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="278ef-129">-Confirm</span></span>
<span data-ttu-id="278ef-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="278ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278ef-131">-WhatIf</span></span>
<span data-ttu-id="278ef-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="278ef-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="278ef-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="278ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278ef-134">CommonParameters</span></span>
<span data-ttu-id="278ef-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278ef-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="278ef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278ef-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="278ef-137">INPUTS</span></span>

### <span data-ttu-id="278ef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="278ef-138">System.String</span></span>

### <span data-ttu-id="278ef-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="278ef-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="278ef-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="278ef-140">OUTPUTS</span></span>

### <span data-ttu-id="278ef-141">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="278ef-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="278ef-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="278ef-142">NOTES</span></span>

## <span data-ttu-id="278ef-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="278ef-143">RELATED LINKS</span></span>
