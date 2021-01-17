---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424387"
---
# <span data-ttu-id="1f22d-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="1f22d-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="1f22d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f22d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f22d-103">Hämtar de rekommenderade informations typerna och känslighets etiketterna för kolumnerna i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="1f22d-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="1f22d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f22d-104">SYNTAX</span></span>

### <span data-ttu-id="1f22d-105">SqlPoolObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1f22d-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f22d-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f22d-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f22d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f22d-107">DESCRIPTION</span></span>
<span data-ttu-id="1f22d-108">Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returnerar de rekommenderade informations typerna och känslighets etiketterna för kolumnerna i SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="1f22d-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="1f22d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f22d-109">EXAMPLES</span></span>

### <span data-ttu-id="1f22d-110">Exempel 1: Hämta rekommenderade informations typer och känslighets etiketter för en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="1f22d-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="1f22d-111">Exempel 2: Hämta rekommenderade informations typer och känslighets etiketter för en Azure Synapse SQL-adresspool med dragning.</span><span class="sxs-lookup"><span data-stu-id="1f22d-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="1f22d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f22d-112">PARAMETERS</span></span>

### <span data-ttu-id="1f22d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f22d-113">-AsJob</span></span>
<span data-ttu-id="1f22d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1f22d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f22d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f22d-115">-DefaultProfile</span></span>
<span data-ttu-id="1f22d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f22d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f22d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f22d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f22d-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1f22d-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f22d-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="1f22d-119">-SqlPoolName</span></span>
<span data-ttu-id="1f22d-120">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="1f22d-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f22d-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="1f22d-121">-SqlPoolObject</span></span>
<span data-ttu-id="1f22d-122">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f22d-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f22d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f22d-123">-WorkspaceName</span></span>
<span data-ttu-id="1f22d-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1f22d-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f22d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f22d-125">CommonParameters</span></span>
<span data-ttu-id="1f22d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f22d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f22d-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f22d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f22d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f22d-128">INPUTS</span></span>

### <span data-ttu-id="1f22d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1f22d-129">System.String</span></span>

### <span data-ttu-id="1f22d-130">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1f22d-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1f22d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f22d-131">OUTPUTS</span></span>

### <span data-ttu-id="1f22d-132">Microsoft. Azure. commands. Synapse. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1f22d-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="1f22d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f22d-133">NOTES</span></span>

## <span data-ttu-id="1f22d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f22d-134">RELATED LINKS</span></span>
