---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269406"
---
# <span data-ttu-id="432d0-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="432d0-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="432d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="432d0-102">SYNOPSIS</span></span>
<span data-ttu-id="432d0-103">Tar bort en resurs från enheten.</span><span class="sxs-lookup"><span data-stu-id="432d0-103">Removes a share from the device.</span></span>

## <span data-ttu-id="432d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="432d0-104">SYNTAX</span></span>

### <span data-ttu-id="432d0-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="432d0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432d0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="432d0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432d0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="432d0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="432d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="432d0-108">DESCRIPTION</span></span>
<span data-ttu-id="432d0-109">Cmdleten **Remove-AzStackEdgeEdgeShare** tar bort de tillhör ande kanterna för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="432d0-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="432d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="432d0-110">EXAMPLES</span></span>

### <span data-ttu-id="432d0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="432d0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="432d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="432d0-112">PARAMETERS</span></span>

### <span data-ttu-id="432d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="432d0-113">-AsJob</span></span>
<span data-ttu-id="432d0-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="432d0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="432d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432d0-115">-DefaultProfile</span></span>
<span data-ttu-id="432d0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="432d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="432d0-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="432d0-117">-DeviceName</span></span>
<span data-ttu-id="432d0-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="432d0-118">Device Name</span></span>

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

### <span data-ttu-id="432d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="432d0-119">-InputObject</span></span>
<span data-ttu-id="432d0-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="432d0-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="432d0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="432d0-121">-Name</span></span>
<span data-ttu-id="432d0-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="432d0-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="432d0-123">-PassThru</span></span>
<span data-ttu-id="432d0-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="432d0-124">returns true if successful</span></span>

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

### <span data-ttu-id="432d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="432d0-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="432d0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="432d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="432d0-127">-ResourceId</span></span>
<span data-ttu-id="432d0-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="432d0-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432d0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="432d0-129">-Confirm</span></span>
<span data-ttu-id="432d0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="432d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="432d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432d0-131">-WhatIf</span></span>
<span data-ttu-id="432d0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="432d0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="432d0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="432d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="432d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432d0-134">CommonParameters</span></span>
<span data-ttu-id="432d0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="432d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432d0-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="432d0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432d0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="432d0-137">INPUTS</span></span>

### <span data-ttu-id="432d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="432d0-138">System.String</span></span>

### <span data-ttu-id="432d0-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="432d0-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="432d0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="432d0-140">OUTPUTS</span></span>

### <span data-ttu-id="432d0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="432d0-141">System.Boolean</span></span>

## <span data-ttu-id="432d0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="432d0-142">NOTES</span></span>

## <span data-ttu-id="432d0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="432d0-143">RELATED LINKS</span></span>
