---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521912"
---
# <span data-ttu-id="fc0d0-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="fc0d0-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="fc0d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0d0-103">Aktiverar känslighets rekommendationer för kolumner (rekommendationer är aktiverade som standard i alla kolumner) i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="fc0d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc0d0-104">SYNTAX</span></span>

### <span data-ttu-id="fc0d0-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fc0d0-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0d0-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc0d0-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0d0-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc0d0-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc0d0-108">DESCRIPTION</span></span>
<span data-ttu-id="fc0d0-109">Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet aktiverar känslighets rekommendationer för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="fc0d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc0d0-110">EXAMPLES</span></span>

### <span data-ttu-id="fc0d0-111">Exempel 1: Aktivera känslighets rekommendationer för en viss kolumn i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="fc0d0-112">Exempel 2: Aktivera känslighets rekommendationer för en viss kolumn Azure Synapse SQL-adresspool med dragning.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="fc0d0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc0d0-113">PARAMETERS</span></span>

### <span data-ttu-id="fc0d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc0d0-114">-AsJob</span></span>
<span data-ttu-id="fc0d0-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fc0d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc0d0-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-116">-ColumnName</span></span>
<span data-ttu-id="fc0d0-117">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-117">Name of column.</span></span>

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

### <span data-ttu-id="fc0d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0d0-118">-DefaultProfile</span></span>
<span data-ttu-id="fc0d0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc0d0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc0d0-120">-InputObject</span></span>
<span data-ttu-id="fc0d0-121">Ett objekt som representerar en känslighets klassificering för SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0d0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc0d0-122">-PassThru</span></span>
<span data-ttu-id="fc0d0-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fc0d0-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fc0d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc0d0-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-126">Resource group name.</span></span>

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

### <span data-ttu-id="fc0d0-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-127">-SchemaName</span></span>
<span data-ttu-id="fc0d0-128">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-128">Name of schema.</span></span>

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

### <span data-ttu-id="fc0d0-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-129">-SqlPoolName</span></span>
<span data-ttu-id="fc0d0-130">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fc0d0-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="fc0d0-131">-SqlPoolObject</span></span>
<span data-ttu-id="fc0d0-132">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fc0d0-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-133">-TableName</span></span>
<span data-ttu-id="fc0d0-134">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-134">Name of table.</span></span>

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

### <span data-ttu-id="fc0d0-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fc0d0-135">-WorkspaceName</span></span>
<span data-ttu-id="fc0d0-136">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fc0d0-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc0d0-137">-Confirm</span></span>
<span data-ttu-id="fc0d0-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0d0-139">-WhatIf</span></span>
<span data-ttu-id="fc0d0-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0d0-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0d0-142">CommonParameters</span></span>
<span data-ttu-id="fc0d0-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0d0-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc0d0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0d0-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc0d0-145">INPUTS</span></span>

### <span data-ttu-id="fc0d0-146">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="fc0d0-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="fc0d0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fc0d0-147">System.String</span></span>

### <span data-ttu-id="fc0d0-148">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fc0d0-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fc0d0-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc0d0-149">OUTPUTS</span></span>

### <span data-ttu-id="fc0d0-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc0d0-150">System.Boolean</span></span>

## <span data-ttu-id="fc0d0-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc0d0-151">NOTES</span></span>

## <span data-ttu-id="fc0d0-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc0d0-152">RELATED LINKS</span></span>
