---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927046"
---
# <span data-ttu-id="ec492-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="ec492-101">New-AzSqlVM</span></span>

## <span data-ttu-id="ec492-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec492-102">SYNOPSIS</span></span>
<span data-ttu-id="ec492-103">Skapar en ny virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="ec492-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="ec492-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec492-104">SYNTAX</span></span>

### <span data-ttu-id="ec492-105">NameParamaterList (standard)</span><span class="sxs-lookup"><span data-stu-id="ec492-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec492-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="ec492-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec492-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec492-107">DESCRIPTION</span></span>
<span data-ttu-id="ec492-108">New-AzSqlVM-cmdleten skapar en virtuell Azure SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="ec492-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="ec492-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec492-109">EXAMPLES</span></span>

### <span data-ttu-id="ec492-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec492-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="ec492-111">Skapar en ny virtuell Azure SQL-dator med namn VM i resurs gruppen ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="ec492-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="ec492-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec492-112">PARAMETERS</span></span>

### <span data-ttu-id="ec492-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec492-113">-AsJob</span></span>
<span data-ttu-id="ec492-114">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="ec492-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ec492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec492-115">-DefaultProfile</span></span>
<span data-ttu-id="ec492-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec492-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec492-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ec492-117">-LicenseType</span></span>
<span data-ttu-id="ec492-118">Licens typ för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="ec492-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ec492-119">-Location</span></span>
<span data-ttu-id="ec492-120">Plats för virtuell dator för SQL.</span><span class="sxs-lookup"><span data-stu-id="ec492-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec492-121">-Name</span></span>
<span data-ttu-id="ec492-122">Namn på SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="ec492-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-123">-Ge</span><span class="sxs-lookup"><span data-stu-id="ec492-123">-Offer</span></span>
<span data-ttu-id="ec492-124">Utbud av virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="ec492-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec492-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec492-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec492-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="ec492-127">-Sku</span></span>
<span data-ttu-id="ec492-128">Typ av SQL Virtual Machine-version.</span><span class="sxs-lookup"><span data-stu-id="ec492-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="ec492-129">-SqlManagementType</span></span>
<span data-ttu-id="ec492-130">Hanterings typ för SQL virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ec492-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="ec492-131">-SqlVM</span></span>
<span data-ttu-id="ec492-132">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="ec492-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ec492-133">-Tag</span></span>
<span data-ttu-id="ec492-134">De taggar som ska kopplas till den virtuella SQL-datorn</span><span class="sxs-lookup"><span data-stu-id="ec492-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec492-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec492-135">-Confirm</span></span>
<span data-ttu-id="ec492-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec492-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec492-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec492-137">-WhatIf</span></span>
<span data-ttu-id="ec492-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec492-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec492-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec492-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec492-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec492-140">CommonParameters</span></span>
<span data-ttu-id="ec492-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec492-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec492-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec492-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec492-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec492-143">INPUTS</span></span>

### <span data-ttu-id="ec492-144">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ec492-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ec492-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec492-145">OUTPUTS</span></span>

### <span data-ttu-id="ec492-146">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ec492-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ec492-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec492-147">NOTES</span></span>

## <span data-ttu-id="ec492-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec492-148">RELATED LINKS</span></span>