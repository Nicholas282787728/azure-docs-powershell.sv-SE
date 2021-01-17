---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424032"
---
# <span data-ttu-id="05521-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="05521-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="05521-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05521-102">SYNOPSIS</span></span>
<span data-ttu-id="05521-103">Anger etiketterna för informations typer och känslighet för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="05521-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="05521-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05521-104">SYNTAX</span></span>

### <span data-ttu-id="05521-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="05521-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05521-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05521-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05521-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="05521-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05521-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05521-108">DESCRIPTION</span></span>
<span data-ttu-id="05521-109">I Set-AzSynapseSqlPoolSensitivityClassification cmdlet anges etiketterna för informations typer och känslighet för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="05521-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="05521-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05521-110">EXAMPLES</span></span>

### <span data-ttu-id="05521-111">Exempel 1: Ange informations typ och känslighets etikett för en kolumn i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="05521-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="05521-112">Exempel 2: Ange rekommenderade informations typer och känslighets etiketter för kolumner i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="05521-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="05521-113">Exempel 3: Ange informations typ och känslighets etikett för en kolumn i en Azure Synapse SQL-pool, med dragning.</span><span class="sxs-lookup"><span data-stu-id="05521-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="05521-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05521-114">PARAMETERS</span></span>

### <span data-ttu-id="05521-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05521-115">-AsJob</span></span>
<span data-ttu-id="05521-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="05521-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05521-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="05521-117">-ClassificationObject</span></span>
<span data-ttu-id="05521-118">Ett objekt som representerar en känslighets klassificering för SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="05521-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="05521-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="05521-119">-ColumnName</span></span>
<span data-ttu-id="05521-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="05521-120">Name of column.</span></span>

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

### <span data-ttu-id="05521-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05521-121">-DefaultProfile</span></span>
<span data-ttu-id="05521-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05521-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05521-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="05521-123">-InformationType</span></span>
<span data-ttu-id="05521-124">Ett namn som beskriver informations typen för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="05521-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05521-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05521-125">-PassThru</span></span>
<span data-ttu-id="05521-126">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="05521-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="05521-127">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="05521-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="05521-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05521-128">-ResourceGroupName</span></span>
<span data-ttu-id="05521-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="05521-129">Resource group name.</span></span>

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

### <span data-ttu-id="05521-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="05521-130">-SchemaName</span></span>
<span data-ttu-id="05521-131">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="05521-131">Name of schema.</span></span>

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

### <span data-ttu-id="05521-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="05521-132">-SensitivityLabel</span></span>
<span data-ttu-id="05521-133">Ett namn som beskriver känsligheten för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="05521-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05521-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="05521-134">-SqlPoolName</span></span>
<span data-ttu-id="05521-135">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="05521-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="05521-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="05521-136">-SqlPoolObject</span></span>
<span data-ttu-id="05521-137">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="05521-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="05521-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="05521-138">-TableName</span></span>
<span data-ttu-id="05521-139">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="05521-139">Name of table.</span></span>

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

### <span data-ttu-id="05521-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05521-140">-WorkspaceName</span></span>
<span data-ttu-id="05521-141">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="05521-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="05521-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05521-142">-Confirm</span></span>
<span data-ttu-id="05521-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05521-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05521-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05521-144">-WhatIf</span></span>
<span data-ttu-id="05521-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05521-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05521-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05521-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05521-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05521-147">CommonParameters</span></span>
<span data-ttu-id="05521-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05521-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05521-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05521-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05521-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05521-150">INPUTS</span></span>

### <span data-ttu-id="05521-151">System. String</span><span class="sxs-lookup"><span data-stu-id="05521-151">System.String</span></span>

### <span data-ttu-id="05521-152">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="05521-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="05521-153">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="05521-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="05521-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05521-154">OUTPUTS</span></span>

### <span data-ttu-id="05521-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05521-155">System.Boolean</span></span>

## <span data-ttu-id="05521-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05521-156">NOTES</span></span>

## <span data-ttu-id="05521-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05521-157">RELATED LINKS</span></span>
