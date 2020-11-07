---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 4d69d14d1129deb1bff580a0e0edfdb922b1544d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924621"
---
# <span data-ttu-id="9cb5f-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cb5f-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="9cb5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb5f-103">Tar bort Edge Storage-kontot för en enhet.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="9cb5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cb5f-104">SYNTAX</span></span>

### <span data-ttu-id="9cb5f-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9cb5f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb5f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb5f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb5f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb5f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cb5f-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb5f-109">Cmdleten **Remove-AzDataBoxEdgeStorageAccount** tar bort ett tillhör ande lagrings konto för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="9cb5f-110">Du kan ange namnet på lagrings kontot för Edge som ska tas bort som en parameter i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="9cb5f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cb5f-111">EXAMPLES</span></span>

### <span data-ttu-id="9cb5f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9cb5f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="9cb5f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cb5f-113">PARAMETERS</span></span>

### <span data-ttu-id="9cb5f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb5f-114">-AsJob</span></span>
<span data-ttu-id="9cb5f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9cb5f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cb5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb5f-116">-DefaultProfile</span></span>
<span data-ttu-id="9cb5f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb5f-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="9cb5f-118">-DeviceName</span></span>
<span data-ttu-id="9cb5f-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="9cb5f-119">Device Name</span></span>

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

### <span data-ttu-id="9cb5f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb5f-120">-InputObject</span></span>
<span data-ttu-id="9cb5f-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="9cb5f-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cb5f-122">-Name</span></span>
<span data-ttu-id="9cb5f-123">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="9cb5f-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb5f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cb5f-124">-PassThru</span></span>
<span data-ttu-id="9cb5f-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="9cb5f-125">returns true if successful</span></span>

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

### <span data-ttu-id="9cb5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9cb5f-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9cb5f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="9cb5f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb5f-128">-ResourceId</span></span>
<span data-ttu-id="9cb5f-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb5f-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="9cb5f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cb5f-130">-Confirm</span></span>
<span data-ttu-id="9cb5f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb5f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb5f-132">-WhatIf</span></span>
<span data-ttu-id="9cb5f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cb5f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb5f-135">CommonParameters</span></span>
<span data-ttu-id="9cb5f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb5f-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb5f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb5f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cb5f-138">INPUTS</span></span>

### <span data-ttu-id="9cb5f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb5f-139">System.String</span></span>

### <span data-ttu-id="9cb5f-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9cb5f-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="9cb5f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cb5f-141">OUTPUTS</span></span>

### <span data-ttu-id="9cb5f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cb5f-142">System.Boolean</span></span>

## <span data-ttu-id="9cb5f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cb5f-143">NOTES</span></span>

## <span data-ttu-id="9cb5f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cb5f-144">RELATED LINKS</span></span>
