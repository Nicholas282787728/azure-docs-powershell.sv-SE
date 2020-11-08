---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: dff83dbb7183c4f9eaf46e883a92a8e615f9cacc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924625"
---
# <span data-ttu-id="3373f-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3373f-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3373f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3373f-102">SYNOPSIS</span></span>
<span data-ttu-id="3373f-103">Tar bort en autentiseringsuppgift för lagrings konton för en enhet.</span><span class="sxs-lookup"><span data-stu-id="3373f-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="3373f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3373f-104">SYNTAX</span></span>

### <span data-ttu-id="3373f-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3373f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3373f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3373f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3373f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3373f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3373f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3373f-108">DESCRIPTION</span></span>
<span data-ttu-id="3373f-109">Cmdleten **Remove-AzDataBoxEdgeStorageAccountCredential** tar bort autentiseringsuppgifterna för lagrings kontot för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="3373f-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="3373f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3373f-110">EXAMPLES</span></span>

### <span data-ttu-id="3373f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3373f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="3373f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3373f-112">PARAMETERS</span></span>

### <span data-ttu-id="3373f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3373f-113">-AsJob</span></span>
<span data-ttu-id="3373f-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3373f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3373f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3373f-115">-DefaultProfile</span></span>
<span data-ttu-id="3373f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3373f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3373f-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="3373f-117">-DeviceName</span></span>
<span data-ttu-id="3373f-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="3373f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3373f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3373f-119">-InputObject</span></span>
<span data-ttu-id="3373f-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="3373f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3373f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3373f-121">-Name</span></span>
<span data-ttu-id="3373f-122">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="3373f-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3373f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3373f-123">-PassThru</span></span>
<span data-ttu-id="3373f-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="3373f-124">returns true if successful</span></span>

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

### <span data-ttu-id="3373f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3373f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3373f-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3373f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3373f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3373f-127">-ResourceId</span></span>
<span data-ttu-id="3373f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3373f-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3373f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3373f-129">-Confirm</span></span>
<span data-ttu-id="3373f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3373f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3373f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3373f-131">-WhatIf</span></span>
<span data-ttu-id="3373f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3373f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3373f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3373f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3373f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3373f-134">CommonParameters</span></span>
<span data-ttu-id="3373f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3373f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3373f-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3373f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3373f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3373f-137">INPUTS</span></span>

### <span data-ttu-id="3373f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3373f-138">System.String</span></span>

### <span data-ttu-id="3373f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3373f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3373f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3373f-140">OUTPUTS</span></span>

### <span data-ttu-id="3373f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3373f-141">System.Boolean</span></span>

## <span data-ttu-id="3373f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3373f-142">NOTES</span></span>

## <span data-ttu-id="3373f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3373f-143">RELATED LINKS</span></span>