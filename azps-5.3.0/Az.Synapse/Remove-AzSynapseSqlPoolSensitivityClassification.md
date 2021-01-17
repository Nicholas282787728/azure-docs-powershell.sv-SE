---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424120"
---
# <span data-ttu-id="b1ed9-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="b1ed9-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="b1ed9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ed9-103">Tar bort data typerna och känslighets etiketterna för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b1ed9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1ed9-104">SYNTAX</span></span>

### <span data-ttu-id="b1ed9-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b1ed9-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1ed9-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1ed9-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1ed9-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1ed9-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1ed9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1ed9-108">DESCRIPTION</span></span>
<span data-ttu-id="b1ed9-109">Remove-AzSynapseSqlPoolSensitivityClassification cmdlet tar bort data typerna och känslighets etiketterna för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b1ed9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1ed9-110">EXAMPLES</span></span>

### <span data-ttu-id="b1ed9-111">Exempel 1: ta bort informations typ och känslighets etikett för en kolumn i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="b1ed9-112">Exempel 2: ta bort aktuella informations typer och känslighets etiketter för kolumner i en Azure Synapse SQL-adresspool med dragning.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="b1ed9-113">Exempel 3: ta bort informations typ och känslighets etikett för en kolumn i en Azure Synapse SQL-pool med dragning.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="b1ed9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1ed9-114">PARAMETERS</span></span>

### <span data-ttu-id="b1ed9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1ed9-115">-AsJob</span></span>
<span data-ttu-id="b1ed9-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b1ed9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1ed9-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="b1ed9-117">-ClassificationObject</span></span>
<span data-ttu-id="b1ed9-118">Ett objekt som representerar en känslighets klassificering för SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-119">-ColumnName</span></span>
<span data-ttu-id="b1ed9-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ed9-121">-DefaultProfile</span></span>
<span data-ttu-id="b1ed9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1ed9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1ed9-123">-PassThru</span></span>
<span data-ttu-id="b1ed9-124">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b1ed9-125">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b1ed9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-126">-ResourceGroupName</span></span>
<span data-ttu-id="b1ed9-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-128">-SchemaName</span></span>
<span data-ttu-id="b1ed9-129">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-130">-SqlPoolName</span></span>
<span data-ttu-id="b1ed9-131">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="b1ed9-132">-SqlPoolObject</span></span>
<span data-ttu-id="b1ed9-133">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-134">-TableName</span></span>
<span data-ttu-id="b1ed9-135">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1ed9-136">-WorkspaceName</span></span>
<span data-ttu-id="b1ed9-137">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ed9-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1ed9-138">-Confirm</span></span>
<span data-ttu-id="b1ed9-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1ed9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1ed9-140">-WhatIf</span></span>
<span data-ttu-id="b1ed9-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1ed9-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1ed9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ed9-143">CommonParameters</span></span>
<span data-ttu-id="b1ed9-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1ed9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ed9-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1ed9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ed9-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1ed9-146">INPUTS</span></span>

### <span data-ttu-id="b1ed9-147">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b1ed9-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="b1ed9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b1ed9-148">System.String</span></span>

### <span data-ttu-id="b1ed9-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b1ed9-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b1ed9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1ed9-150">OUTPUTS</span></span>

### <span data-ttu-id="b1ed9-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1ed9-151">System.Boolean</span></span>

## <span data-ttu-id="b1ed9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1ed9-152">NOTES</span></span>

## <span data-ttu-id="b1ed9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1ed9-153">RELATED LINKS</span></span>
