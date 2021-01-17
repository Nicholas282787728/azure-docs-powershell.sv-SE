---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424400"
---
# <span data-ttu-id="ce864-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ce864-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="ce864-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce864-102">SYNOPSIS</span></span>
<span data-ttu-id="ce864-103">Hämtar de aktuella informations typerna och känslighets etiketterna för kolumnerna i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="ce864-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="ce864-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce864-104">SYNTAX</span></span>

### <span data-ttu-id="ce864-105">SqlPoolObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce864-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce864-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce864-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce864-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce864-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce864-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce864-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce864-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce864-109">DESCRIPTION</span></span>
<span data-ttu-id="ce864-110">Get-AzSynapseSqlPoolSensitivityClassification cmdlet returnerar de aktuella informations typerna och känslighets etiketterna för kolumnerna i Azure Synapse SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="ce864-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="ce864-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce864-111">EXAMPLES</span></span>

### <span data-ttu-id="ce864-112">Exempel 1: hämta aktuella informations typer och känslighets etiketter för en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ce864-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="ce864-113">Exempel 2: hämta aktuella informations typer och känslighets etiketter för en Azure Synapse SQL-pool med rör.</span><span class="sxs-lookup"><span data-stu-id="ce864-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="ce864-114">Exempel 3: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="ce864-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="ce864-115">Exempel 4: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure Synapse SQL-adresspool med dragning.</span><span class="sxs-lookup"><span data-stu-id="ce864-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="ce864-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce864-116">PARAMETERS</span></span>

### <span data-ttu-id="ce864-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce864-117">-AsJob</span></span>
<span data-ttu-id="ce864-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ce864-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce864-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ce864-119">-ColumnName</span></span>
<span data-ttu-id="ce864-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="ce864-120">Name of column.</span></span>

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

### <span data-ttu-id="ce864-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce864-121">-DefaultProfile</span></span>
<span data-ttu-id="ce864-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce864-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce864-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce864-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce864-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ce864-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce864-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ce864-125">-SchemaName</span></span>
<span data-ttu-id="ce864-126">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="ce864-126">Name of schema.</span></span>

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

### <span data-ttu-id="ce864-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="ce864-127">-SqlPoolName</span></span>
<span data-ttu-id="ce864-128">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce864-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce864-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="ce864-129">-SqlPoolObject</span></span>
<span data-ttu-id="ce864-130">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce864-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce864-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="ce864-131">-TableName</span></span>
<span data-ttu-id="ce864-132">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="ce864-132">Name of table.</span></span>

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

### <span data-ttu-id="ce864-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce864-133">-WorkspaceName</span></span>
<span data-ttu-id="ce864-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ce864-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce864-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce864-135">CommonParameters</span></span>
<span data-ttu-id="ce864-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce864-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce864-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce864-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce864-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce864-138">INPUTS</span></span>

### <span data-ttu-id="ce864-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ce864-139">System.String</span></span>

### <span data-ttu-id="ce864-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ce864-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ce864-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce864-141">OUTPUTS</span></span>

### <span data-ttu-id="ce864-142">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ce864-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="ce864-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce864-143">NOTES</span></span>

## <span data-ttu-id="ce864-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce864-144">RELATED LINKS</span></span>
