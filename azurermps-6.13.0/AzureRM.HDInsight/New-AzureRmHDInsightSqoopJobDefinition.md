---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 709c87084cc871814e4760e0d2641c59b0e5a64e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576992"
---
# <span data-ttu-id="12ec5-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12ec5-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="12ec5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="12ec5-103">Skapar ett Sqoop.</span><span class="sxs-lookup"><span data-stu-id="12ec5-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ec5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12ec5-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ec5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="12ec5-106">Cmdleten **New-AzureRmHDInsightSqoopJobDefinition** definierar ett Sqoop Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="12ec5-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="12ec5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="12ec5-108">Exempel 1: skapa en Sqoop</span><span class="sxs-lookup"><span data-stu-id="12ec5-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="12ec5-109">Det här kommandot skapar en Sqoop.</span><span class="sxs-lookup"><span data-stu-id="12ec5-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="12ec5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="12ec5-111">-Kommando</span><span class="sxs-lookup"><span data-stu-id="12ec5-111">-Command</span></span>
<span data-ttu-id="12ec5-112">Anger kommandot Sqoop.</span><span class="sxs-lookup"><span data-stu-id="12ec5-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="12ec5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ec5-113">-DefaultProfile</span></span>
<span data-ttu-id="12ec5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12ec5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ec5-115">-Fil</span><span class="sxs-lookup"><span data-stu-id="12ec5-115">-File</span></span>
<span data-ttu-id="12ec5-116">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="12ec5-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="12ec5-117">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="12ec5-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="12ec5-118">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="12ec5-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="12ec5-119">-Filer</span><span class="sxs-lookup"><span data-stu-id="12ec5-119">-Files</span></span>
<span data-ttu-id="12ec5-120">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="12ec5-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="12ec5-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="12ec5-121">-LibDir</span></span>
<span data-ttu-id="12ec5-122">Anger biblioteks katalogen för Sqoop-jobbet.</span><span class="sxs-lookup"><span data-stu-id="12ec5-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="12ec5-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="12ec5-123">-StatusFolder</span></span>
<span data-ttu-id="12ec5-124">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="12ec5-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="12ec5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ec5-125">CommonParameters</span></span>
<span data-ttu-id="12ec5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ec5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ec5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ec5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ec5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12ec5-128">INPUTS</span></span>

### <span data-ttu-id="12ec5-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="12ec5-129">None</span></span>

## <span data-ttu-id="12ec5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12ec5-130">OUTPUTS</span></span>

### <span data-ttu-id="12ec5-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="12ec5-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="12ec5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12ec5-132">NOTES</span></span>

## <span data-ttu-id="12ec5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12ec5-133">RELATED LINKS</span></span>

[<span data-ttu-id="12ec5-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="12ec5-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


