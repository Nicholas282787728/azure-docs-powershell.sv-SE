---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271066"
---
# <span data-ttu-id="d1270-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d1270-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="d1270-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1270-102">SYNOPSIS</span></span>
<span data-ttu-id="d1270-103">Skapar ett gris-Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="d1270-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="d1270-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1270-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1270-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1270-105">DESCRIPTION</span></span>
<span data-ttu-id="d1270-106">Cmdleten **New-AzHDInsightPigJobDefinition** definierar ett gris-jobb-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="d1270-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d1270-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1270-107">EXAMPLES</span></span>

### <span data-ttu-id="d1270-108">Exempel 1: skapa en jobb definition för gris</span><span class="sxs-lookup"><span data-stu-id="d1270-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="d1270-109">Det här kommandot skapar en jobb definition för gris.</span><span class="sxs-lookup"><span data-stu-id="d1270-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="d1270-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1270-110">PARAMETERS</span></span>

### <span data-ttu-id="d1270-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="d1270-111">-Arguments</span></span>
<span data-ttu-id="d1270-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d1270-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d1270-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d1270-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d1270-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1270-114">-DefaultProfile</span></span>
<span data-ttu-id="d1270-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d1270-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1270-116">-Fil</span><span class="sxs-lookup"><span data-stu-id="d1270-116">-File</span></span>
<span data-ttu-id="d1270-117">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="d1270-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="d1270-118">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="d1270-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="d1270-119">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="d1270-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="d1270-120">-Filer</span><span class="sxs-lookup"><span data-stu-id="d1270-120">-Files</span></span>
<span data-ttu-id="d1270-121">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="d1270-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d1270-122">-Fråga</span><span class="sxs-lookup"><span data-stu-id="d1270-122">-Query</span></span>
<span data-ttu-id="d1270-123">Anger gris-frågan.</span><span class="sxs-lookup"><span data-stu-id="d1270-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="d1270-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d1270-124">-StatusFolder</span></span>
<span data-ttu-id="d1270-125">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="d1270-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d1270-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1270-126">CommonParameters</span></span>
<span data-ttu-id="d1270-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1270-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1270-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1270-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1270-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1270-129">INPUTS</span></span>

### <span data-ttu-id="d1270-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="d1270-130">None</span></span>

## <span data-ttu-id="d1270-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1270-131">OUTPUTS</span></span>

### <span data-ttu-id="d1270-132">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d1270-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="d1270-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1270-133">NOTES</span></span>

## <span data-ttu-id="d1270-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1270-134">RELATED LINKS</span></span>

[<span data-ttu-id="d1270-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d1270-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


