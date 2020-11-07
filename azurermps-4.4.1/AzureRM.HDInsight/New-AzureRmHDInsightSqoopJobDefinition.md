---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757791"
---
# <span data-ttu-id="b1972-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b1972-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b1972-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1972-102">SYNOPSIS</span></span>
<span data-ttu-id="b1972-103">Skapar ett Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b1972-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1972-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1972-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1972-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1972-105">DESCRIPTION</span></span>
<span data-ttu-id="b1972-106">Cmdleten **New-AzureRmHDInsightSqoopJobDefinition** definierar ett Sqoop Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="b1972-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b1972-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1972-107">EXAMPLES</span></span>

### <span data-ttu-id="b1972-108">Exempel 1: skapa en Sqoop</span><span class="sxs-lookup"><span data-stu-id="b1972-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b1972-109">Det här kommandot skapar en Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b1972-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="b1972-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1972-110">PARAMETERS</span></span>

### <span data-ttu-id="b1972-111">-Kommando</span><span class="sxs-lookup"><span data-stu-id="b1972-111">-Command</span></span>
<span data-ttu-id="b1972-112">Anger kommandot Sqoop.</span><span class="sxs-lookup"><span data-stu-id="b1972-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="b1972-113">-Fil</span><span class="sxs-lookup"><span data-stu-id="b1972-113">-File</span></span>
<span data-ttu-id="b1972-114">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="b1972-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b1972-115">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="b1972-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="b1972-116">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="b1972-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b1972-117">-Filer</span><span class="sxs-lookup"><span data-stu-id="b1972-117">-Files</span></span>
<span data-ttu-id="b1972-118">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="b1972-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b1972-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="b1972-119">-LibDir</span></span>
<span data-ttu-id="b1972-120">Anger biblioteks katalogen för Sqoop-jobbet.</span><span class="sxs-lookup"><span data-stu-id="b1972-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="b1972-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b1972-121">-StatusFolder</span></span>
<span data-ttu-id="b1972-122">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="b1972-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b1972-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1972-123">-DefaultProfile</span></span>
<span data-ttu-id="b1972-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1972-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1972-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1972-125">CommonParameters</span></span>
<span data-ttu-id="b1972-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1972-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1972-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1972-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1972-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1972-128">INPUTS</span></span>

## <span data-ttu-id="b1972-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1972-129">OUTPUTS</span></span>

### <span data-ttu-id="b1972-130">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b1972-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b1972-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1972-131">NOTES</span></span>

## <span data-ttu-id="b1972-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1972-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1972-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b1972-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


