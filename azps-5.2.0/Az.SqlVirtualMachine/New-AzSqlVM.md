---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413424"
---
# <span data-ttu-id="b60de-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="b60de-101">New-AzSqlVM</span></span>

## <span data-ttu-id="b60de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b60de-102">SYNOPSIS</span></span>
<span data-ttu-id="b60de-103">Skapar en ny virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b60de-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="b60de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b60de-104">SYNTAX</span></span>

### <span data-ttu-id="b60de-105">NameParamaterList (standard)</span><span class="sxs-lookup"><span data-stu-id="b60de-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b60de-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="b60de-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b60de-107">DESCRIPTION</span></span>
<span data-ttu-id="b60de-108">New-AzSqlVM-cmdleten skapar en virtuell Azure SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b60de-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="b60de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b60de-109">EXAMPLES</span></span>

### <span data-ttu-id="b60de-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b60de-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="b60de-111">Skapar en ny virtuell Azure SQL-dator med namn VM i resurs gruppen ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="b60de-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="b60de-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b60de-112">PARAMETERS</span></span>

### <span data-ttu-id="b60de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b60de-113">-AsJob</span></span>
<span data-ttu-id="b60de-114">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="b60de-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b60de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60de-115">-DefaultProfile</span></span>
<span data-ttu-id="b60de-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b60de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60de-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b60de-117">-LicenseType</span></span>
<span data-ttu-id="b60de-118">Licens typ för SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="b60de-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="b60de-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="b60de-119">-Location</span></span>
<span data-ttu-id="b60de-120">Plats för virtuell dator för SQL.</span><span class="sxs-lookup"><span data-stu-id="b60de-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="b60de-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b60de-121">-Name</span></span>
<span data-ttu-id="b60de-122">Namn på SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b60de-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="b60de-123">-Ge</span><span class="sxs-lookup"><span data-stu-id="b60de-123">-Offer</span></span>
<span data-ttu-id="b60de-124">Utbud av virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="b60de-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="b60de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60de-125">-ResourceGroupName</span></span>
<span data-ttu-id="b60de-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b60de-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b60de-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="b60de-127">-Sku</span></span>
<span data-ttu-id="b60de-128">Typ av SQL Virtual Machine-version.</span><span class="sxs-lookup"><span data-stu-id="b60de-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="b60de-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="b60de-129">-SqlManagementType</span></span>
<span data-ttu-id="b60de-130">Hanterings typ för SQL virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b60de-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="b60de-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="b60de-131">-SqlVM</span></span>
<span data-ttu-id="b60de-132">SQL Virtual Machine-objekt.</span><span class="sxs-lookup"><span data-stu-id="b60de-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="b60de-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b60de-133">-Tag</span></span>
<span data-ttu-id="b60de-134">De taggar som ska kopplas till den virtuella SQL-datorn</span><span class="sxs-lookup"><span data-stu-id="b60de-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="b60de-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b60de-135">-Confirm</span></span>
<span data-ttu-id="b60de-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b60de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60de-137">-WhatIf</span></span>
<span data-ttu-id="b60de-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b60de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60de-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b60de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60de-140">CommonParameters</span></span>
<span data-ttu-id="b60de-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60de-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b60de-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60de-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b60de-143">INPUTS</span></span>

### <span data-ttu-id="b60de-144">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b60de-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b60de-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b60de-145">OUTPUTS</span></span>

### <span data-ttu-id="b60de-146">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b60de-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b60de-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b60de-147">NOTES</span></span>

## <span data-ttu-id="b60de-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b60de-148">RELATED LINKS</span></span>
