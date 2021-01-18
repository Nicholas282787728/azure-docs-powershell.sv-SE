---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521915"
---
# <span data-ttu-id="e962e-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e962e-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="e962e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e962e-102">SYNOPSIS</span></span>
<span data-ttu-id="e962e-103">Inaktiverar (missar) känslighets rekommendationer för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="e962e-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="e962e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e962e-104">SYNTAX</span></span>

### <span data-ttu-id="e962e-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e962e-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e962e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e962e-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e962e-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e962e-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e962e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e962e-108">DESCRIPTION</span></span>
<span data-ttu-id="e962e-109">Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet inaktiverar (missar) känslighets rekommendationer för kolumner i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="e962e-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="e962e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e962e-110">EXAMPLES</span></span>

### <span data-ttu-id="e962e-111">Exempel 1: inaktivera känslighets rekommendationer för en viss kolumn i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e962e-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e962e-112">Exempel 2: inaktivera känslighets rekommendationer för kolumner med känslighets rekommendationer i en Azure Synapse SQL-pool med dragning.</span><span class="sxs-lookup"><span data-stu-id="e962e-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="e962e-113">Exempel 3: inaktivera känslighets rekommendationer för en viss kolumn i en Azure Synapse SQL-adresspool med dragning.</span><span class="sxs-lookup"><span data-stu-id="e962e-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e962e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e962e-114">PARAMETERS</span></span>

### <span data-ttu-id="e962e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e962e-115">-AsJob</span></span>
<span data-ttu-id="e962e-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e962e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e962e-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e962e-117">-ColumnName</span></span>
<span data-ttu-id="e962e-118">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="e962e-118">Name of column.</span></span>

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

### <span data-ttu-id="e962e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e962e-119">-DefaultProfile</span></span>
<span data-ttu-id="e962e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e962e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e962e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e962e-121">-InputObject</span></span>
<span data-ttu-id="e962e-122">Ett objekt som representerar en känslighets klassificering för SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="e962e-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e962e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e962e-123">-PassThru</span></span>
<span data-ttu-id="e962e-124">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="e962e-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e962e-125">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="e962e-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e962e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e962e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e962e-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e962e-127">Resource group name.</span></span>

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

### <span data-ttu-id="e962e-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e962e-128">-SchemaName</span></span>
<span data-ttu-id="e962e-129">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="e962e-129">Name of schema.</span></span>

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

### <span data-ttu-id="e962e-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e962e-130">-SqlPoolName</span></span>
<span data-ttu-id="e962e-131">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="e962e-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e962e-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e962e-132">-SqlPoolObject</span></span>
<span data-ttu-id="e962e-133">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e962e-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e962e-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="e962e-134">-TableName</span></span>
<span data-ttu-id="e962e-135">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="e962e-135">Name of table.</span></span>

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

### <span data-ttu-id="e962e-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e962e-136">-WorkspaceName</span></span>
<span data-ttu-id="e962e-137">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e962e-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e962e-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e962e-138">-Confirm</span></span>
<span data-ttu-id="e962e-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e962e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e962e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e962e-140">-WhatIf</span></span>
<span data-ttu-id="e962e-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e962e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e962e-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e962e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e962e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e962e-143">CommonParameters</span></span>
<span data-ttu-id="e962e-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e962e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e962e-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e962e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e962e-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e962e-146">INPUTS</span></span>

### <span data-ttu-id="e962e-147">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e962e-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="e962e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e962e-148">System.String</span></span>

### <span data-ttu-id="e962e-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e962e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e962e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e962e-150">OUTPUTS</span></span>

### <span data-ttu-id="e962e-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e962e-151">System.Boolean</span></span>

## <span data-ttu-id="e962e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e962e-152">NOTES</span></span>

## <span data-ttu-id="e962e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e962e-153">RELATED LINKS</span></span>
