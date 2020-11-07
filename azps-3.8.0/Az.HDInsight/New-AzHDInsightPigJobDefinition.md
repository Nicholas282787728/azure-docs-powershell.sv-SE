---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928101"
---
# <span data-ttu-id="7a56f-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7a56f-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="7a56f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a56f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a56f-103">Skapar ett gris-Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="7a56f-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="7a56f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a56f-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a56f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a56f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a56f-106">Cmdleten **New-AzHDInsightPigJobDefinition** definierar ett gris-jobb-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="7a56f-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7a56f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a56f-107">EXAMPLES</span></span>

### <span data-ttu-id="7a56f-108">Exempel 1: skapa en jobb definition för gris</span><span class="sxs-lookup"><span data-stu-id="7a56f-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7a56f-109">Det här kommandot skapar en jobb definition för gris.</span><span class="sxs-lookup"><span data-stu-id="7a56f-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="7a56f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a56f-110">PARAMETERS</span></span>

### <span data-ttu-id="7a56f-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="7a56f-111">-Arguments</span></span>
<span data-ttu-id="7a56f-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="7a56f-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="7a56f-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="7a56f-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="7a56f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a56f-114">-DefaultProfile</span></span>
<span data-ttu-id="7a56f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a56f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a56f-116">-Fil</span><span class="sxs-lookup"><span data-stu-id="7a56f-116">-File</span></span>
<span data-ttu-id="7a56f-117">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="7a56f-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="7a56f-118">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="7a56f-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="7a56f-119">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="7a56f-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="7a56f-120">-Filer</span><span class="sxs-lookup"><span data-stu-id="7a56f-120">-Files</span></span>
<span data-ttu-id="7a56f-121">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="7a56f-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="7a56f-122">-Fråga</span><span class="sxs-lookup"><span data-stu-id="7a56f-122">-Query</span></span>
<span data-ttu-id="7a56f-123">Anger gris-frågan.</span><span class="sxs-lookup"><span data-stu-id="7a56f-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="7a56f-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7a56f-124">-StatusFolder</span></span>
<span data-ttu-id="7a56f-125">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="7a56f-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="7a56f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a56f-126">CommonParameters</span></span>
<span data-ttu-id="7a56f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a56f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a56f-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a56f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a56f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a56f-129">INPUTS</span></span>

### <span data-ttu-id="7a56f-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="7a56f-130">None</span></span>

## <span data-ttu-id="7a56f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a56f-131">OUTPUTS</span></span>

### <span data-ttu-id="7a56f-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7a56f-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="7a56f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a56f-133">NOTES</span></span>

## <span data-ttu-id="7a56f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a56f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a56f-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7a56f-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


