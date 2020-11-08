---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091634"
---
# <span data-ttu-id="ec8b9-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec8b9-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ec8b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8b9-103">Tar bort Edge Storage-kontot för en enhet.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="ec8b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec8b9-104">SYNTAX</span></span>

### <span data-ttu-id="ec8b9-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ec8b9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec8b9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec8b9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec8b9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec8b9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec8b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ec8b9-109">Cmdleten **Remove-AzStackEdgeStorageAccount** tar bort ett tillhör ande lagrings konto för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="ec8b9-110">Du kan ange namnet på lagrings kontot för Edge som ska tas bort som en parameter i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="ec8b9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec8b9-111">EXAMPLES</span></span>

### <span data-ttu-id="ec8b9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec8b9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="ec8b9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec8b9-113">PARAMETERS</span></span>

### <span data-ttu-id="ec8b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec8b9-114">-AsJob</span></span>
<span data-ttu-id="ec8b9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ec8b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec8b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8b9-116">-DefaultProfile</span></span>
<span data-ttu-id="ec8b9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec8b9-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="ec8b9-118">-DeviceName</span></span>
<span data-ttu-id="ec8b9-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="ec8b9-119">Device Name</span></span>

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

### <span data-ttu-id="ec8b9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec8b9-120">-InputObject</span></span>
<span data-ttu-id="ec8b9-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="ec8b9-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec8b9-122">-Name</span></span>
<span data-ttu-id="ec8b9-123">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="ec8b9-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec8b9-124">-PassThru</span></span>
<span data-ttu-id="ec8b9-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="ec8b9-125">returns true if successful</span></span>

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

### <span data-ttu-id="ec8b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec8b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec8b9-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ec8b9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ec8b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8b9-128">-ResourceId</span></span>
<span data-ttu-id="ec8b9-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8b9-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="ec8b9-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec8b9-130">-Confirm</span></span>
<span data-ttu-id="ec8b9-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec8b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec8b9-132">-WhatIf</span></span>
<span data-ttu-id="ec8b9-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec8b9-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec8b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8b9-135">CommonParameters</span></span>
<span data-ttu-id="ec8b9-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8b9-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec8b9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8b9-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec8b9-138">INPUTS</span></span>

### <span data-ttu-id="ec8b9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ec8b9-139">System.String</span></span>

### <span data-ttu-id="ec8b9-140">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec8b9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ec8b9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec8b9-141">OUTPUTS</span></span>

### <span data-ttu-id="ec8b9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec8b9-142">System.Boolean</span></span>

## <span data-ttu-id="ec8b9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec8b9-143">NOTES</span></span>

## <span data-ttu-id="ec8b9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec8b9-144">RELATED LINKS</span></span>
