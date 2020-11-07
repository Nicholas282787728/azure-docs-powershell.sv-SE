---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: d5841a7c612bccb760a8d755fc9a1c1364cc52a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744071"
---
# <span data-ttu-id="326c3-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="326c3-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="326c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="326c3-102">SYNOPSIS</span></span>
<span data-ttu-id="326c3-103">Skapar ett Sqoop.</span><span class="sxs-lookup"><span data-stu-id="326c3-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="326c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="326c3-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="326c3-105">DESCRIPTION</span></span>
<span data-ttu-id="326c3-106">Cmdleten **New-AzHDInsightSqoopJobDefinition** definierar ett Sqoop Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="326c3-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="326c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="326c3-107">EXAMPLES</span></span>

### <span data-ttu-id="326c3-108">Exempel 1: skapa en Sqoop</span><span class="sxs-lookup"><span data-stu-id="326c3-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="326c3-109">Det här kommandot skapar en Sqoop.</span><span class="sxs-lookup"><span data-stu-id="326c3-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="326c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="326c3-110">PARAMETERS</span></span>

### <span data-ttu-id="326c3-111">-Kommando</span><span class="sxs-lookup"><span data-stu-id="326c3-111">-Command</span></span>
<span data-ttu-id="326c3-112">Anger kommandot Sqoop.</span><span class="sxs-lookup"><span data-stu-id="326c3-112">Specifies the Sqoop command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326c3-113">-DefaultProfile</span></span>
<span data-ttu-id="326c3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="326c3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="326c3-115">-Fil</span><span class="sxs-lookup"><span data-stu-id="326c3-115">-File</span></span>
<span data-ttu-id="326c3-116">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="326c3-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="326c3-117">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="326c3-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="326c3-118">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="326c3-118">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326c3-119">-Filer</span><span class="sxs-lookup"><span data-stu-id="326c3-119">-Files</span></span>
<span data-ttu-id="326c3-120">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="326c3-120">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326c3-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="326c3-121">-LibDir</span></span>
<span data-ttu-id="326c3-122">Anger biblioteks katalogen för Sqoop-jobbet.</span><span class="sxs-lookup"><span data-stu-id="326c3-122">Specifies the library directory for the Sqoop job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326c3-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="326c3-123">-StatusFolder</span></span>
<span data-ttu-id="326c3-124">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="326c3-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326c3-125">CommonParameters</span></span>
<span data-ttu-id="326c3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326c3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326c3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326c3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="326c3-128">INPUTS</span></span>

### <span data-ttu-id="326c3-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="326c3-129">None</span></span>

## <span data-ttu-id="326c3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="326c3-130">OUTPUTS</span></span>

### <span data-ttu-id="326c3-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="326c3-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="326c3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="326c3-132">NOTES</span></span>

## <span data-ttu-id="326c3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="326c3-133">RELATED LINKS</span></span>

[<span data-ttu-id="326c3-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="326c3-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

